# Microservices Patterns Cursor Rules

## Service Design
- Bounded contexts from Domain-Driven Design
- API-first design (OpenAPI spec before code)
- Database per service (no shared databases)
- Async communication via events (Kafka/RabbitMQ)
- Idempotent endpoints for retry safety

## Communication
- gRPC for internal service-to-service
- REST for external/public APIs
- GraphQL for flexible client queries
- Event-driven for decoupled workflows
- Circuit breaker for fault tolerance

## Data Management
- Saga pattern for distributed transactions
- Event sourcing for audit trails
- CQRS for read-heavy workloads
- Outbox pattern for reliable event publishing
- Eventually consistent data views

## Observability
- Distributed tracing (OpenTelemetry)
- Structured logging with correlation IDs
- Metrics: RED (Rate, Errors, Duration) per service
- Service mesh for mutual TLS
- Chaos engineering for resilience testing

## Deployment
- Containerized services (Docker)
- Orchestration (Kubernetes)
- Blue-green or canary deployments
- Feature flags for gradual rollouts
- Automated rollback on error rate spike
