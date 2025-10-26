# GitHub Issues 完整使用指南 | GitHub Issues Full Guide

> 📌 本指南帮助你在 cto.new 中将 GitHub Issues 作为 ticket provider 使用，涵盖配置、触发方式、工作流程与最佳实践，确保团队能够稳定、可控地让 AI Coding Agent 自动解决 Issue。

---

## 1. 概述 | Overview

### 什么是 GitHub Issues 集成
- **GitHub Issues 集成**是 cto.new 的一类外部 ticket provider，允许平台自动读取 GitHub 仓库中的 Issues，将其转化为可执行的开发任务。
- 通过集成后，cto.new 会监听指定仓库的 Issue 事件，并在满足触发条件时启动 AI Workflow。

### 为什么使用 GitHub Issues
- ✅ **统一任务入口**：开发与产品团队无需切换平台，直接在 GitHub 中创建任务。
- ✅ **原生上下文**：Issue 中的代码片段、讨论历史、关联 Pull Request 都能被 cto.new 理解并引用。
- ✅ **权限一致**：沿用现有的 GitHub 权限体系，无需额外账户管理。

### 与内部草稿任务（Draft Task）的区别
| 对比项 | GitHub Issues | Draft Task |
| --- | --- | --- |
| 创建入口 | GitHub 仓库 UI | cto.new 控制台 |
| 信息来源 | Issue 标题、正文、评论 | 用户手动填写或 AI 规划导入 |
| 触发方式 | Mention / Label / Command | 在平台内点击 Start |
| 适用人群 | 熟悉 GitHub 工作流的团队 | 需要更灵活的任务编辑和模板的团队 |

### 适用场景
- GitHub 已是团队主任务管理平台，希望 AI 与现有流程无缝集成。
- 产品/测试人员直接在 Issue 中描述需求并拉取 AI 协助。
- 希望通过 Issue 模板和标签体系实现标准化的 AI 开发协作。

---

## 2. 快速开始 | Quick Start

