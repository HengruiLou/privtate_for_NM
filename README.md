# Restricted (Private) Datasets — Anonymized Inventory and Access Guidance (pv-CE42)

This repository provides an **anonymized inventory** of the restricted (private) datasets used in the ProgSeer study, together with **clear access constraints** and a **standard request pathway**.  
Because the underlying data consist of **human patient-derived pathology slides** (whole-slide images) and **linked clinical outcomes**, they **cannot be redistributed** in this repository. No raw WSIs, no patient-level clinical tables, and no re-identifiable metadata are hosted here.

## 1) What is restricted and why

The restricted datasets include:
- **Raw whole-slide histopathology images (WSIs)** (e.g., H&E-stained diagnostic slides; gigapixel images).
- **Linked clinical variables and outcomes** (e.g., follow-up time, event indicators, recurrence/metastasis where applicable).
- **Site-specific acquisition metadata** (e.g., scanner, staining batch, local identifiers).

These data are governed by institutional ethics approvals, data-use agreements, and local regulations related to human subject research and privacy. Accordingly, they are made available **only under controlled access** and are **not publicly distributed**.

## 2) Anonymized cohort inventory (summary statistics)

The table below summarizes cohort composition and basic demographics/outcomes by cancer type and site code, corresponding to the multicenter private dataset used in the study.

> Conventions:  
> - **OS** = overall survival (months).  
> - “/” indicates the variable was not collected for that cohort.  
> - Site codes refer to participating medical centers and are intentionally anonymized for double-blind peer review.

| Cancer | Site code | Slides | Patients | Avg. age | Female | Male | Sex NA | Avg. OS (months) |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| HCC (hepatocellular carcinoma) | ZJUFH | 1,502 | 1,502 | 63.07 | 345 | 1,021 | 136 | 56.25 |
|  | ZJUSH | 219 | 219 | 65.95 | 26 | 188 | 5 | 57.46 |
|  | YWCH | 108 | 108 | 67.57 | 26 | 81 | 1 | 53.88 |
|  | GDPH | 162 | 156 | / | / | / | / | 67.51 |
| COAD (colon adenocarcinoma) | ZJUFH | 1,556 | 1,499 | 49.88 | 652 | 829 | 18 | 65.05 |
|  | YWCH | 231 | 231 | 61.69 | 96 | 135 | 0 | 78.64 |
|  | GDPH | 572 | 572 | 62.47 | 295 | 277 | 0 | 59.45 |
| PTC (papillary thyroid carcinoma) | ZJUFH | 773 | 773 | 41.36 | 489 | 284 | 0 | 67.48 |
|  | TZCH | 176 | 176 | 50.77 | 93 | 83 | 0 | 95.86 |
| TNBC (triple-negative breast cancer) | ZJUFH | 1,316 | 1,316 | 51.03 | 1,311 | 5 | 0 | 63.45 |
|  | SDCH | 101 | 101 | 52.89 | 101 | 0 | 0 | 62.31 |
| BLCA (bladder carcinoma) | ZJUFH | 304 | 304 | 61.78 | / | / | 304 | 60.78 |
|  | QDUH | 472 | 472 | 67.08 | 107 | 362 | 3 | 53.98 |
| OSCC (oral squamous cell carcinoma) | ZJUFH | 440 | 440 | 63.59 | 53 | 387 | 0 | 70.47 |
|  | QDUH | 346 | 346 | 65.96 | 46 | 298 | 2 | 84.35 |
| LUAD (lung adenocarcinoma) | ZJUFH | 119 | 119 | 60.87 | 49 | 70 | 0 | 62.78 |
|  | GDPH | 621 | 621 | 61.70 | 216 | 404 | 1 | 70.45 |

## 3) Endpoint definitions (as used in the study)

The prognostic labels are derived from long-term follow-up and are constructed using **two non-overlapping time windows**:
- **Adverse-outcome group**: patients who experienced death or recurrence within **3 years**.
- **Favorable-outcome group**: patients who remained event-free for **more than 5 years**.
- **Intermediate follow-up** (3–5 years): excluded to reduce ambiguity due to potential confounding by treatment heterogeneity, comorbidities, and non-disease factors.

Time-to-event analyses (e.g., Cox regression and Kaplan–Meier/log-rank testing) use:
- **T**: event or last follow-up time
- **E**: event indicator (censoring where E = 0)

## 4) Data modalities and structure (high-level)

Although the underlying files are not redistributed here, the restricted dataset used in this study consists of:
- **H&E-stained WSIs** stored in standard pyramidal whole-slide formats, scanned at routine clinical magnifications.
- **De-identified clinical outcome fields** required for survival analysis and stratification (event indicator, follow-up time), and limited basic demographics where available (e.g., age, sex), recorded at the patient level.

All modeling and evaluation were performed on **patient-level splits** to avoid leakage.

## 5) Access constraints and request pathway

### Controlled access
These restricted datasets are **not publicly downloadable**. Access is controlled to protect patient privacy and to comply with institutional governance and applicable regulations.

### Request procedure
Qualified researchers may request access **through appropriate institutional channels**. Requests are evaluated on a case-by-case basis and typically require:
- A brief research proposal and intended use.
- Evidence of local IRB/ethics approval (or exemption) at the requesting institution.
- A signed data-use agreement (DUA) and compliance commitments (e.g., no re-identification, no redistribution).

To preserve double-blind review, the contact point and formal instructions for submitting requests are provided to editors via the manuscript submission system and will be made available in the non-anonymized public record upon publication/acceptance.

## 6) Ethical and privacy safeguards (summary)

- Retrospective multicenter analysis using de-identified archival pathology materials and associated clinical outcomes.
- Data are handled under institutional approvals and governance frameworks.
- No patient identifiers are included in any shared public artifacts.
- This repository intentionally contains **only aggregated statistics and procedural guidance**.

## 7) Citation

If referencing this inventory in correspondence or review, please cite it as:
- “Restricted (Private) Datasets — Anonymized Inventory and Access Guidance (pv-CE42), ProgSeer study.”
