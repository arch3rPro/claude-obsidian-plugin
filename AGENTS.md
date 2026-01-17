# AGENTS.md - Obsidian Assistant Plugin Development Guide

This plugin extends Claude Code for Obsidian note management. It uses pure Markdown/JSON configuration - no compilation or build steps required.

## Development Commands

### Local Testing
```bash
# Test plugin without installation
claude --plugin-dir .

# Multiple plugins
claude --plugin-dir ./plugin1 --plugin-dir ./plugin2

# Debug mode (shows loading errors)
claude --debug --plugin-dir .
```

### Validation
```bash
# Validate plugin/marketplace structure
claude plugin validate .

# From within Claude Code
/plugin validate .
```

### Troubleshooting
```bash
# Clear plugin cache
rm -rf ~/.claude/plugins/cache
```

## Plugin Structure

**Critical Rule**: Only `plugin.json` goes inside `.claude-plugin/`. All other directories must be at plugin root.

```
claude-obsidian-plugin/
├── .claude-plugin/
│   └── plugin.json          # REQUIRED: Plugin manifest
├── commands/                    # Optional: Slash commands (.md files)
├── agents/                      # Optional: Agent definitions (.md files)
├── skills/                      # Optional: Agent Skills
│   ├── json-canvas/
│   │   └── SKILL.md
│   ├── obsidian-bases/
│   │   └── SKILL.md
│   └── obsidian-markdown/
│       └── SKILL.md
├── hooks/                       # Optional: Event handlers
│   └── hooks.json
├── .mcp.json                   # Optional: MCP server configs
├── .lsp.json                   # Optional: LSP server configs
└── README.md
```

## Code Style Guidelines

### Naming Conventions
- **Plugin names**: kebab-case, lowercase letters, numbers, hyphens only (e.g., `obsidian-assistant`)
- **Agent names**: lowercase, numbers, hyphens only (e.g., `content-creator`)
- **Skill names**: lowercase, numbers, hyphens only, max 64 chars (e.g., `json-canvas`)
- **Command names**: kebab-case `.md` filenames (e.g., `create-note.md`)

### File Formats
- **plugin.json**: JSON with required `name`, `description`, `version`
- **Commands/Agents**: Markdown with YAML frontmatter
- **Skills**: Markdown with YAML frontmatter, must be `SKILL.md` (uppercase)
- **Hooks**: JSON configuration
- **MCP/LSP configs**: JSON with server definitions

### YAML Frontmatter Format
```yaml
---
name: plugin-name          # lowercase, hyphens, max 64 chars
description: Clear description of what this does and when to use it
allowed-tools: Read, Grep    # Optional: Tools without permission
model: claude-sonnet-4-20250514  # Optional: Specific model
context: fork                   # Optional: Run in isolated context
---
```

## Skills Development

### Progressive Disclosure
Keep `SKILL.md` under 500 lines. Move detailed docs to separate files:
```
skill-name/
├── SKILL.md           # Required: Overview and navigation
├── reference.md       # Optional: Detailed API docs
├── examples.md        # Optional: Usage examples
└── scripts/
    └── helper.py    # Optional: Executed, not loaded (zero-cost)
```

### Skill Description Pattern
```
[Action] and [secondary action] [file type/format] with [features]. Use when working with [file types], [use cases], or when user mentions [trigger keywords].
```

Example:
```
Create and edit JSON Canvas files (.canvas) with nodes, edges, groups, and connections. Use when working with .canvas files, creating visual canvases, mind maps, flowcharts, or when the user mentions Canvas files in Obsidian.
```

## Hook Exit Codes
- `0` - Success, continue
- `1` - Error, block with error message
- `2` - Block with custom message (stderr output)

## Environment Variables
- `$CLAUDE_PROJECT_DIR` - Current project directory
- `$CLAUDE_PLUGIN_ROOT` - Plugin installation directory (use for plugin-relative paths)
- `${CLAUDE_SESSION_ID}` - Current session ID (in skills)

## String Substitutions
- `$ARGUMENTS` - All arguments after command name
- `$1`, `$2`, etc. - Individual positional parameters
- `$FILE` - File path (in hooks: `.tool_input.file_path`)

## Best Practices

1. **Testing**: Always test with `--plugin-dir` before distribution
2. **Validation**: Use `claude plugin validate` to catch structure errors
3. **Documentation**: Include README.md with installation instructions
4. **Versioning**: Use semantic versioning (e.g., `1.0.0`)
5. **Skills**: Write detailed descriptions for automatic discovery
6. **Security**: Review hooks before registering (run with your credentials)
7. **Progressive Disclosure**: Keep SKILL.md concise, use supporting files
8. **References**: Link to official documentation in skill files

## Plugin Invocation
Commands: `/plugin-name:command-name arguments`
Agents: Automatic delegation based on description
Skills: Automatic discovery based on description
