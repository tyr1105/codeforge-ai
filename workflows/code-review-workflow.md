# Code Review Workflow

## Review Checklist

### Functionality
- [ ] Code does what the PR description says
- [ ] Edge cases are handled
- [ ] Error handling is appropriate
- [ ] No dead code or commented-out code

### Security
- [ ] Input validation is present
- [ ] No SQL injection / XSS vulnerabilities
- [ ] Authentication/authorization checks
- [ ] No sensitive data in logs or responses
- [ ] Dependencies are from trusted sources

### Performance
- [ ] No N+1 queries
- [ ] Appropriate data structures used
- [ ] Caching where beneficial
- [ ] No unnecessary re-renders (frontend)
- [ ] Database queries are optimized

### Maintainability
- [ ] Code is readable and self-documenting
- [ ] Naming conventions are followed
- [ ] Appropriate level of abstraction
- [ ] No duplicated logic
- [ ] Comments explain WHY, not WHAT

### Testing
- [ ] New code has tests
- [ ] Tests are meaningful (not just coverage)
- [ ] Edge cases tested
- [ ] Mocking is appropriate
- [ ] Tests are isolated and deterministic

## Review Tone
- Be constructive, not critical
- Ask questions, don't demand changes
- Suggest alternatives with reasoning
- Acknowledge good patterns
- Focus on code, not the author
