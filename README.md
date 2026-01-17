<h1 align="center">🤖 Obsidian Assistant</h1>

<p align="center">
  <em>AI-powered Obsidian note and knowledge management assistant</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-v0.2.0-blue.svg" alt="Version v0.2.0">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
  <img src="https://img.shields.io/badge/Obsidian-Plugin-blue.svg" alt="Obsidian Plugin">
  <img src="https://img.shields.io/badge/Claude-Compatible-purple.svg" alt="Claude Compatible">
</p>

<p align="center">
  <a href="README.md"><strong>English</strong></a> |
  <a href="README_ZH.md"><strong>简体中文</strong></a>
</p>

## Overview

Obsidian Assistant is a plugin for Claude Code that enhances your Obsidian experience with AI-powered features. It provides intelligent commands, specialized agents, and powerful skills for handling notes, structured data, and visual representations.

## ✨ Features

### 📝 Commands

| Command | Description | Key Features |
|---------|-------------|--------------|
| **Create AI Note**<br>`/obsidian-assistant:create-note` | Generate new Obsidian notes based on prompts | • Auto-structured formatting<br>• Metadata generation<br>• Content optimization |
| **Summarize Note**<br>`/obsidian-assistant:summarize` | Create concise summaries for existing notes | • Bullet format<br>• Paragraph format<br>• Outline format |
| **Find Related Notes**<br>`/obsidian-assistant:find-related` | Discover semantically related notes | • Semantic search<br>• Connection discovery<br>• Mind mapping |
| **Generate Outline**<br>`/obsidian-assistant:outline` | Create structured outlines for any topic | • Markdown output<br>• Base format<br>• Canvas format |
| **Convert to Canvas**<br>`/obsidian-assistant:to-canvas` | Transform notes into visual representations | • Mind map layout<br>• Flowchart layout<br>• Timeline layout |

### 🤖 Agents

| Agent | Specialization | Skills Used |
|-------|----------------|-------------|
| **Content Creator** | Create well-structured Obsidian notes | `obsidian-markdown`<br>`obsidian-bases` |
| **Visual Architect** | Create visual representations using Canvas | `json-canvas` |
| **Knowledge Miner** | Discover connections and insights in knowledge base | `obsidian-markdown` |

### 🛠️ Skills

| Skill | Description |
|-------|-------------|
| **JSON Canvas** | Create and edit visual Canvas files (`.canvas`) |
| **Obsidian Bases** | Handle structured data views and databases |
| **Obsidian Markdown** | Create and edit Obsidian-style Markdown |

### 🔗 Hooks

| Hook | Trigger | Action |
|------|---------|--------|
| **On File Create** | New file creation | Apply templates and properties |
| **On File Modify** | Significant file modification | Suggest related notes |
| **On Daily Note** | Daily note creation | Enhance daily note management |

## 📦 Installation

### Method 1: Plugin Marketplace

```bash
# 1. Add plugin marketplace
/plugin marketplace add arch3rPro/claude-obsidian-plugin

# 2. Install plugin
/plugin install claude-obsidian-plugin@arch3rPro-claude-obsidian-plugin
```

### Method 2: Interactive Plugin Manager

1. Run `/plugin` to open the plugin manager
2. Navigate to the **Discover** tab
3. Find **"Claude Obsidian Plugin"** in the list
4. Click **Install** and select your preferred scope:
   - 🔹 **User** (Available in all projects)
   - 🔸 **Project** (Available only in current project)
   - ⬇️ **Local** (Available only to you)

## 🚀 Usage

### Basic Commands

Use commands with standard syntax:

```bash
/obsidian-assistant:<command-name> <arguments>
```

**Examples:**

```bash
# Create a new note
/obsidian-assistant:create-note Write a note about effective meeting strategies

# Summarize an existing note
/obsidian-assistant:summarize "My Meeting Notes.md"

# Find related notes
/obsidian-assistant:find-related knowledge management

# Generate an outline
/obsidian-assistant:outline artificial intelligence fundamentals

# Convert to visual Canvas
/obsidian-assistant:to-canvas project roadmap mind map
```

### Access Specialized Agents

```bash
# Content Creator agent
/agents content-creator

# Visual Architect agent
/agents visual-architect

# Knowledge Miner agent
/agents knowledge-miner
```

## ⚙️ Configuration

The plugin supports various configuration options to customize behavior:

| Configuration | Description |
|---------------|-------------|
| **Default Agent** | Preferred agent for default interactions |
| **Auto Tagging** | Automatically generate tags for new notes |
| **Daily Note Template** | Custom template for daily notes |
| **Related Notes** | Settings for connection detection |
| **Content Generation** | Preferences for AI-generated content |
| **Canvas Layout** | Default layout for visual representations |
| **Privacy Options** | Control data processing and storage |

## 🤝 Contributing

Contributions are welcome! Feel free to submit:

- 🐛 **Bug Reports**
- 💡 **Feature Requests**
- 📝 **Documentation Improvements**
- 🔧 **Pull Requests**

## 📄 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for details.
