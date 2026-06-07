# Billy_kb

这是一个面向人类成员和 AI Agent 的 Obsidian 协作知识库。

仓库当前采用单仓库模式：Obsidian 负责人类浏览和写作，GitHub 负责同步和版本记录，Markdown 文件作为长期可迁移的知识载体，`AGENTS.md` 负责约束 Agent 的读取和维护行为。

## 先从哪里开始

人类成员：

1. 先读 [00-使用说明/如何接入Obsidian.md](./00-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E/%E5%A6%82%E4%BD%95%E6%8E%A5%E5%85%A5Obsidian.md)。
2. 日常先把内容写到 `01-投稿箱/你的名字/`。
3. 不要把密码、token、私钥、公司隐私信息写进仓库。
4. 遇到 Git 同步冲突，先停手，保留现场，找维护者处理。

Agent：

1. 先读本文件，理解目录地图。
2. 再读 [AGENTS.md](./AGENTS.md)，理解可信等级、读写规则和安全边界。
3. 查具体主题时，先读对应目录的 `README.md` 或 `00-地图` 目录。
4. 只把 `status: reviewed` 且 `agent_reading: allowed` 或 `agent_reading: cautious` 的文档当作正式依据。

## 总体目录

```text
Billy_kb/
  README.md                         # 仓库总地图，人和 Agent 的第一入口
  AGENTS.md                         # Agent 读取、写入、安全规则

  00-使用说明/                       # 接入、同步、写作、维护规则
  01-投稿箱/                         # 成员投稿区，默认未审
  10-AI-Agent知识/                   # Agent 通用知识、教程、哲学、范式、前沿观察
  20-课题研究/                       # 课题经验、前沿探索、讨论合作、对标论文
  30-Skills-MCP-工具资源/            # Skills、MCP、工具配置、方法范式、自建工具
  90-归档/                           # 过期、废弃、低可信或历史材料
  docs/                              # 仓库结构设计、实施计划、维护记录
```

这个结构遵循“领域 + 生命周期”：

- 顶层目录回答：这份材料属于哪个领域。
- 子目录回答：这份材料处于什么状态，应该如何使用。

## 目录说明

### `00-使用说明/`

放协作规则和操作说明。新成员、维护者和 Agent 都应该优先阅读这里。

重点文件：

- `如何接入Obsidian.md`：安装 Git、打开 vault、配置 Obsidian Git。
- `如何让Agent读取知识库.md`：Agent 检索、引用、整理知识库的规则。
- `写作与整理规范.md`：frontmatter、命名、质量标准、投稿到正式知识的流转规则。

### `01-投稿箱/`

放未审材料。普通成员默认写这里。

适合放：

- 临时想法
- 粗糙笔记
- 会议记录
- 摘录材料
- 等待 Agent 或维护者整理的内容

这里的内容默认是 `status: inbox`，不能直接作为正式事实来源。

### `10-AI-Agent知识/`

放 AI Agent 相关的通用知识。这里不是某个课题的临时讨论区，而是长期可复用的 Agent 知识层。

子目录：

- `00-领域地图/`：本领域索引、关键主题地图、推荐阅读路径。
- `10-入门与教程/`：Codex、Claude Code、Agent 工具链等入门教程。
- `20-Agent设计哲学/`：Agent 设计原则、协作范式、经验判断。
- `30-实践范式/`：可复用工作流，例如调试、写作、代码审查、研究协作。
- `40-前沿观察/`：Agent 领域新论文、新产品、新方法的观察。
- `90-归档/`：过期或不再推荐的 Agent 知识。

### `20-课题研究/`

放课题相关材料。这里允许不完全规范化，因为它的价值在于沉淀“做过什么、走通了什么、哪里不好走”。

子目录：

- `00-课题地图/`：课题列表、方向索引、问题地图。
- `10-前沿探索/`：前沿方向、通用算法、可能的创新点、paper 线索。
- `20-讨论合作/`：正在推进的课题讨论、进展同步、协作记录。
- `30-经验沉淀/`：已经研究过的课题经验、实验路径、失败路线、复盘。
- `40-对标论文/`：高水平期刊论文、目标论文、对比对象。
- `90-归档/`：过期课题材料和不再维护的研究记录。

### `30-Skills-MCP-工具资源/`

