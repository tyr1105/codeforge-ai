# API Design Rubric

## Consistency (30%)
| Score | Criteria |
|-------|----------|
| 1 | Inconsistent naming, mixed conventions |
| 2 | Some consistency, exceptions exist |
| 3 | Consistent naming, standard HTTP methods |
| 4 | HATEOAS links, consistent error format |
| 5 | Idiomatic REST/GraphQL, self-documenting |

## Error Handling (25%)
| Score | Criteria |
|-------|----------|
| 1 | Generic errors, no details |
| 2 | HTTP status codes, minimal messages |
| 3 | Problem details format, actionable messages |
| 4 | Error codes, request IDs, retry guidance |
| 5 | Self-healing hints, documentation links |

## Documentation (25%)
| Score | Criteria |
|-------|----------|
| 1 | No documentation |
| 2 | Basic endpoint list |
| 3 | OpenAPI spec with examples |
| 4 | Interactive docs, try-it-out, auth setup |
| 5 | Guides, tutorials, SDKs, changelog |

## Performance (20%)
| Score | Criteria |
|-------|----------|
| 1 | No pagination, full data dumps |
| 2 | Basic pagination, no caching |
| 3 | Cursor pagination, ETags, compression |
| 4 | GraphQL field selection, batching |
| 5 | CDN-cached, precomputed, edge-optimized |
