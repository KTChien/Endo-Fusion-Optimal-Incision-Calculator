# Endo-Fusion-Optimal-Incision-Calculator

Code and derived parametric data for ANN-based incision distance prediction in lumbar endo-fusion planning.

This repository provides the Google Colab notebooks, de-identified derived measurement datasets, model comparison results, and pretrained model files used in the manuscript:

"Optimizing incision placement for maximum disc and endplate preparation in lumbar endo-fusion using parametric modeling, genetic algorithms, and machine learning"

Submitted to Digital Health.

---

## Repository Contents

- `Incision_&_Area_2026_04_28_journal_revision_final_en(Colab).ipynb`  
  Main Google Colab notebook for model training, validation, model comparison, and prediction.

- `Inter_rater_reliability_results_en(Colab).ipynb`  
  Google Colab notebook for inter-rater reliability analysis.

- `Disc_Training_Validation.xlsx`  
  De-identified development dataset used for model training and internal validation.

- `Disc_Test.xlsx`  
  De-identified independent external validation dataset.

- `inter_rater_raw_measurements.xlsx`  
  De-identified raw measurement data from two raters for inter-rater reliability analysis.

- `inter_rater_summary.xlsx`  
  Output summary of inter-rater reliability analysis.

- `model_comparison_updated.xlsx`  
  Output table summarizing model comparison results.

- `saved_models_2026/`  
  Final trained models and preprocessing bundles. These are also the models used in the Hugging Face deployment.

---

## Required Google Drive Structure

The notebooks are designed to run directly in Google Colab.  
Before running the notebooks, upload the Excel files and create the following folder structure in the root directory of Google Drive:

```text
My Drive/
├── Disc_Training_Validation.xlsx
├── Disc_Test.xlsx
├── inter_rater_raw_measurements.xlsx
└── saved_models_2026/
    ├── incision_model/
    └── disc_area_model/
