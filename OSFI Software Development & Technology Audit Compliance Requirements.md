# OSFI Software Development & Technology Audit Compliance Requirements

## 1. Purpose

This page establishes the minimum technology, software-development, change-management, security, operational-resilience and audit-evidence expectations relevant to software systems developed or maintained within the Bank.

The objective is to ensure that software-development activities are:

- governed and controlled;
- secure by design;
- appropriately tested and approved;
- traceable from requirement through production deployment;
- protected by segregation of duties;
- supported by sufficient audit evidence;
- resilient to operational and cyber disruption; and
- aligned with applicable OSFI regulatory expectations.

The primary regulatory source is **OSFI Guideline B-13: Technology and Cyber Risk Management**. Supporting requirements arise from:

- Guideline B-13 — Technology and Cyber Risk Management
- Guideline E-21 — Operational Risk Management and Resilience
- Guideline B-10 — Third-Party Risk Management
- Guideline E-13 — Regulatory Compliance Management
- Technology and Cyber Security Incident Reporting Advisory
- OSFI Corporate Governance Guideline

Guideline B-13 has been effective since **January 1, 2024**. Guideline B-10 became effective **May 1, 2024**. Full adherence to Guideline E-21 was required by **September 1, 2026**.

---

# 2. Core Software Development Requirements

## 2.1 Technology Governance and Accountability

### OSFI requirement

**B-13 §1.1 — Accountability and organizational structure**

OSFI requires clear responsibility for technology and cyber risk management, supported by defined roles, adequate resources, appropriate expertise and training.

**B-13 §1.3 — Technology and cyber risk management framework**

The technology and cyber risk management framework must include:

- clear accountability;
- risk appetite and risk measures;
- technology/cyber policies and standards;
- processes for identifying, assessing, managing, monitoring and reporting risks;
- exception-management processes; and
- reporting to senior management.

(OSFI, 2022, §§1.1–1.3)

### Development implications

Every application or technology service should have identifiable ownership for:

- business ownership;
- application ownership;
- technical ownership;
- data ownership where applicable;
- security responsibility;
- production support;
- change approval; and
- risk acceptance.

Control ownership must not be ambiguous.

### Expected audit evidence

Examples include:

- application ownership records;
- RACI matrices;
- architecture ownership;
- risk registers;
- approved technology standards;
- documented control exceptions;
- risk acceptances;
- escalation records; and
- governance meeting decisions.

---

# 2.2 Architecture and Secure-by-Design

### OSFI requirement

**B-13 §2.1.2 — Architecture is comprehensive**

OSFI requires systems and infrastructure to be designed using a risk-based approach to achieve:

- availability;
- scalability;
- security; and
- resilience.

The guideline specifically incorporates **Secure-by-Design** and **Resilience-by-Design** principles.

(OSFI, 2022, §2.1.2)

### Development implications

Material systems should have documented architecture showing, as applicable:

- application components;
- infrastructure;
- APIs and interfaces;
- upstream and downstream dependencies;
- data flows;
- authentication/authorization boundaries;
- external integrations;
- failure points;
- resilience design; and
- security controls.

Security should be a design input rather than a control added only before production.

### Expected audit evidence

- architecture diagrams;
- solution design documents;
- architecture-review approvals;
- threat models;
- data-flow diagrams;
- dependency diagrams;
- non-functional requirements;
- security assessments; and
- design decisions/ADRs.

---

# 2.3 Technology Asset Inventory

### OSFI requirement

**B-13 §2.2**

OSFI requires a current and comprehensive inventory of technology assets throughout their lifecycle.

Critical technology assets should be categorized, and important interdependencies should be documented.

Asset configurations should also be recorded and deviations from approved baseline configurations identified and remediated.

(OSFI, 2022, §§2.2.2–2.2.3)

### Development implications

Applications should not exist as unmanaged technology.

Relevant inventories should identify, as applicable:

- application;
- repository;
- runtime environment;
- infrastructure;
- databases;
- interfaces;
- APIs;
- libraries;
- third-party components;
- service accounts;
- operating systems;
- critical dependencies; and
- application criticality.

### Expected audit evidence

- CMDB/application inventory;
- repository inventory;
- dependency records;
- configuration baseline;
- application criticality classification;
- ownership records;
- infrastructure inventory; and
- configuration-drift reports.

