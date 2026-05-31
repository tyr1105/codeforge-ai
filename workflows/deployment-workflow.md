# Deployment Workflow

## Pre-Deployment Checklist
- [ ] All tests pass in CI
- [ ] No security vulnerabilities in dependencies
- [ ] Database migrations tested
- [ ] Environment variables documented
- [ ] Rollback plan documented
- [ ] Monitoring alerts configured
- [ ] Feature flags ready (if applicable)

## Staging Deployment
```bash
# Deploy to staging
npm run deploy:staging

# Run smoke tests
npm run test:smoke -- --env=staging

# Check health endpoints
curl https://staging.example.com/health

# Verify database migration
npm run db:migrate:staging
```

## Production Deployment
```bash
# Create release tag
git tag -a v1.2.0 -m "Release v1.2.0"
git push origin v1.2.0

# Deploy with canary (5% traffic)
npm run deploy:production -- --canary

# Monitor for 15 minutes
# Check error rates, latency, core metrics

# Full rollout
npm run deploy:production -- --rollout

# Post-deploy verification
npm run test:smoke -- --env=production
```

## Rollback Plan
```bash
# Immediate rollback
npm run deploy:production -- --rollback

# Or revert to specific version
npm run deploy:production -- --version=v1.1.9

# Verify rollback
curl https://example.com/health
```

## Post-Deployment
- [ ] Verify all health checks pass
- [ ] Check error monitoring dashboard
- [ ] Verify key user flows manually
- [ ] Update release notes
- [ ] Notify team of deployment
