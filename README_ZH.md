<h1 align="center">🤖 Obsidian Assistant</h1>

<p align="center">
  <em>基于 AI 的 Obsidian 笔记和知识管理助手</em>
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

## 概述

Obsidian 助手是 Claude Code 的一个插件，通过 AI 驱动的功能增强您的 Obsidian 使用体验。它提供了智能命令、专业代理和强大技能，用于处理笔记、结构化数据和可视化表示。

## ✨ 功能特性

### 📝 命令

| 命令 | 描述 | 主要功能 |
|------|------|----------|
| **创建 AI 笔记**<br>`/obsidian-assistant:create-note` | 基于提示生成新的 Obsidian 笔记 | • 自动结构化格式<br>• 元数据生成<br>• 内容优化 |
| **总结笔记**<br>`/obsidian-assistant:summarize` | 为现有笔记创建简洁摘要 | • 要点格式<br>• 段落格式<br>• 大纲格式 |
| **查找相关笔记**<br>`/obsidian-assistant:find-related` | 发现语义相关的笔记 | • 语义搜索<br>• 连接发现<br>• 思维映射 |
| **生成大纲**<br>`/obsidian-assistant:outline` | 为任何主题创建结构化大纲 | • Markdown 输出<br>• Base 格式<br>• Canvas 格式 |
| **转换为 Canvas**<br>`/obsidian-assistant:to-canvas` | 将笔记转换为可视化表示 | • 思维导图布局<br>• 流程图布局<br>• 时间线布局 |

### 🤖 代理

| 代理 | 专业领域 | 使用的技能 |
|------|----------|-----------|
| **内容创建者** | 创建结构良好的 Obsidian 笔记 | `obsidian-markdown`<br>`obsidian-bases` |
| **视觉架构师** | 使用 Canvas 创建可视化表示 | `json-canvas` |
| **知识挖掘者** | 在知识库中发现连接和洞察 | `obsidian-markdown` |

### 🛠️ 技能

| 技能 | 描述 |
|------|------|
| **JSON Canvas** | 创建和编辑可视化 Canvas 文件 (`.canvas`) |
| **Obsidian Bases** | 处理结构化数据视图和数据库 |
| **Obsidian Markdown** | 创建和编辑 Obsidian 风格的 Markdown |

### 🔗 钩子

| 钩子 | 触发时机 | 操作 |
|------|----------|------|
| **文件创建时** | 新文件创建 | 应用模板和属性 |
| **文件修改时** | 文件显著修改 | 建议相关笔记 |
| **每日笔记时** | 每日笔记创建 | 增强每日笔记管理

## 📦 安装

### 方法 1: 插件市场

```bash
# 1. 添加插件市场
/plugin marketplace add arch3rPro/claude-obsidian-plugin

# 2. 安装插件
/plugin install claude-obsidian-plugin@arch3rPro-claude-obsidian-plugin
```

### 方法 2: 交互式插件管理器

1. 运行 `/plugin` 打开插件管理器
2. 进入 **发现** 标签页
3. 在列表中找到 **"Claude Obsidian Plugin"**
4. 点击 **安装** 并选择您的首选范围：
   - 🔹 **用户** (在所有项目中可用)
   - 🔸 **项目** (仅在当前项目中可用)
   - ⬇️ **本地** (仅对您可用)

## 🚀 使用方法

### 基本命令

使用标准语法使用命令：

```bash
/obsidian-assistant:<命令名称> <参数>
```

**示例:**

```bash
# 创建新笔记
/obsidian-assistant:create-note 写一篇关于高效会议策略的笔记

# 总结现有笔记
/obsidian-assistant:summarize "我的会议笔记.md"

# 查找相关笔记
/obsidian-assistant:find-related 知识管理

# 生成大纲
/obsidian-assistant:outline 人工智能基础

# 转换为可视化 Canvas
/obsidian-assistant:to-canvas 项目路线图 思维导图
```

### 访问专业代理

```bash
# 内容创建者代理
/agents content-creator

# 视觉架构师代理
/agents visual-architect

# 知识挖掘者代理
/agents knowledge-miner
```

## ⚙️ 配置

插件支持各种配置选项来定制行为：

| 配置项 | 描述 |
|--------|------|
| **默认代理** | 默认交互的首选代理 |
| **自动标记** | 为新笔记自动生成标签 |
| **每日笔记模板** | 每日笔记的自定义模板 |
| **相关笔记** | 连接检测的设置 |
| **内容生成** | AI 生成内容的偏好 |
| **Canvas 布局** | 可视化表示的默认布局 |
| **隐私选项** | 控制数据处理和存储 |

## 🤝 贡献

欢迎贡献！请随时提交：

- 🐛 **Bug 报告**
- 💡 **功能请求**
- 📝 **文档改进**
- 🔧 **拉取请求**

## 📄 许可证

本项目基于 **MIT 许可证** 授权。

详见 [LICENSE](LICENSE) 文件。