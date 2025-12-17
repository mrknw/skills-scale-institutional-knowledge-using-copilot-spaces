# Risk Escalation Protocol

## Purpose
This protocol provides clear guidance on when and how to escalate risks, ensuring that issues are addressed at the appropriate level with the right urgency. Use this in conjunction with the [Risk Management & Communication Guide](octoacme-risks-and-communication.md).

---

## Risk Severity Levels

### Critical (P0)
**Impact**: Threatens project delivery, major business impact, or critical security/compliance issue  
**Likelihood**: Any  
**Examples**:
- Key dependency blocked or unavailable
- Critical security vulnerability discovered in production
- Major technical decision preventing progress
- Resource loss threatening deliverable completion
- Regulatory or compliance deadline at risk

**Action Required**: Immediate escalation to sponsor level

---

### High (P1)
**Impact**: Significant delay risk (>1 week), affects major features, or medium security concern  
**Likelihood**: High or Medium  
**Examples**:
- Unplanned technical complexity requiring scope negotiation
- Key team member unavailable without coverage
- Third-party integration delayed affecting timeline
- Budget overrun projected
- Cross-team dependency creating critical path delay

**Action Required**: Escalate to Product Lead and PM within 24 hours

---

### Medium (P2)
**Impact**: Minor delay risk (<1 week), affects non-critical features, or quality concerns  
**Likelihood**: High or Medium  
**Examples**:
- Technical debt accumulating that may slow future work
- Testing coverage gaps identified
- Minor scope creep detected
- Communication gaps between teams
- Process inefficiencies slowing delivery

**Action Required**: Discuss at weekly sync, escalate if unresolved after 1 week

---

### Low (P3)
**Impact**: Minimal impact on timeline or quality  
**Likelihood**: Any  
**Examples**:
- Nice-to-have feature at risk
- Minor documentation gaps
- Optimization opportunities
- Future enhancement ideas

**Action Required**: Log in risk register, monitor, address as capacity allows

---

## Escalation Paths

### Level 1: Team Triage
**When**: All risks initially raised at this level  
**Who**: Risk Champion, Project Manager, immediate team  
**Timeline**: Within 24 hours of identification  
**Actions**:
- Document in risk register (ID, description, impact, likelihood, owner)
- Assess severity level using criteria above
- Develop initial mitigation plan
- Assign owner for tracking and mitigation
- Determine if escalation needed

**Communication**: Discussed in daily standup or immediate Slack/Teams message for P0/P1

---

### Level 2: Product & PM Escalation
**When**: P1 risks or P2 risks unresolved after 1 week  
**Who**: Product Lead, Program Manager, Risk Champion  
**Timeline**: Within 24 hours for P1, within 1 week for P2  
**Actions**:
- Present risk with impact analysis and mitigation options
- Escalate to dependent teams if cross-functional coordination needed
- Request resource reallocation or scope adjustments if needed
- Make decisions on risk acceptance vs. mitigation investment
- Set clear deadlines for resolution

**Communication**: Formal escalation email/doc with risk details, plus sync meeting if urgent

---

### Level 3: Sponsor & Leadership Escalation
**When**: P0 risks or P1 risks unresolved after Level 2 escalation  
**Who**: Executive Sponsor, Director/VP level, Product & PM Leads  
**Timeline**: Immediate for P0, within 48 hours for unresolved P1  
**Actions**:
- Present business impact and escalation history
- Recommend course of action with cost-benefit analysis
- Request executive decisions on scope, timeline, or resource changes
- Coordinate organizational-level response
- Set expectations for stakeholder communication

**Communication**: Executive briefing document, escalation meeting, followed by decision log and stakeholder announcement

---

## Escalation Process Flow

```
Risk Identified
    ↓
[Level 1: Team Triage]
- Document in risk register
- Assess severity (P0-P3)
- Develop mitigation plan
    ↓
P0? → YES → [Level 3: Immediate Sponsor Escalation]
    ↓ NO
P1? → YES → [Level 2: PM & Product Lead within 24h]
    ↓ NO
P2? → YES → Monitor at weekly sync
    ↓ NO
P3? → YES → Log and monitor
    ↓
Unresolved after 1 week? → YES → Escalate one level up
    ↓ NO
Continue monitoring and mitigation
```

---

