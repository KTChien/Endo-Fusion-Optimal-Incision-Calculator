# Endo-Fusion-Optimal-Incision-Calculator

Code and derived parametric data for ANN-based incision distance prediction in lumbar endo-fusion planning.

This repository provides the Google Colab notebooks, de-identified derived measurement datasets, model comparison results, and pretrained model files used in the manuscript:

**_Optimizing incision placement for maximum disc and endplate preparation in lumbar endo-fusion using parametric modeling, genetic algorithms, and machine learning_**

Submitted to *Digital Health*.

The provided datasets contain only fully anonymized derived parametric measurements and do not include any identifiable patient imaging data.
---

## Repository Structure

    repo/
    ├── code/
    ├── data/
    ├── results/
    ├── models/
    │   └── saved_models_2026/
    └── README.md

---

## Repository Contents

### Code

- `code/Incision_&_Area_2026_04_28_journal_revision_final_en(Colab).ipynb`  
  Main notebook for model training, validation, and prediction.

- `code/Inter_rater_reliability_results_en(Colab).ipynb`  
  Notebook for inter-rater reliability analysis.

---

### Data

- `data/Disc_Training_Validation.xlsx`  
  Development dataset for model training and internal validation.

- `data/Disc_Test.xlsx`  
  Independent external validation dataset.

- `data/inter_rater_raw_measurements.xlsx`  
  Raw measurements used for inter-rater reliability analysis.

---

### Results

- `results/model_comparison_updated.xlsx`  
  Summary of model performance and comparison.

- `results/inter_rater_summary.xlsx`  
  Inter-rater reliability results (ICC, Bland–Altman, statistical tests).

---

### Models

- `models/saved_models_2026/`  
  Final trained models and preprocessing bundles used in the Hugging Face deployment.

---

## Required Google Drive Structure

The notebooks are designed to run directly in Google Colab.

Before running the notebooks, upload the Excel files and create the following structure:

    My Drive/
    ├── Disc_Training_Validation.xlsx
    ├── Disc_Test.xlsx
    ├── inter_rater_raw_measurements.xlsx
    └── saved_models_2026/
        ├── incision_model/
        └── disc_area_model/

The model files (.keras and .pkl) will be automatically generated after running the notebooks.

---

## Final Trained Models

    saved_models_2026/
    ├── incision_model/
    │   ├── incision_model.keras
    │   └── preprocessing_bundle.pkl
    └── disc_area_model/
        ├── disc_area_model.keras
        └── preprocessing_bundle.pkl

These models are also included in this repository and correspond to the Hugging Face deployment.

---

## How to Run

1. Open the notebooks in Google Colab  
2. Upload required Excel files to Google Drive  
3. Create the `saved_models_2026` folder with the following subdirectories:
```text
saved_models_2026/
├── incision_model/
└── disc_area_model/
```
4. Mount Google Drive  
5. Run all cells sequentially  

The main notebook reads:

- `Disc_Training_Validation.xlsx`
- `Disc_Test.xlsx`

The inter-rater notebook reads:

- `inter_rater_raw_measurements.xlsx`

---

## Data Availability

The original MRI images are not publicly shared due to institutional ethical restrictions and patient privacy considerations.

Only de-identified derived parametric measurements are provided to enable reproducibility of the machine learning analysis.

All patient identifiers were anonymized and replaced with sequential study IDs. Repeated measurements from the same patient were assigned the same anonymized ID to preserve patient-level grouping.
