# Release Checklist

## Purpose
This checklist provides a comprehensive guide for Release Managers and teams to ensure all critical steps are completed before, during, and after a release to production. Use this in conjunction with the [Release & Deployment Guide](octoacme-release-and-deployment.md).

---

## Pre-Release Phase

### Code Readiness
- [ ] All planned features and fixes merged to release branch
- [ ] All acceptance criteria validated and signed off by Product Manager
- [ ] Code freeze communicated to development team
- [ ] No open critical or high-severity bugs in release scope
- [ ] All PRs have passed peer review and approval

### Testing & Quality
- [ ] All unit tests passing (100% of planned tests)
- [ ] Integration tests completed successfully
- [ ] End-to-end smoke tests executed and passing
- [ ] Security scans completed with no critical vulnerabilities
- [ ] Performance testing completed (if applicable)
- [ ] Accessibility testing completed (if applicable)

### Documentation
- [ ] Release notes drafted and reviewed
- [ ] API documentation updated (if applicable)
- [ ] User-facing documentation updated
- [ ] Known issues and limitations documented
- [ ] Migration or upgrade instructions prepared (if applicable)

### Infrastructure & Environment
- [ ] Staging environment deployed and verified
- [ ] Production capacity and scaling reviewed
- [ ] Database migrations tested in staging (if applicable)
- [ ] Configuration changes reviewed and approved
- [ ] Monitoring and alerting rules updated

### Risk Management
- [ ] Release risk assessment completed with Risk Champion
- [ ] Rollback plan documented and tested
- [ ] Incident response team identified and on-call schedule confirmed
- [ ] Dependencies on other teams or systems validated
- [ ] Business impact analysis completed for high-risk changes

### Communication
- [ ] Deployment window scheduled and communicated
- [ ] Stakeholders notified of release timeline
- [ ] Support team briefed on release changes
- [ ] Customer communication prepared (if user-facing changes)
- [ ] Internal announcement drafted

---

## Release Execution Phase

### Deployment Window
- [ ] Final go/no-go decision made with stakeholders
- [ ] Deployment window started and team notified
- [ ] Production backup or snapshot completed (if applicable)
- [ ] Feature flags configured (if using phased rollout)

### Deployment
- [ ] Deployment initiated (automated pipeline or manual process)
- [ ] Deployment progress monitored and logged
- [ ] Database migrations executed (if applicable)
- [ ] Configuration changes applied

### Verification
- [ ] Smoke tests executed in production
- [ ] Key user flows validated
- [ ] Monitoring dashboards reviewed for anomalies
- [ ] Error rates and performance metrics checked
- [ ] Feature flag functionality verified (if applicable)

### Communication During Release
- [ ] Deployment start communicated to stakeholders
- [ ] Any issues or delays communicated immediately
- [ ] Deployment completion confirmed and announced

---

## Post-Release Phase

### Validation
- [ ] Production health checks completed (15 min, 1 hour, 4 hours post-deploy)
- [ ] User-facing features validated by Product Manager
- [ ] Customer success or support reports reviewed
- [ ] Performance and error metrics within acceptable ranges
- [ ] Security monitoring reviewed for unusual activity

### Documentation
- [ ] Final release notes published
- [ ] Release tagged in version control
- [ ] Deployment completed date recorded
- [ ] Post-deployment report completed
- [ ] Known issues log updated

### Communication
- [ ] Release announcement sent to all stakeholders
- [ ] Support team notified of completion
- [ ] Customer communication sent (if applicable)
- [ ] Success metrics shared with leadership

### Learning & Improvement
- [ ] Release retrospective scheduled
- [ ] Deployment metrics collected (duration, downtime, issues)
- [ ] Process improvement suggestions documented
- [ ] Action items assigned with owners and due dates

---

## Rollback Procedures (If Needed)

### Trigger Conditions
Critical issues that warrant immediate rollback:
- Production outage or severe service degradation
- Data loss or data corruption
- Critical security vulnerability introduced
- Functionality breaks critical user workflows

### Rollback Steps
- [ ] Incident declared and stakeholders notified
- [ ] Rollback decision made by Release Manager and PM
- [ ] Rollback procedure initiated
- [ ] Previous version redeployed
- [ ] Database rollback executed (if applicable and safe)
- [ ] Production verification completed
- [ ] Stakeholders notified of rollback completion
- [ ] Post-incident review scheduled

---

## Release Types & Checklist Variations

### Patch Release (Hotfix)
- Expedited checklist may be used for critical fixes
- Minimum required: code review, smoke tests, rollback plan, stakeholder notification

### Minor Release (Incremental Features)
- Standard checklist applies
- Full testing and communication required

### Major Release (Breaking Changes)
- Extended checklist with additional stakeholder approvals
- Comprehensive migration testing and documentation
- Phased rollout or feature flags recommended
- Extended monitoring period (24-48 hours)

---

## Roles & Responsibilities

- **Release Manager**: Owns this checklist, coordinates all release activities, makes go/no-go decisions
- **Developers**: Complete code readiness items, support deployment and verification
- **QA/Test Engineers**: Execute testing phase, validate quality gates
- **Product Manager**: Sign off on feature completeness and business readiness
- **Risk Champion**: Conduct risk assessment, coordinate mitigation plans
- **Communications Lead**: Handle all stakeholder communications throughout release
- **Project Manager**: Ensure release aligns with project timeline and dependencies

---

## Notes
- Tailor this checklist based on release type and risk level
- Not all items may apply to every release—use judgment and document exceptions
- Archive completed checklists for audit and continuous improvement
- Review and update this template quarterly based on retrospective feedback
