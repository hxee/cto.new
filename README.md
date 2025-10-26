# CTO.NEW

<div align="center">

**🚀 AI 驱动的智能开发助手平台**

让 AI 成为你的编程伙伴，自动化处理开发任务、生成代码并创建 Pull Request

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-cto.new-orange.svg)](https://cto.new)

[English](README.en.md) | 简体中文

</div>

---

## 📖 项目简介

### 什么是 CTO.NEW？

CTO.NEW 是一个革命性的 AI 驱动开发平台，旨在通过智能化的方式提升开发团队的生产力。平台基于 Anthropic Claude Sonnet 4.5 强大的 AI 能力，为开发者提供从需求规划到代码实现的全流程自动化支持。

### 愿景与目标

我们的愿景是让每一位开发者都能拥有一个智能的 AI 编程助手，帮助他们：
- **提升开发效率** - 自动化处理重复性编码任务
- **保证代码质量** - AI 生成的代码遵循最佳实践
- **优化工作流程** - 无缝集成到现有的开发工具链
- **降低学习成本** - 快速适应新技术栈和代码库

### 核心价值

✨ **智能规划** - AI Planning Agent 帮助你分解复杂任务，制定清晰的实施计划

🤖 **自动编码** - AI Coding Agent 根据任务描述自动生成高质量代码

🔄 **无缝集成** - 与主流 Git 平台和任务管理工具深度整合

⚡ **极速交付** - 从任务创建到 PR 提交，大幅缩短开发周期

---

## 🌟 核心特性

### AI 智能代理系统

#### 🧠 Planning Agent（规划代理）
- 自动分析复杂需求并拆解成可执行的子任务
- 识别任务依赖关系和执行顺序
- 生成详细的实施计划和技术方案
- 适用于功能开发、架构重构等大型项目

#### 💻 Coding Agent（编码代理）
- 理解代码库结构和上下文
- 根据任务描述自动编写代码
- 遵循项目的代码规范和最佳实践
- 自动运行测试并修复错误
- 生成规范的 Git 提交和 Pull Request

### 多平台集成

#### 🔗 Git 平台支持
- **GitHub** - 完整支持仓库管理、PR 创建和代码审查
- **GitLab** - 支持 GitLab Cloud 和 Self-Hosted 版本
- **Bitbucket** - 无缝对接 Bitbucket 工作流

#### 📋 任务管理平台支持
- **Jira** - 同步 Jira Issues，自动更新任务状态
- **Linear** - 双向同步任务和开发进度
- **Trello** - 从 Trello 卡片直接创建开发任务
- **ClickUp** - 集成 ClickUp 任务到开发流程
- **GitHub Issues** - 原生支持 GitHub Issues 管理

### 🎯 Draft Task（草稿任务）系统

Draft Task 是 CTO.NEW 的核心工作单元，支持：
- 从外部任务平台导入任务
- 手动创建自定义开发任务
- AI 规划生成的子任务
- 灵活的任务编辑和调整
- 任务优先级和标签管理

### 🚀 自动化工作流

- **代码生成** - AI 自动编写符合需求的代码
- **分支管理** - 自动创建和管理功能分支
- **提交历史** - 生成清晰的提交信息
- **PR 创建** - 自动创建 Pull Request 并填写描述
- **测试运行** - 执行单元测试和代码检查
- **错误修复** - 自动识别和修复常见问题

### 🎨 用户体验

- **深色/浅色主题** - 支持暗黑和明亮两种主题模式
- **实时进度** - 查看 AI 代理的工作进度和日志
- **多仓库管理** - 在一个界面管理多个代码仓库
- **快速切换** - 在不同项目间快速切换

---

## 📚 使用方法

### 1. 连接 Git 平台

#### 步骤：
1. 登录 [cto.new](https://cto.new) 平台
2. 进入「设置」页面
3. 选择「Git Providers」选项卡
4. 点击你想连接的 Git 平台（GitHub/GitLab/Bitbucket）
5. 授权 CTO.NEW 访问你的仓库
6. 完成 OAuth 认证流程

#### 权限说明：
- **读取权限** - 读取仓库代码和分支信息
- **写入权限** - 创建分支、提交代码、创建 PR
- **Webhook** - 接收 PR 状态更新（可选）

### 2. 链接代码仓库

#### 步骤：
1. 在「Repositories」页面点击「Add Repository」
2. 从列表中选择需要管理的仓库
3. 配置默认分支（通常是 `main` 或 `master`）
4. 设置工作流偏好（可选）
5. 点击「Link Repository」完成链接

#### 提示：
- 支持同时管理多个仓库
- 可以为不同仓库设置不同的工作流配置
- 支持 Monorepo 和多仓库架构

### 3. 创建 Draft Task（草稿任务）

#### 方式一：手动创建

```markdown
1. 进入目标仓库页面
2. 点击「Create Draft Task」按钮
3. 填写任务信息：
   - 标题：简洁明确的任务名称
   - 描述：详细的需求说明和上下文
   - 优先级：High/Medium/Low
   - 标签：用于分类和筛选
4. 点击「Create」保存草稿
```

#### 方式二：从外部平台导入

```markdown
1. 连接你的任务管理平台（Jira/Linear/Trello 等）
2. 在「External Tasks」页面浏览任务列表
3. 选择需要开发的任务
4. 点击「Import as Draft」导入为草稿任务
5. 根据需要补充技术细节
```

#### 方式三：通过 Planning Agent 生成

```markdown
1. 创建一个 Planning Task
2. 描述你的高层级需求或功能
3. AI Planning Agent 会自动分析并生成多个子任务
4. 审查生成的任务列表
5. 选择需要的任务转换为 Draft Tasks
```

### 4. 启动开发任务

#### 步骤：
1. 在 Draft Tasks 列表中选择一个任务
2. 点击「Start Task」按钮
3. AI Coding Agent 开始工作：
   - 分析代码库结构
   - 理解任务需求
   - 制定实现方案
   - 编写代码
   - 运行测试
   - 创建 Pull Request
4. 监控任务进度和日志
5. 任务完成后审查生成的 PR

#### 实时监控：
- 查看 AI 当前正在执行的操作
- 阅读详细的执行日志
- 了解 AI 的决策过程
- 随时可以暂停或取消任务

### 5. 使用外部任务提供商

#### Jira 集成示例：

```markdown
1. 在「Settings」→「Integrations」中配置 Jira
2. 输入 Jira 域名和 API Token
3. 选择需要同步的项目
4. 在「External Tasks」中查看 Jira Issues
5. 将 Issue 导入为 Draft Task 开始开发
6. 任务完成后状态自动同步回 Jira
```

#### Linear 集成示例：

```markdown
1. 连接 Linear 账号
2. 选择团队和项目
3. 自动同步 Linear Issues
4. 从 Linear 创建 Draft Task
5. PR 合并后自动更新 Linear 状态
```

### 6. 完整工作流程

```
📋 需求输入
    ↓
🧠 Planning Agent（可选）
    ├─ 任务分解
    ├─ 方案设计
    └─ 生成子任务
    ↓
📝 Draft Tasks
    ├─ 任务审查
    ├─ 优先级排序
    └─ 细节完善
    ↓
🚀 Start Task
    ↓
💻 Coding Agent
    ├─ 代码分析
    ├─ 代码生成
    ├─ 测试运行
    └─ 错误修复
    ↓
🔀 Pull Request
    ├─ 代码审查
    ├─ 讨论优化
    └─ 合并代码
    ↓
✅ 任务完成
```

---

## 🛠 技术栈

### AI 引擎
- **Anthropic Claude Sonnet 4.5** - 最先进的 AI 代码生成能力
- **上下文学习** - 深度理解代码库结构和业务逻辑
- **多轮对话** - 支持复杂的推理和决策过程

### 支持的编程语言

#### 完全支持：
- **JavaScript/TypeScript** - React, Vue, Angular, Node.js
- **Python** - Django, Flask, FastAPI
- **Java** - Spring Boot, Jakarta EE
- **Go** - Gin, Echo, Standard Library
- **Rust** - Actix, Rocket, Tokio
- **Ruby** - Rails, Sinatra
- **PHP** - Laravel, Symfony

#### 良好支持：
- **C/C++** - 系统编程和嵌入式开发
- **C#** - .NET, ASP.NET Core
- **Swift** - iOS 应用开发
- **Kotlin** - Android 应用开发
- **Scala** - 函数式编程
- **Elixir** - Phoenix Framework

### 支持的框架和技术

- **前端** - React, Vue, Angular, Svelte, Next.js, Nuxt.js
- **后端** - Express, FastAPI, Spring, Django, Rails
- **数据库** - PostgreSQL, MySQL, MongoDB, Redis
- **DevOps** - Docker, Kubernetes, Terraform
- **测试** - Jest, Pytest, JUnit, Go Test
- **构建工具** - Webpack, Vite, Rollup, esbuild

---

## 💡 最佳实践

### 何时使用 Planning Agent

#### ✅ 适合使用 Planning Agent 的场景：

1. **大型功能开发**
   ```
   示例：构建一个完整的用户认证系统
   - AI 会分解为：数据模型、API 端点、前端组件、测试等多个子任务
   ```

2. **架构重构**
   ```
   示例：将 REST API 迁移到 GraphQL
   - AI 会规划：依赖分析、分步迁移、兼容性处理等
   ```

3. **跨模块功能**
   ```
   示例：实现支付功能（涉及前端、后端、数据库、第三方集成）
   - AI 会协调各模块的开发顺序和依赖关系
   ```

4. **技术债务清理**
   ```
   示例：升级依赖包并修复破坏性变更
   - AI 会识别影响范围并制定迁移计划
   ```

#### ❌ 不需要使用 Planning Agent 的场景：

1. **简单 Bug 修复** - 直接创建 Draft Task
2. **文档更新** - 直接创建 Draft Task
3. **样式调整** - 直接创建 Draft Task
4. **配置变更** - 直接创建 Draft Task

### 任务粒度指南

#### 🎯 理想的任务大小：

| 任务类型 | 预估时间 | 代码变更 | 示例 |
|---------|---------|---------|------|
| 小型任务 | 15-30分钟 | 1-3 个文件 | 修复一个 Bug、添加一个小功能 |
| 中型任务 | 30-90分钟 | 3-10 个文件 | 实现一个组件、添加一个 API 端点 |
| 大型任务 | 90-180分钟 | 10-30 个文件 | 实现一个完整的功能模块 |

#### 📝 任务拆分建议：

**过大的任务示例（不推荐）：**
```markdown
标题：构建电商系统
描述：需要用户管理、商品管理、订单处理、支付集成
❌ 太大，应该拆分成多个独立任务
```

**合理的任务示例（推荐）：**
```markdown
任务 1：实现商品列表 API
描述：
- 创建 Product 数据模型
- 实现 GET /api/products 端点
- 支持分页和筛选
- 编写单元测试
✅ 大小适中，目标明确
```

### 如何编写有效的任务描述

#### 🌟 优秀任务描述的要素：

1. **明确的目标**
   ```markdown
   ✅ 好的例子：
   实现用户注册功能，包括邮箱验证和密码强度检查
   
   ❌ 不好的例子：
   做用户注册
   ```

2. **技术上下文**
   ```markdown
   ✅ 好的例子：
   使用 React Hooks 和 Context API 实现全局主题切换功能，
   主题配置存储在 localStorage 中
   
   ❌ 不好的例子：
   添加主题切换
   ```

3. **验收标准**
   ```markdown
   ✅ 好的例子：
   实现订单列表页面，要求：
   - 显示订单号、日期、金额、状态
   - 支持按状态筛选
   - 支持日期范围搜索
   - 每页显示 20 条记录
   - 响应式设计，支持移动端
   
   ❌ 不好的例子：
   做一个订单列表
   ```

4. **相关文件或参考**
   ```markdown
   ✅ 好的例子：
   修复用户头像上传问题
   相关文件：src/components/ProfileUpload.tsx
   参考实现：src/components/ProductImageUpload.tsx
   错误日志：[附上错误截图或日志]
   
   ❌ 不好的例子：
   修复上传问题
   ```

#### 📋 任务描述模板：

```markdown
## 任务标题
[简洁明确的一句话描述]

## 背景
[为什么需要这个任务，业务价值是什么]

## 详细需求
- 需求点 1
- 需求点 2
- 需求点 3

## 技术要求
- 使用的技术栈
- 需要遵循的规范
- 性能或安全要求

## 验收标准
- [ ] 标准 1
- [ ] 标准 2
- [ ] 标准 3

## 参考资料
- 相关文件路径
- 设计稿链接
- API 文档
```

---

## ❓ 常见问题

### Git 集成相关

**Q: CTO.NEW 需要哪些 Git 权限？**

A: CTO.NEW 需要以下权限：
- 读取仓库代码和分支
- 创建和管理分支
- 提交代码变更
- 创建 Pull Request
- 读取 PR 状态（可选）

我们遵循最小权限原则，不会访问与开发任务无关的数据。

**Q: 我可以使用 Self-Hosted 的 GitLab 吗？**

A: 可以！在连接 GitLab 时，你可以输入自定义的 GitLab 实例 URL。

**Q: 生成的代码会自动合并到主分支吗？**

A: 不会。AI 只会创建 Pull Request，所有代码都需要经过人工审查后才能合并。

**Q: 如何处理代码冲突？**

A: 如果 AI 检测到合并冲突，会在 PR 中标注。你需要手动解决冲突或提供指导让 AI 重新生成。

### 积分系统

**Q: 什么是积分（Credits）？**

A: 积分是 CTO.NEW 的使用单位。每次 AI 执行任务都会消耗一定的积分，消耗量取决于任务的复杂度和代码量。

**Q: 如何获取更多积分？**

A: 
- 新用户注册赠送免费积分
- 订阅月度或年度套餐
- 参与推荐计划获得奖励积分

**Q: 任务失败会扣除积分吗？**

A: 如果任务因系统错误失败，积分会自动退还。如果是因为任务描述不清导致的失败，积分不会退还。

### 任务管理

**Q: 可以同时运行多个任务吗？**

A: 可以！你可以同时在不同仓库运行多个任务。同一仓库也可以运行多个任务，但需要注意避免修改相同的文件。

**Q: 任务运行中可以取消吗？**

A: 可以随时暂停或取消正在运行的任务。已完成的部分会保存，你可以稍后继续或重新开始。

**Q: AI 生成的代码质量如何？**

A: AI 使用 Anthropic Claude Sonnet 4.5，能够生成高质量的代码。但我们仍然建议：
- 仔细审查生成的代码
- 运行完整的测试套件
- 进行安全性检查
- 根据团队标准进行必要的调整

**Q: 支持哪些代码规范检查？**

A: AI 会自动运行项目中配置的 Linter 和格式化工具（如 ESLint, Prettier, Pylint 等），并尝试修复检查出的问题。

**Q: 可以为 AI 提供自定义指令吗？**

A: 可以！在任务描述中加入详细的技术要求和偏好，AI 会遵循这些指令。你也可以在仓库设置中配置通用的编码规范。

**Q: 如何查看任务执行历史？**

A: 在「History」页面可以查看所有任务的执行记录，包括：
- 任务详情和描述
- 执行时间和状态
- 生成的代码变更
- AI 的决策日志
- 最终的 PR 链接

### 团队协作

**Q: 支持团队功能吗？**

A: 支持！你可以创建团队，邀请成员，共享仓库和积分池。

**Q: 可以设置任务审批流程吗？**

A: 可以配置团队设置，要求 Draft Task 在启动前需要团队成员审批。

**Q: 如何避免团队成员的任务冲突？**

A: 平台会检测同一文件的并发修改，并提醒团队成员。建议使用任务标签和优先级进行协调。

---

## 🚀 快速开始

1. **注册账号** - 访问 [cto.new](https://cto.new) 创建免费账号
2. **连接 Git** - 链接你的 GitHub、GitLab 或 Bitbucket 账号
3. **添加仓库** - 选择需要 AI 协助的代码仓库
4. **创建任务** - 写下你的第一个开发任务
5. **启动 AI** - 让 AI Coding Agent 为你工作
6. **审查 PR** - 检查生成的代码并合并

---

## 📞 支持与反馈

- **官方网站** - [https://cto.new](https://cto.new)
- **文档中心** - [https://docs.cto.new](https://docs.cto.new)
- **问题反馈** - [GitHub Issues](https://github.com/cto-new/feedback/issues)
- **邮件支持** - support@cto.new
- **社区讨论** - [Discord Community](https://discord.gg/cto-new)

---

## 📄 许可证

[MIT License](LICENSE)

---

## 🙏 致谢

感谢所有使用 CTO.NEW 的开发者，你们的反馈帮助我们不断改进产品。

特别感谢 Anthropic 提供强大的 Claude AI 能力。

---

<div align="center">

**用 AI 赋能开发，让编程更高效** ✨

Made with ❤️ by CTO.NEW Team

</div>
