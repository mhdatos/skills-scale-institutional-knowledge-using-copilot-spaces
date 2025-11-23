# OctoAcme — Release Roles & Responsibilities

## Purpose
Clarify who does what during the release lifecycle to avoid confusion and ensure all critical tasks are covered.

---

## Release Roles Matrix

| Role | Pre-Release | During Release | Post-Release | Incident/Rollback |
|------|-------------|----------------|--------------|-------------------|
| **Release Manager** | Coordinate release planning<br>Validate pre-release checklist<br>Schedule deployment window | Execute deployment<br>Monitor deployment health<br>Communicate status updates | Verify post-deploy checks<br>Publish release notes<br>Conduct release retrospective | Trigger rollback if needed<br>Coordinate incident response<br>Document root cause |
| **Developer** | Complete PRs and code reviews<br>Prepare smoke test scenarios<br>Document migration steps | Monitor logs and errors<br>Be available for troubleshooting | Validate feature behavior<br>Address urgent bugs | Investigate root cause<br>Implement hotfixes if needed |
| **Product Manager** | Approve release scope<br>Review release notes<br>Align stakeholders | Monitor key metrics<br>Communicate with stakeholders | Measure feature adoption<br>Gather initial feedback | Assess customer impact<br>Prioritize fixes |
| **QA/Testing** | Execute pre-release testing<br>Validate acceptance criteria<br>Prepare smoke tests | Run smoke tests in production<br>Verify critical flows | Monitor bug reports<br>Validate fixes | Re-test after rollback<br>Verify hotfix quality |
| **UX Designer** | Review final implementation<br>Validate design consistency | Monitor user feedback channels | Assess usability in production<br>Identify design improvements | Review UX impact of issues |
| **Security Lead** | Complete security review<br>Validate security controls<br>Approve release from security perspective | Monitor security alerts<br>Be available for security incidents | Review security metrics<br>Validate security posture | Lead security incident response<br>Assess security impact |
| **Customer Success/Support** | Prepare support documentation<br>Review FAQs and runbooks<br>Plan customer communication | Monitor support channels<br>Respond to early questions | Track customer feedback<br>Escalate issues<br>Measure satisfaction | Communicate with affected customers<br>Provide workarounds |
| **Data Analyst** | Baseline metrics before release<br>Prepare dashboards | Monitor release metrics<br>Alert on anomalies | Analyze release impact<br>Report on KPIs | Quantify incident impact<br>Support root cause analysis |
| **Project Manager** | Coordinate cross-team readiness<br>Manage risk register<br>Facilitate go/no-go decision | Facilitate communication<br>Track release progress<br>Escalate blockers | Update project status<br>Capture lessons learned | Coordinate resolution efforts<br>Update stakeholders |

---

## Key Milestones & Checkpoints

### 1 Week Before Release
- [ ] Release Manager validates pre-release checklist complete
- [ ] Security Lead confirms security review passed
- [ ] QA/Testing confirms all tests passing
- [ ] Product Manager approves release scope and notes
- [ ] Customer Success/Support confirms documentation ready

### Day of Release
- [ ] Release Manager conducts go/no-go meeting
- [ ] Developer confirms all code tagged and ready
- [ ] Data Analyst confirms baseline metrics captured
- [ ] Release Manager executes deployment
- [ ] QA/Testing runs smoke tests
- [ ] All roles monitor their respective areas

### Post-Release (24-48 hours)
- [ ] All roles review metrics and feedback
- [ ] Customer Success/Support reports early customer impact
- [ ] Release Manager publishes release summary
- [ ] Project Manager schedules retrospective

---

## Escalation & Decision Authority

| Decision Type | Primary Owner | Escalation Path |
|---------------|---------------|-----------------|
| Go/No-Go for Release | Release Manager | Project Manager → Product Lead |
| Rollback Decision | Release Manager + Developer | Project Manager (if business impact unclear) |
| Scope Changes During Release | Product Manager | Product Lead → Sponsor |
| Security Exception | Security Lead | Security Lead → CISO |
| Customer Communication | Customer Success/Support | Product Manager → Leadership |

---

## Communication Channels

- **Pre-Release**: Weekly release planning sync, release readiness checklist reviews
- **During Release**: Dedicated release channel (e.g., Slack #releases), status updates every 30 min
- **Post-Release**: Release summary email, metrics dashboard, retrospective meeting
- **Incident/Rollback**: Incident channel, page on-call if critical, post-mortem doc
