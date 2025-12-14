# Turborepo Monorepo

A modern monorepo setup using Turborepo with Next.js and Node.js Express server.

## Project Structure

```
├── apps/
│   ├── web/          # Next.js application
│   └── server/       # Node.js Express server
├── packages/
│   └── ui/           # Shared UI component library
├── turbo.json        # Turborepo configuration
└── package.json      # Root package.json with workspaces
```

## What's Inside?

### Apps

- **web**: A [Next.js](https://nextjs.org/) app (App Router)
- **server**: A [Node.js](https://nodejs.org/) Express server

### Packages

- **ui**: A shared React component library used by the web app

## Getting Started

### Prerequisites

- Node.js 18+ and pnpm

### Installation

Install all dependencies:

```bash
pnpm install
```

### Development

Run all apps in development mode:

```bash
pnpm dev
```

This will start:
- Next.js app on [http://localhost:3000](http://localhost:3000)
- Express server on [http://localhost:3001](http://localhost:3001)

### Build

Build all apps and packages:

```bash
pnpm build
```

### Individual App Commands

Navigate to specific apps to run commands:

```bash
# Web app
cd apps/web
pnpm dev    # Start Next.js dev server
pnpm build  # Build for production
pnpm start  # Start production server

# Server
cd apps/server
pnpm dev    # Start Express dev server with hot reload
pnpm build  # Compile TypeScript
pnpm start  # Start production server
```

## Turborepo Features

- **Fast builds**: Turborepo caches build outputs for faster rebuilds
- **Parallel execution**: Runs tasks across workspaces in parallel
- **Pipeline configuration**: Smart task orchestration in `turbo.json`
- **Remote caching**: Share build cache across your team (optional)

## Adding New Packages

To add a new shared package:

1. Create a new directory in `packages/`
2. Add a `package.json` with the package name
3. Update workspace references in apps that use it

## Learn More

- [Turborepo Documentation](https://turbo.build/repo/docs)
- [Next.js Documentation](https://nextjs.org/docs)
- [Express Documentation](https://expressjs.com/)
