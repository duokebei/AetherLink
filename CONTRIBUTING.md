# Contributing to AetherLink | 贡献指南

Thank you for your interest in contributing to AetherLink! | 感谢你对 AetherLink 的关注！

[English](#english) | [中文](#中文)

---

<a name="english"></a>

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment. We expect all contributors to:

- Be respectful and constructive in discussions
- Accept constructive criticism gracefully
- Focus on what is best for the community
- Show empathy towards other community members

## How to Contribute

### Reporting Bugs

Before creating a bug report, please check existing issues to avoid duplicates.

**Bug reports should include:**

1. **Environment** — OS, Node.js version, browser/device
2. **Steps to reproduce** — Clear, minimal reproduction steps
3. **Expected behavior** — What you expected to happen
4. **Actual behavior** — What actually happened
5. **Screenshots/Logs** — If applicable

### Suggesting Features

Feature requests are welcome! Please provide:

1. **Use case** — Why is this feature needed?
2. **Proposed solution** — How should it work?
3. **Alternatives considered** — Other approaches you've thought of

### Pull Requests

1. **Fork** the repository
2. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/issue-description
   ```
3. **Make your changes** following our code standards
4. **Test** your changes thoroughly
5. **Commit** using conventional commits
6. **Push** and create a Pull Request

## Development Setup

### Prerequisites

- Node.js ≥ 22.0.0
- npm ≥ 10.0.0 or Yarn 1.22+
- Git

### Local Development

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/AetherLink.git
cd AetherLink

# Install dependencies
npm install

# Start development server
npm run dev
```

### Useful Commands

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with CORS proxy |
| `npm run build` | Production build |
| `npm run build:ultra` | Full build with type checking |
| `npm run type-check` | Run TypeScript type checking |
| `npm run lint` | Run ESLint |
| `npm run lint:fast` | Run ESLint with cache |

## Code Standards

### TypeScript

- Use TypeScript for all new code
- Avoid `any` type — use proper typing or `unknown`
- Export types/interfaces when they may be reused
- Use strict mode configurations

### React

- Prefer functional components with hooks
- Use React 19 features appropriately
- Keep components focused and single-purpose
- Extract reusable logic into custom hooks

### File Naming

| Type | Convention | Example |
|------|------------|---------|
| Components | PascalCase | `ChatInput.tsx` |
| Hooks | camelCase with `use` prefix | `useModelSelection.ts` |
| Services | PascalCase with `Service` suffix | `TTSService.ts` |
| Types | PascalCase | `Assistant.ts` |
| Utilities | camelCase | `formatUtils.ts` |

### Import Order

```typescript
// 1. External dependencies
import React from 'react';
import { useSelector } from 'react-redux';

// 2. Internal modules (absolute paths)
import { APIService } from '@/shared/services/APIService';
import { useModels } from '@/shared/hooks/useModels';

// 3. Relative imports
import { ChatHeader } from './ChatHeader';

// 4. Types (if separate)
import type { Message } from '@/shared/types';

// 5. Styles
import './styles.css';
```

## Commit Convention

We use [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Types

| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `style` | Code style (formatting, semicolons, etc.) |
| `refactor` | Code refactoring |
| `perf` | Performance improvement |
| `test` | Adding or updating tests |
| `chore` | Build process or auxiliary tool changes |
| `ci` | CI configuration changes |

### Examples

```bash
feat(chat): add voice input support
fix(tts): resolve Azure TTS streaming issue
docs: update README with new build commands
refactor(api): simplify model fetching logic
```

## Pull Request Guidelines

### Before Submitting

- [ ] Code compiles without errors (`npm run build`)
- [ ] Linting passes (`npm run lint`)
- [ ] Type checking passes (`npm run type-check`)
- [ ] Changes are tested locally
- [ ] Commit messages follow conventions

### PR Title Format

Follow the same convention as commits:

```
feat(scope): description
fix(scope): description
```

### PR Description Template

```markdown
## Summary
Brief description of changes.

## Changes
- Change 1
- Change 2

## Testing
How were these changes tested?

## Screenshots
If applicable, add screenshots.

## Related Issues
Fixes #123
```

## Branch Naming

| Type | Format | Example |
|------|--------|---------|
| Feature | `feature/description` | `feature/mcp-tool-support` |
| Bug Fix | `fix/description` | `fix/tts-playback-error` |
| Docs | `docs/description` | `docs/api-documentation` |
| Refactor | `refactor/description` | `refactor/state-management` |

## License

By contributing to AetherLink, you agree that your contributions will be licensed under the [AGPLv3 License](LICENSE).

---

<a name="中文"></a>

## 行为准则

参与本项目即表示你同意维护一个尊重和包容的环境。我们期望所有贡献者：

- 在讨论中保持尊重和建设性
- 优雅地接受建设性批评
- 关注对社区最有利的事情
- 对其他社区成员表示同理心

## 如何贡献

### 报告 Bug

提交 Bug 报告前，请先检查现有 Issue 以避免重复。

**Bug 报告应包括：**

1. **环境** — 操作系统、Node.js 版本、浏览器/设备
2. **复现步骤** — 清晰、简洁的复现步骤
3. **预期行为** — 你期望发生什么
4. **实际行为** — 实际发生了什么
5. **截图/日志** — 如果适用

### 功能建议

欢迎功能建议！请提供：

1. **使用场景** — 为什么需要这个功能？
2. **解决方案** — 它应该如何工作？
3. **备选方案** — 你考虑过的其他方法

### Pull Request

1. **Fork** 仓库
2. 从 `main` **创建分支**：
   ```bash
   git checkout -b feature/your-feature-name
   # 或
   git checkout -b fix/issue-description
   ```
3. 按照代码规范**进行修改**
4. **充分测试**你的更改
5. 使用约定式提交**提交**代码
6. **推送**并创建 Pull Request

## 开发环境设置

### 前置要求

- Node.js ≥ 22.0.0
- npm ≥ 10.0.0 或 Yarn 1.22+
- Git

### 本地开发

```bash
# 克隆你的 fork
git clone https://github.com/YOUR_USERNAME/AetherLink.git
cd AetherLink

# 安装依赖
npm install

# 启动开发服务器
npm run dev
```

### 常用命令

| 命令 | 描述 |
|------|------|
| `npm run dev` | 启动开发服务器（含 CORS 代理） |
| `npm run build` | 生产环境构建 |
| `npm run build:ultra` | 完整构建（含类型检查） |
| `npm run type-check` | TypeScript 类型检查 |
| `npm run lint` | ESLint 检查 |
| `npm run lint:fast` | ESLint 检查（带缓存） |

## 代码规范

### TypeScript

- 所有新代码使用 TypeScript
- 避免使用 `any` 类型 — 使用正确的类型或 `unknown`
- 导出可复用的类型/接口
- 使用严格模式配置

### React

- 优先使用函数组件和 Hooks
- 合理使用 React 19 特性
- 保持组件专注和单一职责
- 将可复用逻辑提取为自定义 Hook

### 文件命名

| 类型 | 规范 | 示例 |
|------|------|------|
| 组件 | PascalCase | `ChatInput.tsx` |
| Hooks | camelCase + `use` 前缀 | `useModelSelection.ts` |
| 服务 | PascalCase + `Service` 后缀 | `TTSService.ts` |
| 类型 | PascalCase | `Assistant.ts` |
| 工具函数 | camelCase | `formatUtils.ts` |

### 导入顺序

```typescript
// 1. 外部依赖
import React from 'react';
import { useSelector } from 'react-redux';

// 2. 内部模块（绝对路径）
import { APIService } from '@/shared/services/APIService';
import { useModels } from '@/shared/hooks/useModels';

// 3. 相对导入
import { ChatHeader } from './ChatHeader';

// 4. 类型（如果单独导入）
import type { Message } from '@/shared/types';

// 5. 样式
import './styles.css';
```

## 提交规范

我们使用 [Conventional Commits](https://www.conventionalcommits.org/)：

```
<type>(<scope>): <description>

[可选的正文]

[可选的脚注]
```

### 类型

| 类型 | 描述 |
|------|------|
| `feat` | 新功能 |
| `fix` | Bug 修复 |
| `docs` | 仅文档更改 |
| `style` | 代码风格（格式化、分号等） |
| `refactor` | 代码重构 |
| `perf` | 性能优化 |
| `test` | 添加或更新测试 |
| `chore` | 构建过程或辅助工具变更 |
| `ci` | CI 配置变更 |

### 示例

```bash
feat(chat): 添加语音输入支持
fix(tts): 修复 Azure TTS 流式播放问题
docs: 更新 README 构建命令
refactor(api): 简化模型获取逻辑
```

## Pull Request 指南

### 提交前检查

- [ ] 代码编译无错误 (`npm run build`)
- [ ] Lint 检查通过 (`npm run lint`)
- [ ] 类型检查通过 (`npm run type-check`)
- [ ] 本地测试通过
- [ ] 提交信息符合规范

### PR 标题格式

遵循与提交相同的规范：

```
feat(scope): 描述
fix(scope): 描述
```

### PR 描述模板

```markdown
## 概述
简要描述更改内容。

## 更改
- 更改 1
- 更改 2

## 测试
这些更改是如何测试的？

## 截图
如果适用，请添加截图。

## 相关 Issue
Fixes #123
```

## 分支命名

| 类型 | 格式 | 示例 |
|------|------|------|
| 功能 | `feature/描述` | `feature/mcp-tool-support` |
| Bug 修复 | `fix/描述` | `fix/tts-playback-error` |
| 文档 | `docs/描述` | `docs/api-documentation` |
| 重构 | `refactor/描述` | `refactor/state-management` |

## 许可证

为 AetherLink 贡献即表示你同意你的贡献将在 [AGPLv3 许可证](LICENSE) 下发布。
