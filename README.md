# nfl-draft-prediction
Machine Learning model for predicting NFL Draft selections using historical player data.
The project is developed for the **GCI World 2026 OmniCampus Competition**.

The objective of this project is to predict whether a college athlete will be selected in the NFL Draft using historical player data.

---

## Project Overview

This project tackles a **binary classification problem**:

- **Target:** Drafted / Not Drafted
- **Evaluation Metric:** ROC-AUC
- **Final Score:** **0.84332 ROC-AUC**
- **Competition Ranking:** Top 20%

---

## Dataset

The dataset contains information about college football players, including:

- Physical attributes
- Athletic performance metrics
- College statistics
- Player characteristics

> Dataset provided as part of the GCI World 2026 competition.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Project Workflow

### 1. Data Exploration

- Investigated missing values
- Analyzed feature distributions
- Explored correlations

### 2. Data Preprocessing

- Handled missing values
- Encoded categorical variables
- Feature engineering

### 3. Model Building

Several machine learning models were explored, including:

- Random Forest
- XGBoost
- Gradient Boosting

### 4. Model Evaluation

Models were evaluated using:

- ROC-AUC Score
- Cross-validation

---

## Results

| Metric | Score |
|---------|-------|
| ROC-AUC | 0.84332 |

The final model achieved a ROC-AUC score of **0.84332**, placing within the **Top 20%** of participants.

---


---

## Author

Anas Bakeer

GitHub: https://github.com/anasbakir185
