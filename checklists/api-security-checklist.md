# API Security Checklist

## Authentication
- [ ] All endpoints require authentication (except public)
- [ ] JWT tokens have short expiry (15 min access)
- [ ] Refresh token rotation implemented
- [ ] API keys hashed in database
- [ ] Failed auth attempts rate-limited
- [ ] Account lockout after N failures

## Authorization
- [ ] Role-based access control (RBAC) implemented
- [ ] Resource ownership verified (IDOR prevention)
- [ ] Principle of least privilege
- [ ] Admin endpoints require elevated auth
- [ ] Cross-tenant data isolation

## Input Validation
- [ ] All inputs validated with schema (Zod/Pydantic)
- [ ] Content-Type verified
- [ ] File upload restrictions (type, size)
- [ ] SQL parameterized queries
- [ ] No string concatenation in queries

## Output
- [ ] No stack traces in error responses
- [ ] No internal IDs leaked
- [ ] Pagination limits enforced
- [ ] Response headers include security headers
- [ ] Rate limiting on responses

## Transport
- [ ] HTTPS only (HSTS header)
- [ ] TLS 1.2+ minimum
- [ ] Certificate pinning for mobile
- [ ] CORS configured restrictively
- [ ] No mixed content

## Monitoring
- [ ] Auth failures logged and alerted
- [ ] Anomalous access patterns detected
- [ ] API usage tracked per key
- [ ] Audit trail for sensitive operations
- [ ] Regular security scanning automated
