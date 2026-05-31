# CLAUDE.md - API Backend Project

## Project Overview
[Project name] is a REST/GraphQL API that [purpose].

## Tech Stack
- Language: Python 3.12+ / TypeScript / Go
- Framework: FastAPI / Express / Axum
- Database: PostgreSQL
- Cache: Redis
- Queue: BullMQ / Celery / Sidekiq
- Auth: JWT + API Keys

## Architecture
- Clean Architecture / Hexagonal
- Repository pattern for data access
- Service layer for business logic
- Controller layer for HTTP handling

## API Design Rules
- Consistent response format: { data, meta, errors }
- Versioned routes: /api/v1/
- OpenAPI spec documentation
- Rate limiting on all endpoints
- Input validation with Zod / Pydantic

## Database
- Migrations are version controlled
- Never run destructive migrations in production
- Use transactions for multi-step operations
- Index foreign keys and query columns

## Testing
- Unit tests for services
- Integration tests for API endpoints
- Test database is reset between tests
- Coverage target: 80%

## Deployment
- Docker containers
- Health check endpoint: /health
- Graceful shutdown
- Environment-based configuration
