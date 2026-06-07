# Skills / MCP / 工具资源

这里存放让人和 Agent 更高效工作的工具资源，包括 Skills、MCP、工具配置、方法范式和自建工具。

## 子目录

```text
30-Skills-MCP-工具资源/
  00-工具地图/
  10-Skills/
  20-MCP/
  30-范式方法/
  40-自建工具/
  90-归档/
```

## 放置规则

- `00-工具地图/`：Skills、MCP、工具链索引。
- `10-Skills/`：已有 skill、领域 skill、自建 skill 的说明和维护记录。
- `20-MCP/`：MCP server 安装、配置、排错、使用范式。
- `30-范式方法/`：SDD、QDD、调研范式、协作范式等方法论。
- `40-自建工具/`：团队自建脚本、插件、工具说明。
- `90-归档/`：废弃工具、过期配置、历史方案。

## 质量要求

工具类文档最好写到能直接复用：

- 这个工具解决什么问题。
- 安装或启用条件是什么。
- 如何验证它可用。
- 常见错误如何排查。
- 适合交给 Agent 的调用方式是什么。

## 建议 frontmatter

```yaml
---
title: 工具或范式标题
status: draft
type: skill
domain: skill-mcp
maintainer: Billy
updated: 2026-06-07
tags:
  - tools
agent_reading: cautious
---
```
