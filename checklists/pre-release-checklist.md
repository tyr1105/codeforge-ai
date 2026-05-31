# Pre-Release Checklist

## Code Quality
- [ ] All TypeScript types are correct (no 'any')
- [ ] ESLint passes with zero warnings
- [ ] Prettier formatting applied
- [ ] No console.log in production code
- [ ] Dead code removed
- [ ] TODO comments resolved or ticketed

## Testing
- [ ] Unit test coverage > 80%
- [ ] All critical paths have integration tests
- [ ] E2E tests pass for main user flows
- [ ] Performance tests pass (no regression > 10%)
- [ ] Cross-browser testing (Chrome, Firefox, Safari)
- [ ] Mobile responsive testing
- [ ] Accessibility audit (Lighthouse > 90)

## Security
- [ ] Dependencies audited (npm audit / pip audit)
- [ ] No secrets in code or config files
- [ ] Input validation on all user inputs
- [ ] CORS configured correctly
- [ ] CSP headers set appropriately
- [ ] Rate limiting configured
- [ ] HTTPS enforced

## Performance
- [ ] Bundle size checked (no unexpected growth)
- [ ] Images optimized (WebP, lazy loading)
- [ ] Database queries optimized
- [ ] Caching headers configured
- [ ] CDN configured for static assets
- [ ] Lighthouse score > 90 (Performance)

## Infrastructure
- [ ] Environment variables documented
- [ ] Docker image builds successfully
- [ ] Health check endpoint works
- [ ] Logging configured (structured JSON)
- [ ] Monitoring and alerting set up
- [ ] Backup and recovery tested

## Documentation
- [ ] README updated
- [ ] API documentation current
- [ ] CHANGELOG updated
- [ ] Migration guide written (if breaking changes)
- [ ] Environment setup guide current
