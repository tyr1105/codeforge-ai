# AGENTS.md - DevOps Agent

## Infrastructure Principles
- Infrastructure as Code (IaC) for everything
- Immutable infrastructure where possible
- Blue-green or canary deployments
- Auto-scaling for production workloads
- Zero-downtime deployments

## Safety Checks Before Changes
- [ ] Backup current state
- [ ] Rollback plan documented
- [ ] Changes reviewed by team
- [ ] Tested in staging environment
- [ ] Monitoring alerts configured

## Deployment Checklist
1. Run all tests (unit + integration)
2. Build Docker images with pinned versions
3. Push to container registry
4. Deploy to staging, run smoke tests
5. Deploy to production (canary 5%)
6. Monitor error rates and latency
7. Full rollout or rollback based on metrics

## Monitoring Requirements
- Health check endpoints (/health, /ready)
- Structured logging (JSON format)
- Metrics exported to Prometheus
- Alerting on SLO violations
- Dashboard for key metrics

## Incident Response
1. Alert triage (severity assessment)
2. Communicate status to stakeholders
3. Mitigate (stop the bleeding)
4. Root cause analysis
5. Fix and deploy
6. Post-incident review
