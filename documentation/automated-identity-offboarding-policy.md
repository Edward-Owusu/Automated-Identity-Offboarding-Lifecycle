# Corporate Policy — Automated Identity Offboarding Lifecycle

**Document Reference:** PL-SEC-007  
**Version:** 1.0

## 1.0 Purpose

This policy establishes requirements for timely and controlled revocation of information-system access and related permissions when personnel separate from the organization.

## 2.0 Scope

This policy applies to employees, contractors, third-party personnel, temporary personnel, and other users whose access is managed through corporate directory, identity-provider, network, or cloud-application infrastructure.

## 3.0 Mandatory Controls

### 3.1 Automated Offboarding

Where technically feasible, approved HR separation events must trigger an automated identity lifecycle workflow.

### 3.2 24-Hour Account Revocation Standard

Directory accounts, SSO access, and applicable administrative access must be disabled or revoked within **24 hours** of the official termination timestamp, subject to documented organizational procedures and emergency workflows.

### 3.3 Active Session and Token Invalidation

The offboarding workflow must terminate active sessions and revoke supported OAuth/API tokens. The portfolio control target is **within 60 minutes** of offboarding initiation.

### 3.4 Reconciliation

HR separation records must be reconciled against identity-provider status. Exceptions must be investigated, assigned, and tracked to closure.

### 3.5 Integration Security

HRIS-to-IdP connectors and service accounts must use least privilege, secure authentication, logging, change management, and monitoring.

### 3.6 Evidence Retention

Offboarding logs, reconciliation reports, exceptions, and relevant change records must be retained according to the organization's records-retention requirements.

## 4.0 Exceptions

Any exception to the established SLA must be documented and approved according to organizational risk and governance procedures.

## 5.0 Enforcement

Failure to follow this policy may result in audit escalation, corrective action, access-control review, or disciplinary action consistent with organizational policy.

## 6.0 Review

This policy should be reviewed periodically and whenever major changes occur to HR systems, identity infrastructure, regulatory requirements, or the organization's access-control model.

> This document is a portfolio template and should be reviewed by qualified legal, privacy, security, and compliance stakeholders before operational use.