---

# 2.4 Technology Currency and Unsupported Technology

### OSFI requirement

**B-13 §2.2.5 — Technology currency is continuously assessed and managed**

Software and hardware currency must be continuously monitored.

Risks arising from unsupported, outdated or unpatched technology must be actively managed, with replacement or upgrades planned before support ends.

(OSFI, 2022, §2.2.5)

### Development implications

Teams should monitor:

- runtime versions;
- operating-system support dates;
- database versions;
- frameworks;
- libraries;
- packages;
- middleware; and
- other material technology dependencies.

### Expected audit evidence

- end-of-life inventories;
- dependency reports;
- remediation plans;
- upgrade roadmaps;
- vulnerability records;
- approved exceptions; and
- risk acceptances.

---

# 2.5 Technology Project Governance

### OSFI requirement

**B-13 §2.3.1**

Technology projects should operate under an enterprise-wide project-management framework.

OSFI also expects project performance and associated risks to be measured, monitored and periodically reported.

(OSFI, 2022, §2.3.1)

### Development implications

Material technology projects should maintain clear records of:

- objectives;
- scope;
- requirements;
- ownership;
- risks;
- dependencies;
- milestones;
- decisions;
- testing;
- implementation; and
- closure.

### Expected audit evidence

- project documentation;
- Jira/ADO records;
- requirements;
- risk/issues logs;
- design decisions;
- approvals;
- milestone reporting; and
- implementation records.

---

# 2.6 System Development Life Cycle — SDLC

### OSFI requirement

**B-13 Principle 7 and §2.4.1**

OSFI requires an SDLC framework governing the:

- secure development;
- acquisition; and
- maintenance

of technology systems.

Processes and controls must exist throughout the lifecycle to achieve the required security and functionality.

(OSFI, 2022, §§2.4–2.4.1)

### Development implications

The SDLC should establish identifiable control points covering:

**Requirement → Design → Development → Review → Testing → Approval → Deployment → Verification → Maintenance**

The requirement applies regardless of whether the Bank uses:

- Agile;
- Waterfall;
- DevOps;
- DevSecOps; or
- another development methodology.

---

# 2.7 Security Controls Throughout the SDLC

### OSFI requirement

**B-13 §2.4.2 — Security requirements are embedded throughout the SDLC**

OSFI requires control gates so that security requirements are incorporated in each phase of the lifecycle.

This expectation explicitly continues to apply in Agile environments.

(OSFI, 2022, §2.4.2)

### Development implications

Security consideration should not be postponed until production readiness.

Depending on system risk, controls may include:

- threat modelling;
- security requirements;
- authentication design;
- authorization design;
- encryption requirements;
- secrets management;
- dependency scanning;
- SAST;
- DAST;
- vulnerability scanning;
- penetration testing; and
- security approval.

### Expected audit evidence

- security requirements;
- threat assessments;
- security review records;
- vulnerability reports;
- remediation tickets;
- security-control approvals; and
- documented exceptions.

---

# 2.8 Secure Coding and Third-Party/Open-Source Code

### OSFI requirement

**B-13 §2.4.5 — Coding principles provide for secure and stable code**

OSFI requires defined coding principles and practices covering areas including:

- secure coding;
- third-party code;
- open-source code;
- code repositories; and
- development tools.

(OSFI, 2022, §2.4.5)

### Development implications

Development standards should address:

- secure coding;
- peer review;
- source control;
- branch protection;
- dependency management;
- secrets;
- third-party libraries;
- open-source packages;
- vulnerable components; and
- approved development tooling.

### Expected audit evidence

- coding standards;
- pull requests;
- peer-review history;
- dependency scans;
- repository permissions;
- branch-protection configuration;
- security scans;
- package inventories; and
- exception records.

---

# 2.9 Application Security Testing

### OSFI requirement

**B-13 §3.2.9**

Where feasible, static and/or dynamic scanning and testing should be used so that new applications and changes to existing applications are assessed for vulnerabilities **before production release**.

(OSFI, 2022, §3.2.9)

### Development implications

The CI/CD process should incorporate security testing appropriate to the application's risk.

For example:

- SAST;
- DAST;
- software composition analysis;
- dependency vulnerability scanning;
- container scanning;
- infrastructure-as-code scanning; and
- penetration testing where applicable.

