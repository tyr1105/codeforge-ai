# CLAUDE.md - Monorepo Project

## Project Overview
This is a monorepo containing [list of apps/packages].

## Tech Stack
- Build: Turborepo / Nx
- Package manager: pnpm
- Language: TypeScript
- Shared: UI components, config, types

## Structure
```
apps/
  web/          # Next.js frontend
  api/          # Backend API
  docs/         # Documentation site
packages/
  ui/           # Shared UI components
  config/       # Shared configs (ESLint, TS, etc.)
  types/        # Shared TypeScript types
  utils/        # Shared utilities
```

## Development Rules
- Changes to packages/ should be backwards compatible
- Each package has its own tests
- Use workspace:* for internal dependencies
- Changesets for versioning across packages
- Run affected tests only in CI

## Common Commands
- pnpm dev              # Start all apps
- pnpm build            # Build all packages
- pnpm test             # Run all tests
- pnpm lint             # Lint everything
- pnpm changeset        # Create a changeset
- pnpm version-packages # Version changed packages

## IMPORTANT
- Never use relative imports across packages
- Shared types in packages/types only
- Keep packages focused and small
- No circular dependencies between packages
