# KCDB Reference Data Architecture  
## Mapping the Initiative to TOGAF ADM

**Version:** 0.2  
**Status:** Draft (Updated)  
**Date:** 2025-12-22  
**Owner:** BIPM / KCDB Architecture Working Group  
**Author:** genAI corrected by Peter B.

---

## Introduction

The KCDB Reference Data Architecture initiative establishes a **canonical,
machine-readable information architecture** for reporting key and supplementary
comparison (KC/SC) results and for enabling **systematic validation of CMC claims**
based on Degrees of Equivalence (DoE).

What is being designed is not merely a new exchange format, but a sustainable
**cross-domain architecture capability** that:

- harmonises highly diverse reporting practices across Consultative Committees,
- makes comparison results **machine-actionable**,
- and provides a trusted evidence base for CMC review and future digital services.

This document describes how the initiative aligns with the
**TOGAF Architecture Development Method (ADM)**, with strong emphasis on
**Phase C – Data Architecture**, while keeping Business and Application layers aligned.

---

## 1. Why TOGAF Fits the KCDB Context

The KCDB problem space exhibits all characteristics for which TOGAF is intended:

- Many stakeholders: BIPM, CCs, NMIs/DIs, reviewers, IT providers.
- Strong heterogeneity of existing formats (Excel, Word, PDFs, XML, ad-hoc tools).
- Long lifecycle with scientific traceability requirements.
- Need for a **common target architecture** accepted across domains.
- Continuous evolution driven by new methods, domains, and Digital SI.

Baseline analysis shows high variability in:

- reference values (KCRV, CRV, artefact-based, class-based),
- DoE definitions and coverage metrics (u(DoE), En, limits),
- measurand complexity (scalar, vector, complex, parameterised),
- and relationships between comparisons and CMC claims.

This is therefore the design of a:

> **KCDB Reference Information Architecture Capability**,  
> not simply a schema harmonisation exercise.

---

## 2. Mapping the Initiative to the TOGAF ADM Cycle

### Preliminary Phase — Establish the Architecture Capability

**Purpose:** Set scope, authority, and governance.

**KCDB context:**

- Sponsorship by BIPM leadership.
- Establish a permanent architecture working group.
- Position this as the **BIPM reference data architecture** for comparisons.
- Define architecture principles, e.g.:
  - Single canonical core model.
  - Core + domain extensions.
  - Machine-readable by default.
  - Provenance and traceability by design.
  - Backward compatibility and controlled evolution.
  - Open standards and sustainability.

**Deliverables:**

- Architecture charter.  
- Architecture principles.  
- Governance structure and review boards.

---

### Phase A — Architecture Vision

**Purpose:** Why and what success looks like.

**KCDB context:**

- Business drivers:
  - Improve consistency and quality of KC reporting.
  - Enable DoE-based CMC validation.
  - Reduce manual ingestion and review effort.
  - Enable automation, analytics, and reuse.
- Scope:
  - Comparisons, measurands, participant results,
  - reference values, DoEs, uncertainties, provenance,
  - links to CMC claims.
- Identify stakeholders and enumerate concerns.

**Deliverables:**

- Architecture Vision document.  
- Stakeholder map and concerns.  
- Vision statement:  
  *“Harmonised digital KC reporting as a trusted evidence base for KCDB and CMC workflows.”*

---

### Phase B — Business Architecture

**Purpose:** Align with real processes and decisions.

**KCDB context – key processes:**

- Plan and register comparisons.
- Collect and validate participant submissions.
- Compute reference values and DoEs.
- Review and approve results.
- Publish in KCDB.
- Use results for CMC validation.

**Focus:**

- Roles (Pilot, CC WGs, reviewers, KCDB team, NMIs/DIs).
- Information flows and decision gates.

**Deliverables:**

- Business process models (BPMN).  
- Business functions and actors.  
- Information flow diagrams.

---

### Phase C — Data Architecture (Core of the Initiative)

**Purpose:** Define baseline and target data architecture.

#### Baseline

- Inventory of existing formats and practices.
- Observed variability in:
  - DoE definitions and uncertainty reporting,
  - CRV/KCRV derivation and provenance,
  - measurand representations,
  - linking between comparisons,
  - availability and publication status.