### Expected audit evidence

- pipeline execution records;
- scan results;
- vulnerability tickets;
- remediation evidence;
- accepted-risk records; and
- production-release gates.

---

# 2.10 Change and Release Management

### OSFI requirement

**B-13 §2.5.1**

Production changes must be:

> “documented, assessed, tested, approved, implemented and verified”

in a controlled manner.

Emergency changes must also be subject to defined controls and safeguards.

(OSFI, 2022, §2.5.1)

### Development implications

A production release should therefore have traceable evidence of:

1. requested change;
2. business/technical requirement;
3. impact or risk assessment;
4. implementation;
5. code review;
6. testing;
7. approval;
8. deployment;
9. production verification; and
10. rollback or remediation approach where applicable.

### Expected audit evidence

- change ticket;
- linked requirement;
- source-control commit;
- pull request;
- code-review approval;
- test evidence;
- release approval;
- pipeline/deployment record;
- deployment timestamp;
- production verification; and
- emergency-change approval where applicable.

---

# 2.11 Segregation of Duties

### OSFI requirement

**B-13 §2.5.2**

OSFI identifies segregation of duties as a key control against unauthorized changes.

The same individual should not have unrestricted ability to:

- develop;
- authorize;
- execute; and
- move releases between production and non-production environments.

(OSFI, 2022, §2.5.2)

### Development implications

A developer should not normally be able to unilaterally write a production change, approve it and deploy it without an independent control.

CI/CD automation can provide segregation if approval and access controls are appropriately designed.

### Expected audit evidence

- repository permission model;
- production-access lists;
- CI/CD permissions;
- protected branches;
- required reviewers;
- release approvers;
- privileged-access records; and
- periodic access attestations.

---

# 2.12 End-to-End Change Traceability

### OSFI requirement

**B-13 §2.5.3 — Changes to technology assets are traceable**

OSFI requires controls protecting the **traceability and integrity of the change record and the asset being changed** throughout the change-management lifecycle.

(OSFI, 2022, §2.5.3)

### Development implications

Ideally, an auditor should be able to take a production release and trace it backward:

**Production deployment  
→ release/build  
→ commit  
→ pull request  
→ developer  
→ review/approval  
→ change ticket  
→ business requirement  
→ testing  
→ risk/security assessment**

and trace a requirement forward to the production implementation.

This is one of the most important controls for an audit-ready development process.

---

# 2.13 Testing

### OSFI requirement

Testing appears throughout B-13.

Most importantly:

- SDLC controls must ensure systems perform as expected — §2.4;
- production changes must be tested — §2.5.1;
- patches must be tested before production deployment — §2.6.1;
- vulnerabilities must be assessed — §3.1.3;
- applications should undergo vulnerability testing before release — §3.2.9.


### Development implications

Testing should be proportionate to risk and could include:

- unit testing;
- integration testing;
- system testing;
- regression testing;
- user-acceptance testing;
- security testing;
- performance testing;
- reconciliation/data testing; and
- post-deployment verification.

Testing must produce sufficient evidence to demonstrate what was tested and the outcome.

---

# 2.14 Vulnerability and Patch Management

### OSFI requirement

**B-13 §3.1.3**

Regular vulnerability assessments must be performed and vulnerabilities assessed according to risk.

**B-13 §3.2.6**

Security vulnerabilities must be remediated on a risk basis, including vendor software and internally developed applications.

Patch status, remediation backlog and exceptions should be monitored and reported.

(OSFI, 2022, §§3.1.3, 3.2.6)

### Expected audit evidence

- vulnerability scan;
- severity classification;
- remediation SLA;
- remediation ticket;
- patch records;
- overdue-vulnerability report;
- exception approval;
- compensating control; and
- management reporting.

---

# 2.15 Identity and Access Management

### OSFI requirement

**B-13 §3.2.7**

OSFI expects risk-based identity and access controls, including MFA and privileged-access management.

Relevant controls include:

- least privilege;
- access attestation;
- privileged-account protection;
- account-activity logging;
- service-account management; and
- monitoring for unauthorized use.

(OSFI, 2022, §3.2.7)

### Development implications

This requirement applies not only to end-user applications but also to development infrastructure such as:

