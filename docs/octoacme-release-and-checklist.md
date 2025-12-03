```markdown
# OctoAcme — Release Checklist

Purpose: Standardize pre-release and post-release activities to reduce deployment risk and speed recovery if needed.

Pre-release (validate before scheduling)
- [ ] All linked issues' acceptance criteria met
- [ ] All PRs merged and CI green (unit, integration, e2e where applicable)
- [ ] Security scanning completed and any critical findings addressed
- [ ] Release notes drafted and reviewed
- [ ] Rollback/mitigation plan documented and owners assigned
- [ ] Stakeholders and support teams notified of planned release window

Staging verification
- [ ] Deploy to staging and run smoke tests for critical flows
- [ ] Run automated regression tests (as available)
- [ ] Validate observability: logs, metrics, and dashboards show healthy signals

Production deployment
- [ ] Confirm deployment automation is configured and tested
- [ ] Execute deployment (canary/blue-green preferred where available)
- [ ] Run post-deploy smoke checks
- [ ] Monitor alerts and key metrics for the defined observation window

Post-release
- [ ] Announce release to stakeholders and support channels
- [ ] Open follow-up items for any known issues
- [ ] Run a short post-release check-in and capture action items
- [ ] If an incident occurred, follow the Incident Playbook and schedule a blameless retrospective

Escalation & rollback
- [ ] If critical issues detected, follow rollback steps and notify affected parties
- [ ] Update the risk register and retrospective notes with learnings

Templates referenced
- Release notes template (docs/octoacme-release-and-deployment.md)
- Incident checklist (docs/octoacme-release-and-deployment.md)
```