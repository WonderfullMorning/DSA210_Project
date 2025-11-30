# DSA210_Project

# Project Overwiev
This project is driven by the observation that complex diseases, such as Coronary Artery Disease (CAD), exhibit discernible probabilistic patterns correlated with a wide array of clinical and biometric risk markers.

The core objective is to develop a robust, data-driven framework for CAD risk prediction. This involves a comprehensive methodological approach: first, comparing and benchmarking different machine learning algorithms against each other and against the selected Large Language Model (LLM) approach for superior performance. Rigorous performance evaluation metrics will be applied across models. Furthermore, the study will conduct a comparative analysis of two distinct health datasets to ensure model generalization and robustness. The primary goal is to leverage the chosen model to perform sophisticated probabilistic risk stratification for CAD and, crucially, to identify the most influential clinical and biometric variables that serve as key determinants of the disease. This will translate complex clinical measurements into actionable insights for diagnostic support and preventative care strategies.

# CAD Context and Definition

Coronary Artery Disease (CAD) is a prevalent heart condition characterized by the buildup of atherosclerotic plaque within the arterial lumen. Blood flow impairment reduces oxygen delivery to the myocardium  (StatPearls, 2024).

Citation:
StatPearls. (2024). Coronary Artery Disease. Retrieved from https://www.ncbi.nlm.nih.gov/books/NBK564304/


# Objectives

The successful execution of this project is defined by the following five key deliverables:

1.Optimized CAD Prediction Model: A highly performant machine learning model (including the LLM-based approach) capable of accurate probabilistic risk prediction for Coronary Artery Disease based on clinical measurements.

2.Comparative Model Benchmarking Report: A detailed analysis comparing the performance (e.g., AUC, precision, recall, F1-score) of the LLM approach against multiple traditional classification algorithms.

3.Clinical Factor Importance Atlas: A comprehensive identification and ranking of the most salient clinical and biometric factors contributing to CAD risk, derived using explainable AI (XAI) techniques.

4.Dataset Generalization Study: A report detailing the structural and predictive differences observed between the two utilized datasets, validating the model's robustness and generalizability across clinical cohorts.

5.Actionable Health Insights: A documented set of findings that translate complex model outputs into practical recommendations for preventative health measures and diagnostic screening.

# Data source
2 datasets are taken from kaggle.
- CAD.csv link: https://www.kaggle.com/datasets/saeedeheydarian/classification-of-coronary-artery-disease?resource=download
- DataClean-fullage.csv link: https://www.kaggle.com/datasets/homelysmile/datacad

# Datasets to use
The columns of the first dataset:
- Sex (Male or Female, Categorical)
- Age (Numerical)
- BMI (Numerical)
- DM (Diabetes Mellitus, Yes or No, Categorical)
- HTN (Hyper tension, Yes or no, Categorical)
- Current Smoker (Yes or No, Categorical)
- Ex-Smoker (Yes or No, Categorical)
- FH (family history, Yes or No, Categorical)
- FBS (Fasting blood sugar, mg/dl, Numerical)
- Cr (Creatine, mg/dl, Numerical)
- TG (Triglyceride, mg/dl, Numerical)
- LDL (Low density lipoprotein, mg/dl, Numerical)
- HDL (High density lipoprotein, mg/dl, Numerical)
- HB (Hemoglobin, g/dl, Numerical)
- WBC (White blood cell, cells/ml, Numerical)
- EF (Ejection fraction, %, Numerical)
- CAD (Cad for Yes; Normal for No, Categorical)

The columns of the second dataset:
- Gender (M or F, Categorical)
- Age (Numerical)
- alchohol (0 for No, 1 for Yes, Categorical)
- leuk_count (Leukcyte count, Numerical)
- eject_fraction (Left ventricular ejection fraction, %, Numerical)
- glucose (Blood glucose level, mg/dl,Numerical)
- creatinine (mg/dl, Numerical)
- urea (Blood urea nitrogen, mg/dl, Numerical)
- platelets (Platelet count, Numerical)
- bnp (Brain natriuretic peptide, pg/ml, Numerical)
- haemoglobin (Hemoglobin, g/dl, Numerical)
- raised_cardiac (Elevated cardiac enzymes, 0 for No ;1 for Yes, Categorical
- cad (0 for Absence, 1 for Presence, Categorical)

A crucial step in the data preparation phase will be:

Target Harmonization: Converting the categorical target variable (CAD in the First Dataset) into the binary (0/1) format to match the target variable (cad in the Second Dataset) for consistent model training and generalization testing.

Unit Consistency: All categorical features will undergo binary encoding. Numerical features, especially those related to blood counts (WBC, leuk_count, platelets), will be inspected for common scaling issues (e.g., reporting in thousands vs. actual count) and normalized where necessary to ensure comparable influence during modeling.

# Hypothesis
The central hypotheses guiding this research are:

1.Established Risk Factor Dominance: Primary established risk factors for CAD—specifically Age, Hypertension (HTN), and markers of Dyslipidemia (LDL, HDL, TG)—will exhibit the strongest individual statistical association with the presence of CAD in the primary dataset.

2.Functional Marker Contribution: Features representing cardiac function and metabolic stress, particularly Ejection Fraction (EF) and Fasting Blood Sugar (FBS), will be ranked among the top five features for predictive power (Feature Importance) in the final optimized model.

3.Cross-Cohort Reliability: The relative ranking of feature importance for common clinical factors (Age, HTN, DM, Smoking) will show a high degree of correlation ($\ge 0.80$) between models trained and evaluated on the two distinct datasets, confirming the reliability of these factors across different patient cohorts.

# Conclusion
The project has established a strong foundation by defining a clear motivation, specific objectives, and detailed data requirements. The next crucial phase involves rigorous data cleaning, harmonization of features (particularly the target variable across datasets), and feature engineering to prepare the two clinical datasets for comparative machine learning model training. Upon completion, the project is expected to yield a high-performing and highly interpretable model that enhances diagnostic risk assessment for Coronary Artery Disease.