- Git repositories;
- CI/CD;
- databases;
- cloud consoles;
- production servers;
- service accounts;
- secrets-management systems; and
- administrative interfaces.

---

# 2.16 Security Logging

### OSFI requirement

**B-13 §3.3.1**

OSFI expects continuous security logging and centralized capabilities to aggregate and access security-event logs.

Minimum log-retention periods must also be established.

(OSFI, 2022, §3.3.1)

### Important note

B-13 requires the Bank to establish minimum retention periods but does **not** prescribe one universal retention duration for every application.

Therefore, a specific retention period should not be represented as an OSFI requirement unless supported by another applicable regulatory requirement or Bank policy.

---

# 2.17 Incident and Problem Management

### OSFI requirement

**B-13 §2.7**

Technology incidents must be detected, logged, managed, resolved, monitored and reported.

Processes should include:

- incident classification;
- escalation;
- response;
- recovery;
- communications;
- testing of incident procedures;
- root-cause investigation; and
- lessons learned.

Post-incident findings should feed back into controls, including change and release management.

(OSFI, 2022, §§2.7.1–2.7.3)

### Expected audit evidence

- incident record;
- severity classification;
- timeline;
- escalation;
- incident communications;
- remediation;
- RCA;
- corrective actions;
- lessons learned; and
- evidence of control improvements.

---

# 2.18 OSFI Technology/Cyber Incident Notification

A separate regulatory reporting requirement applies to reportable technology and cyber incidents.

OSFI requires a qualifying technology or cyber incident to be reported to OSFI:

> **within 24 hours, or sooner if possible.**

Regular updates are expected as additional information becomes available.

(OSFI, 2021)

Development and application-support teams therefore need established escalation mechanisms so that a potentially reportable incident reaches the appropriate Bank incident-management/regulatory-reporting function without delay.

---

# 2.19 Disaster Recovery, Backup and Resilience

### OSFI requirement

**B-13 §2.9**

OSFI requires an Enterprise Disaster Recovery Program covering:

- responsibility for technology recovery;
- key dependencies;
- recovery procedures;
- data backup;
- recovery testing; and
- severe-but-plausible scenario testing.

Critical third-party and upstream/downstream dependencies should be included in recovery testing.

(OSFI, 2022, §§2.9.1–2.9.3)

### Expected audit evidence

- application recovery classification;
- RTO/RPO where applicable;
- backup records;
- restoration tests;
- DR plans;
- DR test results;
- dependency mapping;
- failover tests;
- remediation items; and
- evidence that identified deficiencies were addressed.

---

# 3. E-21 Operational Risk and Software Change

## 3.1 Significant Technology Changes

### OSFI requirement

**E-21 §4.4 — Change management**

Significant changes include the implementation of new technology systems and significant modifications to business processes.

OSFI expects significant changes to include:

- operational-risk assessment and monitoring;
- robust project management throughout the lifecycle;
- consideration of changes to risk appetite;
- contingency planning;
- testing before introduction; and
- post-implementation effectiveness metrics.

(OSFI, 2024, §4.4)

### Development implications

Large migrations, new platforms, major architecture changes and high-impact releases require more than a normal development ticket.

Evidence should demonstrate that operational risk arising from the transformation itself was evaluated.

---

# 3.2 Data Risk Management

### OSFI requirement

**E-21 §4.7**

Effective data-risk management should ensure that data is:

- accurate;
- complete;
- timely;
- secure; and
- protected.

The data-risk-management program should address:

- governance;
- data architecture;
- data lineage;
- classification;
- protection;
- integrity;
- confidentiality;
- availability;
- incidents; and
- relevant training.

(OSFI, 2024, §4.7)

### Development implications

For applications performing material transformations or calculations, documentation should allow important data to be traced through:

**Source → ingestion → transformation → calculation → storage → output**

Controls should exist for data quality and integrity at appropriate stages.

### Expected audit evidence

- source-to-target mappings;
- data lineage;
- transformation rules;
- reconciliation controls;
- data-quality checks;
- exception reporting;
- data classification; and
- ownership documentation.

---

# 4. Third-Party Software, Vendors and Cloud — B-10

## 4.1 Accountability Cannot Be Outsourced

OSFI explicitly states that a FRFI retains accountability for activities and services outsourced to third parties.

