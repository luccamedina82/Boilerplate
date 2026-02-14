# 🎾 Padel AppMonorepo

> **Scalable, High-Performance Monorepo Architecture**
## 🏗️ Architecture Overview

This repository uses a **Monorepo** strategy to share logic, interfaces, and configurations between the Backend and Frontend instantly.

| **Scope** | **Tech Stack** | **Port** | **Description** |
| :--- | :--- | :--- | :--- |
| **Backend** | NestJS + **Fastify** | `3000` | High-performance API. Uses `fastify-adapter`. |
| **Frontend** | Next.js 15 + **React Compiler** | `3001` | Modern Web App using App Router & experimental React Compiler. |
| **Shared** | TypeScript Interfaces | - | Shared DTOs, Enums, and Utilities. **Zero duplication.** |
| **Config** | TSConfig | - | Orchestration, linting, and git hooks. | ESLint and Husky need to be configurated

## 🚀 Getting Started

### Prerequisites
- **Node.js** (v20+ recommended)
- **pnpm** (Required for workspaces)
  ```bash
  npm install -g pnpm

1. Installation
Install all dependencies across apps and packages:

  Bash
  pnpm install

2. Running Development Server
Start the entire ecosystem (API + Web) in parallel:

  Bash
  pnpm dev
  

📂 Project Structure
├── apps/
│   ├── api/            # NestJS Backend (Port 3000)
│   └── web/            # Next.js Frontend (Port 3001)
│
├── packages/
│   ├── shared/         # Shared Types (DTOs, Interfaces)
│   ├── config/       # Shared TypeScript Configurations
│   └── eslint-config/  # Shared Linting Rules
│
└── pnpm-workspace.yaml # Workspace Definition


Command,Action
pnpm dev   --> Starts all apps in watch mode.
pnpm build --> Builds all apps and packages using Turbo cache.
pnpm lint  --> Runs ESLint across the entire monorepo.
pnpm clean --> Removes node_modules and dist folders (Manual cleanup). --> needs to be configurated 
