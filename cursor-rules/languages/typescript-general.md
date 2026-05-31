# TypeScript General Cursor Rules

## Type System
- Use 'interface' for object shapes, 'type' for unions/intersections
- Prefer unknown over any; use type guards
- Use const assertions for literal types
- Discriminated unions for state machines
- Template literal types for string patterns
- Utility types: Partial, Required, Pick, Omit, Record

## Patterns
- Result type for error handling: type Result<T> = { ok: true; data: T } | { ok: false; error: string }
- Builder pattern for complex configurations
- Factory functions over classes for simple cases
- Branded types for domain primitives: type UserId = string & { __brand: 'UserId' }

## Async
- async/await over .then()
- AbortController for cancellation
- Promise.allSettled for parallel ops
- Retry with exponential backoff
- Timeout wrappers

## Imports
- Use path aliases (@/*) configured in tsconfig
- Named imports (no import *)
- Group: builtins → external → internal → types
- Type-only imports: import type { X } from 'y'

## Error Handling
- Never catch and swallow errors silently
- Log errors with context
- Use custom error classes
- Wrap third-party errors

## Testing
- Vitest for unit tests
- describe/it/expect pattern
- Mock only external dependencies
- Test edge cases: null, undefined, empty, overflow
