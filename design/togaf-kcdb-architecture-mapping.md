# KCDB Reference Data Architecture  
## Mapping the Initiative to TOGAF ADM

**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  

---

## Introduction

The KCDB data model initiative maps very naturally to **TOGAF**. What is being designed is not just a schema, but a **cross-domain information architecture capability** to support harmonised digital reporting of key comparison results and automated validation of CMCs.

This document describes how the initiative aligns with the **TOGAF Architecture Development Method (ADM)**, with emphasis on **Data Architecture**, while keeping Business and Application layers aligned.

---

## 1. Why TOGAF Fits the KCDB Problem

The KCDB context exhibits the key characteristics TOGAF is designed for:

- Many stakeholders (BIPM, CCs, NMIs/DIs, IT providers).
- High heterogeneity of existing solutions and formats.
- Need for a **common target architecture**.
- Long lifecycle with controlled evolution.
- Strong semantic, scientific, and compliance requirements.

This is therefore not merely a format harmonisation exercise, but the design of a:

> **KCDB Reference Information Architecture Capability.**

---

## 2. Mapping the Initiative to the TOGAF ADM Cycle

### Preliminary Phase — Establish the Architecture Capability

**Purpose:** Set the ground rules.

**KCDB context:**
- Define sponsorship (BIPM leadership).
- Establish an architecture team / working group.
- Position this as a **BIPM reference data architecture** initiative.
- Define architecture principles, for example:
  - Single canonical model for comparison reporting.
  - Core + extensions.
  - Machine-readable by default.
  - Backward compatibility.

**Deliverables:**
- Architecture charter.  
- Architecture principles.  
- Governance setup.

---

### Phase A — Architecture Vision

**Purpose:** Why are we doing this and what does success look like?

**KCDB context:**
- Business drivers:
  - Improve consistency of KC reporting.
  - Enable CMC validation.
  - Reduce manual processing.
  - Enable automation and analytics.
- High-level scope:
  - Comparisons, results, DoEs, reference values.
  - Exclude internal lab raw data (initially).
- Identify stakeholders and their concerns.

**Deliverables:**
- Architecture Vision document.  
- Stakeholder map.  
- High-level target statement:  
  *“Harmonised digital KC reporting feeding KCDB and CMC workflows.”*

---

### Phase B — Business Architecture

**Purpose:** Understand processes and use cases.

**KCDB context – key processes:**
- Plan comparison.
- Collect participant data.
- Compute KCRV and DoEs.
- Review and publish results.
- Validate CMCs.
- Update KCDB.

**Identify:**
- Actors (Pilot, CC working groups, KCDB team, NMIs/DIs).
- Information used and produced at each step.

**Deliverables:**
- Business process maps (e.g., BPMN, activity diagrams).  
- Business functions.  
- Information flows.

This ensures the data model supports **real workflows**, not just abstract structures.

---

### Phase C — Data Architecture (Core of the Effort)

**Purpose:** Define baseline and target data architectures.

#### Baseline Data Architecture
- Inventory current formats:
  - Excel sheets.
  - Word annexes.
  - XML files.
  - Ad-hoc databases.
- Identify inconsistencies and gaps.

#### Target Data Architecture
- Canonical conceptual model.
- Core + extension strategy.
- Explicit semantics:
  - quantities,
  - units,
  - uncertainty,
  - vocabularies.
- Governance metadata:
  - versioning,
  - status,
  - provenance.

This is where:
- conceptual model extraction,
- PlantUML core modeling,
- DoE-centric design  
fit directly.

**Deliverables:**
- Baseline data architecture description.  
- Target conceptual and logical data model.  
- Data principles.  
- Mapping from baseline to target.

---

### Phase D — Application Architecture

**Purpose:** Define how applications will use the data.

**KCDB context:**
- Data submission tools (forms, APIs).
- Validation services.
- KCRV/DoE computation tools.
- KCDB backend.
- CMC validation services.
- Reporting and visualisation tools.

