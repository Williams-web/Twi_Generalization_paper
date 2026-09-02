# Dataset Analysis & Preparation Summary

**Updated:** 2026-09-02

## Dataset sizes
| Dataset | Total | Positive | Negative | Neutral |
|---|---:|---:|---:|---:|
| AfriSenti-Twi | 5,914 | 3,542 | 1,064 | 1,308 |
| AsanteTwiSenti | 4,818 | 2,277 | 1,815 | 726 |

## Duplicate analysis
- AfriSenti duplicate text rows: 474
- AsanteTwiSenti duplicate text rows: 672
- Exact cross-dataset text overlap: 0

## Leakage-controlled test sizes
- AfriSenti test: 888 raw → 782 evaluated
- AsanteTwiSenti test: 949 raw → 754 evaluated

## Experiments
E1–E4 are implemented and saved under `05_Results/`.
