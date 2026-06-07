# 模板

这里的模板主要给 Agent 使用。它们是生成提示，不是人类必须填满的表单。

## 模板列表

- `project-readme.md`：项目 README。
- `memory.md`：项目当前记忆。
- `lesson.md`：经验和失败路线。
- `paper-note.md`：论文笔记。
- `tutorial.md`：教程。
- `how-to.md`：操作指南。
- `reference.md`：参考说明。
- `explanation.md`：解释性文章。

## Agent 规则

使用模板时：

- 信息不足就写“待核验”。
- 不要为了填满模板而编造。
- 生成项目材料后，检查是否需要同步 `memory.md`。
