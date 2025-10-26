# CTO.NEW

<div align="center">

**🚀 AI-Powered Intelligent Development Assistant Platform**

Let AI become your programming partner, automating development tasks, generating code, and creating Pull Requests

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-cto.new-orange.svg)](https://cto.new)

English | [简体中文](README.md)

</div>

---

## 📖 Project Introduction

### What is CTO.NEW?

CTO.NEW is a revolutionary AI-driven development platform designed to enhance development team productivity through intelligent automation. Built on the powerful AI capabilities of Anthropic Claude Sonnet 4.5, the platform provides developers with end-to-end automation support from requirements planning to code implementation.

### Vision and Goals

Our vision is to empower every developer with an intelligent AI programming assistant that helps them:
- **Boost Development Efficiency** - Automate repetitive coding tasks
- **Ensure Code Quality** - AI-generated code follows best practices
- **Optimize Workflows** - Seamlessly integrate with existing development toolchains
- **Reduce Learning Curve** - Quickly adapt to new tech stacks and codebases

### Core Value Propositions

✨ **Intelligent Planning** - AI Planning Agent helps you break down complex tasks and create clear implementation plans

🤖 **Automated Coding** - AI Coding Agent automatically generates high-quality code based on task descriptions

🔄 **Seamless Integration** - Deep integration with mainstream Git platforms and task management tools

⚡ **Rapid Delivery** - Significantly shorten development cycles from task creation to PR submission

---

## 🌟 Core Features

### AI Intelligent Agent System

#### 🧠 Planning Agent
- Automatically analyzes complex requirements and breaks them down into executable subtasks
- Identifies task dependencies and execution order
- Generates detailed implementation plans and technical solutions
- Suitable for large-scale projects like feature development and architecture refactoring

#### 💻 Coding Agent
- Understands codebase structure and context
- Automatically writes code based on task descriptions
- Follows project coding standards and best practices
- Automatically runs tests and fixes errors
- Generates standardized Git commits and Pull Requests

### Multi-Platform Integration

#### 🔗 Git Platform Support
- **GitHub** - Full support for repository management, PR creation, and code review
- **GitLab** - Supports GitLab Cloud and Self-Hosted versions
- **Bitbucket** - Seamless integration with Bitbucket workflows

#### 📋 Task Management Platform Support
- **Jira** - Sync Jira Issues, automatically update task status
- **Linear** - Bidirectional sync of tasks and development progress
- **Trello** - Create development tasks directly from Trello cards
- **ClickUp** - Integrate ClickUp tasks into development workflow
- **GitHub Issues** - Native support for GitHub Issues management

### 🎯 Draft Task System

Draft Task is the core work unit of CTO.NEW, supporting:
- Import tasks from external task platforms
- Manually create custom development tasks
- AI planning-generated subtasks
- Flexible task editing and adjustment
- Task priority and tag management

### 🚀 Automated Workflow

- **Code Generation** - AI automatically writes code that meets requirements
- **Branch Management** - Automatically create and manage feature branches
- **Commit History** - Generate clear commit messages
- **PR Creation** - Automatically create Pull Requests with descriptions
- **Test Execution** - Run unit tests and code checks
- **Error Fixing** - Automatically identify and fix common issues

### 🎨 User Experience

- **Dark/Light Theme** - Support for both dark and light theme modes
- **Real-time Progress** - View AI agent work progress and logs
- **Multi-repository Management** - Manage multiple code repositories in one interface
- **Quick Switching** - Quickly switch between different projects

---

## 📚 Usage Guide

### 1. Connect Git Platform

#### Steps:
1. Log in to the [cto.new](https://cto.new) platform
2. Go to the "Settings" page
3. Select the "Git Providers" tab
4. Click on the Git platform you want to connect (GitHub/GitLab/Bitbucket)
5. Authorize CTO.NEW to access your repositories
6. Complete the OAuth authentication flow

#### Permission Details:
- **Read Permissions** - Read repository code and branch information
- **Write Permissions** - Create branches, commit code, create PRs
- **Webhook** - Receive PR status updates (optional)

### 2. Link Code Repositories

#### Steps:
1. Click "Add Repository" on the "Repositories" page
2. Select repositories you want to manage from the list
3. Configure default branch (usually `main` or `master`)
4. Set workflow preferences (optional)
5. Click "Link Repository" to complete the linking

#### Tips:
- Support managing multiple repositories simultaneously
- Can set different workflow configurations for different repositories
- Support Monorepo and multi-repository architectures

### 3. Create Draft Tasks

#### Method 1: Manual Creation

```markdown
1. Go to the target repository page
2. Click the "Create Draft Task" button
3. Fill in task information:
   - Title: Concise and clear task name
   - Description: Detailed requirements and context
   - Priority: High/Medium/Low
   - Tags: For categorization and filtering
4. Click "Create" to save the draft
```

#### Method 2: Import from External Platforms

```markdown
1. Connect your task management platform (Jira/Linear/Trello, etc.)
2. Browse the task list on the "External Tasks" page
3. Select tasks that need development
4. Click "Import as Draft" to import as draft tasks
5. Supplement technical details as needed
```

#### Method 3: Generate via Planning Agent

```markdown
1. Create a Planning Task
2. Describe your high-level requirements or features
3. AI Planning Agent will automatically analyze and generate multiple subtasks
4. Review the generated task list
5. Select needed tasks to convert to Draft Tasks
```

### 4. Start Development Tasks

#### Steps:
1. Select a task from the Draft Tasks list
2. Click the "Start Task" button
3. AI Coding Agent begins working:
   - Analyze codebase structure
   - Understand task requirements
   - Create implementation plan
   - Write code
   - Run tests
   - Create Pull Request
4. Monitor task progress and logs
5. Review the generated PR after task completion

#### Real-time Monitoring:
- View current operations being performed by AI
- Read detailed execution logs
- Understand AI's decision-making process
- Can pause or cancel tasks at any time

### 5. Use External Task Providers

#### Jira Integration Example:

```markdown
1. Configure Jira in "Settings" → "Integrations"
2. Enter Jira domain and API Token
3. Select projects to sync
4. View Jira Issues in "External Tasks"
5. Import Issues as Draft Tasks to start development
6. Status automatically syncs back to Jira after task completion
```

#### Linear Integration Example:

```markdown
1. Connect Linear account
2. Select teams and projects
3. Automatically sync Linear Issues
4. Create Draft Tasks from Linear
5. Automatically update Linear status after PR merge
```

### 6. Complete Workflow

```
📋 Requirements Input
    ↓
🧠 Planning Agent (Optional)
    ├─ Task Decomposition
    ├─ Solution Design
    └─ Generate Subtasks
    ↓
📝 Draft Tasks
    ├─ Task Review
    ├─ Priority Sorting
    └─ Detail Enhancement
    ↓
🚀 Start Task
    ↓
💻 Coding Agent
    ├─ Code Analysis
    ├─ Code Generation
    ├─ Test Execution
    └─ Error Fixing
    ↓
🔀 Pull Request
    ├─ Code Review
    ├─ Discussion & Optimization
    └─ Code Merge
    ↓
✅ Task Complete
```

---

## 🛠 Tech Stack

### AI Engine
- **Anthropic Claude Sonnet 4.5** - Most advanced AI code generation capabilities
- **Contextual Learning** - Deep understanding of codebase structure and business logic
- **Multi-turn Dialogue** - Support complex reasoning and decision-making processes

### Supported Programming Languages

#### Full Support:
- **JavaScript/TypeScript** - React, Vue, Angular, Node.js
- **Python** - Django, Flask, FastAPI
- **Java** - Spring Boot, Jakarta EE
- **Go** - Gin, Echo, Standard Library
- **Rust** - Actix, Rocket, Tokio
- **Ruby** - Rails, Sinatra
- **PHP** - Laravel, Symfony

#### Good Support:
- **C/C++** - System programming and embedded development
- **C#** - .NET, ASP.NET Core
- **Swift** - iOS application development
- **Kotlin** - Android application development
- **Scala** - Functional programming
- **Elixir** - Phoenix Framework

### Supported Frameworks and Technologies

- **Frontend** - React, Vue, Angular, Svelte, Next.js, Nuxt.js
- **Backend** - Express, FastAPI, Spring, Django, Rails
- **Databases** - PostgreSQL, MySQL, MongoDB, Redis
- **DevOps** - Docker, Kubernetes, Terraform
- **Testing** - Jest, Pytest, JUnit, Go Test
- **Build Tools** - Webpack, Vite, Rollup, esbuild

---

## 💡 Best Practices

### When to Use Planning Agent

#### ✅ Scenarios Suitable for Planning Agent:

1. **Large Feature Development**
   ```
   Example: Build a complete user authentication system
   - AI will break down into: data models, API endpoints, frontend components, tests, and other subtasks
   ```

2. **Architecture Refactoring**
   ```
   Example: Migrate REST API to GraphQL
   - AI will plan: dependency analysis, step-by-step migration, compatibility handling, etc.
   ```

3. **Cross-module Features**
   ```
   Example: Implement payment functionality (involving frontend, backend, database, third-party integration)
   - AI will coordinate development order and dependencies across modules
   ```

4. **Technical Debt Cleanup**
   ```
   Example: Upgrade dependency packages and fix breaking changes
   - AI will identify impact scope and create migration plan
   ```

#### ❌ Scenarios Not Requiring Planning Agent:

1. **Simple Bug Fixes** - Create Draft Task directly
2. **Documentation Updates** - Create Draft Task directly
3. **Style Adjustments** - Create Draft Task directly
4. **Configuration Changes** - Create Draft Task directly

### Task Sizing Guidelines

#### 🎯 Ideal Task Sizes:

| Task Type | Estimated Time | Code Changes | Example |
|-----------|----------------|--------------|---------|
| Small Task | 15-30 minutes | 1-3 files | Fix a bug, add a small feature |
| Medium Task | 30-90 minutes | 3-10 files | Implement a component, add an API endpoint |
| Large Task | 90-180 minutes | 10-30 files | Implement a complete functional module |

#### 📝 Task Decomposition Suggestions:

**Example of Oversized Task (Not Recommended):**
```markdown
Title: Build E-commerce System
Description: Need user management, product management, order processing, payment integration
❌ Too large, should be split into multiple independent tasks
```

**Example of Reasonable Task (Recommended):**
```markdown
Task 1: Implement Product List API
Description:
- Create Product data model
- Implement GET /api/products endpoint
- Support pagination and filtering
- Write unit tests
✅ Appropriate size, clear objectives
```

### How to Write Effective Task Descriptions

#### 🌟 Elements of Excellent Task Descriptions:

1. **Clear Objectives**
   ```markdown
   ✅ Good Example:
   Implement user registration functionality, including email verification and password strength checking
   
   ❌ Bad Example:
   Do user registration
   ```

2. **Technical Context**
   ```markdown
   ✅ Good Example:
   Implement global theme switching using React Hooks and Context API,
   theme configuration stored in localStorage
   
   ❌ Bad Example:
   Add theme switching
   ```

3. **Acceptance Criteria**
   ```markdown
   ✅ Good Example:
   Implement order list page, requirements:
   - Display order number, date, amount, status
   - Support filtering by status
   - Support date range search
   - Display 20 records per page
   - Responsive design, support mobile
   
   ❌ Bad Example:
   Make an order list
   ```

4. **Related Files or References**
   ```markdown
   ✅ Good Example:
   Fix user avatar upload issue
   Related files: src/components/ProfileUpload.tsx
   Reference implementation: src/components/ProductImageUpload.tsx
   Error logs: [Attach error screenshots or logs]
   
   ❌ Bad Example:
   Fix upload issue
   ```

#### 📋 Task Description Template:

```markdown
## Task Title
[Concise one-sentence description]

## Background
[Why this task is needed, what's the business value]

## Detailed Requirements
- Requirement 1
- Requirement 2
- Requirement 3

## Technical Requirements
- Tech stack to use
- Standards to follow
- Performance or security requirements

## Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

## Reference Materials
- Related file paths
- Design links
- API documentation
```

---

## ❓ Frequently Asked Questions

### Git Integration Related

**Q: What Git permissions does CTO.NEW need?**

A: CTO.NEW needs the following permissions:
- Read repository code and branches
- Create and manage branches
- Commit code changes
- Create Pull Requests
- Read PR status (optional)

We follow the principle of least privilege and will not access data unrelated to development tasks.

**Q: Can I use Self-Hosted GitLab?**

A: Yes! When connecting GitLab, you can enter a custom GitLab instance URL.

**Q: Will generated code be automatically merged to the main branch?**

A: No. AI only creates Pull Requests, and all code requires manual review before merging.

**Q: How are code conflicts handled?**

A: If AI detects merge conflicts, it will be noted in the PR. You need to manually resolve conflicts or provide guidance for AI to regenerate.

### Credit System

**Q: What are Credits?**

A: Credits are the usage unit of CTO.NEW. Each AI task execution consumes a certain amount of credits, depending on task complexity and code volume.

**Q: How can I get more credits?**

A: 
- New users receive free credits upon registration
- Subscribe to monthly or annual plans
- Participate in referral program to earn bonus credits

**Q: Are credits deducted if a task fails?**

A: If a task fails due to system errors, credits are automatically refunded. If failure is due to unclear task descriptions, credits are not refunded.

### Task Management

**Q: Can multiple tasks run simultaneously?**

A: Yes! You can run multiple tasks simultaneously in different repositories. Multiple tasks can also run in the same repository, but be careful to avoid modifying the same files.

**Q: Can tasks be canceled while running?**

A: You can pause or cancel running tasks at any time. Completed parts are saved, and you can continue later or restart.

**Q: How is the quality of AI-generated code?**

A: AI uses Anthropic Claude Sonnet 4.5, capable of generating high-quality code. However, we still recommend:
- Carefully review generated code
- Run complete test suites
- Perform security checks
- Make necessary adjustments according to team standards

**Q: What code standard checks are supported?**

A: AI automatically runs configured Linters and formatting tools in the project (such as ESLint, Prettier, Pylint, etc.) and attempts to fix detected issues.

**Q: Can I provide custom instructions to AI?**

A: Yes! Include detailed technical requirements and preferences in task descriptions, and AI will follow these instructions. You can also configure general coding standards in repository settings.

**Q: How can I view task execution history?**

A: You can view all task execution records on the "History" page, including:
- Task details and descriptions
- Execution time and status
- Generated code changes
- AI decision logs
- Final PR links

### Team Collaboration

**Q: Are team features supported?**

A: Yes! You can create teams, invite members, and share repositories and credit pools.

**Q: Can task approval processes be set up?**

A: You can configure team settings to require team member approval before Draft Tasks can be started.

**Q: How to avoid task conflicts among team members?**

A: The platform detects concurrent modifications to the same file and reminds team members. It's recommended to use task tags and priorities for coordination.

---

## 🚀 Quick Start

1. **Sign Up** - Visit [cto.new](https://cto.new) to create a free account
2. **Connect Git** - Link your GitHub, GitLab, or Bitbucket account
3. **Add Repositories** - Select code repositories that need AI assistance
4. **Create Tasks** - Write your first development task
5. **Launch AI** - Let the AI Coding Agent work for you
6. **Review PR** - Check generated code and merge

---

## 📞 Support & Feedback

- **Official Website** - [https://cto.new](https://cto.new)
- **Documentation Center** - [https://docs.cto.new](https://docs.cto.new)
- **Issue Reporting** - [GitHub Issues](https://github.com/cto-new/feedback/issues)
- **Email Support** - support@cto.new
- **Community Discussion** - [Discord Community](https://discord.gg/cto-new)

---

## 📄 License

[MIT License](LICENSE)

---

## 🙏 Acknowledgments

Thank you to all developers using CTO.NEW. Your feedback helps us continuously improve the product.

Special thanks to Anthropic for providing powerful Claude AI capabilities.

---

<div align="center">

**Empower Development with AI, Make Programming More Efficient** ✨

Made with ❤️ by CTO.NEW Team

</div>