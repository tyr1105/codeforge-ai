# SQL Database Cursor Rules

## Query Writing
- CTEs for readability (WITH clause)
- Window functions for analytics (ROW_NUMBER, LAG, LEAD)
- Parameterized queries only (no string interpolation)
- EXPLAIN ANALYZE before merging complex queries
- Use COALESCE and NULLIF for null handling

## Schema Design
- UUIDs for primary keys (avoid auto-increment in distributed)
- Timestamps: created_at, updated_at with triggers
- Soft delete with deleted_at column
- JSONB for flexible attributes (PostgreSQL)
- Proper indexing: B-tree for equality/range, GIN for JSON/full-text

## Migration Rules
- Always reversible (write DOWN migrations)
- No data loss in migrations
- Add columns as nullable first, backfill, then add constraint
- Index creation CONCURRENTLY in production
- Test migrations against production-like data volume

## Performance
- Index foreign keys
- Composite indexes for multi-column WHERE
- Partial indexes for filtered queries
- Materialized views for heavy aggregations
- Connection pooling (PgBouncer or built-in)
