![Churn Prediction Banner](assets/Video_Streaming_Service.png)

# Churn Prediction for a Video Streaming Service

This project builds and evaluates machine learning models to predict **customer churn** for a video streaming subscription service.  
It was originally inspired by a Coursera capstone challenge but has since been extended to explore advanced modeling techniques, automated hyperparameter tuning, and model explainability.

---

> **Want a clean view of the Jupyter Notebook?**  
> 👉 [Click here to view it in nbviewer.org](https://nbviewer.org/url/raw.githubusercontent.com/Timensider/churn-prediction-streaming-service/main/notebooks/ChurnPrediction11_cleaned_final.ipynb)

## Project Overview

Churn — the likelihood of a customer canceling their subscription — is a critical metric for any subscription-based business.

This project aims to:  
 - Train a classifier to predict churn likelihood.  
 - Output well-calibrated churn probabilities.  
 - Analyze performance and key drivers of customer retention.  

### Dataset Structure

- `train.csv`: labeled dataset with customer features and a churn label
- `test.csv`: Unlabeled dataset; evaluated externally via ROC-AUC.


> ⚠️ **Note**: The dataset is not included in this repository due to Coursera content policies.
> However, the notebook retains all code, visualizations, and model results to fully demonstrate the solution. 
> If you have access to the original dataset, the notebook will run end-to-end.

---

## Tech Stack

- **Python**
- **scikit-learn**, **LightGBM**, **XGBoost**
- **Optuna** (for hyperparameter optimization)
- **SHAP**, **matplotlib**, **seaborn** (for interpretability and visualization)
- **imbalanced-learn** (for class imbalance techniques)

---

## Model Evaluation Summary

| Model            | ROC-AUC    | Log Loss   | Precision | Recall  | F1 Score |
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

This version of the project was developed **after completing the original Coursera challenge** to practice:  
 - Building more robust models  
 - Automating tuning with Optuna  
 - Interpreting results with SHAP  

AI tools were used for research, code drafting, and documentation — reflecting a modern, real-world workflow.  

---

## License

This project is open-source and released under the MIT License.
