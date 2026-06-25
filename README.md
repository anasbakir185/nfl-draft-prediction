# NFL Draft Prediction 🏈

Machine Learning model for predicting NFL Draft selections using historical player data.  
Developed for the **GCI World 2026 OmniCampus Competition**.

---

## Project Overview

This project tackles a **binary classification problem**:

- **Target:** Drafted (1) vs Not Drafted (0)
- **Evaluation Metric:** ROC-AUC
- **Final Score:** **0.84332 ROC-AUC**
- **Competition Ranking:** Top 20%

The goal is to predict whether a college athlete will be selected in the NFL Draft based on physical performance metrics, position information, and athletic test results.

---

## Dataset

The dataset contains information about college football players, including:

- Physical attributes (height, weight, BMI)
- Athletic performance metrics (40-yard dash, vertical jump, bench press)
- Agility tests (3-cone drill, shuttle run)
- Player position and type
- Draft outcome (target variable)

> Dataset provided as part of the GCI World 2026 OmniCampus Competition.

---

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost, LightGBM
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Project Workflow

### 1. Exploratory Data Analysis
- Class balance assessment
- Missing value patterns
- Feature distributions and correlations
- Position-based draft rate analysis

### 2. Feature Engineering & Preprocessing
- Created composite scores (Speed Score, Explosive Score)
- Categorical encoding (weight/height/speed categories)
- Smoothed target encoding for position features
- Group-based missing value imputation
- Missing-value indicator flags

### 3. Model Building
Multiple classifiers evaluated with RandomizedSearchCV:

- Gradient Boosting Classifier
- Random Forest Classifier
- XGBoost Classifier ✅ **(Final Model)**
- LightGBM Classifier

### 4. Model Evaluation
- **Validation Strategy:** Stratified K-Fold Cross-Validation (5 folds)
- **Prediction:** Averaged probabilities across all folds
- **Metric:** ROC-AUC

---

## Results

| Metric | Score |
|--------|-------|
| **ROC-AUC** | **0.84332** |
| **Ranking** | Top 20% |

![Competition Score](score_screenshot.png)

The final XGBoost model achieved a ROC-AUC score of **0.84332**, placing within the **Top 20%** of competition participants.

The test predictions were submitted to the OmniCampus GCI World competition platform for final evaluation.

---

## Repository Contents

- `nfl_draft_prediction.ipynb` — Complete notebook with EDA, feature engineering, model training, and evaluation
- `README.md` — Project documentation
- `score_screenshot.png` — Competition leaderboard result

---

## Author

**Anas Bakeer**

- GitHub: [@anasbakir185](https://github.com/anasbakir185)

---

## Acknowledgments

- OmniCampus GCI World 2026 Competition organizers
- Scikit-learn, XGBoost, and LightGBM communities

---

*Built as part of the GCI World 2026 Data Science Competition*