## Escalation Communication Template

When escalating a risk, use this template to ensure clear, actionable communication:

### Subject Line
`[RISK ESCALATION - P{0-3}] {Brief Risk Description} - {Project Name}`

### Email/Document Body

**Risk ID**: {From risk register}  
**Severity**: P0 | P1 | P2 | P3  
**Project**: {Project name}  
**Identified Date**: {Date}  
**Escalation Date**: {Date}

**Risk Description**:  
{Clear, concise description of the risk}

**Business Impact**:  
- Timeline impact: {e.g., 2-week delay to release}
- Feature impact: {e.g., Feature X at risk}
- Customer impact: {e.g., Affects 50% of users}
- Financial impact: {e.g., $XX budget overrun}

**Current Status**:  
{What has been tried so far, why it's insufficient}

**Mitigation Options**:  
1. **Option A**: {Description, pros/cons, timeline, resources needed}
2. **Option B**: {Description, pros/cons, timeline, resources needed}
3. **Option C**: {Description, pros/cons, timeline, resources needed}

**Recommendation**:  
{Recommended course of action with rationale}

**Decision Needed By**: {Date/time}  
**Contact**: {Risk Champion or PM name, contact info}  
**Next Steps**: {What happens after decision}

---

## Special Escalation Scenarios

### Security Incidents
- **Trigger**: Any security vulnerability or breach detected
- **Path**: Follow security incident runbook → Notify Security on-call immediately → Parallel escalation to PM and Product Lead
- **Timeline**: Immediate (within 15 minutes)
- **Authority**: Security team has authority to make containment decisions

### Regulatory/Compliance Issues
- **Trigger**: Risk of missing compliance deadline or regulatory requirement
- **Path**: PM → Product Lead → Legal/Compliance → Sponsor
- **Timeline**: Immediate for P0, within 24 hours for P1
- **Authority**: Legal/Compliance team must review before decisions made

### Customer-Impacting Production Issues
- **Trigger**: Production issue affecting customers, even if not originally a "risk"
- **Path**: Incident response team → On-call → PM → Communications Lead → Stakeholders
- **Timeline**: Immediate incident declaration
- **Authority**: Incident Commander has authority to make resolution decisions

### Budget Overruns
- **Trigger**: Projected costs exceed approved budget by >10%
- **Path**: PM → Finance → Sponsor → Leadership
- **Timeline**: Within 48 hours of identification
- **Authority**: Finance approval required for budget increases

---

## Risk Champion Responsibilities

The Risk Champion ensures this protocol is followed consistently:

- **Daily**: Review risk register for new or updated risks
- **Daily Standups**: Surface new risks and mitigation updates
- **Weekly Syncs**: Present risk status summary, flag items needing escalation
- **Monthly**: Review risk trends and protocol effectiveness with PM
- **Ongoing**: Coach team on risk identification and escalation criteria

---

## De-escalation

When risks are mitigated or resolved:
- Update risk register with resolution date and final status
- Notify all escalation participants of resolution
- Document lessons learned for retrospective
- Update mitigation strategies for similar future risks

---

## Continuous Improvement

This protocol should be reviewed and updated:
- After major incidents or escalations (retrospective)
- Quarterly as part of process improvement reviews
- When organizational structure or roles change
- Based on feedback from Risk Champions and Project Managers

Track protocol effectiveness metrics:
- Average time from risk identification to escalation
- % of risks escalated appropriately vs. under/over-escalated
- % of escalated risks successfully mitigated
- Team feedback on protocol clarity and usefulness

---

## Roles Referenced

- **Risk Champion**: Owns day-to-day risk monitoring and escalation initiation
- **Project Manager**: Coordinates escalation process and stakeholder communication
- **Product Lead**: Decision authority at Level 2, escalates to sponsor at Level 3
- **Sponsor/Leadership**: Final decision authority on critical risks
- **Communications Lead**: Manages stakeholder communication during escalations
- **Release Manager**: Consulted for release-related risks and go/no-go decisions

---

## Related Documents

- [Risk Management & Communication](octoacme-risks-and-communication.md) - Overall risk management approach
- [Roles & Personas](octoacme-roles-and-personas.md) - Detailed role definitions including Risk Champion
- [Project Management Overview](octoacme-project-management-overview.md) - Context on project governance