This includes data exchanged with or accessible by third parties.

(OSFI, 2023)

Using:

- SaaS;
- cloud infrastructure;
- external APIs;
- managed services;
- contractors;
- software vendors; or
- other technology providers

does not transfer the Bank's regulatory accountability to the vendor.

---

# 4.2 Third-Party Due Diligence

### OSFI requirement

**B-10 §2.2.2**

Due diligence must be performed before entering an arrangement and continue thereafter, proportionate to its risk and criticality.

(OSFI, 2023, §2.2.2)

### Expected audit evidence

- third-party risk assessment;
- security assessment;
- due-diligence documentation;
- criticality classification;
- approvals;
- remediation requirements; and
- periodic reassessment.

---

# 4.3 Third-Party Data Security

### OSFI requirement

**B-10 §2.3.2**

Appropriate measures must protect the confidentiality, integrity and availability of records and data throughout the third-party arrangement.

Contracts should define security responsibilities and access to information.

(OSFI, 2023, §2.3.2)

---

# 4.4 Audit and Information Rights

### OSFI requirement

**B-10 §2.3.3**

Third-party arrangements should give the FRFI timely access to information necessary to oversee performance and risk.

The FRFI should also have the ability to conduct or commission independent audits where appropriate.

OSFI should be able to evaluate risk-management practices relating to the service and access relevant audit reports.

(OSFI, 2023, §2.3.3)

---

# 4.5 Cloud

### OSFI requirement

**B-10 §§4.3–4.4**

Cloud arrangements should be subject to cloud-specific requirements and governance.

Controls should address areas including:

- data protection;
- key management;
- container management;
- interoperability;
- concentration risk;
- exit strategy; and
- portability.

(OSFI, 2023, §§4.3–4.4)

---

# 5. Auditability and Documentation — E-13

## 5.1 Adequate Documentation

### OSFI requirement

**E-13 §IV(vii) — Adequate Documentation**

OSFI expects clearly documented roles and responsibilities and sufficient documentation demonstrating how regulatory compliance risk is managed.

Documentation should support periodic assessment of the compliance framework.

(OSFI, 2014, §IV(vii))

### Development implication

A control that occurs but leaves no verifiable evidence is considerably harder to demonstrate to an auditor.

For material controls, evidence should establish:

**Who → did what → to what → why → when → based on what approval → with what result**

---

# 5.2 Independent Review

### OSFI requirement

E-13 expects compliance oversight to be subject to validation by Internal Audit or another independent review function on a regular, risk-based basis.

Significant findings and corresponding remediation should be reported and tracked.

(OSFI, 2014, §IV(vi))

OSFI's current Supervisory Framework similarly describes Internal Audit as providing independent assurance over:

- internal controls;
- risk management; and
- governance processes.

---

# 6. Minimum Audit Evidence for a Production Change

For material production changes, the following provides a practical OSFI-aligned evidence chain:

| Control | Minimum evidence |
|---|---|
| Requirement | Jira/ADO/requirement record |
| Business authorization | Approved requirement or business owner approval |
| Design | Technical/solution design where material |
| Risk assessment | Technology/security/operational risk assessment where applicable |
| Development | Source-control commit |
| Peer review | Pull request and reviewer |
| Testing | Test case/result or automated pipeline evidence |
| Security | Security scan/review where applicable |
| Approval | Authorized change/release approval |
| Segregation of duties | Evidence developer did not unilaterally approve/deploy |
| Deployment | CI/CD or deployment record |
| Traceability | Change ↔ PR ↔ commit ↔ build ↔ deployment linkage |
| Production verification | Post-deployment validation |
| Incident/rollback | Rollback/incident evidence if the release fails |
| Exception | Documented risk acceptance where a control was bypassed |

This evidence set is an **implementation approach derived from the OSFI requirements above**; OSFI does not prescribe this exact Jira/CI/CD artefact list.

---

# 7. Core Audit Principle: Evidence Must Be Reconstructable

A useful standard for development teams is:

> For every material production change, an independent reviewer should be able to reconstruct what changed, why it changed, who developed it, who reviewed and approved it, how it was tested, when and how it entered production, and whether it operated as intended.

This supports the combined expectations of:

