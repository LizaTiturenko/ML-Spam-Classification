# ML Assignment - Spam Classification

## Overview
This project implements a complete Machine Learning pipeline for SMS spam detection.
The goal is to automatically classify SMS messages as **spam** or **ham** (not spam).

## Dataset
- **Name:** SMS Spam Collection Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- **Size:** 5,572 SMS messages labeled as spam or ham
- **Split:** 80% training (4,457 messages) / 20% testing (1,115 messages)

## Algorithm
**Naive Bayes** - implemented from scratch (no sklearn for the core algorithm)

How it works:
1. During training, the model learns which words appear most often in spam vs ham
2. For each new message, it calculates the probability of spam and ham
3. It picks the class with the higher probability

## Feature Engineering
- **TF-IDF with Unigrams + Bigrams** (`ngram_range=(1,2)`, `max_features=7000`)
- Special preprocessing: replacing phone numbers, money amounts, and URLs with tokens

## Results

| Metric | Score |
|--------|-------|
| F1 Score (spam) | 0.9220 |
| Accuracy | 98% |
| Precision | 98% |
| Recall | 87% |
| False Positive Rate | 0.1% |

## Bonus Sections
- **6A:** Grid Search with 5-Fold Cross Validation (45 total runs)
- **6B:** Feature Engineering experiments (Unigrams vs Bigrams vs Preprocessing)
- **6C:** Hyperparameter experiments (alpha and min_df)
- **6D:** Imbalanced data handling (Oversampling, Undersampling, SMOTE)
- **6E:** Special quality evaluation (False Positive Rate, Confusion Matrix)
- **6F:** Explainability (Top spam/ham words, local message analysis)
- **6G:** Summary of all experiments

## Best Parameters Found
| Parameter | Value |
|-----------|-------|
| Feature Engineering | TF-IDF Unigrams + Bigrams |
| max_features | 7000 |
| alpha | 0.1 |
| min_df | 1 |
| Sampling | None |
| Best Average F1 | 0.9529 |

## Project Structure
```
ML_Assignment_Spam_Classification.ipynb  # Main notebook with all code and results
README.md                                # This file
```

## Student
- **Name:** Liza Titurenko
- **Course:** Machine Learning, Holon Institute of Technology

## AI Assistance
- **Tool:** Claude AI (claude.ai)
- **Purpose:** Help with code structure, explanations, and debugging
