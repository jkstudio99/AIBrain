---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/automation
  - topic/maintenance
  - topic/obsidian
  - status/evergreen
related:
  - "[[MOCs/Automation MOC]]"
  - "[[08 - Automation/Automation]]"
  - "[[10 - Meta/Vault Health/Vault Health Checks]]"
  - "[[03 - Resources/Claude Integration/Commands Folder]]"
  - "[[CLAUDE.md]]"
aliases:
  - Vault Maintenance
  - Vault Health Scripts
---

# Vault Maintenance Scripts

A vault that grows without maintenance becomes a liability instead of an asset. This guide covers the `/vault-health` command, individual maintenance scripts, and a scheduled maintenance cadence.

> [!info] Maintenance Philosophy
> Run audits in read-only mode first. Review every proposed change. Apply fixes incrementally, not in bulk. When in doubt, archive rather than delete.

---

## `/vault-health` Command

The `/vault-health` skill (mapped to `.claude/commands/vault-health.md`) runs a comprehensive audit across six dimensions:

| Dimension | What It Checks |
|---|---|
| **Orphan notes** | Notes with no inbound links |
| **Broken links** | Wikilinks pointing to non-existent notes |
| **Stale notes** | Notes not modified in 60+ days with `#status/seedling` |
| **Missing frontmatter** | Notes lacking required YAML fields |
| **Tag consistency** | Tags outside the official taxonomy |
| **Empty notes** | Notes with < 50 words of content |

The output is a health report note saved to:
`10 - Meta/Vault Health/Health Report YYYY-MM-DD.md`

---

## Individual Maintenance Tasks

### 1. Orphan Detection

Orphan notes have no inbound links — nothing in the vault points to them. They're either dead weight or undiscovered gems.

**Dataview query:**

```dataview
TABLE file.inlinks AS "Inbound Links"
FROM ""
WHERE length(file.inlinks) = 0
AND !contains(file.path, "00 - Inbox")
AND !contains(file.path, "Templates")
AND !contains(file.path, "Attachments")
SORT file.mtime ASC
```

**Action options:**
- Add a wikilink from a relevant MOC → removes orphan status
- Add to a related note as a see-also link
- Archive if genuinely irrelevant: move to `04 - Archive/`
- Delete if it's an empty stub

---

### 2. Broken Link Detection

Broken wikilinks occur when a note is renamed or deleted without updating references.

**Shell script (dry run — lists only):**

```bash
#!/bin/bash
# broken-links.sh — List all wikilinks that point to non-existent notes
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"

# Extract all [[wikilinks]] from all markdown files
grep -roh '\[\[[^\]]*\]\]' "$VAULT" --include="*.md" | \
  sed 's/\[\[//;s/\]\]//' | \
  sed 's/#.*//' | \
  sed 's/|.*//' | \
  sort -u | \
  while read -r link; do
    # Check if a note with that title exists
    if ! find "$VAULT" -name "${link}.md" -not -path "*/.obsidian/*" | grep -q .; then
      echo "BROKEN: $link"
    fi
  done
```

**Obsidian method:** The core "Unresolved links" section in Settings → Files and Links shows all broken wikilinks natively.

---

### 3. Stale Note Detection

Stale notes are still-seedling notes that haven't been touched in a long time — they've been abandoned without being archived.

**Dataview query:**

```dataview
TABLE file.mtime AS "Last Modified", tags
FROM ""
WHERE contains(tags, "status/seedling")
AND date(today) - file.mtime > dur(60 days)
SORT file.mtime ASC
LIMIT 20
```

**Action options for stale notes:**
- Develop: promote to `#status/growing` with a brief update
- Merge: fold content into a more developed note
- Archive: move to `04 - Archive/` with tag `#status/archived`
- Delete: if the content has no value

---

### 4. Missing Frontmatter

Notes without proper frontmatter can't participate in Dataview queries and break MOC automation.

**Dataview — Missing `type` field:**

```dataview
TABLE file.path
FROM ""
WHERE !type
AND !contains(file.path, "Templates")
AND !contains(file.path, ".obsidian")
SORT file.mtime DESC
LIMIT 30
```

**Dataview — Missing `created` date:**

```dataview
TABLE file.path
FROM ""
WHERE !created
AND !contains(file.path, "Templates")
SORT file.mtime DESC
LIMIT 30
```

**Shell script to count notes missing frontmatter:**

```bash
#!/bin/bash
# frontmatter-audit.sh
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"

echo "Notes missing YAML frontmatter:"
find "$VAULT" -name "*.md" \
  -not -path "*/.obsidian/*" \
  -not -path "*/Templates/*" | \
  while read -r file; do
    head -1 "$file" | grep -q "^---$" || echo "$file"
  done | wc -l
```

---

### 5. Tag Cleanup

Over time, ad-hoc tags accumulate outside the official taxonomy.

**Dataview — Find non-taxonomy tags:**

```dataview
TABLE tags
FROM ""
FLATTEN tags AS tag
WHERE !startswith(tag, "type/")
  AND !startswith(tag, "status/")
  AND !startswith(tag, "area/")
  AND !startswith(tag, "topic/")
  AND !startswith(tag, "prompt/")
GROUP BY tag
```