- B-13 §2.4 — SDLC;
- B-13 §2.5 — change and release management;
- B-13 §2.5.2 — segregation of duties;
- B-13 §2.5.3 — traceability;
- E-13 §IV(vii) — adequate documentation; and
- E-13 §IV(vi) — independent review.

---

# 8. Control Exceptions

Where a required control cannot be followed, the exception should not be handled informally.

An appropriate exception process should normally record:

- control being bypassed;
- reason;
- affected system;
- risk;
- duration;
- compensating controls;
- accountable owner;
- approval/risk acceptance;
- remediation date; and
- closure.

This aligns with B-13's expectation that the technology and cyber risk-management framework include processes for managing exceptions.

---

# 9. Regulatory Traceability Matrix

| Area | Primary OSFI reference |
|---|---|
| Technology accountability | B-13 §1.1 |
| Technology/cyber risk framework | B-13 §1.3 |
| Architecture | B-13 §2.1 |
| Asset inventory/configuration | B-13 §2.2 |
| Technology currency | B-13 §2.2.5 |
| Project management | B-13 §2.3 |
| SDLC | B-13 §2.4 |
| Security-by-design | B-13 §2.4.2; §3.2.1 |
| Secure coding/open-source | B-13 §2.4.5 |
| Change/release management | B-13 §2.5 |
| Segregation of duties | B-13 §2.5.2 |
| Change traceability | B-13 §2.5.3 |
| Patch management | B-13 §2.6 |
| Incident/problem management | B-13 §2.7 |
| Disaster recovery | B-13 §2.9 |
| Vulnerability management | B-13 §§3.1.3, 3.2.6 |
| Identity/access management | B-13 §3.2.7 |
| Application security testing | B-13 §3.2.9 |
| Security logging | B-13 §3.3.1 |
| Significant-change risk | E-21 §4.4 |
| Data risk | E-21 §4.7 |
| Third-party due diligence | B-10 §2.2.2 |
| Third-party data/security | B-10 §2.3.2 |
| Third-party audit rights | B-10 §2.3.3 |
| Third-party monitoring | B-10 §2.4 |
| Cloud | B-10 §4 |
| Compliance documentation | E-13 §IV(vii) |
| Independent assurance | E-13 §IV(vi) |
| Regulatory incident notification | Technology and Cyber Security Incident Reporting Advisory |

---

# 10. References

Office of the Superintendent of Financial Institutions. (2014, November 30). *Regulatory compliance management (RCM) – Guideline E-13.* [OSFI — Guideline E-13](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/regulatory-compliance-management-rcm-guideline-2014?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2018, September 30). *Corporate governance guideline.* [OSFI — Corporate Governance Guideline](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/corporate-governance-guideline-2018?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2021, August 13). *Technology and cyber security incident reporting.* [OSFI — Technology and Cyber Security Incident Reporting](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/technology-cyber-security-incident-reporting?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2022, July 31). *Technology and cyber risk management: Guideline B-13.* [OSFI — Guideline B-13](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/technology-cyber-risk-management?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2023, April 30). *Third-party risk management guideline: Guideline B-10.* [OSFI — Guideline B-10](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/third-party-risk-management-guideline?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2024, August 22). *Operational risk management and resilience: Guideline E-21.* [OSFI — Guideline E-21](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/operational-risk-management-resilience-guideline?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (2025, January 15). *OSFI technology and cyber incident report – Detailed instructions.* [OSFI — Incident Reporting Instructions](https://www.osfi-bsif.gc.ca/en/guidance/guidance-library/osfi-technology-cyber-incident-report-detailed-instructions?utm_source=chatgpt.com)

Office of the Superintendent of Financial Institutions. (n.d.). *Supervisory framework.* [OSFI — Supervisory Framework](https://www.osfi-bsif.gc.ca/en/supervision/supervisory-practices/supervisory-framework-0?utm_source=chatgpt.com)

---

## Regulatory interpretation note

OSFI's guidelines are principles- and risk-based. This page should therefore be used as a regulatory traceability and control baseline rather than as a substitute for the Bank's approved policies, enterprise SDLC, technology-risk standards, information-security standards, records-retention requirements, legal advice or Internal Audit methodology.

Where Bank policy imposes a more stringent control than the minimum regulatory expectation identified here, the Bank policy should govern.