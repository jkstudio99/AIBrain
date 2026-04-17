---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/visualization
  - topic/graph
  - status/growing
related:
  - "[[MOCs/Visualization MOC]]"
  - "[[03 - Resources/Core Plugins/Graph View Enhancers]]"
  - "[[09 - Visualization/Visualization]]"
  - "[[09 - Visualization/Knowledge Maps/Knowledge Maps Guide]]"
---

# Graph View Optimization

> [!abstract] Overview
> Obsidian's Graph View is a powerful diagnostic tool when configured deliberately. This guide covers color coding, force physics, filtering, and graph-driven workflows that turn the graph from decoration into a navigation and analysis system.

## Why Graph View Matters

The graph view renders your entire vault as a live force-directed network. Every note is a node; every wikilink is an edge. At a glance you can see:

- Which notes are hubs (many connections) — likely MOCs or evergreen notes
- Which notes are isolated (no connections) — orphans that need integration
- Which notes bridge two clusters — high-leverage "bridge notes"
- How dense vs. sparse different domains are

Without configuration, the graph is visually overwhelming and hard to read. With the right settings, it becomes a diagnostic instrument.

---

## Current Graph Configuration

### Color Groups

Assign colors by folder path or tag to make domains visually distinct at a glance.

| Color | Rule | Meaning |
|---|---|---|
| Blue | `path:MOCs` | Maps of Content — hubs |
| Green | `path:06 - Knowledge` | Knowledge notes |
| Yellow | `path:01 - Projects` | Active projects |
| Orange | `path:05 - Daily Systems` | Daily notes |
| Red | `tag:#status/seedling` | Immature notes needing attention |
| Purple | `path:07 - Prompt Library` | Prompts and tools |
| Teal | `path:03 - Resources` | Reference material |
| Gray | `path:04 - Archive` | Archived — de-emphasize |

> [!tip] Setup Steps
> In Graph View, open the settings panel (gear icon) → Appearance → Groups → Add group → enter the path or tag rule and select a color. Drag groups to set priority order (higher = takes precedence when multiple rules match).

### Force Physics Settings

| Setting | Recommended Value | Effect |
|---|---|---|
| Center force | 0.1 | Pulls everything toward center; reduce to spread out |
| Repel force | 150 | Pushes nodes apart; increase for less crowding |
| Link force | 1.0 | Strength of link attraction; default is fine |
| Link distance | 80 | Length of edges; increase to spread clusters |

> [!note] Tuning by vault size
> For vaults under 200 notes: center force 0.05, repel 120. For 200–500 notes: center 0.1, repel 150. For 500+ notes: center 0.15, repel 200. Large vaults need more repulsion or they collapse into a hairball.

### Filters

Use filters to remove noise and focus on structure:

- **Hide unresolved links** — removes ghost nodes for notes you have linked but not yet created. Reveals intended structure vs. actual structure.
- **Hide orphans** — useful for seeing the connected core of your vault
- **Show orphans only** — useful for finding notes that need integration
- **Tag filter** — show only notes with a specific tag (e.g., `#status/seedling`) for targeted maintenance sessions

---

## Reading the Graph

### Clusters

A cluster is a group of densely interconnected notes with fewer connections to other groups. Clusters represent **domains** — areas where you have developed knowledge. Healthy clusters:

- Have at least one high-degree hub (an MOC or major evergreen note)
- Have multiple notes at 2–5 connections (mid-tier integration)
- Have some notes at 1 connection (recent additions being integrated)

> [!warning] Unhealthy Cluster Signs
> - A cluster with no hub — needs an MOC created
> - A cluster that is completely isolated from the rest of the vault — may need a bridge note
> - A cluster where all notes connect to one node — "star pattern" indicates over-centralization; notes should also link to each other

### Bridges

A bridge note connects two otherwise-separate clusters. It has connections on both sides. These are among the most valuable notes in any vault because they represent cross-domain insights. When you find bridge notes:

1. Add them to relevant MOCs on both sides
2. Consider whether the insight deserves a dedicated evergreen note
3. Check if the two clusters should have more direct connections

### Orphans

Orphan notes (zero connections) fall into three categories:

1. **Recently captured** — in `00 - Inbox/`, waiting to be processed. Expected and normal.
2. **Forgotten notes** — old notes that were never linked. Need integration or archiving.
3. **Reference material** — some attachments and resources have no natural links. Consider whether they should.

> [!tip] Orphan Triage
> Run a filter showing only orphans. For each one: either add a wikilink from a relevant note, link it to a relevant MOC, or move it to `04 - Archive/`.

---

## Local Graph vs. Global Graph

### Global Graph

The default view — shows every note in the vault simultaneously.

**Best uses:**
- Weekly review health check
- Spotting new clusters that have formed
- Identifying large-scale orphan zones
- Validating that MOCs are properly connected

### Local Graph

Open via right-click on a note or the "Open local graph" command. Shows only the note you are currently reading plus its neighbors, at a configurable depth (1–5 hops).

**Best uses:**
- Navigating related notes while reading or writing
- Checking that a specific note is well-integrated
- Finding notes that are two hops away (often useful neighbors)
- Debugging a note that feels isolated

**Recommended local graph settings:**
- Depth: 2 (shows notes linked to your links — often where the interesting connections are)
- Show incoming and outgoing links
- Filter out archived notes

