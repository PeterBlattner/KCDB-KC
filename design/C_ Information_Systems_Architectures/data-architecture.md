# Phase C – Data Architecture  
## KCDB Reference Data Architecture

**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  
**Owner:** BIPM / KCDB Architecture Working Group  
**Author:** genAI corrected by Peter B.

---

## 1. Purpose

This document defines the **Data Architecture** for the KCDB Reference Data
Architecture initiative, in accordance with **TOGAF Phase C**.

Its purpose is to:

- describe the **baseline data architecture** for KC reporting,
- define the **target data architecture** based on a canonical model,
- identify gaps between baseline and target,
- and provide principles and guidance for subsequent schema and tool design.

The focus is on data required to report **key comparison results** and to enable
**CMC validation based on Degrees of Equivalence (DoE)**.

---

## 2. Scope

### In Scope
- Key and supplementary comparison reporting.
- Participant results, uncertainties, reference values, DoEs.
- Correlation and covariance information relevant to DoE uncertainty.
- Comparison metadata and provenance.
- Domain extensions for physics, chemistry and biology fields.


### Out of Scope (initially)
- Raw measurement time series.
- Pilot comparisons
- Internal laboratory LIMS structures.
- Detailed numerical algorithms (only inputs/outputs and provenance).

---

## 3. Stakeholders

| Stakeholder | Interest |
|-------------|----------|
BIPM KCDB Secretariat | Data base management, ingestion, publication |
Consultative Committees | Scientific correctness, domain fit |
Pilot Laboratories | Practical reporting and tooling |
NMIs / DIs | Responsible for their data, effort, reuse for CMCs |
CMC Review Bodies | DoE evidence and traceability |
IT Providers | Stable schemas and APIs |

---

## 4. Baseline Data Architecture

### 4.1 Overview

The current baseline is characterised by:

- Multiple heterogeneous formats:
  - Excel spreadsheets,
  - Word annexes,
  - PDF reports,
  - (domain-specific XML),
- Strong domain dependence of structure and terminology.
- Limited machine-actionable semantics.
- Manual consolidation and validation steps.

### 4.2 Key Issues

- Lack of a common conceptual model.
- Ambiguity in representation of uncertainties and DoEs.
- Inconsistent use of identifiers and metadata.
- Limited support for automated validation.
- High manual workload for KCDB ingestion and review.

---

## 5. Target Data Architecture

### 5.1 Vision

Establish a **canonical, machine-readable data model** for KC reporting that:

- captures core metrological concepts consistently,
- supports DoE and DoE uncertainty as first-class data,
- enables automation of validation and ingestion,
- allows domain-specific extensions under governance,
- is stable, versioned, and sustainable.

---

### 5.2 Core Design Principles

- **Canonical Core:** One shared core model for all domains.
- **Core + Extensions:** Domain-specific needs handled via extensions.
- **Explicit Semantics:** Quantities, units, uncertainty, provenance are explicit.
- **Machine-Readable:** JSON/XML Schema as primary physical representation.
- **Immutability:** Published datasets are versioned and immutable.
- **Traceability:** Provenance links inputs, methods, and outputs.
- **Governed Evolution:** Changes via formal process.

---

### 5.3 Canonical Conceptual Model (Overview)

The target conceptual model includes the following core concepts:

- **Comparison**
- **Measurand**
- **Participant**
- **ReportedResult**, including uncertainties
- **ReferenceValue**
- **DegreeOfEquivalence**, including its uncertainty
- **UncertaintyStatement**
- **CorrelationModel**
- **Provenance** and Versioning

Each concept is uniquely identified and related through defined cardinalities.

The model is maintained as a **PlantUML conceptual and logical model** and serves
as the authoritative source for schema derivation.

---

### 5.4 Key Information Objects

