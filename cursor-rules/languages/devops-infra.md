# DevOps & Infrastructure Cursor Rules

## Docker
- Multi-stage builds for small images
- Non-root user in containers
- .dockerignore for node_modules, .git
- Pin base image versions (no :latest)
- Health checks in Dockerfile/Compose

## CI/CD
- Fail fast on lint/type errors
- Cache dependencies (node_modules, pip, cargo)
- Matrix builds for multi-version testing
- Artifact retention policies
- Secrets via environment variables, never hardcoded

## Kubernetes
- Resource limits on all containers
- Readiness and liveness probes
- ConfigMaps for config, Secrets for sensitive data
- Horizontal Pod Autoscaler for production
- Network policies for security

## Infrastructure as Code
- Terraform for cloud resources
- Modules for reusable patterns
- State locking with remote backend
- Plan before apply
- Tag all resources for cost tracking

## Monitoring
- Structured logging (JSON format)
- Metrics with Prometheus labels
- Alerting on SLOs, not individual metrics
- Distributed tracing for microservices
- Dashboard as code (Grafana JSON models)