**Ensure:**
- All applications use the canonical schema.
- APIs and contracts are schema-driven.

**Deliverables:**
- Application portfolio.  
- Target application interaction diagrams.  
- API contracts aligned to JSON Schema.

---

### Phase E — Opportunities & Solutions

**Purpose:** Shape solution building blocks and options.

**KCDB context:**
- Schema registry.
- Reference implementation.
- Conversion tools from legacy formats.
- Pilot CC deployments.
- Tooling stack (validation, storage, APIs).

**Deliverables:**
- Solution concept.  
- High-level roadmap.  
- Work packages.

---

### Phase F — Migration Planning

**Purpose:** Get from current state to target state.

**KCDB context:**
- Which CCs pilot first?
- Which comparisons first use the new model?
- Coexistence period with legacy submissions.
- Strategy for historical data migration (if any).

**Deliverables:**
- Phased migration plan.  
- Risks and mitigations.

---

### Phase G — Implementation Governance

**Purpose:** Ensure conformance to the architecture.

**KCDB context:**
- Review tools and schemas against the architecture.
- Validate and approve CC extensions.
- Control schema versions.
- Enforce principles (e.g., no CC-specific forks of the core).

**Deliverables:**
- Governance process.  
- Conformance checklists.  
- Review boards.

---

### Phase H — Architecture Change Management

**Purpose:** Evolve architecture safely.

**KCDB context:**
- Manage:
  - new domains,
  - new uncertainty models,
  - Digital SI evolutions,
  - new reporting requirements.
- Formal change request process for schemas.

**Deliverables:**
- Change management workflow.  
- Versioning and deprecation policy.

---

## 3. Mapping Earlier Design Steps to TOGAF

| Design Step                    | TOGAF Phase                |
|--------------------------------|----------------------------|
| Corpus & inventory             | Phase C (Baseline)         |
| Concept mining & glossary      | Phase C (Target)           |
| Core + extensions design       | Phase C                    |
| PlantUML conceptual model      | Phase C                    |
| JSON Schema derivation         | Phase C / D                |
| Prototyping with real cases    | Phase E                    |
| Tooling discussion             | Phase D / E                |
| Versioning & governance        | Preliminary, Phase G / H   |
| Adoption roadmap               | Phase F                    |

---

## 4. Artifacts Alignment

Concrete mappings to TOGAF artifacts:

- **Canonical PlantUML model** → Logical Data Model.  
- **JSON Schema** → Physical Data Model.  
- **Glossary** → Data Dictionary.  
- **Examples** → Architecture Building Blocks (ABBs).  
- **Schema registry** → Architecture Repository.  
- **CC extensions** → Solution Building Blocks (SBBs).

---

## 5. Running the Initiative as a TOGAF Program

Suggested work packages:

1. Architecture Vision & Principles (Preliminary + Phase A)  
2. Baseline Assessment (Phase B + Phase C baseline)  
3. Canonical Conceptual Model (Phase C target)  
4. Schema & Semantics Design (Phase C / D)  
5. Reference Tooling & Prototype (Phase D / E)  
6. Pilot CC Implementations (Phase F)  
7. Governance Setup (Phase G / H)

Each package includes:
- stakeholders,
- deliverables,
- review gates.

---

## 6. Why This Helps Politically and Practically

Using TOGAF framing provides:

- A shared language with IT and management.
- Clear separation between:
  - business needs,
  - data semantics,
  - technical implementation.
- Justification for:
  - governance,
  - iteration,
  - phased rollout.
- A way to avoid “just another schema project”.

This positions the initiative as:

> **KCDB Reference Data Architecture**, not merely a format change.

---

## Summary

The KCDB data model initiative aligns strongly with TOGAF:

- Use the **ADM** as the program backbone.  
- Focus technical work in **Phase C (Data Architecture)**.  
- Keep business processes (Phase B) and tools (Phase D) aligned.  
- Use Phases **G/H** to govern schema evolution long term.

This provides structure, legitimacy, and sustainability for a multi-domain,
multi-stakeholder transformation.

---
