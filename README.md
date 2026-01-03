🧓 SHARE-Health-and-Longevity-Modeling
Modeling self-perceived health and longevity using the SHARE (Survey of Health, Ageing and Retirement in Europe) dataset. The project applies causal feature selection, panel-aware modeling, and multiple ML techniques in a fully reproducible Jupyter Notebook.

📚 Project Overview
This case study analyzes high-dimensional panel data from SHARE (≈3,000 variables, multiple countries and waves) to identify the most influential determinants of:
Self-Perceived Health (categorical outcome)
Age (continuous proxy for longevity)
Special care is taken to avoid tautology, prevent data leakage, and ensure interpretability.

🎯 Objectives
Build separate models for health and longevity
Perform causal-oriented feature selection
Leverage the panel structure (countries, waves, individuals)
Compare multiple modeling approaches
Deliver a fully reproducible workflow in a single notebook

📦 Dataset
Source: SHARE Survey
Main file: statisticsexp.csv
Codebook: Coding tables.xlsx
Observations: Older adults across Europe
Design: Longitudinal, multi-country panel

🧹 Data Preparation
Key preprocessing steps include:
Handling missing values (drop, impute, flag)
Removing redundant and leaky variables
Encoding categorical variables (one-hot)
Scaling and transforming numeric features
Outlier control (realistic age bounds)

⚠️ Direct outcome indicators (e.g. ADL limitations, diagnosed diseases) are excluded from health models to avoid circular reasoning.

📊 Exploratory Data Analysis (EDA)
The EDA explores:
Distribution of self-rated health categories
Age distribution and longevity patterns
Country and wave effects
Lifestyle, education, and smoking patterns
Comparisons between younger-old and oldest-old groups
Key insights include strong links between physical activity and health, education gradients, gender survival advantages, and notable cross-country differences.

🧠 Feature Selection (Causality-Oriented)
Feature selection focuses on plausible determinants, not consequences:
Demographics (age group, gender)
Socioeconomic status (education, income)
Lifestyle (physical activity, smoking)
Social factors (household structure, support)
Cultural and country-level effects
Methods used:
LASSO regularization
Random Forest importance
Correlation screening

🧬 Panel Data Structure
The longitudinal design is leveraged by:
Country and language dummies
Wave controls (avoiding temporal leakage)
Individual-level train/test splits
Optional lagged variables

🧠 Panel-aware design helps control for unobserved heterogeneity and improves interpretability.

🤖 Modeling Approaches
Different methods are applied and compared:
Logistic Regression
CHAID Decision Trees
Random Forests
Support Vector Machines (SVM)
Bayesian Networks (where applicable)

🎯 Separate pipelines are built for:
Health classification
Age (longevity) regression

📏 Evaluation Metrics
Health models: Accuracy, F1-score, AUC
Age models: MAE, R²
Model performance is reported alongside interpretability.

📈 Results & Interpretation
Results are summarized in a comparative table highlighting factors with consistent effects on health and longevity, emphasizing:
Lifestyle behaviors
Socioeconomic gradients
Social support
Cultural and country context

🔁 Reproducibility
Single Jupyter Notebook
Fixed random seeds
Modular structure
Clear markdown explanations
CRISP-DM inspired workflow

🧾 Conclusion
This project demonstrates end-to-end modeling of self-perceived health and longevity using complex SHARE panel data. By combining causal reasoning, rigorous feature selection, and multiple ML techniques, the analysis delivers interpretable insights into healthy ageing across Europe.
