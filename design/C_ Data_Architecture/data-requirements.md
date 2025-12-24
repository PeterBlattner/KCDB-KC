# Data Requirements  
## KCDB Reference Data Architecture (TOGAF Phase C)

**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  
**Owner:** BIPM / KCDB Architecture Working Group  
**Author:** genAI prompted by Peter B.

---

## 1. Purpose

This document captures **data requirements** derived from Phase C baseline inventory
(observations and hypotheses) for the KCDB Reference Data Architecture initiative.

The requirements are structured to support:

- Harmonised reporting of key/supplementary comparisons (KC/SC),
- Publication and traceability in/with KCDB,
- Validation of CMC claims using **Degrees of Equivalence (DoE)** and associated uncertainty.

Each requirement is assigned a stable identifier (**DR-xx**) and is traceable to the
baseline inventory items (**INV-nn**).

---

## 2. Scope

### In Scope

- Comparison metadata, measurands, participants.
- Reported results, reference values (KCRV/CRV), DoEs and uncertainties.
- Correlation/covariance information relevant to DoE uncertainty.
- Links between comparisons and links between KC/SC and CMC claims.
- Publication/availability metadata and provenance/versioning.

### Out of Scope (initially)

- Raw measurement time series.
- Internal laboratory information systems (LIMS) structures.
- Full specification of numerical algorithms (only inputs/outputs + provenance).

---

## 3. Baseline Inventory Traceability

**Inventory Items (INV-01 … INV-34)** refer to the numbered list collected in Phase C.

---

## 4. Data Requirements

### 4.1 Identity, Versioning, and Provenance

**DR-01 — Unique identifiers**  
The model shall support unique, persistent identifiers for:

- comparisons (KC/SC),
- measurands,
- participants,
- reported results,
- reference values,
- DoEs,
- and publication packages.  
**Traceability:** INV-33

**DR-02 — Versioning of submitted and published data**  

The model shall support versioning of:
- participant submissions,
- computed reference values and DoEs,
- publication packages,
and shall allow immutable published versions.  
**Traceability:** INV-31, INV-32

**DR-03 — Provenance for derived data**  
The model shall capture provenance for derived objects (e.g., KCRV/CRV, DoE),
including:

- input dataset versions,
- method/algorithm identifier,
- parameterization/assumptions (incl. correlation assumptions),
- timestamp and responsible party.  
**Traceability:** INV-23, INV-12, INV-31, INV-32

---

### 4.2 Comparison Structure and Measurands

**DR-04 — Multiple measurands per comparison**  
The model shall support one or more measurands per KC/SC.  
**Traceability:** INV-10

**DR-05 — Measurand value structure**  
The model shall support measurands where reported values and/or DoEs are:

- scalar,
- vector (e.g., spectral),
- complex,
- complex vector.  
**Traceability:** INV-13, INV-14, INV-15, INV-16

**DR-06 — Parameterised measurands / external parameters**  
The model shall support reporting results and DoEs as a function of one or more
external parameters (e.g., current, frequency), including the parameter definition,
units, and sampling points.  
**Traceability:** INV-28

---

### 4.3 Participant Results (Submissions)

**DR-07 — Participant reported results**  
The model shall support participant-submitted results for each measurand, including:

- value(s),
- unit(s),
- uncertainty statement,
- method summary (optional).  
**Traceability:** INV-34, INV-10, INV-13–INV-16

**DR-08 — Participant uncertainty is explicitly representable**  
The model shall represent the participant’s stated uncertainty explicitly and
independently of DoE uncertainty.  
**Traceability:** INV-34

---

### 4.4 Reference Values (KCRV/CRV) and Variants

**DR-09 — Reference values are first-class objects**  
The model shall represent reference values as first-class objects linked to a
measurand, including value(s), unit(s), and uncertainty statements.  
**Traceability:** INV-03, INV-05

**DR-10 — Support multiple reference value types and provenance**  
The model shall support reference value types, including at minimum:

- KCRV,
- CRV (supplementary comparisons),
- artefact-specific CRV,
- artefact-class-based CRV,
- external/reference-from-other-comparison.  
Provenance shall identify the defining party and method.  
**Traceability:** INV-03, INV-05, INV-12, INV-18, INV-20, INV-27

**DR-11 — Comparisons may reference reference values from other comparisons**  
The model shall support explicit linkage where a KC/SC refers to a KCRV/CRV defined
in another KC/SC, including reference type and rationale.  
**Traceability:** INV-12, INV-07, INV-22

**DR-12 — Support “consistency-only” outcomes**  
The model shall support cases where supplementary comparisons present participant
consistency statements without defining a CRV in the traditional sense, while still
capturing the methodological basis and outputs.  
**Traceability:** INV-21

---

### 4.5 Degrees of Equivalence (DoE) and Coverage Metrics

**DR-13 — DoE is first-class and linked to participant and measurand**  
The model shall represent DoE as a first-class object for a participant and
measurand, linked to the applicable reference value.  
**Traceability:** INV-04, INV-06

