# Automated Identity Offboarding Lifecycle — GRC / IT Audit Project

A portfolio-ready GRC / IT Audit case study focused on the risk of delayed or incomplete access revocation when employees, contractors, vendors, or temporary personnel leave an organization.

## Project Lifecycle

**Risk Identification → Risk Assessment → Framework Mapping → Control Design → Audit Testing → Evidence → Metrics → Remediation → Policy**

## Executive Summary

The project addresses **orphaned identities**: accounts, active sessions, tokens, or downstream application access that remain available after a person's employment or engagement ends.

The modeled risk is:

- **Risk ID:** RSK-004
- **Inherent Likelihood:** 4/5
- **Inherent Impact:** 5/5
- **Inherent Risk Score:** 20/25
- **Residual Likelihood:** 1/5
- **Residual Impact:** 5/5
- **Residual Risk Score:** 5/25
- **Modeled Risk Reduction:** 75%

### Core Control Strategy

1. Connect the HR system to the identity provider so termination events can trigger automated deprovisioning.
2. Disable directory/SSO access within the defined **24-hour offboarding SLA**.
3. Revoke active sessions and OAuth/API tokens as part of the offboarding workflow, with a **60-minute target** for session/token invalidation.
4. Run daily reconciliation between HR separation records and identity-provider status.
5. Monitor integration/API errors and investigate exceptions.
6. Maintain evidence suitable for internal audit and compliance testing.

## Framework Alignment

The project uses control-alignment examples from:

- **ISO/IEC 27001:2022** — termination/change-of-employment access controls, access rights, and authentication information management.
- **SOC 2 Trust Services Criteria** — logical access, user registration/removal, and access authorization concepts.
- **HIPAA Security Rule** — termination procedures under 45 CFR §164.308(a)(3)(ii)(C), where applicable.
- **GDPR** — security and confidentiality principles, including Articles 5(1)(f) and 32, where applicable.
- **PCI DSS v4.0** — user/account lifecycle and access-control requirements where cardholder-data environments are in scope.

> Framework references are presented as portfolio control-alignment examples, not legal advice or a claim of certification.

## Audit Testing

| Control | Frequency | Target |
|---|---|---|
| AUD-005.1 — HRIS/IdP reconciliation | Daily | 100% of separated identities offboarded within 24 hours |
| AUD-005.2 — Emergency/off-cycle access removal | Quarterly | 0 active corporate sessions/tokens remaining beyond the defined SLA |
| AUD-005.3 — HRIS API connector health | Semi-Annually | 0 critical synchronization errors unresolved for more than 4 hours |

## Evidence Examples

- HR termination event logs
- Identity-provider account-status history
- Reconciliation and exception reports
- OAuth/session revocation logs
- Downstream application access verification
- Ticket timestamps
- API error logs
- Integration configuration/change records
- IAM administrative change tickets

## Repository Structure

```text
Automated-Identity-Offboarding-Lifecycle-GRC-Project/
├── README.md
├── .gitignore
├── data/
│   └── Automated_Identity_Offboarding_Lifecycle_GRC_Project.xlsx
└── documentation/
    ├── risk-assessment.md
    ├── control-mapping.md
    ├── audit-testing.md
    ├── remediation-plan.md
    └── automated-identity-offboarding-policy.md
```

## Skills Demonstrated

- GRC
- IT Audit
- IT Risk Assessment
- Identity & Access Management (IAM)
- Access Lifecycle Management
- Control Design
- Control Testing
- Evidence Collection
- Compliance Mapping
- Security Metrics / KPIs
- Remediation Planning
- Security Policy Development

## Disclaimer

This is a sanitized educational portfolio case study. It does not represent confidential organizational information, a real audit opinion, or a certification of compliance.
