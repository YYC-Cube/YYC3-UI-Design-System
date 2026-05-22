---
file: CONTRIBUTING.md
description: YYC³ Design System 贡献指南 — 开发环境设置、代码规范、提交规范和 PR 流程
author: YanYuCloudCube Team <admin@0379.email>
version: v2.0.0
created: 2026-02-22
updated: 2026-05-22
status: stable
tags: [contributing],[guide],[development],[workflow]
category: guide
language: zh-CN
---

> ***YanYuCloudCube***
> *言启象限 | 语枢未来*
> ***Words Initiate Quadrants, Language Serves as Core for Future***
> *万象归元于云枢 | 深栈智启新纪元*
> ***All things converge in cloud pivot; Deep stacks ignite a new era of intelligence***

---

# 贡献指南

感谢您对 YYC³ Design System 的关注！本文档帮助您快速参与项目贡献。

## 📋 目录

- [行为准则](#行为准则)
- [环境要求](#环境要求)
- [开发流程](#开发流程)
- [代码规范](#代码规范)
- [提交规范](#提交规范)
- [Pull Request 流程](#pull-request-流程)
- [测试要求](#测试要求)

## 行为准则

参与本项目即表示您同意遵守我们的 [Code of Conduct](CODE_OF_CONDUCT.md)。

## 环境要求

| 工具 | 最低版本 | 推荐版本 |
|------|----------|----------|
| Node.js | 22.0.0 | 22.x LTS |
| pnpm | 10.0.0 | 10.x |
| Git | 2.30.0 | latest |

## 开发流程

### 1. Fork & Clone

```bash
git clone https://github.com/YOUR_USERNAME/YYC3-Design-System.git
cd YYC3-Design-System
pnpm install
```

### 2. 创建分支

```bash
git checkout -b feature/your-feature-name
```

分支命名规范：

| 类型 | 格式 | 示例 |
|------|------|------|
| 新功能 | `feature/*` | `feature/button-loading-state` |
| Bug 修复 | `bugfix/*` | `bugfix/modal-close-focus` |
| 紧急修复 | `hotfix/*` | `hotfix/security-xss` |
| 文档 | `docs/*` | `docs/api-reference` |
| 重构 | `refactor/*` | `refactor/theme-system` |

### 3. 开发 & 测试

```bash
pnpm dev              # 启动开发服务器 (port 3200)
pnpm storybook        # 启动 Storybook (port 6006)
pnpm test             # 运行测试
pnpm test:watch       # 监听模式
pnpm lint             # 代码检查
pnpm typecheck        # 类型检查
```

### 4. 提交代码

```bash
git add .
git commit -m 'feat: add loading state to Button component'
git push origin feature/your-feature-name
```

## 代码规范

### TypeScript / React

- 遵循项目内 ESLint + Prettier 配置
- 所有组件使用 TypeScript strict mode
- 新组件必须包含 JSDoc 文件头注释（参照 YYC³ 规范）
- 使用函数式组件 + Hooks

### 组件文件头模板

```typescript
/**
 * file: ComponentName.tsx
 * description: 组件功能简要描述
 * author: Your Name
 * version: v1.0.0
 * created: 2026-05-22
 * updated: 2026-05-22
 * status: active
 * tags: [component],[ui]
 */
```

### 样式

- 使用 Tailwind CSS utility classes
- 复杂样式使用 `class-variance-authority` (CVA) 定义变体
- 遵循 shadcn/ui 的 `cn()` 合并模式

### 测试

- 新组件必须包含单元测试
- 关键交互必须包含集成测试
- 测试文件与源文件同目录：`Button.tsx` → `Button.test.tsx`

## 提交规范

遵循 [Conventional Commits](https://www.conventionalcommits.org/)：

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### 提交类型

| 类型 | 说明 |
|------|------|
| `feat` | 新功能 |
| `fix` | Bug 修复 |
| `docs` | 文档更新 |
| `style` | 代码格式（不影响功能） |
| `refactor` | 代码重构 |
| `perf` | 性能优化 |
| `test` | 测试相关 |
| `chore` | 构建/工具变动 |
| `ci` | CI/CD 相关 |

### 示例

```
feat(button): add loading state variant
fix(dialog): resolve focus trap issue on close
docs(readme): update installation instructions
refactor(theme): extract color tokens to shared module
```

## Pull Request 流程

### PR 检查清单

- [ ] 代码通过 `pnpm lint` 无错误
- [ ] 类型检查通过 `pnpm typecheck`
- [ ] 所有测试通过 `pnpm test`
- [ ] 新功能有对应的测试覆盖
- [ ] 文件头注释完整
- [ ] 无硬编码密钥或敏感信息

### PR 标题格式

与提交规范一致：`feat(button): add loading state variant`

### PR 描述模板

```markdown
## 变更类型
- [ ] feat: 新功能
- [ ] fix: Bug 修复
- [ ] refactor: 重构
- [ ] docs: 文档

## 变更说明
简要描述本次变更的内容和原因

## 影响范围
列出受影响的组件或模块

## 测试
描述如何验证本次变更
```

## 报告 Bug

1. 搜索 [已有 Issues](https://github.com/YYC-Cube/YYC3-Design-System/issues) 确认未被报告
2. 使用 Bug 报告模板
3. 包含：复现步骤、预期行为、实际行为、环境信息

## 提出新功能

1. 在 [Discussions](https://github.com/YYC-Cube/YYC3-Design-System/discussions) 发起讨论
2. 描述功能需求和使用场景
3. 说明对项目的价值

---

<div align="center">

感谢您的贡献！每一个 PR 都让 YYC³ Design System 更好。

</div>
