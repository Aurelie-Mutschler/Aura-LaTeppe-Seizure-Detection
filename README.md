# Aura-LaTeppe-Seizure-Detection

## What is done in this repository
- Explore files from database LaTeppe
- Create train/test splitting
- Implement seizure detection algorithms
- Evaluate performances


## Content
Explore_prepare_database_LaTeppe/
* figures/ : html figures from EDA
  * output from 0-Explore_dataset_LaTeppe.ipynb
* res/ : data files (ignored in commits)
  * output from the three .ipynb notebooks
* 0-Explore_dataset_LaTeppe.ipynb : Loads all session files, computes basic statistics and create figures
  * input : "/home/DATA/output/cons-v0_6/cons_PAT_*.csv"
  * output : "res/general/"
* 1-Concatenate_files_and_analysis_per_patient.ipynb : Merge session files into a unique data file per patient (deprecated, has to be re-implemented)
  * input : "/home/DATA/output/cons-v0_6/cons_PAT_*.csv"
  * output : "res/patient_files/"
* 2-Train_test_splitting.ipynb : Reads patient files and performs a traint/test splitting
  * input : "res/patient_files/*.csv"
  * output : "res/ML_ready/*.csv" (one file per patient)


Seizure_detection_database_LaTeppe/
* Baseline_threshold_HR/ : baseline model based on personnalized threshold on heart rate (please refer to the structure of this directory to create new models)
  * figures/ : summary of performances of the model (output from Evaluate_performances.ipynb)
  * predictions/ : seizure detection performed by the model on all patient files
  * 0-Baseline_threshold_HR.ipynb : implementation of the model
    * input : "../../Explore_prepare_database_LaTeppe/res/ML_ready/*.csv"
    * output : "predictions/*.csv"



