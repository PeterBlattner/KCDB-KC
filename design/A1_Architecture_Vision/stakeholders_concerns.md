## X. Stakeholder Concerns

The following stakeholder concerns have been identified for the
"Harmonised Digital Model for KCDB Comparison Reporting and CMC Validation"
architecture initiative. They will guide scope, priorities, and trade-offs
in subsequent architecture phases.

Each concern is assigned an identifier for traceability.

---

### C-01 -- Scientific correctness across domains
**Stakeholders:** Consultative Committees, domain experts  
**Concern:**  
The data model must correctly represent the scientific meaning of
measurements, uncertainties, reference values, and DoEs in all relevant
fields (physics and chemistry), without oversimplification.

**Implication:**  
Strong involvement of domain experts; core + extension strategy.

---

### C-02 -- Support for DoE-based CMC validation
**Stakeholders:** CMC review bodies, BIPM  
**Concern:**  
The model must explicitly support Degrees of Equivalence and their
uncertainties in a form that enables automated or semi-automated
CMC validation.

**Implication:**  
DoE and uncertainty become first-class concepts in the core model.

---

### C-03 -- Harmonisation vs. domain diversity
**Stakeholders:** CCs, NMIs  
**Concern:**  
A common model is needed, but must not force unnatural structures on
domains with specific practices.

**Implication:**  
Minimal core, governed extensions per domain.

---

### C-04 -- Ease of submission for NMIs/DIs
**Stakeholders:** NMIs, pilot laboratories  
**Concern:**  
Submitting data should not significantly increase workload or require
specialised IT expertise.

**Implication:**  
Clear schemas, templates, tooling, and conversion from common formats.

---

### C-05 -- Backward compatibility and legacy data
**Stakeholders:** BIPM, CCs  
**Concern:**  
Existing KCDB records and historical comparisons must remain usable,
and transition to the new model should not disrupt operations.

**Implication:**  
Versioning strategy, coexistence period, possible migration tools.

---

### C-06 -- Automation and machine actionability
**Stakeholders:** BIPM IT, data users  
**Concern:**  
The model should enable automated validation, ingestion, analysis,
and reuse of KC data without manual intervention.

**Implication:**  
Strict schemas, controlled vocabularies, explicit semantics.

---

### C-07 -- Governance and controlled evolution
**Stakeholders:** BIPM, CC leadership  
**Concern:**  
Changes to the model must be transparent, controlled, and agreed,
avoiding fragmentation or uncontrolled forks.

**Implication:**  
Formal change process, versioning, architecture governance.

---

### C-08 -- Transparency and traceability
**Stakeholders:** Reviewers, auditors, NMIs  
**Concern:**  
It must be possible to trace published results and DoEs back to
submitted data, methods, assumptions, and versions.

**Implication:**  
Provenance, immutable versions, computation metadata.

---

### C-09 -- Interoperability with digital metrology standards
**Stakeholders:** BIPM, digital SI initiatives  
**Concern:**  
The model should align with existing or emerging standards for
quantities, units, vocabularies, and FAIR data.

**Implication:**  
Reuse of established vocabularies (e.g., units, quantities) where possible.

---

### C-10 -- Security and access control
**Stakeholders:** BIPM IT, participants  
**Concern:**  
Submissions, reviews, and unpublished data must be protected against
unauthorised access or modification.

**Implication:**  
Authentication, authorisation, and role concepts in services.

---

### C-11 -- Long-term sustainability
**Stakeholders:** BIPM management  
**Concern:**  
The solution must be maintainable over decades, independent of
specific tools or vendors.

**Implication:**  
Open standards, simple core, strong documentation.

---

### C-12 -- Measurable value and adoption
**Stakeholders:** All  
**Concern:**  
The initiative must demonstrate clear benefits and be adopted by
the community, not remain a theoretical exercise.

**Implication:**  
Early pilots, visible wins, strong communication.

---

These concerns will be used to:
- define scope and priorities,
- derive architecture principles,
- assess options and trade-offs,
- and evaluate success.