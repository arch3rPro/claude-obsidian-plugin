---
description: Discover semantically related notes in the vault and present connections with mind mapping visualization
---

# Find Related Notes

Help the user discover semantically related notes in their Obsidian vault and visualize connections.

## Process

### 1. Understand the Query
- Parse the user'\''s search query or topic
- Identify key concepts, themes, and keywords
- Extract any specific note titles mentioned

### 2. Search Strategy

Use these approaches to find related notes:

**Approach A: Direct Keyword Search**
- Search for exact matches of key terms in note titles
- Look for matching tags
- Check frontmatter properties

**Approach B: Semantic Analysis**
- Identify notes discussing similar concepts
- Find notes with overlapping themes
- Look for notes in the same subject area

**Approach C: Link Traversal**
- Start from existing notes the user mentions
- Follow wikilinks `[[Note]]` to find connected notes
- Explore backlinks (notes linking to current note)

### 3. Prioritization

Rank related notes by relevance:
1. **Direct matches** (exact keyword/title matches) - High priority
2. **Semantic similarity** (same themes, concepts) - Medium priority
3. **Linked notes** (connected via wikilinks) - Medium-High priority
4. **Tag-based** (shared tags) - Medium priority
5. **Related by property** (same categories, etc.) - Low-Medium priority

### 4. Presentation Format

Present results in this structure:

```
## Found N Related Notes

### Direct Matches (High Relevance)
- [[Note Title 1]] - Brief explanation of relevance
- [[Note Title 2]] - Brief explanation of relevance

### Semantic Matches (Medium Relevance)
- [[Note Title 3]] - Shared concept: X
- [[Note Title 4]] - Shared concept: Y

### Linked Notes (Medium-High Relevance)
- [[Note Title 5]] - Connected via: X
- [[Note Title 6]] - Connected via: Y

### Tag-Based Matches
- [[Note Title 7]] - Shared tags: #tag1, #tag2

## Visualization

### Connection Map
```
[Central Topic: User'\''s query]
├── [Direct Match] → [[Note 1]]
├── [Semantic] → [[Note 2]]
├── [Semantic] → [[Note 3]]
├── [Linked] → [[Note 4]]
└── [Tag-based] → [[Note 5]]
```

## Next Steps

Based on the related notes, suggest:
1. **New connections**: Notes the user might want to link to
2. **Gaps**: Topics that could be better documented
3. **Themes**: Recurring themes across related notes
4. **Actions**: Possible next steps or research directions

If no related notes are found, suggest:
1. Broader search terms
2. Different keywords or synonyms
3. Creating a new note on the topic
