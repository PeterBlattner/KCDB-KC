# Preliminary Phase – Establishing the Architecture Capability  
## KCDB Reference Data Architecture

**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  
**Owner:** BIPM / FORUM-MD-WG-CC / FORUM-MD-TG-MS ?

---

## 1. Purpose

This document defines the outcomes of the **TOGAF Preliminary Phase** for the
KCDB Reference Data Architecture initiative.

Its purpose is to:

- establish the **architecture capability** within BIPM,
- define governance, roles, and responsibilities,
- agree on architecture principles,
- and set the foundation for executing the ADM phases for the KCDB context.

The capability created here is intended to be **long-lived**, supporting the
continuous evolution of comparison reporting and CMC validation.

---

## 2. Scope of the Architecture Capability

The architecture capability covers:

- The **KCDB Reference Data Architecture**:
  - canonical data models and schemas,
  - vocabularies and semantics,
  - extension mechanisms.
- Supporting application and integration architectures:
  - submission, validation, computation, KCDB backend, CMC validation.
- Governance processes:
  - schema changes,
  - extension approval,
  - versioning and deprecation.
- Alignment with business processes for:
  - comparisons lifecycle,
  - publication,
  - CMC review.

It applies to all KC/SC domains coordinated through BIPM and the CCs.

---

## 3. Sponsorship and Mandate

### 3.1 Executive Sponsorship
The initiative is sponsored by:

- **BIPM**, in coordination with FORUM-MD-WG-CC.

### 3.2 Mandate
The architecture capability is mandated to:

- define and maintain the **reference architecture** for KC reporting,
- ensure interoperability across domains,
- support automation and digital transformation,
- and provide authoritative guidance to CCs and tool developers.

---

## 4. Architecture Governance

### 4.1 Governance Structure

The following bodies are established:

- **Architecture Working Group (AWG)**  
  Responsible for developing and maintaining the architecture.
- **Architecture Review Board (ARB)**  
  Provides oversight and approves major decisions, releases, and extensions.
- **Domain Extension Panels (per CC)**  
  Propose and review domain-specific extensions.

### 4.2 Responsibilities

| Role | Responsibility |
|------|----------------|
AWG | Develop models, schemas, principles, roadmap |
ARB | Approve architecture, changes, releases |
Domain Panels | Propose/maintain CC extensions |
KCDB Team | Operate systems, provide feedback |
IT Providers | Implement conformant tools |
Stakeholders | Review and validate fitness for purpose |

---

## 5. Architecture Repository

An **Architecture Repository** is established to store:

- Architecture Vision and ADM artifacts.
- Baseline inventory and analyses.
- Conceptual and logical data models (PlantUML).
- JSON Schemas and extension schemas.
- Vocabularies and code lists.
- Example datasets and test cases.
- Governance records and change logs.
- Roadmaps and migration plans.

The repository shall be version-controlled and publicly accessible where possible.

---

## 6. Architecture Principles

The following principles govern the KCDB Reference Data Architecture.

### P1. Canonical Core Model
A single canonical core data model shall be maintained for all KC/SC reporting.

### P2. Core + Extensions
Domain-specific needs shall be addressed through governed extensions, not forks.

### P3. DoE and Reference Values as First-Class Data
Degrees of Equivalence and reference values shall be explicitly represented,
including uncertainties and provenance.

### P4. Machine-Readable by Default
All specifications shall be machine-readable and support automated validation.

### P5. Explicit Semantics
Quantities, units, uncertainties, and conditions shall be explicit and unambiguous.

### P6. Provenance and Traceability
All derived data shall carry provenance and version metadata.

### P7. Open Standards
Open, widely adopted standards shall be used wherever possible.

### P8. Backward Compatibility
Changes shall minimise disruption and support coexistence where feasible.

### P9. Governed Evolution
All changes shall follow a formal review and approval process.

### P10. Reuse Beyond KCDB
The architecture shall support reuse for CMC validation and future digital services.

---

## 7. Architecture Method and Framework

- The initiative adopts **TOGAF ADM** as the primary architecture method.
- Phase C (Data Architecture) is the technical core.
- Business (Phase B) and Application (Phase D) architectures ensure alignment.
- Phases G and H provide long-term governance and change management.

Supporting methods:

- UML/PlantUML for conceptual and logical modeling.
- JSON Schema for physical models.
- Markdown for specifications.
- Mermaid for diagrams.

---

## 8. Tools and Environment

The architecture capability will use:

- Version control system (e.g., Git).
- Markdown-based documentation.
- PlantUML for models.
- JSON Schema validators.
- Issue tracking for change requests.
- CI pipelines for schema validation and examples.

---

## 9. Architecture Maturity and Skills

The AWG shall ensure availability of skills in:

- Metrology domain expertise.
- Data modeling and semantics.
- Uncertainty and correlation modeling.
- JSON Schema and APIs.
- Architecture governance.
- Tooling and automation.

Training and knowledge sharing shall be organised as needed.

---

## 10. Success Criteria

The architecture capability is considered established when:

- Governance bodies are operational.
- Principles are approved and adopted.
- Repository is in place and used.
- ADM phases are actively executed.
- CCs and pilots engage with the architecture.
- First conformant schemas and tools are produced.

---

## 11. Risks and Mitigations

| Risk | Mitigation |
|------|------------|
Lack of CC buy-in | Early involvement and pilots |
Overly complex model | Iterative design and MVP |
Resource constraints | Phased roadmap |
Fragmentation via forks | Strong governance |
Legacy burden | Coexistence and conversion tools |

---

## 12. Next Steps

- Approve this Preliminary Phase document.
- Formally establish AWG and ARB.
- Publish principles and repository.
- Launch Phase A – Architecture Vision.
- Initiate baseline inventory and Phase C activities.

---

## Summary

This Preliminary Phase establishes the **KCDB Reference Data Architecture capability**
as a strategic, governed function within BIPM, providing the foundation for
harmonised digital comparison reporting and CMC evidence for years to come.

---