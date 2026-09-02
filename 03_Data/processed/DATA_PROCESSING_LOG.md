# Data Processing Log

## AfriSenti-Twi
- Raw: 5,996 rows.
- Kept: 5,914 positive/negative/neutral rows.
- Removed: 82 non-target or ambiguous rows.
- Duplicate text rows in processed data: 474.

## AsanteTwiSenti
- Raw/processed: 4,818 rows.
- Official split sizes: 3,481 train, 388 validation, 949 test.
- Duplicate text rows: 672.

## Standardization
Both datasets are stored as `text,label` with labels `positive`, `negative`, `neutral`.

## Leakage control
Raw data are not modified. Test examples whose exact text appears in their corresponding training data are excluded during evaluation.
