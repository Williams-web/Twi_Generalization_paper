# Dataset Compatibility Audit

## AfriSenti-Twi
- Raw source: `03_Data/raw/afrisenti_twi/labeledl_twi_tweets.csv`
- Raw records: **5,996**
- Sentiment records retained: **5,914**
- Retained labels: positive, negative, neutral
- Raw non-target/ambiguous rows removed: **82**
- Platform: X/Twitter
- Language: Twi subset
- Split used here: stratified 70/15/15, random_state=42

## AsanteTwiSenti
- Raw source: `03_Data/raw/asantetwi/train.tsv`, `dev.tsv`, `test.tsv`
- Records: **4,818**
- Split sizes: **3,481 / 388 / 949**
- Labels: positive, negative, neutral
- Language variety: Asante Twi
- Platform/domain: social-media text from X/Twitter

## Compatibility
Both datasets use the same three sentiment labels and social-media domain, but differ in collection/annotation procedures and class distributions. Exact text overlap across the two processed datasets was checked and found to be **0**.

## Duplicate control
Processed text duplicate rows: AfriSenti **474**, AsanteTwiSenti **672**. To reduce exact-text train/test leakage, evaluation examples whose exact text occurs in the corresponding training set are excluded. Raw data remain unchanged.
