# API Design Pattern Cursor Rules

## REST Conventions
- Plural nouns for collections: /users, /orders
- Nested resources for ownership: /users/:id/orders
- Filter with query params: ?status=active&page=1
- Use HTTP methods correctly: GET (read), POST (create), PUT (full update), PATCH (partial), DELETE
- Consistent response envelope: { data, meta, errors }

## Authentication
- Bearer token in Authorization header
- Refresh token rotation
- Scope-based permissions
- Rate limiting per user/IP
- API key for service accounts

## Versioning
- URL-based: /api/v1/ (preferred for public APIs)
- Header-based for internal APIs
- Sunset header for deprecation notices
- Migration guide per version

## Error Responses
- RFC 7807 Problem Details format
- Consistent error codes (not HTTP status codes)
- Human-readable message + machine-readable code
- Include request ID for debugging
- Don't expose stack traces in production

## Performance
- Pagination (cursor-based for large datasets)
- Field selection: ?fields=id,name,email
- Embedding: ?include=orders.items
- ETags for caching
- Compression (gzip/brotli)
