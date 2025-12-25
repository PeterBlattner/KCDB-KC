# Architecture Description  
(ISO/IEC/IEEE 42010 Compliant)

**Title:** KCDB Reference Data Architecture  
**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  
**Owner:** BIPM / KCDB Architecture Working Group  
**Author:** GenAI prompted by Peter B.

---

## 1. Introduction

### 1.1 Purpose
This document is the Architecture Description (AD) for the **KCDB Reference Data Architecture**.  
It describes the architecture in conformance with ISO/IEC/IEEE 42010, identifying stakeholders
and concerns, defining viewpoints, and presenting views that collectively specify a canonical,
machine-readable information architecture for comparison reporting and CMC validation.  [oai_citation:0‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

### 1.2 Scope
The scope covers:

- Key and supplementary comparison (KC/SC) reporting,
- Results, uncertainties, reference values (KCRV/CRV), Degrees of Equivalence (DoE),
- Provenance and traceability,
- Interfaces to submission, computation, publication, and CMC validation services.

Out of scope (initially):

- Raw laboratory time series,
- Internal LIMS systems,
- Detailed numerical algorithms (interfaces only).  [oai_citation:1‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

### 1.3 Conformance
This architecture description conforms to ISO/IEC/IEEE 42010.

---

## 2. System of Interest

### 2.1 Identification
The system of interest is the **KCDB Reference Information Architecture Capability**:
a cross-domain, sustainable architecture enabling harmonised, machine-readable reporting
of KC/SC results and their use as evidence for CMC validation.  [oai_citation:2‡togaf-kcdb-architecture-mapping.md](sediment://file_00000000882c71f4aa94091484e92c9b)

### 2.2 Context
The system operates within:

- BIPM and the KCDB Secretariat,
- Consultative Committees (CCs),
- NMIs/DIs and pilot laboratories,
- CMC review bodies,
- Supporting IT and digital SI initiatives.  [oai_citation:3‡togaf-kcdb-architecture-mapping.md](sediment://file_00000000882c71f4aa94091484e92c9b)

---

## 3. Stakeholders and Concerns

### 3.1 Stakeholders

| ID | Stakeholder | Role / Interest |
|----|-------------|----------------|
S-01 | BIPM KCDB Secretariat | Data quality, automation, publication |
S-02 | Consultative Committees | Scientific correctness, domain fit |
S-03 | Pilot laboratories | Practical submission & tools |
S-04 | NMIs / DIs | Effort, reuse for CMCs |
S-05 | CMC review bodies | Transparent DoE-based evidence |
S-06 | IT providers | Stable schemas & APIs |
S-07 | BIPM Management | Sustainability & governance |

 [oai_citation:4‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

### 3.2 Concerns

| ID | Concern |
|-----|---------|
C-01 | Scientific correctness across domains |
C-02 | Support for DoE-based CMC validation (incl. NMI uncertainty) |
C-03 | Harmonisation vs. domain diversity |
C-04 | Ease of submission |
C-05 | Backward compatibility & legacy data |
C-06 | Automation & machine actionability |
C-07 | Governance & controlled evolution |
C-08 | Transparency & traceability |
C-09 | Interoperability with digital metrology standards |
C-10 | Security & access control |
C-11 | Long-term sustainability |
C-12 | Measurable value & adoption |

 [oai_citation:5‡stakeholders_concerns.md](sediment://file_0000000073d0720aba7e0621c7b648c7)

---

## 4. Viewpoints

### 4.1 Business Viewpoint

- **Stakeholders:** S-01, S-02, S-03, S-05  
- **Concerns:** C-04, C-07, C-12  
- **Model kinds:** Process and role models  
- **Notations:** BPMN, activity diagrams  
- **Purpose:** Describe lifecycle of comparisons and decision points.

### 4.2 Data Viewpoint

- **Stakeholders:** S-01, S-02, S-04, S-05, S-06  
- **Concerns:** C-01, C-02, C-03, C-05, C-06, C-08, C-09  
- **Model kinds:** Conceptual/logical models, schemas  
- **Notations:** UML/PlantUML, JSON Schema  
- **Purpose:** Define canonical semantics for results, DoEs, uncertainties, provenance.

### 4.3 Application Viewpoint

- **Stakeholders:** S-01, S-05, S-06  
- **Concerns:** C-04, C-06, C-10, C-12  
- **Model kinds:** Application interactions, services, APIs  
- **Notations:** Component/sequence diagrams  
- **Purpose:** Show how systems consume and produce canonical data.

### 4.4 Technology Viewpoint

- **Stakeholders:** S-06, S-07  
- **Concerns:** C-10, C-11  
- **Model kinds:** Platform and infrastructure models  
- **Notations:** Deployment diagrams  
- **Purpose:** Define hosting, security, and sustainability.

### 4.5 Migration & Governance Viewpoint

- **Stakeholders:** S-01, S-02, S-07  
- **Concerns:** C-05, C-07, C-11  
- **Model kinds:** Roadmaps, governance processes  
- **Purpose:** Control adoption and evolution.

---

## 5. Architecture Views

### 5.1 View: Business Process View

- **Viewpoint:** Business  
- **Concerns:** C-04, C-07, C-12  
- **Description:** End-to-end KC/SC lifecycle: plan, submit, compute, review, publish, validate CMCs.  
- **Artifacts:** BPMN diagrams (to be produced in Phase B).

### 5.2 View: Conceptual Data Model

- **Viewpoint:** Data  
- **Concerns:** C-01, C-02, C-03, C-08  
- **Description:** Canonical entities for comparisons, participants, measurands, results,
  reference values, DoEs, uncertainties, correlations, provenance.  
- **Artifacts:** PlantUML conceptual model (Phase C).

### 5.3 View: Logical/Physical Data Model

- **Viewpoint:** Data  
- **Concerns:** C-02, C-05, C-06, C-09  
- **Description:** Logical model and JSON Schemas implementing the canonical core and extensions.  
- **Artifacts:** JSON Schema set with examples (Phase C).

### 5.4 View: Application Interaction View

- **Viewpoint:** Application  
- **Concerns:** C-04, C-06, C-10  
- **Description:** Submission, validation, computation, KCDB repository, CMC validation services.  
- **Artifacts:** Interaction diagrams, API contracts (Phase D).  [oai_citation:6‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

### 5.5 View: Target Architecture Overview

- **Viewpoint:** Application  
- **Concerns:** C-02, C-06, C-12  
- **Description:** High-level flow from NMIs to KCDB and CMC validation.  
- **Artifacts:** Vision flow diagram.  [oai_citation:7‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

---

## 6. Correspondences and Traceability

### 6.1 Correspondence Rules

- Every business information object maps to ≥1 data entity.
- Every data entity exposed maps to ≥1 application service.
- Every DoE links to:
  - its reference value,
  - its uncertainty,
  - the contributing participant results.
- Every CMC claim references supporting DoEs and typical NMI uncertainties.  [oai_citation:8‡stakeholders_concerns.md](sediment://file_0000000073d0720aba7e0621c7b648c7)

### 6.2 Example Correspondences

| Business Element | Data Entity | Application Service |
|------------------|-------------|---------------------|
Participant result submission | ParticipantResult | Submission API |
Compute DoE | DegreeOfEquivalence | Computation Service |
Publish comparison | ComparisonRecord | KCDB API |
Validate CMC | CMCClaimEvidence | CMC Validation Service |

---

## 7. Architecture Decisions and Rationale

| ID | Decision | Rationale | Affected Views |
|----|----------|-----------|----------------|
AD-01 | Single canonical core model | Interoperability, consistency | Data, Application |
AD-02 | Core + governed extensions | Support domain diversity | Data |
AD-03 | DoE as first-class object | Enable CMC validation | Data, Application |
AD-04 | JSON Schema as physical model | Automation & validation | Data, Application |
AD-05 | Versioned, immutable records | Traceability & auditability | Data, Governance |



---

## 8. Constraints and Assumptions

### 8.1 Constraints

- Must coexist with legacy KCDB records.
- Must rely on open standards and sustainable tooling.
- Must gain acceptance across CC domains.  [oai_citation:9‡architekture_vision.md](sediment://file_00000000845071f4a9ae9fd087ac9bd8)

### 8.2 Assumptions

- CCs will participate in extension design.
- Pilot implementations will guide refinement.
- Governance bodies will be established.  [oai_citation:10‡togaf-kcdb-architecture-mapping.md](sediment://file_00000000882c71f4aa94091484e92c9b)

---

## 9. Architecture Lifecycle and Change

### 9.1 Version History

| Version | Date | Description |
|---------|------|-------------|
0.1 | 2025-12-22 | Initial populated Architecture Description |

### 9.2 Change Management

Changes follow TOGAF Phase H:

- Formal change requests,
- Impact analysis,
- Review by governance boards,
- Versioned releases with deprecation policy.  [oai_citation:11‡togaf-kcdb-architecture-mapping.md](sediment://file_00000000882c71f4aa94091484e92c9b)

---

## 10. References

- Architecture Vision – Harmonised Digital Model for KCDB Reporting & CMC Validation.  
- Stakeholder Concerns Catalogue.  
- KCDB Reference Data Architecture – TOGAF Mapping.  



---

## Appendix A – Glossary

- **KC/SC:** Key / Supplementary Comparison  
- **KCRV/CRV:** Key / Comparison Reference Value  
- **DoE:** Degree of Equivalence  
- **CMC:** Calibration and Measurement Capability  

---

## Appendix B – Architecture Artifacts Index

| ID | Artifact | Type | Location |
|----|----------|------|----------|
A-01 | Architecture Vision | Document | architekture_vision.md |
A-02 | Stakeholder Concerns | Document | stakeholders_concerns.md |
A-03 | TOGAF Mapping | Document | togaf-kcdb-architecture-mapping.md |
A-04 | Conceptual Data Model | PlantUML | (Phase C) |
A-05 | JSON Schemas | Schema | (Phase C) |

---