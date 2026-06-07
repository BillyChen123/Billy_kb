# AI Agent 知识

这里存放 AI Agent 相关的通用知识。重点是长期可复用，而不是某个临时课题的讨论记录。

## 子目录

```text
10-AI-Agent知识/
  00-领域地图/
  10-入门与教程/
  20-Agent设计哲学/
  30-实践范式/
  40-前沿观察/
  90-归档/
```

## 放置规则

- `00-领域地图/`：Agent 知识索引、主题地图、阅读路径。
- `10-入门与教程/`：Codex、Claude Code、Agent 工具链等教程。
- `20-Agent设计哲学/`：Agent 设计原则、协作方式、判断标准。
- `30-实践范式/`：可复用工作流，例如调试、写作、代码审查、研究协作。
- `40-前沿观察/`：Agent 领域的新论文、新产品、新方法。
- `90-归档/`：过期或不再推荐的 Agent 知识。

## 质量要求

正式文档至少说明：

- 这个知识解决什么 Agent 使用问题。
- 适用场景和不适用场景。
- 推荐做法。
- 常见坑。
- 可交给 Agent 执行的检查清单或流程。

## 建议 frontmatter

```yaml
---
title: 文档标题
status: draft
type: guide
domain: ai-agent
maintainer: Billy
updated: 2026-06-07
tags:
  - ai-agent
agent_reading: cautious
---
```
