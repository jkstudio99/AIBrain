---
type: resource
created: "2026-04-16"
tags:
  - type/resource
  - area/plugins
  - topic/canvas
related:
  - "[[MOCs/Visualization MOC]]"
---

# 🔗 Advanced URI & Canvas

## Obsidian URI Scheme
Obsidian supports deep linking via `obsidian://` URIs — useful for automation, bookmarks, and cross-app integration.

### Basic URIs
```
obsidian://open?vault=AI%20Brain&file=🏠%20Home
obsidian://new?vault=AI%20Brain&file=00%20-%20Inbox/Quick%20Note&content=Hello
obsidian://search?vault=AI%20Brain&query=tag:status/seedling
obsidian://open?vault=AI%20Brain&file=MOCs/Knowledge%20MOC
```

### Advanced URI Plugin
Extends the URI scheme with more actions:
```
obsidian://advanced-uri?vault=AI%20Brain&filepath=01%20-%20Projects/My%20Project.md&heading=Tasks
obsidian://advanced-uri?vault=AI%20Brain&daily=true
obsidian://advanced-uri?vault=AI%20Brain&commandid=app:open-settings
```

### Use Cases
- **Quick capture shortcuts**: macOS/iOS Shortcuts that create inbox notes
- **Cross-app links**: Link from task managers, calendars to specific notes
- **Automation**: Scripts that open/create notes programmatically
- **Dashboard buttons**: Clickable links in MOC notes

## Canvas

### What is Canvas?
Obsidian Canvas (`.canvas` files) provides an infinite spatial workspace for:
- Visual brainstorming
- Connecting ideas spatially
- Project planning boards
- Mind mapping
- Research overview maps

### Canvas File Format (JSON Canvas)
```json
{
  "nodes": [
    {
      "id": "node1",
      "type": "text",
      "x": 0, "y": 0,
      "width": 300, "height": 200,
      "text": "# Core Idea\nThis is the main concept."
    },
    {
      "id": "node2",
      "type": "file",
      "x": 400, "y": 0,
      "width": 300, "height": 200,
      "file": "06 - Knowledge/Evergreen Notes/My Note.md"
    }
  ],
  "edges": [
    {
      "id": "edge1",
      "fromNode": "node1",
      "toNode": "node2",
      "label": "supports"
    }
  ]
}
```

### Node Types
| Type | Description |
|------|-------------|
| `text` | Markdown text block |
| `file` | Embedded note from vault |
| `link` | External URL embed |
| `group` | Visual grouping container |

### Canvas Workflows

#### Research Overview
1. Create `09 - Visualization/Canvas Workspaces/Research - [Topic].canvas`
2. Add literature notes as file nodes
3. Add text nodes for your own thoughts
4. Draw edges showing relationships
5. Group by theme or sub-topic

#### Project Planning
1. Create canvas for the project
2. Add columns: Backlog → In Progress → Done
3. Use text nodes as task cards
4. Group by priority or milestone

#### Knowledge Map
1. Start with a central concept
2. Branch out to related evergreen notes
3. Color-code by domain/area
4. Add edge labels for relationship type

### Creating Canvas with Claude
Use the `json-canvas` skill:
```
"Create a canvas file mapping the connections between my evergreen notes 
about [topic]. Use the json-canvas format."
```

## 🔗 Related
- [[MOCs/Visualization MOC]]
- [[09 - Visualization/Canvas Workspaces/Canvas Workspaces Guide]]
- [[03 - Resources/Core Plugins/Graph View Enhancers]]
