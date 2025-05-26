![Churn Prediction Banner](assets/video_streaming.png)

# Churn Prediction for a Video Streaming Service

This project builds and evaluates machine learning models to predict **customer churn** for a video streaming subscription service.  
It was originally inspired by a Coursera capstone challenge but has since been extended to explore advanced techniques and additional evaluation strategies.

---

## Project Overview

Churn — the likelihood of a customer canceling their subscription — is a major concern for any subscription-based business.  
This project aims to predict churn probabilities using features derived from customer behavior and history. A classifier is trained to output **well-calibrated probabilities** of churn.

### Dataset Structure

- `train.csv`: labeled dataset with customer features and a churn label
- `test.csv`: unlabeled dataset (no `y` column); predictions are evaluated externally using ROC-AUC


> ⚠️ **Note**: The dataset is not included in this repository due to Coursera content policies.
> The notebook retains all code, visualizations, and results to showcase modeling ability.  
> If you have access to the original dataset, the notebook will run end-to-end.

---

## Tech Stack

- **Python**
- **scikit-learn**, **LightGBM**, **XGBoost**
- **Optuna** (for hyperparameter optimization)
- **SHAP**, **matplotlib**, **seaborn** (for explainability and visualization)
- **imbalanced-learn** (for handling class imbalance)

---

## Model Evaluation Summary

| Model            | CV ROC-AUC | CV Log Loss | Precision | Recall  | F1 Score |
|------------------|------------|-------------|-----------|---------|----------|
| LogisticRegression | 0.7498   | 0.5869      | 0.3246    | 0.6823  | 0.4399   |
| RandomForest      | 0.6801    | 0.5416      | 0.3103    | 0.3924  | 0.3465   |
| LightGBM          | 0.6960    | 0.5131      | 0.3328    | 0.3582  | 0.3450   |
| LGBM (Optuna)     | **0.6961**| **0.5126**  | **0.3325**| 0.3618  | 0.3465   |
| XGBoost           | 0.6936    | 0.8775      | 0.2476    | 0.2476  | 0.3801   |

---

## Repository Structure

```
.
├── notebooks/
│   └── ChurnPrediction11_cleaned_final.ipynb
├── data/                # Not included
├── assets
│   └── video_streaming.png
├── requirements.txt     
└── README.md
```

---

## Running the Project

```bash
pip install -r requirements.txt
```

Then run the notebook:
```
notebooks/ChurnPrediction11_cleaned_final.ipynb
```

---

## Author’s Note

This version of the project was developed **after completing the original Coursera challenge**, as a way to practice advanced modeling, optimization, and evaluation techniques.

This project was developed independently, collaborating with AI tools and documentation along the way — just as in a real-world workflow.

---

## License

This project is open-source and released under the MIT License.
