# OSFI-Aligned Operating Principles  
## Quick Reference for Software Delivery

### Purpose

This page summarizes key operating principles for software delivery where business requirements, technology controls, data ownership, regulatory considerations and auditability intersect.

For detailed regulatory requirements and citations, refer to the full **OSFI Software Development & Technology Audit Compliance Requirements** page.

---

# 1. Core Operating Principle

**OSFI reference:** B-13 §§2.1.1, 2.4.1; E-21 §§1.2–1.4.

> **Business functions define the required business outcome. Technology is responsible for implementing the approved requirement in a secure, reliable, controlled and traceable manner.**

Business, Risk, Compliance, Data and Technology responsibilities remain distinct, with shared accountability where control objectives overlap.

---

# 2. Business and Technology Control Boundaries

**OSFI reference:** E-21 §§1.2–1.4; E-13 §IV; B-13 §§2.4–2.5.

### Business / Regulatory Control

Typically covers:

- business rules and process requirements;
- accounting or financial treatment;
- permitted exceptions;
- business approvals;
- regulatory and policy interpretation; and
- acceptance of business risk.

**Typical ownership:** Business, Finance, Risk, Compliance, Data Owner.

### Technology Control

Typically covers:

- implementation correctness;
- access control;
- secure development;
- testing;
- change and release management;
- logging and traceability;
- system availability and resilience; and
- technical risk management.

**Typical ownership:** Technology, Technology Risk, Security.

---

# 3. Requirement and Implementation Ownership

**OSFI reference:** B-13 §§2.4.1–2.4.3, 2.5.1–2.5.3; E-21 §§1.2–1.3.

Business requirements and business-control decisions remain with the appropriate business or control function.

Technology translates approved requirements into system behaviour and is responsible for the associated technical controls.

Where clarification or risk assessment is required, the relevant owner provides the decision before implementation.

Required technology controls remain applicable irrespective of the underlying business decision.

---

# 4. Control Ownership by Domain

**OSFI reference:** E-21 §§1.2–1.4, 4.7; B-13 §§1.1, 2.4, 2.5, 3.2; E-13 §IV.

| Area | Primary ownership |
|---|---|
| Business rule or calculation treatment | Business |
| Regulatory or policy interpretation | Compliance / Risk |
| Source-data quality | Data / Source Owner |
| Application implementation | Technology |
| Security and access control | Technology / Security |
| Production change control | Technology |
| Operational resilience | Shared |
| Independent control assurance | Internal Audit / Independent Risk |

Technology remains responsible for assessing the system impact of issues originating outside the application boundary.

Ownership of the underlying issue remains with the relevant source or control function unless formally transferred.

---

# 5. Control Placement

**OSFI reference:** E-21 §§1.2–1.3, 2.3; E-13 §IV; B-13 §§1.3, 2.4–2.5.

Controls may exist at different layers depending on the nature of the risk.

Common control locations include:

- business procedures;
- approval workflows;
- reconciliation;
- data-quality controls;
- access management;
- monitoring;
- exception management;
- application validation; and
- automated system controls.

Control design aligns the control mechanism with the nature and ownership of the underlying risk.

---

# 6. Operational Resilience and Knowledge Continuity

**OSFI reference:** B-13 §1.1.2; E-21 §§1.1, 4.1.2–4.1.3.

Critical technology services require sufficient continuity of support and technical knowledge.

Relevant measures may include:

- defined primary and secondary ownership;
- cross-training;
- technical documentation;
- operational runbooks;
- knowledge transfer;
- automation of routine activities; and
- sufficient technical capability across the support model.

Specialist expertise may remain concentrated where appropriate, provided critical operational activities remain supportable.

---

# 7. Maintainability and Operability

**OSFI reference:** B-13 §§1.1.2, 2.1.2, 2.4.1–2.4.5, 2.7.

Application design and support processes support consistent and controlled development and operational activities.

Relevant considerations include:

- manageable system complexity;
- automation of repetitive activities;
- clear validation and error handling;
- effective logging and observability;
- standardized deployment;
- documented operating procedures; and
- understandable and supportable system behaviour.

Maintainability, automation and documentation complement appropriate technical expertise and support operational resilience.

---

# 8. Ownership Classification

**OSFI reference:** E-21 §§1.2–1.4; B-13 §§2.1.1, 2.4.1.

A practical distinction can be made between:

### Business decision

Defines **what outcome or treatment is required**.

### Technology decision

Defines **how the approved outcome is implemented, controlled and operated**.

Where both elements are present, responsibilities may be shared while the underlying ownership remains distinct.

---

# 9. Operating Model

**OSFI reference:** E-21 §§1.2–1.4; E-13 §IV; B-13 §§1.1, 2.4–2.5.

**Business**  
Defines the required business outcome

↓

**Risk / Compliance**  
Provides independent challenge and regulatory or policy interpretation where applicable

↓

**Technology**  
Designs and implements the approved requirement

↓

**Technology Controls**  
Provide security, testing, segregation of duties, traceability and resilience

↓

**Business**  
Validates that the delivered outcome meets the approved requirement

↓

**Internal Audit / Independent Assurance**  
Assesses control design and operating effectiveness

---

# 10. Key Principles

**OSFI reference:** B-13 §§1.1–1.3, 2.4–2.5; E-21 §§1.1–1.4, 4.1, 4.7; E-13 §IV.

1. **Business-rule ownership and technical-control ownership are distinct.**
2. **Technology implementation does not transfer ownership of the underlying business decision.**
3. **Business approval does not remove required technology controls.**
4. **Control ownership aligns with the source and nature of the risk.**
5. **Operational resilience depends on both system design and sufficient technical capability.**
6. **Material decisions and production changes require appropriate traceability and evidence.**

---

## Core OSFI References

Office of the Superintendent of Financial Institutions. (2022). *Technology and cyber risk management: Guideline B-13.*

Office of the Superintendent of Financial Institutions. (2024). *Operational risk management and resilience: Guideline E-21.*

Office of the Superintendent of Financial Institutions. (2014). *Regulatory compliance management: Guideline E-13.*

Office of the Superintendent of Financial Institutions. (2023). *Third-party risk management: Guideline B-10.*

