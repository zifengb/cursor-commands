# Cursor Commands

⭐ **特别推荐：[Cursor](https://x.com/ericzakariasson/status/1973932448200413539) 官方精选**

一个精心策划的 Cursor 斜杠命令提示词集合，为您的团队提供可重用、版本控制的 AI 工作流，直接集成在 Cursor IDE 中。

🔗 另请查看 [Cursor Hooks](https://github.com/hamzafer/cursor-hooks) - 在每次文件编辑后自动运行

## 什么是 Cursor Commands？

Cursor Commands 是以 Markdown 文件形式保存在 `.cursor/commands/` 目录中的可重用 AI 提示词。当您在 Cursor 的聊天输入框中输入 `/` 时，IDE 会列出项目和全局库中的所有命令，让您可以立即插入提示词。它们就像 AI 驱动的快捷方式，可以自动化重复任务、强化团队标准并保持反馈的一致性。

## 功能特点

- **🚀 快速访问**：输入 `/` 即可调出所有命令，无需离开工作流
- **🔄 可重用**：为整个团队标准化常见任务的提示词
- **👥 可共享**：将命令存储在 git 中，随仓库一起分发
- **🎯 专注**：每个命令针对特定工作流，结构清晰
- **📝 可自定义**：编辑或扩展 Markdown 文件以匹配您的流程

## 命令工作原理

命令可以存放在两个位置：

- 项目命令：将 Markdown 文件存储在仓库内的 `.cursor/commands` 目录中
- 全局命令：将个人命令存储在机器上的 `~/.cursor/commands` 目录中

当您输入 `/` 时，Cursor 会自动扫描这两个目录，合并结果，并将所选命令插入聊天中，准备运行。

## 如何使用

1. 在 Cursor 的 AI 聊天或 Agent 输入框中输入 `/`
2. 从可用命令中选择
3. 让 AI 使用相关项目上下文执行提示词

## 创建命令

- 在项目根目录创建 `.cursor/commands` 目录
- 添加具有描述性名称的 `.md` 文件（例如 `code-review.md`、`run-all-tests-and-fix.md`）
- 编写清晰的 Markdown 指令，描述命令应完成的任务
- 打开 Cursor，输入 `/`，选择新命令立即执行

示例结构：

```text
.cursor/
└── commands/
    ├── accessibility-audit.md
    ├── add-documentation.md
    ├── add-error-handling.md
    ├── address-github-pr-comments.md
    ├── code-review.md
    ├── create-pr.md
    ├── database-migration.md
    ├── debug-issue.md
    ├── fix-compile-errors.md
    ├── fix-git-issues.md
    ├── generate-api-docs.md
    ├── generate-pr-description.md
    ├── light-review-existing-diffs.md
    ├── lint-fix.md
    ├── lint-suite.md
    ├── onboard-new-developer.md
    ├── optimize-performance.md
    ├── refactor-code.md
    ├── run-all-tests-and-fix.md
    ├── security-audit.md
    ├── security-review.md
    ├── setup-new-feature.md
    └── write-unit-tests.md
```

## 可用命令

### 代码质量与维护

- `lint-fix.md` – 自动分析并修复当前文件中的代码检查问题
- `lint-suite.md` – 运行项目代码检查工具，应用修复，确保代码库符合格式要求
- `refactor-code.md` – 在保持功能的同时提高代码质量
- `optimize-performance.md` – 分析和优化代码性能
- `add-error-handling.md` – 在变更集中实现全面的错误处理

### 审查与协作

- `code-review.md` – 带有结构化步骤和重点领域的全面审查检查清单
- `address-github-pr-comments.md` – 处理审查者反馈并撰写周到的回复
- `light-review-existing-diffs.md` – 快速检查以突出风险差异和清理项目
- `create-pr.md` – 准备结构良好的拉取请求和验证检查清单
- `generate-pr-description.md` – 自动起草详细的拉取请求描述

### 测试与可靠性

- `run-all-tests-and-fix.md` – 执行完整套件，分类失败并确认修复
- `write-unit-tests.md` – 生成具有适当覆盖率的专注单元测试
- `debug-issue.md` – 用于隔离缺陷的逐步调试工作流
- `fix-compile-errors.md` – 快速诊断并解决编译失败

### 文档与入职

- `add-documentation.md` – 捕获全面的产品或代码文档
- `generate-api-docs.md` – 生成带有模式和示例的丰富 API 文档
- `onboard-new-developer.md` – 为新团队成员提供检查清单驱动的入职流程
- `setup-new-feature.md` – 为新工作规划需求、分支和架构

### 安全性、无障碍性与基础设施

- `security-audit.md` – 代码更改的结构化安全检查清单
- `security-review.md` – 更广泛的漏洞和风险评估工作流
- `accessibility-audit.md` – 审查 WCAG 合规性问题
- `database-migration.md` – 规划、创建和验证带回滚的数据库迁移
- `fix-git-issues.md` – 安全地解决合并冲突和仓库问题

## 快速开始

1. 克隆此仓库或将 `.cursor/commands/` 目录复制到您的项目中
2. 在 Cursor IDE 中打开项目
3. 在 AI 聊天中输入 `/` 浏览可用命令
4. 选择一个命令，让 Cursor 使用您的代码上下文执行提示词

## 安装选项

```bash
# 选项 1：克隆仓库
git clone https://github.com/hamzafer/cursor-commands.git
cd cursor-commands
```

```bash
# 选项 2：将命令复制到现有项目
cp -r cursor-commands/.cursor /path/to/your/project/
```

或者，手动创建目录：

1. 在项目根目录创建 `.cursor/commands/`
2. 复制或编写您需要的 Markdown 命令文件

## 编写自己的命令

使用现有文件作为模板或从头开始：

```bash
touch .cursor/commands/my-custom-command.md
```

```markdown
# 我的自定义命令

此命令功能的简要描述。

## 目标
任务和预期结果的详细说明。

## 要求
- 具体要求或约束
- 要遵循的编码标准
- 预期的格式或结构

## 输出
AI 应产生内容的描述。

为 AI 提供清晰的遵循指令。
```

## 示例提示词

```markdown
# 生成 API 文档

为当前代码创建全面的 API 文档。包括：

- 端点描述和 HTTP 方法
- 带示例的请求/响应模式
- 身份验证要求
- 错误码和响应
- 速率限制信息

格式化为 OpenAPI/Swagger 规范。
```

```markdown
# 安全审计

对当前代码执行安全审计。检查：

- SQL 注入漏洞
- XSS 攻击向量
- 身份验证和授权问题
- 输入验证问题
- 敏感数据暴露

为发现的每个问题提供具体的修复步骤。
```

## 最佳实践

- **具体明确**：描述预期结果和验收标准
- **提供上下文**：引用项目约定、架构或标准
- **设定边界**：明确范围、假设和工具限制
- **包含示例**：在有帮助时展示预期的格式或响应
- **保持专注**：让每个命令针对单一、明确的目标
- **共同审查**：像对待代码更改一样，在 PR 中审查命令更改
- **使用描述性名称**：让文件名反映命令的目的

## 参考资料

- [更新日志 – v1.6](https://cursor.com/changelog)
- [文档 – 自定义斜杠命令](https://cursor.com/docs/agent/chat/commands)
- [公告帖子 1](https://x.com/cursor_ai/status/1967990959645528195)
- [公告帖子 2](https://x.com/cursor_ai/status/1970185277923615188)

## 支持

- 在 [issue](https://github.com/hamzafer/cursor-commands/issues) 中提交反馈或请求
- 参考此 README 获取随提示词一起提供的命令索引

## 许可证

本项目是开源的，采用 [MIT 许可证](LICENSE)。

