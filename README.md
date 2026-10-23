
# Duplicate Report Detection

## Overview

This project identifies potentially duplicate or similar text reports using TF-IDF vectorization and cosine similarity.

## Technologies

- Python
- Pandas
- Scikit-learn
- Google Colab

## Approach

1. Load the JSON dataset.
2. Extract report IDs and text.
3. Identify and exclude empty reports.
4. Convert text into numerical vectors using TF-IDF.
5. Calculate cosine similarity between report pairs.
6. Apply a configurable similarity threshold to identify potentially duplicate reports.

## Threshold Analysis

The model was tested with similarity thresholds of 0.4 and 0.5. Both thresholds returned the same four report pairs in the observed results.

The R2–R3 pair had a similarity score of 0.315, so it was excluded at both thresholds.

## Limitations

TF-IDF measures textual similarity, which does not always indicate that two reports describe the same incident. The threshold should be evaluated using manually verified examples to balance false positives and missed duplicates.
