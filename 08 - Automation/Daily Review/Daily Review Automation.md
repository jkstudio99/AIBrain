---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/automation
  - topic/review
  - topic/claude
  - status/evergreen
related:
  - "[[MOCs/Automation MOC]]"
  - "[[MOCs/Daily Systems MOC]]"
  - "[[08 - Automation/Automation]]"
  - "[[08 - Automation/Summary Generation/Summary Generation]]"
  - "[[03 - Resources/Claude Integration/Commands Folder]]"
  - "[[05 - Daily Systems/Daily Notes/Daily Notes]]"
  - "[[07 - Prompt Library/Reflection/Reflection & Synthesis]]"
  - "[[CLAUDE.md]]"
aliases:
  - Daily Review
  - Daily Automation
---

# Daily Review Automation

The daily review is the keystone habit of a working knowledge system. This guide explains how the `/daily-review` command works, what Claude analyzes, how to customize the output, and how to connect it to longer-cycle synthesis.

> [!info] Purpose
> The daily review has two goals: (1) close the loop on today's captures and tasks, and (2) surface patterns and connections that aren't obvious in the moment.

---

## How `/daily-review` Works

The command is stored at `.claude/commands/daily-review.md` (mapped to the `daily-review` skill). When invoked, Claude:

1. **Reads today's daily note** from `05 - Daily Systems/Daily Notes/`
2. **Scans Inbox** for notes created or modified today (`00 - Inbox/`)
3. **Pulls open tasks** from all notes with `status:: todo` or `status:: in-progress`
4. **Checks weekly context** — what was the focus this week based on recent notes?
5. **Generates the review** in a structured format

---

## What Claude Analyzes

### Today's Notes

Claude reads every note with `created` or `modified` matching today's date. For each note it assesses:
- What type is it (fleeting, literature, project)?
- Does it have adequate frontmatter?
- Is there a wikilink opportunity to existing notes?
- Should it be processed further or can it stay as-is?

### Open Tasks

```dataview
TASK
FROM ""
WHERE !completed
AND (status = "todo" OR status = "in-progress")
SORT priority DESC, due ASC
```

Claude categorizes tasks by:
- **Due today or overdue** — needs immediate attention
- **In-progress** — ongoing work
- **Someday/maybe** — low priority or undated

### Captures from Inbox

For each item in `00 - Inbox/`:
- Is it ready to be processed (moved to a PARA folder)?
- Does it need more context before it can be filed?
- Is it a duplicate of an existing note?

### Weekly Pattern Context

Claude looks at notes from the past 7 days and identifies:
- Recurring topics (what have you been thinking about?)
- Unfinished threads (ideas started but not developed)
- Momentum (what's been most active?)

---

## The Review Output

A generated daily review note is saved to:
`05 - Daily Systems/Daily Notes/YYYY-MM-DD Review.md`

### Example Output

---

*Example: Daily Review for 2026-04-16*

```markdown
---
type: daily
created: "2026-04-16"
tags:
  - type/daily
  - status/growing
---

# Daily Review — April 16, 2026

## Today's Summary

Active day focused on vault automation. Created 6 new resource notes for
the 08 - Automation folder. Inbox cleared to 0.

## Notes Created Today

- [[08 - Automation/Automation]] — Master automation overview (evergreen)
- [[08 - Automation/Custom Skills/Custom Claude Skills]] — Skills guide
- [[08 - Automation/Auto-Tagging/Auto-Tagging & Linking]] — Tag system
- [[08 - Automation/Summary Generation/Summary Generation]] — Summaries
- [[08 - Automation/Daily Review/Daily Review Automation]] — This note
- [[08 - Automation/Vault Maintenance/Vault Maintenance Scripts]] — Health

## Open Tasks

### Due Today / Overdue
- [ ] Review Automation MOC and update links — due 2026-04-16

### In Progress
- [ ] Finalize [[01 - Projects/Vault Setup/Vault Setup]] — in-progress

## Patterns This Week

The dominant theme this week has been **vault infrastructure** — building
the automation and prompt systems that will support future knowledge work.
Less input (reading, capturing) than usual; more processing and
meta-work. This is appropriate for a setup week.

**Unfinished threads to revisit:**
- The connection between [[08 - Automation/Custom Skills/Custom Claude Skills]]
  and actual skill deployment hasn't been tested yet
- [[07 - Prompt Library/Thinking Tools/Thinking Tools]] references commands
  that aren't fully written

## Suggested Connections

- [[08 - Automation/Automation]] and [[MOCs/Automation MOC]] — MOC needs
  a links section update to reflect the new sub-notes
- [[10 - Meta]] — Consider a meta note on "vault setup philosophy"

## Reflection

**What went well:** Systematic file creation with consistent frontmatter.
**What to improve:** Need to test the commands in practice, not just document them.
**Tomorrow's focus:** Begin using `/daily-review` daily instead of just documenting it.
```

---

## Customizing the Review Prompt

The review prompt at `.claude/commands/daily-review.md` (or the `daily-review` skill) can be customized. Key parameters:

### Adjust Scope

Control what Claude reads:

```markdown
## Scope
- Today's daily note: YES
- Inbox items: YES (limit 10)
- Open tasks: YES (priority HIGH and MEDIUM only)
- Notes from past 7 days: YES
- Completed tasks: NO
```

### Adjust Output Format

Customize the sections you want:

```markdown
## Required Sections
1. Today's Summary (3 sentences max)
2. Notes Created
3. Open Tasks (due today only)
4. One Pattern or Insight

## Optional Sections (only include if relevant)
- Suggested Connections
- Evening Reflection
```

### Adjust Tone

Add a tone directive at the top of the prompt:

```markdown
Tone: Direct and concise. No fluff. Use bullet points over prose wherever
possible. Reflection section should be honest, not performative.
```

---

## Connecting Daily Review to Weekly Synthesis

The daily review feeds directly into the weekly synthesis via the `/weekly-synthesis` skill.

```
Monday daily review
Tuesday daily review    ──→  Weekly Synthesis  ──→  Monthly Review
Wednesday daily review           (Sunday)             (Month end)
...
```

### What Weekly Synthesis Draws From

The weekly synthesis skill reads all daily review notes from the past 7 days and:
- Identifies the week's dominant themes
- Surfaces the most important captures worth developing
- Checks progress on active projects
- Generates the weekly note in `05 - Daily Systems/Weekly Reviews/`

### Ensuring Continuity

For the weekly synthesis to work well, daily reviews should:
- Always include the "Patterns" section (this is the main feed)
- Use consistent wikilink formatting for note titles
- Tag completed tasks with `status:: done`

> [!tip] Daily → Weekly Habit
> Even a 5-minute daily review (run `/daily-review`, skim output, add one reflection sentence) is enough to make the weekly synthesis meaningful. The key is consistency, not depth.

---

## Troubleshooting

| Problem | Likely Cause | Fix |
|---|---|---|
| Review misses today's notes | Notes have wrong `created` date | Check frontmatter date format |
| Tasks list is too long | Old completed tasks not marked done | Bulk-close completed tasks |
| Patterns section is generic | Not enough notes to find patterns | Keep capturing; improves over time |
| Review takes too long | Too many Inbox items to process | Clear Inbox before running review |

---

*Part of [[MOCs/Automation MOC]] · See also [[MOCs/Daily Systems MOC]] · [[08 - Automation/Automation]]*
