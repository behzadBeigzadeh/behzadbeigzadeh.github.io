---
layout: page
title: Privacy-Preserving Clinical AI via Federated Learning
description: A clinical AI pipeline for note de-identification, structured extraction, and federated readmission prediction.
importance: 1
category: research
github: https://github.com/behzadBeigzadeh/privacy-preserving-clinical-ai-federated-learning
---

This project brings clinical text processing and federated learning into one reproducible pipeline. It removes personal identifiers from notes, extracts structured clinical information, and predicts 30-day hospital readmission across three simulated hospital sites.

### What the project implements

- Rule-based de-identification that replaces personal identifiers while preserving the clinical text.
- Structured extraction of diagnoses, medications, allergies, smoking status, and numeric values, with handling for negated conditions and stopped medications.
- A NumPy logistic-regression model trained with sample-weighted Federated Averaging (FedAvg) on 120 synthetic records, with local and centralized models for comparison.
- A separate client-level differential-privacy prototype using update clipping, Gaussian noise, and privacy-budget accounting.

### Reported results

The repository reports these scores on 30 public synthetic validation cases:

| Task | Score |
| --- | ---: |
| De-identification | 15 / 15 |
| Structured extraction | 15 / 15 |
| Readmission prediction | 7.88 / 10 |
| Total | 37.88 / 40 |

The reported readmission ROC-AUC is **0.7986**.

### Scope and limitations

These scores describe development performance on a small public synthetic dataset. They do not establish clinical effectiveness. Training runs as a local simulation, secure aggregation is not implemented, and the final predictions use standard FedAvg rather than differential privacy.

### Code and reproducibility

[Source code and setup](https://github.com/behzadBeigzadeh/privacy-preserving-clinical-ai-federated-learning) · [Experiment report](https://github.com/behzadBeigzadeh/privacy-preserving-clinical-ai-federated-learning/blob/main/REPORT.md)

The repository includes the data, training and prediction scripts, evaluator, schemas, and tests needed to reproduce the experiment. Tests cover text processing, FedAvg weighting, privacy accounting, and prediction independence from validation labels.
