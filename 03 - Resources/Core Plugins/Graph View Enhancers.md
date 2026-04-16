---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/graph
related:
  - "[[MOCs/Visualization MOC]]"
---

# 🕸️ Graph View Enhancers

## Overview
The Graph View visualizes connections between notes as an interactive node-link diagram. It's the visual heartbeat of a Zettelkasten vault.

## Current Graph Configuration
Color groups are configured in `.obsidian/graph.json`:

| Group | Color | Query |
|-------|-------|-------|
| Projects | Blue | `path:"01 - Projects"` |
| Knowledge | Green | `path:"06 - Knowledge"` |
| Daily Systems | Orange | `path:"05 - Daily Systems"` |
| MOCs | Red | `path:"MOCs"` |

## Graph View Controls

### Filters
| Filter | Effect |
|--------|--------|
| Search | Filter to notes matching query |
| Tags | Show/hide tag nodes |
| Attachments | Show/hide attachment nodes |
| Orphans | Show/hide unlinked notes |
| Existing files only | Hide unresolved links |

### Display
| Setting | Recommended |
|---------|-------------|
| Arrows | On (shows link direction) |
| Text fade | 0 (always show titles) |
| Node size | 1 (scale by link count) |

### Forces
| Force | Value | Effect |
|-------|-------|--------|
| Center | 0.5 | How strongly nodes pull to center |
| Repel | 10 | How much nodes push apart |
| Link | 1 | How strongly linked nodes pull together |
| Distance | 250 | Ideal distance between linked nodes |

## Local Graph View
Open on any note to see its immediate neighborhood:
- `Ctrl/Cmd + P` → "Open local graph"
- Shows only notes directly connected to current note
- Adjust depth to see 2nd and 3rd degree connections

### Best Uses for Local Graph
- **MOC notes**: See all topics in an area
- **Evergreen notes**: Discover connection clusters
- **Project notes**: View related resources
- **Hub detection**: Find notes with many connections

## Graph View Strategies

### 1. Cluster Discovery
1. Open global graph
2. Remove filter (show all)
3. Look for dense clusters — these are well-connected topics
4. Look for isolated nodes — these need more links
5. Look for bridge notes — connecting different clusters

### 2. Knowledge Gap Analysis
1. Filter by `path:"06 - Knowledge"`
2. Look for disconnected subgraphs
3. These represent knowledge silos needing bridges
4. Create synthesis notes to connect them

### 3. MOC Validation
1. Open local graph on a MOC
2. Check that expected notes are linked
3. Missing connections = notes that should be added to the MOC

### 4. Orphan Rescue
1. Filter to show orphans only
2. For each orphan, decide: link it, or archive it
3. Goal: zero orphan notes (except templates)

## Graph View Enhancer Plugins
Consider these community plugins:
- **Graph Analysis**: Add centrality metrics, bridge detection
- **Juggl**: Alternative 3D graph with more layout options
- **Breadcrumbs**: Hierarchical navigation between notes

## 🔗 Related
- [[09 - Visualization/Graph View Optimization]]
- [[09 - Visualization/Knowledge Maps/Knowledge Maps Guide]]
- [[MOCs/Visualization MOC]]
