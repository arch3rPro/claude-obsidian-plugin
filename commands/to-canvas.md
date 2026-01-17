---
description: Transform notes into visual representations using JSON Canvas format with mind map, flowchart, or timeline layouts
---

# Convert to Canvas

Transform a note or set of notes into a visual Canvas representation in Obsidian.

## Input Acceptance

Accept these input types:
1. **Single note path**: `/obsidian-assistant:to-canvas My Note.md`
2. **Multiple notes**: User describes which notes to include
3. **Content**: Direct text content to visualize

## Layout Types

Offer these layout options or choose the most appropriate based on content:

### Type 1: Mind Map Layout
Best for: Brainstorming, concept mapping, exploring ideas

Structure:
```
Central Topic (center)
├── Related Concept 1 (left)
├── Related Concept 2 (right)
├── Related Concept 3 (top)
└── Related Concept 4 (bottom)
```

Node positioning:
- Central node: Center of canvas (x: 0, y: 0)
- Primary branches: 250-300px from center
- Secondary branches: 150-200px from branch nodes
- Color coding: Use different colors for thematic grouping

### Type 2: Flowchart Layout
Best for: Processes, workflows, decision trees, algorithms

Structure:
```
[Start] → [Decision] → [Branch 1] → [End]
                         └→ [Branch 2] → [End]
```

Edge styling:
- Use arrow endpoints for flow direction
- Color edges to indicate different paths
- Add labels on edges for conditions or transitions

### Type 3: Timeline Layout
Best for: Chronological events, project milestones, history

Structure:
```
Time →

[Event 1] → [Event 2] → [Event 3] → [Event 4]
```

Positioning:
- Horizontal layout (time flows left to right)
- Equal spacing between nodes (150-200px)
- Add timestamp labels or descriptions

### Type 4: Grouped Layout
Best for: Organizing related notes, topic clusters, research notes

Structure:
```
[Group: Topic A]
├── Note 1
├── Note 2
└── Note 3

[Group: Topic B]
├── Note 4
└── Note 5
```

## Canvas Generation Rules

1. **Node Types**
   - Use `text` nodes for content
   - Use `file` nodes to link to existing notes
   - Use `group` nodes for organizing sections
   - Use `link` nodes for external resources

2. **Node Attributes**
   - All nodes require: `id`, `type`, `x`, `y`, `width`, `height`
   - Add `color` for visual grouping (preset 1-6 or hex)
   - Text nodes include: `text` with Markdown content
   - File nodes include: `file` path to note

3. **Edge Rules**
   - Each edge requires: `id`, `fromNode`, `toNode`
   - Optional: `fromSide`, `toSide` for cleaner connections
   - Optional: `fromEnd`, `toEnd` (none/arrow)
   - Optional: `color`, `label` for additional context

4. **Positioning**
   - Avoid overlaps (use sensible spacing)
   - Group related items together
   - Center main concept or first step
   - Leave room for expansion

5. **ID Generation**
   - Generate unique 16-character hex IDs for all nodes and edges
   - Format: lowercase a-z and 0-9

## Output Format

Return the complete JSON Canvas structure:

```json
{
  "nodes": [
    {
      "id": "unique-16-char-id",
      "type": "text|file|link|group",
      "x": 0,
      "y": 0,
      "width": 300,
      "height": 100,
      "color": "1",
      "text": "Markdown content",
      "file": "Path/to/note.md",
      "label": "Group label"
    }
  ],
  "edges": [
    {
      "id": "unique-16-char-id",
      "fromNode": "node-id",
      "toNode": "node-id",
      "fromSide": "top|right|bottom|left",
      "toSide": "top|right|bottom|left",
      "fromEnd": "none|arrow",
      "toEnd": "none|arrow",
      "color": "1",
      "label": "Edge label"
    }
  ]
}
```

## Saving Options

After generating Canvas, offer to:
1. **Save as .canvas file** - Create new Canvas file in vault
2. **Overwrite existing** - Replace an existing Canvas
3. **Preview structure** - Show node count, edge count, layout type

## Additional Features

Offer to add:
- **Callout nodes** - Visual markers for important points
- **Image nodes** - Embed images or screenshots
- **External link nodes** - References to web resources
- **Color themes** - Apply consistent color scheme
