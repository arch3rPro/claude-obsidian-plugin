---
description: Create concise summaries for existing notes in bullet, paragraph, or outline format
---

# Summarize Note

Create a concise summary of the provided note. Follow these guidelines:

## Summary Formats

Based on user preference or note content, choose the most appropriate format:

### 1. Bullet Format
- Use bullet points for key ideas
- Group related points together
- Keep each point concise (1-2 sentences max)
- Example:
  ```
  - Main topic: Brief explanation
  - Point 1: Key detail
  - Point 2: Another key detail
  ```

### 2. Paragraph Format
- Write 1-2 paragraphs
- Focus on main themes and key takeaways
- Maintain flow between ideas
- Keep total length under 150 words

### 3. Outline Format
```
# Note Title

## Main Themes
- Theme 1: Brief description
- Theme 2: Brief description

## Key Points
1. First major point
2. Second major point
3. Third major point

## Conclusion
Brief wrap-up of the main message
```

## Extraction Guidelines

When summarizing, focus on:
1. **Main topic**: What is this note primarily about?
2. **Key concepts**: What are the core ideas?
3. **Important details**: What information is essential?
4. **Action items**: Are there any tasks or next steps?
5. **Connections**: How does this relate to other notes?

## Output

Return the summary in the requested format. If no format is specified, ask the user which format they prefer:
- Bullet format (concise, scannable)
- Paragraph format (flowing text)
- Outline format (structured hierarchy)

Provide the summary clearly labeled with the format type.
