# Quality-Adaptive Deep Learning Approach for Oral Lesion Detection in Teledentistry

## Overview

This research project investigates the robustness of deep learning models for oral lesion classification under variations in image quality.

The initial classification task focuses on two categories:
- Oral Leukoplakia
- Oral Squamous Cell Carcinoma (OSCC)

The study evaluates whether degradation-aware training can improve classification performance when images are affected by simulated blur, noise, darkness, and JPEG compression.

## Research Objectives

1. Develop a baseline oral lesion classification model.
2. Evaluate the impact of simulated image-quality degradation on classification performance.
3. Investigate degradation-aware training as a strategy for improving robustness.
4. Compare baseline and degradation-aware models under different test conditions.
5. Examine model predictions using appropriate evaluation metrics and, where implemented, Grad-CAM.

## Dataset

The experiments use the NDB-UFES oral cancer and leukoplakia dataset.

Current dataset summary:
- Total images: 237
- Patients: 69
- Leukoplakia images: 146
- OSCC images: 91

Patient-level cross-validation is used to reduce the risk of patient overlap between training and evaluation folds.

The original dataset is not included in this repository. Access and use must comply with its licensing and privacy requirements.

## Methodology

The planned experimental workflow includes:

1. Image preprocessing and dataset validation.
2. Patient-level five-fold cross-validation.
3. Baseline model training.
4. Controlled image degradation at multiple severity levels.
5. Degradation-aware model training.
6. Evaluation on clean and degraded images.
7. Comparison using metrics such as ROC-AUC, sensitivity, specificity, and macro-F1.

## Preliminary Findings

Initial single-seed experiments suggest that degradation-aware training may improve robustness to certain simulated degradations, particularly blur, noise, and darkness.

The observed effects vary by degradation type. JPEG robustness showed little difference between the models in the initial comparison.

These findings are preliminary and require further validation using multiple random seeds, confidence intervals, and appropriate control experiments.

No clinical validation is claimed.

## Repository Contents

- `oral.ipynb` — initial experimental notebook containing the implemented workflow.

Additional source files, experiment configurations, and evaluation summaries may be added as the implementation develops.

## Limitations

- The dataset is relatively small.
- Image degradations are simulated rather than collected from real-world teledentistry settings.
- Initial comparisons use a single training seed.
- Generalization to unseen degradation types remains to be evaluated.
- The current approach investigates degradation-aware training; it does not yet establish a genuinely adaptive architecture.

## Intended Use

This project is an academic research prototype. It is not intended to provide autonomous clinical diagnoses or replace professional dental assessment.
