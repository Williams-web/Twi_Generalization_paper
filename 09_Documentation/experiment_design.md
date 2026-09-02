# Experiment Design

## Research Question
How well does a Twi sentiment classifier trained on one dataset generalize to another independently constructed Twi sentiment dataset?

## Hypothesis
Within-dataset performance will be higher than cross-dataset performance, indicating that dataset-specific differences may affect generalization.

## Baseline
TF-IDF + Logistic Regression. TF-IDF uses up to 5,000 features, unigrams and bigrams, min_df=2, max_df=0.95, lowercase=True, and preserves diacritics. Logistic Regression uses lbfgs, max_iter=1000, class_weight=balanced and random_state=42.

## Splits
AfriSenti-Twi: stratified 70/15/15 split, random_state=42, because the local source is a single labeled CSV.
AsanteTwiSenti: official train/dev/test TSV splits supplied with the dataset (3,481 / 388 / 949).

## Leakage control
For each within-dataset evaluation, test texts occurring in the corresponding training set are excluded. The same rule is applied to cross-dataset test sets with respect to their source training set. Raw datasets are never modified.

## Experiments
- E1: AfriSenti → AfriSenti
- E2: AfriSenti → AsanteTwiSenti
- E3: AsanteTwiSenti → AsanteTwiSenti
- E4: AsanteTwiSenti → AfriSenti

## Metrics
Accuracy, macro precision, macro recall, Macro F1, weighted F1, classification reports and confusion matrices.

## Main analysis
For each direction, compare within-dataset Macro F1 with cross-dataset Macro F1. Generalization gap = within-dataset Macro F1 − cross-dataset Macro F1. This measures transfer performance loss; it does not by itself prove why the loss occurs.
