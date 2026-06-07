# Billy_kb

这是一个 AI-native 的 Obsidian 协作知识库。

核心规则、目录结构、Agent 读写协议都在 [AGENTS.md](./AGENTS.md)。人和 Agent 都应该先读它。

## 快速开始

人类成员：

1. 接入 Obsidian：读 [00-使用说明/如何接入Obsidian.md](./00-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E/%E5%A6%82%E4%BD%95%E6%8E%A5%E5%85%A5Obsidian.md)。
2. 不知道放哪的内容，先放 `01-收件箱/`。
3. 推进课题时，让 Agent 进入 `10-项目/项目名/` 并同步 `memory.md`。
4. 不要把密码、token、私钥、cookie、公司隐私信息写进仓库。

Agent：

1. 必须先读 [AGENTS.md](./AGENTS.md)。
2. 处理项目时，必须先读该项目的 `README.md` 和 `memory.md`。
3. 每次实质推进后，判断是否需要运行 `/sync_memory`。

## 当前功能知识地图

星级是先验重要性判断，表示这条知识对当前 AI-native 工作流的潜在杠杆；不是客观质量排名。

| 类别 | 知识/功能 | 重要性 | 维护/来源 | 适合用来做什么 |
|---|---|---:|---|---|
| 项目 | [自建中转站](<./10-项目/自建中转站/README.md>) | ★★★★ | Billy 提出，Agent 整理 | 沉淀自建中转站的目标、评测维度、实现路线和踩坑经验 |
| AI-Agent 入门 | [入门 Codex 和 Claude Code](<./20-主题库/AI-Agent/入门Codex和Claude Code.md>) | ★★★★ | Billy 提供视频资源，Agent 整理 | 新成员快速理解 Codex、Claude Code 和 Agent 工作方式 |
| AI-Agent 资源 | [外部中转站评测](<./20-主题库/AI-Agent/外部中转站评测.md>) | ★★★ | Billy 提供链接，Help AIO 来源，Agent 整理 | 对比 Claude、Codex、Gemini 等中转站服务，辅助自建中转站项目 |
| 方法范式 | [OpenSpec](<./20-主题库/方法范式/OpenSpec.md>) | ★★★★★ | OpenSpec GitHub，Agent 解读 | 用需求驱动开发范式约束 AI coding，先写规格再实现 |
| 方法范式 | [QDD](<./20-主题库/方法范式/QDD.md>) | ★★★★★ | Billy / QDD GitHub，Agent 解读 | 用问题驱动方式推进科研探索，沉淀 study、memory 和 artifacts |
| Skills | [开发 Skills](<./20-主题库/Skills/开发Skills.md>) | ★★★★ | 外部 GitHub 来源，Agent 整理 | 前端设计、工程协作、Remotion 视频制作等开发类任务 |
| Skills | [科研 Skills](<./20-主题库/Skills/科研Skills.md>) | ★★★★ | 外部 GitHub 来源，Agent 整理 | 科研绘图、论文表达、组会和汇报 PPT 生成 |

## 目录

```text
00-使用说明/      接入、同步、协作说明
01-收件箱/        临时输入、粗糙笔记、待整理材料
10-项目/          按课题或项目聚合当前工作和历史经验
20-主题库/        跨项目复用的主题知识
30-模板/          给 Agent 生成高质量文档用的轻模板
90-归档/          过期、废弃、历史材料
docs/             仓库设计和维护记录
```

这个仓库的重点不是让人手动维护一套复杂 wiki，而是让 Agent 在工作过程中自动沉淀 memory、lesson 和可复用知识。