#### Target

- Canonical conceptual and logical model.
- **DoE and reference values as first-class objects.**
- Explicit uncertainty and correlation representation.
- Flexible measurand model (scalar, vector, complex, parameterised).
- Evidence-based links between KC/SC and CMC claims.
- Core + governed extensions.
- Versioning and provenance metadata.

This is where:

- conceptual model extraction,
- PlantUML modeling,
- and JSON Schema derivation  
are anchored.

**Deliverables:**

- Baseline findings and inventory.  
- Target conceptual & logical data model.  
- Data principles and requirements.  
- Baseline → target mapping.

---

### Phase D — Application Architecture

**Purpose:** Define how systems realise the data architecture.

**KCDB context:**

- Submission portals and APIs.
- Validation services.
- KCRV/DoE computation engines.
- KCDB backend and registry.
- CMC validation services.
- Reporting and visualisation tools.

**Ensure:**

- All applications consume and produce canonical data.
- APIs are schema-driven.
- Provenance flows end-to-end.

**Deliverables:**

- Application portfolio.  
- Interaction diagrams.  
- API contracts aligned to JSON Schema.

---

### Phase E — Opportunities & Solutions

**Purpose:** Shape concrete solution building blocks.

**KCDB context:**

- Schema registry and versioning service.
- Reference validators and converters.
- Example libraries and test cases.
- Pilot CC deployments.
- Toolchain prototypes.

**Deliverables:**

- Solution concept.  
- Work packages.  
- High-level roadmap.

---

### Phase F — Migration Planning

**Purpose:** Plan adoption.

**KCDB context:**

- Pilot domains and comparisons.
- Coexistence with legacy submissions.
- Strategy for historical data (where feasible).
- Incremental rollout.

**Deliverables:**

- Migration roadmap.  
- Risks and mitigations.

---

### Phase G — Implementation Governance

**Purpose:** Ensure conformance.

**KCDB context:**

- Review of schemas, tools, and extensions.
- Approval of domain extensions.
- Version control and release gates.
- Conformance criteria.

**Deliverables:**

- Governance process.  
- Conformance checklists.  
- Review boards.

---

### Phase H — Architecture Change Management

**Purpose:** Manage evolution.

**KCDB context:**

- New domains and measurands.
- New uncertainty and correlation models.
- Digital SI evolution.
- New reporting and validation needs.

**Deliverables:**

- Change workflow.  
- Versioning and deprecation policy.

---

## 3. Positioning of Core Artifacts

- **Canonical PlantUML model** → Logical Data Model.  
- **JSON Schemas** → Physical Data Model.  
- **Glossary & vocabularies** → Data Dictionary.  
- **Example datasets** → Architecture Building Blocks.  
- **Schema registry** → Architecture Repository.  
- **Domain extensions** → Solution Building Blocks.

---

## 4. Program Structure

Suggested work packages:

1. Architecture Vision & Principles.  
2. Baseline Inventory & Analysis.  
3. Canonical Conceptual Model.  
4. Data Requirements & Semantics.  
5. Schema & API Design.  
6. Reference Tooling & Prototypes.  
7. Pilot Implementations.  
8. Governance & Change Management.

Each with defined stakeholders, deliverables, and review gates.

---

## 5. Why This Matters

This architecture approach:

- Creates a **shared language** across science, IT, and management.
- Separates:
  - business needs,
  - data semantics,
  - technical implementation.
- Provides justification for:
  - governance,
  - phased rollout,
  - long-term sustainability.
- Avoids a fragmented “many schemas” future.

It positions the initiative as:

> **KCDB Reference Data Architecture**,  
> the digital backbone for comparison reporting and CMC evidence.

---

## Summary

The KCDB initiative aligns strongly with TOGAF:

- Use the **ADM** as the program backbone.  
- Concentrate technical effort in **Phase C – Data Architecture**.  
- Keep business processes (Phase B) and tools (Phase D) aligned.  
- Use **Phases G/H** to govern evolution.

This provides structure, legitimacy, and sustainability for a
multi-domain, multi-stakeholder transformation.

---
