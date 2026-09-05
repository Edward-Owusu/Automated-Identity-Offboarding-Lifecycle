# Control Mapping

## Mapping Overview

The project demonstrates how one operational risk can be translated into control objectives across multiple frameworks.

| Control Objective | ISO/IEC 27001:2022 | SOC 2 | HIPAA | GDPR | PCI DSS v4.0 |
|---|---|---|---|---|---|
| Terminate access when employment/engagement ends | A.6.5 — Responsibilities after termination/change of employment | CC6 logical access / user removal concepts | 45 CFR §164.308(a)(3)(ii)(C) | Art. 32 security of processing | Access-control/user lifecycle requirements where applicable |
| Restrict and manage access rights | A.5.15, A.5.18 | CC6 | 45 CFR §164.312(a) concepts | Art. 32 | Req. 7/8 access and identification controls |
| Monitor access and exceptions | A.8.15 logging; A.8.16 monitoring | CC7 monitoring | Audit controls / activity review concepts | Art. 32 | Logging and monitoring requirements where applicable |
| Protect authentication/session information | A.5.17 authentication information | CC6 | 45 CFR §164.312(d) authentication | Art. 32 | Req. 8 authentication/access controls |

> Exact applicability depends on the organization's scope, implementation, system architecture, and adopted control set. Framework mapping should be validated against the current authoritative standard and the organization's compliance program.

## Control Design

### CTRL-004.1 — Automated HRIS-to-IdP Deprovisioning

**Objective:** Ensure separation events trigger timely suspension/removal of identity access.

**Design:** Event-driven integration from HRIS to IdP/directory services with monitored success/failure states.

**Evidence:** HR event logs, IdP audit logs, connector logs, exception reports.

### CTRL-004.2 — Active Session and Token Invalidation

**Objective:** Prevent a separated user from retaining access through an already-authenticated browser or API session.

**Design:** Offboarding workflow invokes session termination and OAuth/API token revocation across supported platforms.

**Evidence:** Session revocation logs, token revocation records, downstream application verification.

### CTRL-004.3 — Reconciliation and Exception Management

**Objective:** Detect identities that did not transition to the expected disabled state.

**Design:** Daily comparison of HR separation records against IdP/account state with automated alerts and owner assignment.

**Evidence:** Reconciliation reports, exception tickets, remediation timestamps.

### CTRL-004.4 — Integration Governance

**Objective:** Prevent unauthorized or unnoticed changes to the offboarding automation.

**Design:** Restrict connector privileges, use change management, monitor API errors, and review configuration periodically.

**Evidence:** API logs, configuration snapshots, privileged-access logs, change tickets.