**Shell script — Count all unique tags:**

```bash
#!/bin/bash
# tag-audit.sh — List all tags used in the vault with frequency
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"

grep -roh '#[a-zA-Z][a-zA-Z0-9/_-]*' "$VAULT" --include="*.md" | \
  sort | uniq -c | sort -rn | head -50
```

**Tag rename script:**

```bash
#!/bin/bash
# rename-tag.sh OLD_TAG NEW_TAG
# Usage: ./rename-tag.sh "#old-name" "#new-name"
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"
OLD="$1"
NEW="$2"

echo "Preview — files that will change:"
grep -rl "$OLD" "$VAULT" --include="*.md"

echo ""
read -p "Apply rename? (y/N) " confirm
if [ "$confirm" = "y" ]; then
  grep -rl "$OLD" "$VAULT" --include="*.md" | \
    xargs sed -i '' "s/${OLD}/${NEW}/g"
  echo "Done."
fi
```

---

### 6. Vault Statistics

Track vault growth over time.

**Shell script — Vault stats:**

```bash
#!/bin/bash
# vault-stats.sh — Print key vault metrics
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"

echo "=== Vault Statistics ==="
echo "Date: $(date '+%Y-%m-%d')"
echo ""

echo "Total notes:"
find "$VAULT" -name "*.md" -not -path "*/.obsidian/*" | wc -l

echo ""
echo "Notes by folder:"
for dir in "00 - Inbox" "01 - Projects" "02 - Areas" "03 - Resources" \
           "04 - Archive" "05 - Daily Systems" "06 - Knowledge" \
           "07 - Prompt Library" "08 - Automation" "09 - Visualization" \
           "10 - Meta"; do
  count=$(find "$VAULT/$dir" -name "*.md" 2>/dev/null | wc -l | tr -d ' ')
  echo "  $dir: $count"
done

echo ""
echo "Total word count:"
find "$VAULT" -name "*.md" -not -path "*/.obsidian/*" \
  -exec wc -w {} + | tail -1

echo ""
echo "Notes created in last 7 days:"
find "$VAULT" -name "*.md" -not -path "*/.obsidian/*" \
  -newer "$VAULT/.obsidian" -mtime -7 | wc -l
```

---

## Scheduled Maintenance

```mermaid
gantt
    title Vault Maintenance Schedule
    dateFormat  dddd
    axisFormat  %A

    section Daily
    Inbox review         :a1, Monday, 1d
    Task check           :a2, Monday, 1d

    section Weekly (Sunday)
    Run /vault-health    :b1, Sunday, 1d
    Orphan review        :b2, Sunday, 1d
    Stale note triage    :b3, Sunday, 1d
    Weekly synthesis     :b4, Sunday, 1d

    section Monthly (Last day)
    Full tag audit       :c1, after b4, 1d
    Archive stale notes  :c2, after c1, 1d
    Vault stats snapshot :c3, after c2, 1d
    Backup verification  :c4, after c3, 1d
```

### Weekly Maintenance Checklist

Run every Sunday alongside the weekly synthesis:

- [ ] Run `/vault-health` command
- [ ] Review orphan list — link, archive, or delete each
- [ ] Review stale notes — develop, merge, or archive each
- [ ] Check broken links report
- [ ] Clear any `00 - Inbox` items older than 7 days

### Monthly Maintenance Checklist

Run on the last day of each month:

- [ ] Run tag audit — identify and clean non-taxonomy tags
- [ ] Archive completed projects to `04 - Archive/`
- [ ] Run `vault-stats.sh` and record metrics in `10 - Meta/Vault Stats/`
- [ ] Verify backup integrity (iCloud, git, or manual)
- [ ] Review the `10 - Meta/` folder for outdated documentation

---

## Backup Strategy

> [!warning] Critical
> The vault is plain-text markdown — it can be backed up with any file sync tool. Use at least two backup methods.

**Recommended setup:**

1. **iCloud / Dropbox sync** — Continuous, automatic, versioned
2. **Git repository** — Periodic commits with meaningful messages, hosted on GitHub
3. **Manual export** — Monthly zip archive to external drive

**Git backup script:**

```bash
#!/bin/bash
# vault-backup.sh — Commit all vault changes to git
VAULT="/Users/lunio/Desktop/DevPortal/AI Brain"
cd "$VAULT"
git add -A
git commit -m "vault: auto-backup $(date '+%Y-%m-%d %H:%M')"
echo "Backup complete."
```

---

> [!success] Healthy Vault Indicators
> - Inbox stays near 0 (processed within 48 hours)
> - Less than 5% of notes are orphans
> - No `#status/seedling` notes older than 60 days
> - All notes have `type` and `created` frontmatter
> - Tag taxonomy has less than 10% drift

---

*Part of [[MOCs/Automation MOC]] · See also [[08 - Automation/Automation]] · [[10 - Meta/Vault Health/Vault Health Checks]]*
