# Git 创建提交

## 概述

创建简短、聚焦的提交信息并提交暂存的更改。

## 步骤

1. **审查更改**
    - 检查差异：`git diff --cached`（如果更改已暂存）或 `git diff`（如果未暂存）
    - 理解更改了什么以及为什么
2. **询问问题编号（可选）**
    - 检查分支名称中是否有问题编号（Linear、Jira、GitHub issue 等）
    - 如果问题编号（例如 POW-123、PROJ-456、#123）在聊天或提交上下文中尚不可用，可选择询问用户是否要包含一个
    - 这是可选的 - 提交可以不包含问题编号
3. **暂存更改（如果尚未暂存）**
    - `git add -A`
4. **创建简短的提交信息**
    - 基于差异中的实际更改编写信息
    - 示例：`git commit -m "fix(auth): handle expired token refresh"`
    - 带问题编号的示例：`git commit -m "PROJ-123: fix(auth): handle expired token refresh"`

## 模板

- `git commit -m "<type>(<scope>): <简短摘要>"`
- 带问题编号：`git commit -m "<issue-key>: <type>(<scope>): <简短摘要>"`

## 规则

- **长度：** <= 72 个字符
- **祈使语气：** 使用 "fix"、"add"、"update"（而不是 "fixed"、"added"、"updated"）
- **首字母大写：** 摘要的首字母应大写
- **无句号：** 不要在主题行末尾加句号
- **描述原因：** 不仅仅是做了什么 - "fix stuff" 毫无意义

