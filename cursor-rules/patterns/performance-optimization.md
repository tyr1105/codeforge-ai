# Performance Optimization Cursor Rules

## Frontend
- Code splitting at route level
- Lazy load images (Intersection Observer)
- Virtual scrolling for long lists
- Debounce/throttle event handlers
- Web Workers for CPU-heavy computation
- Service Worker for offline caching
- Measure: Lighthouse, Web Vitals (LCP, FID, CLS)

## Backend
- Connection pooling for databases
- Caching layers (Redis, CDN)
- Async I/O for non-blocking operations
- Batch database queries (N+1 prevention)
- Response compression
- Database query optimization (indexes, EXPLAIN)

## Database
- Index columns in WHERE, JOIN, ORDER BY
- Avoid SELECT *, fetch only needed columns
- Pagination (cursor > offset for large tables)
- Read replicas for heavy read workloads
- Partitioning for time-series data

## Infrastructure
- CDN for static assets
- Auto-scaling for variable load
- Container resource limits
- Graceful shutdown for zero-downtime deploys
- Health checks for load balancer
