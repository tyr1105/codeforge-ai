# CLAUDE.md - Full-Stack SaaS Project

## Project Overview
[Project name] is a [description] built for [target users].

## Tech Stack
- Frontend: Next.js 15 (App Router) + React 19 + TypeScript
- Styling: Tailwind CSS 4 + shadcn/ui
- Auth: Supabase Auth (email + OAuth)
- Database: PostgreSQL via Supabase
- Payments: Stripe
- Hosting: Vercel
- ORM: Drizzle ORM
- State: TanStack Query v5

## Project Structure
```
app/
  (auth)/        # Auth pages (login, signup)
  (dashboard)/   # Protected dashboard
  api/           # API routes
components/
  ui/            # shadcn/ui components
  features/      # Feature-specific components
lib/
  db/            # Database schema & queries
  stripe/        # Stripe helpers
  supabase/      # Auth & DB client
```

## Coding Conventions
- Server Components by default
- 'use client' only when needed
- Named exports for components
- TypeScript strict mode
- Zod for validation
- Error boundaries at route level

## Testing
- Vitest for unit tests
- Playwright for E2E
- Test files: __tests__/ or .test.ts

## Common Tasks
- New page: Create app/[route]/page.tsx
- New API: Create app/api/[route]/route.ts
- New component: Create components/[feature]/ComponentName.tsx
- DB migration: npx drizzle-kit generate && npx drizzle-kit migrate

## IMPORTANT
- Never expose service role keys to client
- Always validate user auth before data access
- Use server actions for mutations when possible
- Stripe webhooks must verify signature
