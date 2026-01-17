---
description: Generate new Obsidian notes based on prompts with auto-structured formatting and metadata generation
---

# Create AI Note

Create a well-structured Obsidian note based on the user'\''s prompt. Follow these guidelines:

## Structure

1. **Title**: Create a clear, descriptive title (H1 heading)
2. **Frontmatter**: Include YAML frontmatter with:
   - `title`: Note title
   - `date`: Current date (YYYY-MM-DD)
   - `tags`: Relevant tags for the note
   - `created`: Timestamp when note was created
   - Optional: `aliases`, `cssclasses`, custom properties

3. **Content**: Organize content with:
   - Clear introduction
   - Main sections with H2/H3 headings
   - Bullet points or numbered lists for details
   - Callouts for important notes
   - Relevant internal links using wikilinks `[[Note Name]]`
   - Code blocks with language specifications when applicable

## Formatting Rules

- Use **Obsidian Flavored Markdown** syntax
- Include **wikilinks** to connect related notes
- Add **callouts** for important information:
  ```
  > [!tip] Helpful hint
  > [!note] Important note
  > [!warning] Warning
  ```
- Use **code blocks** with language specification for any code examples
- Add **tags** in content using `#tag` format (in addition to frontmatter)

## Metadata Generation

Automatically generate relevant tags based on:
- Topic keywords
- Domain/subject area
- Related concepts

Create 3-5 descriptive tags for better discoverability.

## Output

Return the complete note content ready to be written to a file. Ask the user if they want to:
1. Save it to a specific file path
2. Preview it before saving
3. Create additional related notes
