# Baseline Inventory of Observations and Hypotheses  
## KCDB Reference Data Architecture – Phase C

**Version:** 0.1  
**Status:** Draft  
**Date:** 2025-12-22  
**Owner:** BIPM / KCDB Architecture Working Group  

---

## 1. Purpose

This document captures the **baseline inventory** of observations and hypotheses
identified during Phase C (Data Architecture) of the KCDB Reference Data Architecture
initiative.

The inventory reflects:
- current practices found in KC and SC reports,
- assumptions that require validation,
- and sources of variability that must be addressed by the target data model.

Each item is assigned a stable identifier (**INV-nn**) and grouped by category.

---

## 2. Inventory Table

| ID | Kind | Statement | Category | Examples |
|----|------|-----------|----------|----------|
| INV-01 | Hypothesis | A KC/SC can support more than one CMC claims | KC/SC ↔ CMC relationships | |
| INV-02 | Hypothesis | A CMC claim can be supported by more than one KC/SC | KC/SC ↔ CMC relationships | |
| INV-03 | Hypothesis | All KCs have one or more KCRV | Reference values (KCRV/CRV) and variants | APMP.AUV.A-K5; AFRIMETS.AUV.V-K5; APMP.EM-K12; CCM.F-K23; APMP.L-K3 |
| INV-04 | Hypothesis | All KCs have one or more DOE | Degrees of Equivalence and coverage metrics | APMP.AUV.A-K5; AFRIMETS.AUV.V-K5; APMP.EM-K12; CCM.F-K23; APMP.L-K3 |
| INV-05 | Observation | Some SC have one or more CRV | Reference values (KCRV/CRV) and variants | EURAMET.EM-S36; GULFMET.EM-S8; APMP.L-S5.2.n01; CCQM-K144; APMP.T-S16; AFRIMETS.L-S6.1.n03; CCT-K9 |
| INV-06 | Observation | Some SC have one or more DOE | Degrees of Equivalence and coverage metrics | EURAMET.EM-S36 |
| INV-07 | Observation | Some KCs are linked to other KCs | Linking and networks of comparisons | SIM.M.M-K6; CCT-K9.2 |
| INV-08 | Hypothesis | All DOEs are associated with a U(DOE) | Degrees of Equivalence and coverage metrics | |
| INV-09 | Observation | Some KC/SC are reporting the mutual/unilateral DOEs | Degrees of Equivalence and coverage metrics | CCT-K8; CCT-K3; CCPR-K1.a; SIM.EM.RF-K5.b.CL |
| INV-10 | Observation | Some KC/SC have more than one measurand | Measurand complexity | EURAMET.EM-S36 |
| INV-11 | Hypothesis | Some KC measurands have a corresponding CMC measurand | KC/SC ↔ CMC relationships | |
| INV-12 | Observation | Some KC/SC are referring to KCRV of other KC/SC | Linking and networks of comparisons | SIM.M.M-K6; CCT-K9.2; CCT-K3.1 |
| INV-13 | Observation | Some measurands are scalars | Measurand complexity | BIPM.RI(II)-K1.Pa-231 |
| INV-14 | Observation | Some measurands are vectors (e.g. spectral) | Measurand complexity | APMP.AUV.A-K5 |
| INV-15 | Observation | Some measurands are complex | Measurand complexity | CCEM.RF-K23.F |
| INV-16 | Observation | Some measurands are complex vectors | Measurand complexity | CCEM.RF-K5.c.CL |
| INV-17 | Hypothesis | Some measurement conditions in the KC/SC are the same as in the related CMC | KC/SC ↔ CMC relationships | |
| INV-18 | Observation | Some KC/SC calculate specific-artefact-based CRVs only | Reference values (KCRV/CRV) and variants | EURAMET.EM-S36; CCM.FF-K2.2011; APMP.AUV.V-S1; CCEM.RF-K26; CCEM.RF-K23.F |
| INV-19 | Observation | Some SC are reporting En factors | Degrees of Equivalence and coverage metrics | APMP.L-S5.2.n01; SIM.M.F-S6; APMP.M.P-S7; APMP.T-S16; COOMET.EM-S21 |
| INV-20 | Observation | In some SC the CRV is defined by the pilot laboratory | Reference values (KCRV/CRV) and variants | COOMET.M.F-S1 |
| INV-21 | Observation | Some SC are only showing consistency between participants | Reference values (KCRV/CRV) and variants | SIM.M.M-S18; SIM.QM-S3 |
| INV-22 | Observation | Some SC are linked to other KCs | Linking and networks of comparisons | APMP.M.P-S7 |
| INV-23 | Observation | Different methods exist to calculate the DOE (e.g. NIST decision tree) | Degrees of Equivalence and coverage metrics | CCQM-K155; SIM.QM-S11 |
| INV-24 | Observation | Some KC/SC provide guidance on the CMC claims | KC/SC ↔ CMC relationships | CCQM-K155; SIM.QM-S11; EURAMET.L-S2.3.n02 |
| INV-25 | Observation | Some KC report a limit in the DOE table | Degrees of Equivalence and coverage metrics | CCQM-K133 |
| INV-26 | Observation | Some KC report minimal relative expanded uncertainties (UminCMC) consistent with the KCRV | KC/SC ↔ CMC relationships | CCQM-K170 |
| INV-27 | Observation | Some KC/SC calculate artefact-"class"-based CRVs only | Reference values (KCRV/CRV) and variants | AFRIMETS.AUV.V-K5 |
| INV-28 | Observation | Some KC/SC report DOEs for more than one external parameter | Degrees of Equivalence and coverage metrics | APMP.EM-K12 |
| INV-29 | Hypothesis | All U(DOE)s are reported at a confidence level of 95% | Degrees of Equivalence and coverage metrics | |
| INV-30 | Observation | Some uncertainty distributions of DOEs are asymetrical (U_pos <> U_neg) | Degrees of Equivalence and coverage metrics | CCM.D-K2 |
| INV-31 | Observation | Not all KCs have DOE graphs and tables published directly at KCDB | Publication and availability | CCEM.RF-K5.c.CL |
| INV-32 | Observation | Some KC reports are not available through the KCDB webpage | Publication and availability | CCPR-K3.a |
| INV-33 | Hypothesis | All KC/SC have a unique identifier (e.g. "CCPR-K3.a") | Publication and availability | |
| INV-34 | Hypothesis | For CMC review, DOE and U(DOE) are not sufficient; associated NMI uncertainty is also needed | KC/SC ↔ CMC relationships | |
| INV-35 | Observation | Some DOEs are primary reported as a function of a parameter and not for different NMIs | Degrees of Equivalence and coverage metrics | SIM.M.FF-K6.2017 |
| INV-36 | Observation | Some KC are adding artifact name/type when reproting DOE of an NMI | Degrees of Equivalence and coverage metrics | CCQM-K113 |

---

## 3. Category Overview

- **KC/SC ↔ CMC relationships:** INV-01, 02, 11, 17, 24, 26, 34  
- **Reference values (KCRV/CRV) and variants:** INV-03, 05, 18, 20, 21, 27  
- **Degrees of Equivalence and coverage metrics:** INV-04, 06, 08, 09, 19, 23, 25, 28, 29, 30, 35, 36  
- **Measurand complexity:** INV-10, 13, 14, 15, 16  
- **Linking and networks of comparisons:** INV-07, 12, 22  
- **Publication and availability:** INV-31, 32, 33  

---

## 4. Usage in Phase C

This inventory is used to:

- derive **data requirements**,
- identify **hypotheses to validate** with stakeholders,
- stress-test the canonical conceptual model,
- and justify architectural choices such as:
  - core + extensions,
  - first-class DoE objects,
  - flexible measurand modeling,
  - explicit provenance and linking.

Each INV item is traceable to requirements (DR-xx) and model elements.

---

## 5. Next Steps

- Validate hypotheses (INV-xx marked as Hypothesis) with CC and CMC experts.
- Map INV items to conceptual entities and relationships.
- Refine requirements and update this inventory as needed.

---
