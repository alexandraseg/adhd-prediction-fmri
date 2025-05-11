# adhd-prediction-fmri

## Project Overview

Neuropsychiatric disorders like ADHD often present differently across sexes. Using functional connectivity matrices from fMRI scans and behavioral metadata, this project aims to:

- Predict whether a participant is diagnosed with ADHD (`ADHD_Outcome`)
- Predict the biological sex (`Sex_F`)

## Dataset Structure

The dataset is structured into:

```
root/
├── TRAIN_NEW/
│   ├── TRAIN_FUNCTIONAL_CONNECTOME_MATRICES.csv  
│   ├── TRAIN_QUANTITATIVE_METADATA.csv  
│   ├── TRAIN_CATEGORICAL.csv  
│   └── TRAINING_SOLUTIONS.csv  
├── TEST/
│   ├── TEST_FUNCTIONAL_CONNECTOME_MATRICES.csv  
│   ├── TEST_QUANTITATIVE_METADATA.csv  
│   └── TEST_CATEGORICAL.csv  
├── Data_Dictionary_WiDS2025.xlsx  
├── sample_submission.csv  
└── adhd_model.ipynb  
```

## Insights

Key predictive features included:

- fMRI connectivity features (e.g., `174throw_191thcolumn`)
- SDQ behavioral scores like `SDQ_SDQ_Prosocial`
- Parental assessment scores (e.g., `APQ_P_APQ_P_OPD`)
- Minor contributions from handedness and color vision scores

## Requirements

- Python ≥ 3.8
- pandas, numpy, scikit-learn, imbalanced-learn, xgboost, shap, matplotlib, seaborn