**DR-14 — DoE variants (unilateral/mutual)**  
The model shall support reporting:

- unilateral DoE,
- mutual DoE,
including a clear designation of the DoE type and definition used.  
**Traceability:** INV-09

**DR-15 — DoE uncertainty statement**  
The model shall support an uncertainty statement associated with each DoE
(e.g., u(DoE), U(DoE), U_neg(DOE), U_pos(DOE), k, coverage probability), including cases where only partial
information is available.  
**Traceability:** INV-08, INV-29, INV-30

**DR-16 — DoE computation method metadata**  
The model shall capture the method used to calculate DoEs (e.g., named method,
decision-tree approach), including references to documentation.  
**Traceability:** INV-23

**DR-17 — Optional limits and qualifiers in DoE tables**  
The model shall support reporting table-level or row-level limits/constraints
(e.g., bounds, thresholds, notes) as published in DoE tables.  
**Traceability:** INV-25

**DR-18 — Coverage metrics (e.g., En)**  
The model shall support optional coverage/consistency metrics associated with a
participant and measurand (e.g., En, z-score), including parameters used.  
**Traceability:** INV-19

**DR-19 — Reporting minimal uncertainties (UminCMC) where provided**  
The model shall support reporting minimal relative expanded uncertainties (UminCMC)
consistent with a proposed KCRV/CRV, including associated assumptions.  
**Traceability:** INV-26

---

### 4.6 Correlation / Covariance

**DR-20 — Correlation model representation**  
The model shall support representation of correlation/covariance information
relevant to reference value and DoE uncertainty, including:

- none / assumed zero,
- pairwise correlations,
- matrix forms,
and scope (which results/measurands).  
**Traceability:** INV-23, INV-15–INV-16 (complex), INV-08

---

### 4.7 Linking Between Comparisons

**DR-21 — Comparison linking**  
The model shall support explicit links between comparisons (KC↔KC, SC↔KC, etc.)
including link type (e.g., uses reference from, related to, continuation) and
rationale.  
**Traceability:** INV-07, INV-22, INV-12

---

### 4.8 KC/SC ↔ CMC Relationships (Evidence Model)

**DR-22 — Many-to-many KC/SC to CMC claim relationships**  
The model shall support the relationship that:

- a KC/SC can support multiple CMC claims, and
- a CMC claim can be supported by multiple KCs/SCs.  
**Traceability:** INV-01, INV-02

**DR-23 — Measurand mapping between KC/SC and CMC**  
The model shall support mapping between KC/SC measurands and corresponding CMC
measurands where such a relationship exists, including mapping type and rationale
(exact match, partial match, derived).  
**Traceability:** INV-11

**DR-24 — Conditions mapping between KC/SC and CMC**  
The model shall support capturing whether measurement conditions in KC/SC are the
same as or differ from those in the linked CMC claim, including the relevant
conditions set.  
**Traceability:** INV-17

**DR-25 — CMC guidance notes (optional)**  
The model shall support storing qualitative guidance notes associated with CMC
evaluation (e.g., interpretive guidance), including attribution and scope.  
**Traceability:** INV-24

**DR-26 — Evidence sufficiency**  
The model shall support representing the fact that DoE and U(DoE) alone may be
insufficient for CMC review and that participant/NMI uncertainty information may
also be required as evidence inputs.  
**Traceability:** INV-34

---

### 4.9 Publication and Availability

**DR-27 — Availability metadata**  
The model shall support metadata indicating whether:

- DoE tables/graphs are available via KCDB,
- reports are available via KCDB or externally,
including links and status codes.  
**Traceability:** INV-31, INV-32

---

## 5. Assumptions and Hypotheses to Validate

The following hypotheses require validation with stakeholders and/or corpus evidence:

- H-01: All KCs have one or more KCRVs. (INV-03)
- H-02: All KCs have one or more DoEs. (INV-04)
- H-03: All DoEs have associated U(DoE). (INV-08)
- H-04: All U(DoE) are reported at 95% confidence. (INV-29)
- H-05: All KC/SC have unique identifiers. (INV-33)
- H-06: Some KC measurands correspond directly to CMC measurands. (INV-11)
- H-07: Some KC/SC conditions match CMC conditions. (INV-17)

Validated outcomes shall be recorded as architecture decisions and may lead to
updates in requirement statements or optionality.

---

## 6. Open Issues

- Level of detail required for uncertainty budgets (components vs summary only).
- Identifier scheme and canonical URI pattern.
- Strategy for representing complex-valued uncertainties and correlations.
- Migration and completeness strategy for legacy comparisons.

---

## 7. Next Steps

- Review and confirm requirements with CC and CMC stakeholder representatives.
- Map DR-xx requirements to conceptual entities (PlantUML) and schema elements.
- Define controlled vocabularies and enumeration sets.
- Produce example instances representing key variability cases.
- Feed validated requirements into Phase D (Application Architecture) and Phase E (Solutions).

---