| Object | Description |
|--------|-------------|
Comparison | Metadata describing a comparison (type, dates, status). |
Measurand | Definition of the quantity and conditions under comparison. |
Participant | NMI/DI participating in the comparison. |
ReportedResult | Value and uncertainty submitted by a participant. |
ReferenceValue | Agreed reference value and uncertainty (e.g., KCRV). |
DegreeOfEquivalence | Delta and uncertainty relative to the reference value. |
UncertaintyStatement | Standard/expanded uncertainty, k, coverage, method. |
CorrelationModel | Correlations/covariances relevant to uncertainty. |
Metrological traceability | Tracebility to an international agreed reference |
Provenance | Metadata on source, method, versions, timestamps. |

---

### 5.5 DoE and Uncertainty as First-Class Data

The target architecture treats:

- **Degree of Equivalence (DoE)** and
- **its associated uncertainty**

as explicit, persistent data objects, not merely derived values in reports. In addition the uncertainty reported by the NMI in the comparison needs to be considered. 

This enables:

- systematic CMC validation,
- automated consistency checks,
- traceable recomputation if required.

Correlation information is explicitly represented where it influences DoE
uncertainty.

---

### 5.6 Core + Extension Strategy

The data architecture is structured into:

- **Core schema**  
  Common across all domains (comparison, results, uncertainties, DoEs).

- **Domain extensions**  
  CC- or field-specific descriptors (e.g., chemistry sample prep, electrical
  waveforms, radiation qualities).

Extensions:

- must reference core entities,
- must not redefine core semantics,
- are governed and versioned.

---

### 5.7 Physical Representation

The physical target representation is:

- **JSON Schema** for data exchange and validation.
- Versioned schema identifiers.
- Controlled vocabularies for enumerations.
- Examples and test instances as part of the specification.

Other representations (e.g., XML) may be derived if required, but JSON Schema is
authoritative.

---

## 6. Gap Analysis (Baseline → Target)

| Area | Baseline | Target |
|------|----------|--------|
Conceptual model | Implicit, domain-specific | Explicit canonical model |
Format | Excel, Word, PDF, ad-hoc XML | JSON instances validated by schema |
Semantics | Often implicit | Explicit quantities, units, uncertainty |
DoE representation | In tables/reports | First-class structured data |
Validation | Manual | Automated schema + semantic checks |
Traceability | Limited | Provenance & version metadata |
Governance | Informal | Formal change & version control |

---

## 7. Data Principles

1. All KC reporting data shall conform to the canonical schema.
2. Core semantics shall not be redefined by extensions.
3. Published datasets shall be immutable and versioned.
4. Identifiers shall be globally unique and persistent.
5. Units and quantities shall use controlled vocabularies.
6. Uncertainty representation shall be explicit and structured.
7. Provenance shall be captured for all derived data.

---

## 8. Architecture Building Blocks (ABBs)

Key data-related ABBs include:

- Canonical conceptual data model (PlantUML).
- Core JSON Schema.
- Domain extension schemas.
- Controlled vocabulary sets.
- Example instance library.
- Schema registry.

These ABBs form the basis for solution building blocks in later phases.

---

## 9. Traceability to Stakeholder Concerns

The target data architecture addresses key concerns such as:

- Scientific correctness → explicit semantics & domain extensions.
- DoE for CMC validation → first-class DoE objects.
- Ease of submission → clear schema & tooling.
- Automation → machine-readable schemas.
- Governance → versioning & controlled evolution.
- Traceability → provenance metadata.

A detailed concern-to-requirement mapping is maintained separately.

---

## 10. Next Steps

Following this Phase C definition:

- Refine and validate the conceptual model with CC experts.
- Derive the logical model and JSON Schemas.
- Define controlled vocabularies.
- Produce example datasets from real comparisons.
- Feed requirements into Phase D (Application Architecture).

---

## 11. Open Issues

- Level of detail required for uncertainty budgets.
- Representation of full covariance matrices vs summaries.
- Identifier scheme for comparisons, measurands, and results.
- Strategy for historical data migration.
- Alignment with Digital SI vocabularies.

These issues will be addressed in subsequent iterations.

---
