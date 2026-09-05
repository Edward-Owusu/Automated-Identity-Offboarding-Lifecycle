# Remediation Plan

## Remediation Objective

Reduce the likelihood of orphaned identities by replacing manual, fragmented offboarding steps with an automated, monitored lifecycle.

| Phase | Action | Owner | Priority | Success Measure |
|---|---|---|---|---|
| 1 | Inventory HR, IdP, directory, SaaS, and privileged-access dependencies | IAM + HR | High | 100% critical systems inventoried |
| 2 | Define authoritative termination event and data fields | HR + IAM | High | Approved event specification |
| 3 | Build HRIS-to-IdP event-driven workflow | IAM Engineering | High | Successful automated test cases |
| 4 | Implement session/token revocation | IAM + App Owners | High | Supported apps invalidate sessions/tokens |
| 5 | Build daily reconciliation and exception queue | IAM + GRC | High | 100% separations reconciled |
| 6 | Add connector monitoring and alerting | IAM Engineering | Medium | Critical failures alert within defined threshold |
| 7 | Establish change-management and privileged-access controls | IT Governance | Medium | Approved changes are fully traceable |
| 8 | Run control testing and tune workflow | Internal Audit / GRC | Medium | Testing meets target metrics |

## RACI-Style Accountability

- **HR:** owns authoritative employment-status events.
- **IAM:** owns identity lifecycle automation.
- **Application Owners:** validate downstream access removal.
- **Security/GRC:** owns monitoring, risk tracking, evidence, and compliance alignment.
- **Internal Audit:** independently tests control design and operating effectiveness.

## Exceptions

Exceptions should have:

1. A documented reason.
2. An accountable owner.
3. A risk assessment where required.
4. A target remediation date.
5. Evidence of closure.

## Metrics

Recommended dashboard metrics:

- % offboarded within 24 hours
- Median termination-to-disable time
- % sessions/tokens revoked within target
- Number of orphaned identities detected
- Number of critical connector failures
- Mean time to remediate offboarding exceptions
- Number of unauthorized changes to lifecycle automation
