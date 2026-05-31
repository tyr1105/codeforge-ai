# Security Hardening Cursor Rules

## Input Validation
- Validate ALL inputs (server-side, not just client)
- Whitelist allowed values, don't blacklist
- Sanitize HTML with DOMPurify or equivalent
- Validate file uploads: type, size, content
- Rate limit all public endpoints

## Authentication & Authorization
- Never store plaintext passwords (bcrypt/argon2)
- JWT with short expiry + refresh tokens
- CSRF tokens for cookie-based auth
- Principle of least privilege
- Audit log for sensitive operations

## Data Protection
- Encrypt at rest (AES-256) and in transit (TLS 1.3)
- PII fields encrypted separately
- Database credentials rotated regularly
- Secrets in vault (not env vars in code)
- Data retention policies enforced

## Dependency Security
- Pin dependency versions
- Automated vulnerability scanning (Dependabot/Snyk)
- Review changelogs before upgrading
- Minimal dependency footprint
- Lock file committed to VCS

## Common Vulnerabilities
- SQL injection: use parameterized queries
- XSS: context-aware output encoding
- CSRF: SameSite cookies + tokens
- SSRF: allowlist internal URLs
- IDOR: verify ownership before access
