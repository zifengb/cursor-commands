# Git 推送（与远程同步）

## 概述

将当前分支推送到远程仓库并与远程更新同步。

## 步骤

1. **拉取并变基到最新的 main 分支（可选但推荐）**
    - `git fetch origin`
    - `git rebase origin/main || git rebase --abort`（如果不在 main 分支，将你的功能分支变基到最新的 main）
2. **推送当前分支**
    - `git push -u origin HEAD`
3. **如果因远程更新导致推送被拒绝**
    - 变基并推送：`git pull --rebase && git push`

## 注意事项

- 优先使用 `rebase` 而非 `merge`，以保持线性历史记录。
- 如果变基后需要强制推送：需要询问用户是否要强制推送：`git push --force-with-lease`。

