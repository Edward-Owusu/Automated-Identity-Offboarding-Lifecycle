# Risk Assessment — RSK-004

## Risk Statement

Delayed or incomplete revocation of employee system credentials after separation can create orphaned accounts that remain exploitable for unauthorized access, data exfiltration, or insider-threat activity.

## Risk Scoring

| Factor | Likelihood | Impact | Score |
|---|---:|---:|---:|
| Inherent | 4/5 | 5/5 | **20/25** |
| Residual | 1/5 | 5/5 | **5/25** |

**Modeled reduction: 75%.**

The impact remains high because a compromised identity can still provide access to sensitive systems; the control strategy primarily reduces the likelihood through faster, automated deprovisioning and monitoring.

## Key Risk Drivers

- Manual HR-to-IT notification delays
- Multiple identity stores and downstream SaaS applications
- Active browser sessions and refresh tokens
- Emergency or off-cycle terminations
- Integration/API failures
- Shadow or locally managed accounts
- Incomplete reconciliation between HR records and IdP state

## Risk Treatment

**Treatment:** Mitigate.

The proposed approach combines preventive, detective, and corrective controls:

- Preventive: event-driven automated account suspension
- Preventive: session/token invalidation
- Detective: daily HRIS-to-IdP reconciliation
- Detective: exception alerting
- Corrective: escalation and remediation of failed offboarding events

## Risk Acceptance Considerations

Any exception to the 24-hour SLA should be documented, risk-assessed, assigned to an owner, and tracked to closure. Emergency terminations should follow an accelerated workflow where technically feasible.

## Assumptions

The modeled scores are portfolio assumptions used to demonstrate GRC methodology. A real organization should calibrate likelihood and impact using its approved risk methodology, asset criticality, threat intelligence, and historical incident data.
