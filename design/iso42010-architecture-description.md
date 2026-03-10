# Architecture Description  
(ISO/IEC/IEEE 42010 Compliant)

**Title:** <Architecture name>  
**Version:** <x.y>  
**Status:** Draft / Approved  
**Date:** <YYYY-MM-DD>  
**Owner:** <Architecture authority>  

---

## 1. Introduction

### 1.1 Purpose
This document is the **Architecture Description (AD)** for <system/enterprise>,
prepared in accordance with **ISO/IEC/IEEE 42010**.

It identifies stakeholders and concerns, defines viewpoints, and presents views
that collectively describe the architecture.

### 1.2 Scope
Describe the scope of the system/enterprise being architected and what is
in/out of scope for this description.

### 1.3 Conformance
This architecture description conforms to ISO/IEC/IEEE 42010.

---

## 2. System of Interest

### 2.1 Identification
Name and brief description of the system, enterprise, or capability being
architected.

### 2.2 Context
Describe the environment, external systems, organisations, and constraints
that influence the system of interest.

---

## 3. Stakeholders and Concerns

### 3.1 Stakeholders

| ID | Stakeholder | Role / Interest |
|----|-------------|----------------|
S-01 | <name/group> | <interest> |
S-02 | … | … |

### 3.2 Concerns

| ID | Concern | Stakeholders |
|----|---------|--------------|
C-01 | <concern description> | S-01, S-02 |
C-02 | … | … |

---

## 4. Viewpoints

This section defines the viewpoints used in this architecture description.
Each viewpoint addresses specific stakeholder concerns and defines conventions
for constructing views.

### 4.1 <Viewpoint Name>

- **Stakeholders:** <who uses this viewpoint>
- **Concerns addressed:** <concern IDs>
- **Model kinds:** <e.g., process models, data models>
- **Notations:** <e.g., BPMN, UML, ArchiMate>
- **Purpose:** <what questions this viewpoint answers>

(Repeat for each viewpoint, e.g., Business, Data, Application, Technology, Migration, Governance.)

---

## 5. Architecture Views

This section presents the actual architecture views, each conforming to a
defined viewpoint.

### 5.1 View: <View Name>

- **Viewpoint:** <reference to Section 4.x>
- **Concerns addressed:** <concern IDs>
- **Description:** <what this view shows>
- **Artifacts:** <links to diagrams, models, files>

(Repeat for all views.)

---

## 6. Correspondences and Traceability

This section documents correspondences between views and models to ensure
consistency and traceability.

### 6.1 Correspondence Rules
Define rules such as:

- how business elements map to data elements,
- how data elements map to applications,
- how requirements map to architecture elements.

### 6.2 Correspondence Tables

| Source View/Element | Target View/Element | Rule / Rationale |
|--------------------|--------------------|------------------|
<element> | <element> | <rule> |

---

## 7. Architecture Decisions and Rationale

This section captures key architecture decisions and their rationale.

| ID | Decision | Rationale | Affected Views |
|----|----------|-----------|----------------|
AD-01 | <decision> | <why> | <views> |
AD-02 | … | … | … |

---

## 8. Architecture Constraints and Assumptions

### 8.1 Constraints
List technical, organisational, regulatory, or resource constraints.

### 8.2 Assumptions
List assumptions made during architecture development.

---

## 9. Architecture Lifecycle and Change

### 9.1 Version History

| Version | Date | Description |
|---------|------|-------------|
1.0 | <date> | Initial release |
1.1 | <date> | <change> |

### 9.2 Change Management

Describe how changes to this architecture description are proposed, reviewed,
approved, and incorporated.

---

## 10. References

List related documents, standards, models, and external references.

---

## Appendix A – Glossary

Define key terms used in this architecture description.

---

## Appendix B – Architecture Artifacts Index

Index of all files, models, and diagrams referenced in this description.

| ID | Artifact | Type | Location |
|----|----------|------|----------|
A-01 | <name> | <diagram/model> | <path/link> |
A-02 | … | … | … |

---