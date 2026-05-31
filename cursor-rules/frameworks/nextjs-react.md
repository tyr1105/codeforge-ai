# Next.js + React Cursor Rules

## Project Structure
- App Router only (no Pages Router)
- Server Components by default
- Use 'use client' only when needed (event handlers, hooks, browser APIs)
- Co-locate components: app/[route]/components/
- Use TypeScript strictly (no 'any' types)

## Component Patterns
- Functional components with named exports
- Props defined as interface, not type alias
- Use React.memo for expensive renders
- Destructure props in function signature
- Children prop: use { children }: { children: React.ReactNode }

## Styling
- Tailwind CSS classes inline (no @apply in globals unless shared)
- Use cn() utility for conditional classes
- Mobile-first responsive design
- Dark mode: use 'dark:' prefix

## Data Fetching
- Server Components for data fetching
- Use 'use server' for Server Actions
- Suspend with loading.tsx for streaming
- Use React cache() for deduplication
- Error boundaries with error.tsx

## State Management
- URL state for filters/pagination (searchParams)
- React Context for theme/locale only
- Zustand for complex client state
- Server state: TanStack Query v5

## API Routes
- Route Handlers: app/api/[route]/route.ts
- Validate with Zod schemas
- Return { data, error } pattern
- Use NextResponse.json() for responses

## Testing
- Vitest for unit tests
- Playwright for E2E
- Testing Library for component tests
- Test files: __tests__/ directory or .test.ts suffix
