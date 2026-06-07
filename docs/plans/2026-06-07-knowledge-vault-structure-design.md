# Knowledge Vault Structure Design

更新时间：2026-06-07

## 背景

Billy_kb 是一个面向人类成员和 AI Agent 的 Obsidian 协作知识库。用户希望团队成员主要通过 Obsidian 投稿和浏览，维护者与 Agent 负责整理、沉淀和检索。知识库当前采用单仓库模式。

## 目标

建立一套让人和 Agent 都容易定位信息的目录结构，并用规则文档保证每篇 Markdown 的基本质量。

具体目标：

- 根 `README.md` 成为仓库总地图。
- `AGENTS.md` 成为 Agent 读写和安全协议。
- 顶层目录按领域划分。
- 领域内部按材料生命周期划分。
- 每篇正式文档通过 frontmatter 暴露状态、类型、领域和 Agent 可读性。

## 目录设计

采用“领域 + 生命周期”结构：

```text
00-使用说明/
01-投稿箱/
10-AI-Agent知识/
20-课题研究/
30-Skills-MCP-工具资源/
90-归档/
```

其中 `10/20/30` 是正式知识区，内部再按地图、教程、探索、讨论、沉淀、归档等生命周期组织。

## `.obsidian` 策略

保留 `.obsidian` 中的插件内容和基础配置，方便协作者打开 vault 后获得一致体验。

继续忽略个人状态和敏感配置：

```gitignore
.obsidian/workspace*
.obsidian/plugins/*/data.json
.trash/
.DS_Store
Thumbs.db
```

## frontmatter 设计

最小 schema：

```yaml
---
title: 文档标题
status: inbox | draft | discussion | reviewed | deprecated
type: guide | note | paper | project | skill | mcp | pattern | discussion | lesson
domain: ai-agent | research | skill-mcp | ops
maintainer: Billy
updated: 2026-06-07
tags:
  - example
agent_reading: allowed | cautious | ignore
---
```

核心字段是 `status` 和 `agent_reading`。Agent 只有在文档达到 `reviewed + allowed/cautious` 时，才能把它作为正式依据。

## 取舍

没有采用严格项目制目录，因为当前知识库早期会有大量灵感、草稿、讨论、paper 线索和经验碎片。过早项目制会增加投稿门槛。

没有完全忽略 `.obsidian`，因为用户希望保留插件内容，降低协作者接入成本。风险通过忽略 `workspace*` 和插件 `data.json` 控制。
