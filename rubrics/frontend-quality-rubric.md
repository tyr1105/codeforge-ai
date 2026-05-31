# Frontend Quality Rubric

## Component Design (30%)
| Score | Criteria |
|-------|----------|
| 1 | God components, mixed concerns |
| 2 | Some separation, still coupled |
| 3 | Clear responsibility, reasonable size |
| 4 | Composable, reusable, well-props |
| 5 | Library-quality, fully documented |

## State Management (25%)
| Score | Criteria |
|-------|----------|
| 1 | Props drilling, global mutation |
| 2 | Some state management, inconsistent |
| 3 | Appropriate patterns (local vs global) |
| 4 | Optimistic updates, loading states |
| 5 | Offline-first, cache invalidation |

## User Experience (25%)
| Score | Criteria |
|-------|----------|
| 1 | Broken interactions, no feedback |
| 2 | Basic interactions, missing edge cases |
| 3 | Responsive, accessible, loading states |
| 4 | Animations, keyboard nav, error recovery |
| 5 | Delightful, accessible, performant |

## Performance (20%)
| Score | Criteria |
|-------|----------|
| 1 | Unusable on slow connections |
| 2 | Heavy bundle, unnecessary re-renders |
| 3 | Code-split, lazy-loaded, memo where needed |
| 4 | Optimistic UI, virtual scrolling for lists |
| 5 | Sub-second LCP, zero CLS, <100ms FID |
