# NFL Draft Prediction 🏈

**GCI World 2026 — OmniCampus Competition**  
Competition Period: April 29, 2026 – June 12, 2026  

---

## Project Overview

- **Goal:** Predict whether a college athlete will be selected in the NFL Draft (binary classification)
- **Evaluation Metric:** ROC-AUC
- **Final Score:** **0.84332 AUC (Top 20%)**

---

## Approach Summary

1. **Exploratory Data Analysis** — class balance, missing values, correlations, feature distributions by draft status
2. **Feature Engineering** — speed score, explosive score, weight/height categories, missing-value flags, composite athletic features, smoothed target encoding
3. **Smart Missing Value Imputation** — group-based medians by position/weight/speed categories instead of simple mean
4. **Model Selection** — RandomizedSearchCV across Gradient Boosting, Random Forest, and XGBoost
5. **Final Model** — XGBoost with Stratified K-Fold (5 folds), predictions averaged across folds

---

## Key Features Engineered

| Feature | Description |
|---------|-------------|
| `speed_score` | Composite of 40-yard dash, shuttle, and 3-cone drill (normalized) |
| `explosion` | Composite of vertical jump and broad jump |
| `power_cat` | Bench press strength category |
| `overall_score` | Weighted sum of athletic categories (speed double-weighted) |
| `Position_Type_te` | Smoothed target encoding for position |
| `is_top_school` | Flag for top-40 schools by prospect volume |
| `combine_tests_completed` | Count of completed combine tests (missingness is informative) |

---

## Models Compared

| Model | Best CV AUC |
|-------|-------------|
| XGBoost | **0.8485** ✅ |
| Gradient Boosting | 0.8462 |
| Random Forest | 0.8421 |

---

## Results

| Metric | Score |
|--------|-------|
| **ROC-AUC** | **0.84332** |
| **Ranking** | Top 20% |

![Competition Score](score_screenshot.png)

The test predictions were submitted to the **OmniCampus GCI World** competition platform for final evaluation.

---

## Repository Contents

- `nfl_draft_prediction.ipynb` — Complete notebook: EDA, feature engineering, model training, and submission generation
- `README.md` — Project documentation
- `score_screenshot.png` — Competition result

---

## Technologies Used

- Python (Pandas, NumPy)
- Scikit-learn (RandomizedSearchCV, StratifiedKFold)
- XGBoost
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Author

**Anas Bakeer**

- GitHub: [@anasbakir185](https://github.com/anasbakir185)

---

*Built as part of the GCI World 2026 Data Science Competition*