### 步骤 1：启用 GitHub Issues 集成
1. 登录 [cto.new](https://cto.new) 平台。
2. 前往 **Settings → Integrations → Ticket Providers**。
3. 选择 **GitHub Issues** 并点击 **Connect**。
4. 完成 GitHub OAuth 授权，允许 cto.new 访问目标组织或仓库。

### 步骤 2：配置仓库映射
1. 在 **Repositories → Linked Repositories** 中找到目标仓库。
2. 打开 **Ticket Provider** 标签页，选择 **GitHub Issues**。
3. 指定需要监听的 Issue 标签、Assignee 或 Milestone（可选）。
4. 保存配置后，cto.new 会开始同步符合条件的 Issues。

### 步骤 3：创建第一个测试任务
1. 在 GitHub 仓库中创建一条新 Issue。
2. 使用推荐模板填写标题和描述（见第 3 章）。
3. 添加触发标签或 @mention cto.new Bot（见第 4 章）。
4. 在 cto.new 控制台的 **Tasks → External Tickets** 中确认 Issue 已同步并启动执行。

---

## 3. 创建 Issue 任务 | Authoring Issues

### Issue 标题规范
- 使用动宾结构，突出业务价值或技术动作，例如：`feat: 支持用户导出 CSV 报表`。
- 前缀可使用惯用标签：`feat`, `fix`, `chore`, `docs`。
- 控制在 50~70 字符，便于列表浏览。

### 描述内容要求
在 Issue 正文中提供必要上下文，建议结构：
1. **背景（Background）**：描述问题来源或业务缘由。
2. **目标（Goal）**：明确预期结果或验收标准。
3. **上下文（Context）**：链接相关 PR、Issue、设计文档。
4. **检查项（Checklist）**：列出子任务或测试项。
5. **附加信息（Attachments）**：截图、日志、错误信息。

### 推荐的 Issue 模板
```markdown
---
title: "{{ placeholder_title }}"
labels: ["cto:ready", "feature"]
assignees: ["{{ github_handle }}"]
---

## 背景 Background
简要说明问题产生的场景和业务影响。

## 目标 Goal
- [ ] 清晰列出预期产出或功能需求

## 方案 Proposal
- 建议步骤 1
- 建议步骤 2

## 验收标准 Acceptance Criteria
- 条件 A
- 条件 B

## 其他信息 Additional Context
- 相关链接：#123, PR #456
- 日志或截图：请附上
```
> 💡 将模板保存为 `.github/ISSUE_TEMPLATE/cto-new.md`，并在仓库设置中启用。

### 标签使用建议
- `cto:ready`：标记 Issue 可交给 cto.new。
- `priority:high` / `priority:medium` / `priority:low`：帮助 AI 判断紧迫性。
- `area:frontend`、`area:backend`：提供代码区域提示。
- 避免在同一 Issue 上混用互斥标签（例如 `bug` 与 `feature`）。

---

## 4. 触发 cto.new | Triggering the Workflow

### @mention 方式
- 在 Issue 评论中输入 `@cto-new-bot start`。
- 适合需要人工确认后再启动的流程。

### 标签触发方式
- 为 Issue 添加预置标签（如 `cto:ready`）。
- cto.new 监测到标签变更后会自动拾取任务。

### 命令触发方式
- 在 Issue 评论中使用斜杠指令，例如：
  ```text
  /cto run draft
  ```
- 常用指令：`/cto run`（立即开始）、`/cto plan`（仅生成实施计划）、`/cto status`（获取最新状态）。

### 触发时机建议
- 确认需求信息完整、附件齐全后再触发，避免反复往返。
- 对多参与者的 Issue，先完成内部讨论或审批再触发。
- 建议在工作日早间触发，确保团队有足够时间审查生成的 PR。

---

## 5. 工作流程 | End-to-End Flow

1. **Issue 创建**：团队在 GitHub 中撰写 Issue 并应用触发条件。
2. **同步到 cto.new**：平台将 Issue 映射成 External Ticket，并校验权限与配置。
3. **计划阶段（Planning Agent）**：
   - 分析 Issue 描述，拆解子任务。
   - 可选地产生实施计划草稿并回写到 Issue 评论。
4. **编码阶段（Coding Agent）**：
   - 签出独立分支，拉取最新主干代码。
   - 编写代码、生成测试、运行必要的检查。
   - 创建 Pull Request 并附上变更摘要。
5. **自动响应**：cto.new 在 Issue 中发布状态更新，包括任务开始、测试结果、PR 链接。
6. **状态同步**：当 PR 合并或关闭，cto.new 自动更新 Issue 状态（如添加完成评论、修改状态字段）。
7. **Issue 自动关闭**：
   - 当 PR 合并且满足 `Fixes #<issue-number>` 等自动关闭规则时，Issue 会关闭。
   - 如果未自动关闭，可在 Issue 评论中使用 `/cto close` 提醒团队关闭。

---

## 6. 权限说明 | Permissions

### ✅ cto.new 可以做
- 读取 Issue 标题、正文、评论历史。
- 在 Issue 中添加评论（状态更新、执行计划、PR 链接）。
- 将自动创建的 Pull Request 关联到对应 Issue。

### ❌ cto.new 不能做
- **不能创建 Issue**：需要由人工或其他自动化流程创建。
- **不能修改 Issue 内容**：不会编辑标题、正文或删除评论。
- **不能调整标签**：不会主动添加或移除标签，避免干扰团队流程。
- **不能手动关闭 Issue**：关闭操作由团队成员执行或依赖 GitHub 自动关闭规则。

---

## 7. 实际示例 | Real-World Examples

### 示例 1：简单功能任务
- **标题**：`feat: 支持仪表盘导出 CSV`
- **关键描述**：
  ```markdown
  ## 背景
  用户需要导出财务概览数据。

  ## 目标
  - [ ] 在 Dashboard 页面新增 Export CSV 按钮
  - [ ] 导出字段与「财务报表」接口保持一致

  ## 验收
  - 导出文件名包含日期
  - 空数据时显示提示
  ```
- **触发方式**：添加标签 `cto:ready`。
- **结果**：cto.new 创建分支 `feature/export-csv`, 提交代码并生成 PR。

### 示例 2：Bug 修复任务
- **标题**：`fix: 修复移动端登录闪退`
- **关键描述**：
  ```markdown
  ## 现象
  iOS Safari 登录后刷新页面会返回登录页。

  ## 重现步骤
  1. 打开登录页并输入账号密码
  2. 登录成功后立即刷新页面

  ## 日志
  - 见附加的 `safari-console.log`

  ## 验收
  - 刷新后保持会话状态
  ```
- **触发方式**：评论 `@cto-new-bot start`。
- **结果**：cto.new 更新 Session 管理逻辑，生成包含单元测试的 PR 并在 Issue 内评论链接。

### 示例 3：复杂任务（多模块）
- **标题**：`feat: 多仓库同步的审计日志系统`
- **关键描述**：
  ```markdown
  ## 背景
  为满足合规要求，需要记录多仓库同步时的变更明细。

  ## 目标
  - [ ] 设计审计日志 schema
  - [ ] 在 Sync Service 中新增写入逻辑
  - [ ] 提供 `/audit/logs` API 查询

  ## 依赖
  - 参考设计文档：https://example.com/design/audit

  ## 验收
  - 日志写入成功率 ≥ 99%
  - API 支持过滤条件 tenantId、dateRange
  ```
- **触发方式**：评论 `/cto plan` 获取计划 → 确认后 `/cto run`。
- **结果**：cto.new 先生成分阶段计划，再逐步提交到 PR，整个过程中的进度更新均同步到 Issue 评论。

---

## 8. 最佳实践 | Best Practices

- ✍️ **Issue 写作技巧**：使用 Markdown 标题和列表，让 AI 更容易解析结构化信息。
- 📏 **任务大小判断**：若 Issue 涉及三个以上独立模块，建议先使用 `/cto plan` 拆分，必要时拆成多个 Issue。
- 🏷️ **标签管理**：维护统一的标签命名规范，避免出现重复语义（如 `frontend` 与 `ui` 同时存在）。
- 🔄 **定期校准模板**：每季度审查 Issue 模板是否仍符合团队流程。
- 📣 **反馈回路**：在 PR 或 Issue 中对 AI 输出的质量给出反馈，便于后续优化。

---

## 9. 常见问题 | FAQ

### 故障排查
- **Issue 未同步到 cto.new**
  - 检查仓库是否在 cto.new 中已链接。
  - 确认 Issue 是否满足标签或 Assignee 条件。
  - 查看 Integrations 日志，确认 Webhook 是否正常触发。
- **AI 没有响应**
  - 确认已 @mention 或添加触发标签。
  - 使用 `/cto status` 获取最新执行状态。
  - 检查 cto.new 控制台的任务队列是否存在排队。

### 权限问题
- **无法读取 Issue**：确保授权范围包含 `repo` 和 `read:org`（针对私有仓库）。
- **评论失败**：检查是否对 Bot 账号开启了「限制协作者」设置；必要时在仓库的 **Settings → Collaborators & Teams** 中为 cto.new 服务账号添加 `Write` 权限。
- **PR 未关联 Issue**：确保 PR 描述中包含关键字 `Fixes #<issue-number>` 或在 cto.new 设置中启用自动关联。

---

## 10. 对比表格 | Ticket Provider Comparison

| Ticket Provider | 优势 | 典型触发方式 | 推荐使用场景 |
| --- | --- | --- | --- |
| **GitHub Issues** | 原生代码上下文、与 PR 深度关联 | Mention、Label、Slash Command | GitHub 中心化团队，直接在仓库内协作 |
| **Jira** | 丰富的工作流、复杂字段支持 | 状态流转、Webhook | 大型企业或需要定制化流程的项目 |
| **Linear** | 极简体验、快速操作 | 状态更改、API Hook | 创业团队、追求高效的产品迭代 |
| **Trello** | 看板视图、轻量化管理 | 卡片移动、Checklist 完成 | 跨职能团队、初创或非技术项目 |
| **Draft Task（cto.new 内建）** | 灵活编辑、AI 原生支持 | 平台内 Start、计划一键生成 | 需要快速试验或尚未确定 ticket provider 的团队 |

---

通过以上步骤与实践，你可以在 GitHub Issues 中构建结构化的任务描述，并让 cto.new 在正确的时间点接手开发工作，最终实现从 Issue 到 Pull Request 的自动化闭环。祝使用顺利！