---

## Graph-Driven Workflows

### Cluster Discovery

1. Open global graph with color coding enabled
2. Look for dense areas you have not named
3. Create a new MOC for any cluster that lacks a hub note
4. Link the new MOC to `[[🏠 Home]]` and to relevant existing MOCs

### Gap Analysis

1. Filter the graph to show only a specific domain tag
2. Look at the edges of the cluster — what concepts are mentioned in notes but have no note of their own?
3. Those are your knowledge gaps — add them to `00 - Inbox/` as seeds to develop

### MOC Validation

1. Open local graph on a MOC note at depth 2
2. Every note in the MOC's list should appear as a node
3. Any note in the cluster that does NOT appear in the MOC list — check if it should be added
4. Any MOC entry that does NOT appear in the local graph — check if the note was renamed or deleted

### Orphan Integration Sprint

1. Enable "Show orphans only" filter
2. Export the list (screenshot or manual) — aim for a short session of 10–15 orphans
3. For each orphan: add it to the most relevant MOC, add at least one outgoing wikilink, add one incoming wikilink from a related note

---

## Practical Settings Recommendations

```
Graph View Settings (recommended starting point):
─────────────────────────────────────────────────
Filters:
  ☑ Show attachments: OFF (reduces clutter)
  ☑ Show existing files only: ON
  ☑ Show orphans: depends on workflow

Groups (in priority order):
  1. path:MOCs         → Blue     (hubs always visible)
  2. tag:#status/seedling → Red   (attention items)
  3. path:01 - Projects  → Yellow
  4. path:06 - Knowledge → Green
  5. path:03 - Resources → Teal
  6. path:05 - Daily Systems → Orange
  7. path:07 - Prompt Library → Purple
  8. path:04 - Archive   → Gray (lowest priority)

Forces:
  Center force:   0.10
  Repel force:    150
  Link force:     1.0
  Link distance:  80
```

> [!example] Saved Workspaces
> Use the Workspaces plugin to save different graph configurations:
> - **"Overview"** — full vault, all colors, no orphans hidden
> - **"Cleanup"** — orphans only, no color groups
> - **"Projects"** — filtered to `path:01 - Projects` and their neighbors

---

## Neon Glow Styling — สไตล์กราฟเรืองแสงแบบในภาพอ้างอิง

The glossy "knowledge-graph-as-starfield" look (bright nodes, soft glow, dark space background) is achieved with a CSS snippet plus tuned force physics — not a separate plugin. Three files do the work together:

| File | Role |
|---|---|
| `.obsidian/snippets/graph-glow.css` | Overrides node / line / text / background colors and adds a drop-shadow glow on the canvas |
| `.obsidian/graph.json` | Defines color groups (by folder + tag) and force settings that spread nodes out so the glow is visible |
| `.obsidian/appearance.json` | Lists `graph-glow` under `enabledCssSnippets` so the snippet is active |

### How the look is built

1. **Background** — the `.workspace-leaf-content[data-type="graph"] .view-content` selector paints a radial dark-blue-to-black gradient behind the canvas. That is what makes colored nodes "pop."
2. **Node colors** — Obsidian's graph renderer reads CSS variables like `.graph-view.color-fill`, `.graph-view.color-fill-focused`, `.graph-view.color-line`, and `.graph-view.color-text`. The snippet overrides each with neon-leaning values (`#7ec8e3` default node, `rgba(130,200,230,0.18)` lines, `rgba(235,240,255,0.88)` labels).
3. **Color groups** — `colorGroups` in `graph.json` maps folders / tags to bright decimal RGB values: MOCs = white, `06 - Knowledge` = cyan, `01 - Projects` = orange, `07 - Prompt Library` = magenta, `#status/seedling` = red, and so on. This is what gives each cluster its own hue instead of one uniform color.
4. **Outer glow** — `filter: drop-shadow(...)` applied to the graph `<canvas>` creates the soft halo around bright nodes.
5. **Physics** — repel strength raised (`18`), link distance extended (`280`), center strength softened (`0.35`), and `nodeSizeMultiplier` bumped to `1.35`. Nodes breathe apart instead of clumping, which is what lets the glow read.

> [!tip] Toggle the look
> Open **Settings → Appearance → CSS snippets** and flip `graph-glow` on or off. No restart needed — the graph restyles live.

### Tweak cheatsheet

- Want stronger glow? Increase the second `drop-shadow()` blur radius (`4px` → `8px`).
- Want a different cluster palette? Change the `rgb` decimal in `graph.json` — each value is `R*65536 + G*256 + B`.
- Want a lighter canvas? Edit the radial-gradient stops in the CSS — e.g. `#0e2038` → `#1a2e4a` for a softer navy.
- Want even more spread (close to the reference screenshot)? Push `repelStrength` to `25` and `linkDistance` to `350` for large vaults.

---

## Related Notes

- [[09 - Visualization/Visualization]] — Master overview of all visualization tools
- [[09 - Visualization/Knowledge Maps/Knowledge Maps Guide]] — Graph complements knowledge maps
- [[MOCs/Visualization MOC]] — Visualization hub
- [[03 - Resources/Core Plugins/Graph View Enhancers]] — Plugin documentation and advanced settings
