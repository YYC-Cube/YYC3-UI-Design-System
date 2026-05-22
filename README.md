---
file: README.md
description: YYC³ Design System — 五高五标五化框架驱动的企业级开源设计系统
author: YanYuCloudCube Team <admin@0379.email>
version: v2.1.0
created: 2026-02-22
updated: 2026-05-22
status: stable
tags: [design-system],[react],[typescript],[tailwindcss],[open-source]
category: general
language: bilingual
---

<div align="center">

# YYC³ Design System

<img src="public/Design-System-001.png" alt="YYC³ Design System" width="720" />

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-blue)](https://github.com/YYC-Cube/YYC3-Design-System/actions)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?logo=TypeScript&logoColor=white)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=React&logoColor=white)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?logo=Vite&logoColor=white)](https://vitejs.dev/)
[![pnpm](https://img.shields.io/badge/pnpm-10-F69220?logo=pnpm&logoColor=white)](https://pnpm.io/)

---

> ***YanYuCloudCube***
> *言启象限 | 语枢未来*
> ***Words Initiate Quadrants, Language Serves as Core for Future***
> *万象归元于云枢 | 深栈智启新纪元*
> ***All things converge in cloud pivot; Deep stacks ignite a new era of intelligence***

**[🌐 Live Demo](https://design-ui.yyc3.top/)**
·
**[📖 Documentation](./docs/)**
·
**[🧩 Storybook](http://localhost:6006)**

**Language**: [English](#-english) | [简体中文](#-简体中文)

</div>

---

## 🇬🇧 English

### ✨ Overview

YYC³ Design System is an enterprise-grade, open-source design system built on the **Five-High / Five-Standard / Five-Implementation** philosophy. It provides a complete design solution with three switchable themes, bilingual support (Chinese/English), and comprehensive testing infrastructure.

#### Key Features

- 🎨 **Three Theme System** — Future (tech), Cyber (punk), Business (professional), each with light/dark modes
- 🎯 **OKLCH Color Space** — Perceptually uniform colors with HEX fallback
- 🧩 **50+ UI Components** — Built on Radix UI primitives + shadcn/ui patterns
- 🌍 **Bilingual (zh/en)** — Real-time language switching with persistent storage
- ♿ **WCAG 2.1 AA** — Full accessibility compliance via Radix UI
- ⚡ **High Performance** — Gzip < 200KB, code splitting, tree shaking
- 🔒 **Security Hardened** — XSS protection, CSP, input sanitization
- 🧪 **Comprehensive Testing** — Unit, integration, E2E, a11y, visual regression

### 🚀 Quick Start

#### Prerequisites

- Node.js >= 22.0.0
- pnpm >= 10.0.0

#### Install & Run

```bash
git clone https://github.com/YYC-Cube/YYC3-Design-System.git
cd YYC3-Design-System
pnpm install
pnpm dev
```

The dev server starts at **<http://localhost:3200>**

#### Build for Production

```bash
pnpm build
```

Output is in `dist/`, deployed to **<https://design-ui.yyc3.top/>**

### 🛠️ Tech Stack

| Layer | Technology | Version |
|-------|-----------|---------|
| UI Framework | React | 18.3 |
| Language | TypeScript | 5.9 |
| Build Tool | Vite | 5.4 |
| Styling | Tailwind CSS | 4.2 |
| UI Primitives | Radix UI | latest |
| Component Patterns | shadcn/ui | custom |
| State Management | Zustand | 5.x |
| Routing | React Router | 7.x |
| Package Manager | pnpm | 10.x |

### 📜 Scripts

| Command | Description |
|---------|-------------|
| `pnpm dev` | Start dev server (port 3200) |
| `pnpm build` | Production build |
| `pnpm preview` | Preview production build |
| `pnpm test` | Run unit/integration tests |
| `pnpm test:coverage` | Run tests with coverage |
| `pnpm test:e2e` | Run E2E tests (Playwright) |
| `pnpm lint` | ESLint check |
| `pnpm format:check` | Prettier check |
| `pnpm typecheck` | TypeScript type check |
| `pnpm storybook` | Start Storybook (port 6006) |
| `pnpm build-storybook` | Build Storybook static site |
| `pnpm qa` | Full QA pipeline (typecheck + lint + test + e2e) |

### 🎭 Themes

| Theme | Style | Use Case |
|-------|-------|----------|
| **Future** | Neon blue, purple, cyan gradients | Technology, innovation, startups |
| **Cyber** | Pink, red, neon green accents | Gaming, entertainment, creative |
| **Business** | Blue, gray, white palette | Enterprise, corporate, professional |

Each theme supports **light** and **dark** mode.

### 🌍 Internationalization

- **zh-CN** — 简体中文
- **en-US** — English (United States)

Locale files: `src/i18n/locales/zh-CN.json`, `src/i18n/locales/en-US.json`

### 🧪 Testing

| Type | Tool | Command |
|------|------|---------|
| Unit / Integration | Jest + Testing Library | `pnpm test` |
| E2E | Playwright | `pnpm test:e2e` |
| Visual Regression | Chromatic | `pnpm chromatic` |
| Accessibility | jest-axe | `pnpm test:a11y` |
| Performance | Lighthouse CI | `pnpm test:perf` |

### 📦 Project Structure

```
yyc3-UI-Design-System/
├── .github/workflows/     # CI/CD pipelines
├── .storybook/            # Storybook configuration
├── config/                # App-level configuration
├── design/                # Design tokens (JSON source)
├── docs/                  # Project documentation
├── public/                # Static assets (CNAME, PWA icons, favicon)
├── src/
│   ├── ai/                # AI-powered features
│   ├── components/        # React components + shadcn/ui
│   ├── components/ui/     # Base UI primitives (Radix)
│   ├── context/           # React context providers
│   ├── i18n/              # Internationalization
│   ├── pages/             # Application pages
│   ├── stores/            # Zustand state stores
│   ├── styles/            # CSS / Tailwind styles
│   └── main.tsx           # Entry point
├── LICENSE                # MIT License
├── CHANGELOG.md           # Version history
├── CONTRIBUTING.md        # Contribution guide
├── CODE_OF_CONDUCT.md     # Community standards
└── package.json           # Project manifest
```

### 🤝 Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md).

#### Quick Contribution Flow

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make changes and add tests
4. Run QA: `pnpm qa`
5. Commit: `git commit -m 'feat: add amazing feature'`
6. Push: `git push origin feature/amazing-feature`
7. Open a Pull Request

### 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

Copyright (c) 2026 YanYuCloudCube Team

---

<div align="center">

**[⬆ Top](#yyc-design-system)** · **[🇨🇳 切换到中文](#-简体中文)**

</div>

---
---

## 🇨🇳 简体中文

### ✨ 概述

YYC³ Design System 是基于**「五高五标五化」**核心理念构建的企业级开源设计系统。提供三套可切换主题、中英双语支持以及完整的测试基础设施。

#### 核心特性

- 🎨 **三主题系统** — Future（科技）、Cyber（赛博朋克）、Business（商务），每套支持浅色/暗色模式
- 🎯 **OKLCH 色彩空间** — 感知均匀色彩，带 HEX 兼容回退
- 🧩 **50+ UI 组件** — 基于 Radix UI 原语 + shadcn/ui 模式构建
- 🌍 **中英双语** — 实时语言切换，本地持久化存储
- ♿ **WCAG 2.1 AA** — 通过 Radix UI 实现完整可访问性合规
- ⚡ **高性能** — Gzip < 200KB，代码分割，Tree Shaking
- 🔒 **安全加固** — XSS 防护、CSP、输入净化
- 🧪 **全面测试** — 单元、集成、E2E、可访问性、视觉回归

### 🚀 快速开始

#### 环境要求

- Node.js >= 22.0.0
- pnpm >= 10.0.0

#### 安装与运行

```bash
git clone https://github.com/YYC-Cube/YYC3-Design-System.git
cd YYC3-Design-System
pnpm install
pnpm dev
```

开发服务器启动在 **<http://localhost:3200>**

#### 生产构建

```bash
pnpm build
```

构建产物在 `dist/`，自动部署到 **<https://design-ui.yyc3.top/>**

### 🛠️ 技术栈

| 层级 | 技术 | 版本 |
|------|------|------|
| UI 框架 | React | 18.3 |
| 编程语言 | TypeScript | 5.9 |
| 构建工具 | Vite | 5.4 |
| 样式方案 | Tailwind CSS | 4.2 |
| UI 原语 | Radix UI | latest |
| 组件模式 | shadcn/ui | custom |
| 状态管理 | Zustand | 5.x |
| 路由 | React Router | 7.x |
| 包管理器 | pnpm | 10.x |

### 📜 常用脚本

| 命令 | 说明 |
|------|------|
| `pnpm dev` | 启动开发服务器（端口 3200） |
| `pnpm build` | 生产构建 |
| `pnpm preview` | 预览生产构建 |
| `pnpm test` | 运行单元/集成测试 |
| `pnpm test:coverage` | 运行测试并生成覆盖率 |
| `pnpm test:e2e` | 运行 E2E 测试（Playwright） |
| `pnpm lint` | ESLint 检查 |
| `pnpm format:check` | Prettier 格式检查 |
| `pnpm typecheck` | TypeScript 类型检查 |
| `pnpm storybook` | 启动 Storybook（端口 6006） |
| `pnpm build-storybook` | 构建 Storybook 静态站点 |
| `pnpm qa` | 完整 QA 流水线（类型检查 + 代码检查 + 测试 + E2E） |

### 🎭 主题

| 主题 | 风格 | 适用场景 |
|------|------|----------|
| **Future** | 霓虹蓝、紫、青渐变 | 科技、创新、初创 |
| **Cyber** | 粉、红、霓虹绿点缀 | 游戏、娱乐、创意 |
| **Business** | 蓝、灰、白配色 | 企业、商务、正式 |

每套主题均支持**浅色**和**暗色**模式。

### 🌍 国际化

- **zh-CN** — 简体中文
- **en-US** — English (United States)

语言文件：`src/i18n/locales/zh-CN.json`、`src/i18n/locales/en-US.json`

### 🧪 测试

| 类型 | 工具 | 命令 |
|------|------|------|
| 单元/集成 | Jest + Testing Library | `pnpm test` |
| E2E | Playwright | `pnpm test:e2e` |
| 视觉回归 | Chromatic | `pnpm chromatic` |
| 可访问性 | jest-axe | `pnpm test:a11y` |
| 性能 | Lighthouse CI | `pnpm test:perf` |

### 📦 项目结构

```
yyc3-UI-Design-System/
├── .github/workflows/     # CI/CD 流水线
├── .storybook/            # Storybook 配置
├── config/                # 应用级配置
├── design/                # 设计令牌（JSON 源文件）
├── docs/                  # 项目文档
├── public/                # 静态资源（CNAME、PWA 图标、网站图标）
├── src/
│   ├── ai/                # AI 功能模块
│   ├── components/        # React 组件 + shadcn/ui
│   ├── components/ui/     # 基础 UI 原语（Radix）
│   ├── context/           # React Context 提供者
│   ├── i18n/              # 国际化
│   ├── pages/             # 应用页面
│   ├── stores/            # Zustand 状态仓库
│   ├── styles/            # CSS / Tailwind 样式
│   └── main.tsx           # 入口文件
├── LICENSE                # MIT 许可证
├── CHANGELOG.md           # 版本日志
├── CONTRIBUTING.md        # 贡献指南
├── CODE_OF_CONDUCT.md     # 社区行为准则
└── package.json           # 项目清单
```

### 🤝 参与贡献

欢迎参与贡献！请阅读 [贡献指南](CONTRIBUTING.md) 和 [社区行为准则](CODE_OF_CONDUCT.md)。

#### 快速贡献流程

1. Fork 本仓库
2. 创建功能分支：`git checkout -b feature/amazing-feature`
3. 编写代码并添加测试
4. 运行 QA：`pnpm qa`
5. 提交：`git commit -m 'feat: add amazing feature'`
6. 推送：`git push origin feature/amazing-feature`
7. 发起 Pull Request

### 📜 许可证

本项目基于 **MIT 许可证** 开源，详见 [LICENSE](LICENSE) 文件。

Copyright (c) 2026 YanYuCloudCube Team

---

<div align="center">

**[⬆ 返回顶部](#yyc-design-system)** · **[🇬🇧 Switch to English](#-english)**

Made with ❤️ by [YYC³ Team](https://github.com/YYC-Cube)

</div>
