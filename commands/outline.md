---
description: Generate structured outlines for any topic in Markdown, Canvas, or Base format
---

# Generate Outline

Create a well-structured outline for any topic provided by the user.

## Output Formats

Based on user preference, generate in one of these formats:

### Format 1: Markdown Outline
```
# [Topic Title]

## Section 1
### Subsection 1.1
- Point 1
- Point 2

### Subsection 1.2
- Point 3

## Section 2
- Major point 1
- Major point 2
```

### Format 2: Obsidian Base Format
Create an outline that can be used as a structure for related notes:
```
# [Topic Title] Outline

## Main Categories
- Category 1
- Category 2
- Category 3

## Detailed Breakdown
### Category 1
- Sub-item 1
- Sub-item 2

### Category 2
- Sub-item 1
```

### Format 3: Canvas Format (JSON Canvas)
Generate a visual mind map structure as JSON Canvas:
```json
{
  "nodes": [
    {
      "id": "central-topic",
      "type": "text",
      "text": "# Main Topic",
      "x": 0,
      "y": 0,
      "width": 300,
      "height": 100,
      "color": "4"
    },
    {
      "id": "section-1",
      "type": "text",
      "text": "## Section 1",
      "x": -100,
      "y": 150,
      "width": 250,
      "height": 80
    },
    {
      "id": "section-2",
      "type": "text",
      "text": "## Section 2",
      "x": 350,
      "y": 150,
      "width": 250,
      "height": 80
    }
  ],
  "edges": [
    {
      "id": "edge-1",
      "fromNode": "central-topic",
      "toNode": "section-1",
      "fromSide": "bottom",
      "toSide": "left"
    },
    {
      "id": "edge-2",
      "fromNode": "central-topic",
      "toNode": "section-2",
      "fromSide": "bottom",
      "toSide": "right"
    }
  ]
}
```

## Structure Guidelines

### Depth and Hierarchy
- Use 2-4 levels of hierarchy (H1 → H2 → H3 → H4)
- Keep sections balanced (3-6 main sections, 2-4 subsections each)
- Maintain logical flow and grouping

### Content Principles
- Each point should be a single, complete thought
- Use parallel structure (items at same level should be similar scope)
- Progressive elaboration (broad concepts → specific details)

### Organization
```
1. [Introduction/Hook]
   1.1. [Context/Background]
   1.2. [Purpose/Goal]

2. [Main Sections]
   2.1. [Section Topic]
       - [Detail 1]
       - [Detail 2]
   2.2. [Section Topic]
       - [Detail 3]
       - [Detail 4]

3. [Conclusion/Summary]
   3.1. [Key Takeaways]
   3.2. [Next Steps]
```

## Interactive Elements

For certain outline types, include interactive elements:

### Task Checklists
```
## Tasks
- [ ] Task 1: Description
- [ ] Task 2: Description
- [x] Task 3: Description
```

### Callouts
```
> [!info] Important Note
This section requires additional research.

> [!tip] Best Practice
Use bullet points for better scanability.

> [!warning] Consideration
This topic is complex and may need to be split.
```

### Code Blocks
When outlining technical topics:
```language
// Example code or configuration
```

## Output Format Selection

Ask the user which format they prefer:
1. **Markdown** - Best for text documentation and note structure
2. **Canvas** - Best for visual mind maps and brainstorming
3. **Base** - Best for task lists and project organization

Default to Markdown if not specified.

## Additional Options

After generating outline, offer to:
1. **Expand specific sections** with more detail
2. **Convert to Canvas** with proper node layout
3. **Create a new note** with the outline
4. **Link to existing notes** based on outline topics