放让人和 Agent 更高效工作的工具资源。

子目录：

- `00-工具地图/`：Skills、MCP、工具链索引。
- `10-Skills/`：已有 skill、领域 skill、自建 skill 的说明。
- `20-MCP/`：MCP server 安装、配置、排错、使用范式。
- `30-范式方法/`：SDD、QDD、调研范式、协作范式等方法论。
- `40-自建工具/`：团队自建脚本、插件、工具说明。
- `90-归档/`：废弃工具、过期配置、历史方案。

### `90-归档/`

放不再作为当前知识使用的材料。归档不是删除，而是保留历史上下文，避免同样的坑反复踩。

### `docs/`

放仓库结构设计、实施计划和维护记录。这里不是主要知识区，Agent 可读取它理解历史决策，但不能把实施计划当作领域事实。

## 新内容应该放哪里

| 内容类型 | 建议位置 | 默认状态 |
|---|---|---|
| 随手想法、粗糙笔记、待整理材料 | `01-投稿箱/你的名字/` | `inbox` |
| Codex/Claude Code 入门教程 | `10-AI-Agent知识/10-入门与教程/` | `draft` 或 `reviewed` |
| Agent 设计原则、协作哲学 | `10-AI-Agent知识/20-Agent设计哲学/` | `draft` 或 `reviewed` |
| 可复用 Agent 工作流 | `10-AI-Agent知识/30-实践范式/` | `reviewed` |
| 前沿 Agent 产品、论文、方法观察 | `10-AI-Agent知识/40-前沿观察/` | `draft` |
| 前沿研究方向、paper 灵感 | `20-课题研究/10-前沿探索/` | `draft` |
| 正在推进的课题讨论 | `20-课题研究/20-讨论合作/` | `discussion` |
| 已经做过的课题经验和复盘 | `20-课题研究/30-经验沉淀/` | `reviewed` |
| 高水平对标论文 | `20-课题研究/40-对标论文/` | `draft` 或 `reviewed` |
| Skill 说明和设计 | `30-Skills-MCP-工具资源/10-Skills/` | `draft` 或 `reviewed` |
| MCP 安装和排错 | `30-Skills-MCP-工具资源/20-MCP/` | `reviewed` |
| SDD、QDD 等方法范式 | `30-Skills-MCP-工具资源/30-范式方法/` | `draft` 或 `reviewed` |
| 自建工具说明 | `30-Skills-MCP-工具资源/40-自建工具/` | `draft` 或 `reviewed` |
| 过期材料 | 对应目录的 `90-归档/` 或根 `90-归档/` | `deprecated` |

## 文档 frontmatter

正式文档建议在开头使用统一属性：

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

最重要的是 `status` 和 `agent_reading`：

- `reviewed + allowed`：可以作为正式依据。
- `reviewed + cautious`：可以引用，但需要说明限制或上下文。
- `draft/discussion/inbox`：只能作为线索。
- `deprecated/ignore`：不能作为当前结论依据。

## 从投稿到正式知识

推荐流转：

```text
01-投稿箱/
  -> 维护者或 Agent 初步整理
  -> 放入 10/20/30 的合适子目录
  -> 补 frontmatter、背景、结论、限制
  -> status 改为 draft
  -> 经过人工确认后改为 reviewed
```

不要为了追求规范而阻止投稿。投稿区可以粗糙，正式区要可读、可追溯、可复用。

## `.obsidian` 入库规则

本仓库允许保留 `.obsidian` 中的插件内容和基础配置，以保证协作者打开 vault 后体验一致。

继续忽略个人和敏感状态：

```gitignore
.obsidian/workspace*
.obsidian/plugins/*/data.json
.trash/
.DS_Store
Thumbs.db
```

不要把 GitHub token、API key、账号凭据、个人私钥写入任何 Obsidian 配置或 Markdown 文件。

## 协作边界

- 普通成员优先写 `01-投稿箱/你的名字/`。
- 正式知识区可以由维护者或明确授权的 Agent 整理。
- 大改正式文档前，先搜索是否已有相近文档，避免重复造页。
- 遇到互相矛盾的信息，保留冲突并标注“待核验”，不要强行合并成单一结论。

更详细的 Agent 规则见 [AGENTS.md](./AGENTS.md)。
