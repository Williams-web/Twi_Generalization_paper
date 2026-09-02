# Research Log

## 2026-09-01 — Dataset preparation
- Obtained AfriSenti-Twi and AsanteTwiSenti source files.
- Standardized both datasets to `text,label`.
- Retained positive, negative and neutral sentiment labels.
- Documented excluded AfriSenti non-target/ambiguous labels.
- Performed class-distribution, text-length, missing-value, duplicate and cross-dataset overlap checks.

## 2026-09-02 — Methodology and baseline
- Corrected raw dataset directory naming.
- Corrected documentation inconsistencies in dataset counts and split descriptions.
- Added reproducible stratified splits.
- Added exact-text train/test leakage control.
- Implemented TF-IDF + Logistic Regression experiments E1–E4.
- Saved metrics, classification reports, confusion matrices and error files.

## Next
- Inspect E2–E4 results.
- Perform focused error analysis.
- Complete literature review and paper.
