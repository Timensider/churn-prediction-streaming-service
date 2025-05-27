![Churn Prediction Banner](assets/video_streaming_service__.png)

# Churn Prediction for a Video Streaming Service

This project builds and evaluates machine learning models to predict **customer churn** for a video streaming subscription service.  
It was originally inspired by a Coursera capstone challenge but has since been extended to explore advanced modeling techniques, automated hyperparameter tuning, and model explainability.

---

> **Want a clean view of the Jupyter Notebook?**  
>  This notebook includes all model outputs, plots, and results.  
> It may show errors in Colab when attempting to re-run cells that depend on restricted or missing data (not included per Coursera policy).
>  
> Use this notebook as a read-only showcase — all results are already included.
> 
- [Open in Colab](https://colab.research.google.com/github/Timensider/churn-prediction-streaming-service/blob/main/notebook/ChurnPrediction.ipynb)
- [Try in nbviewer](https://nbviewer.org/url/raw.githubusercontent.com/Timensider/churn-prediction-streaming-service/main/notebook/ChurnPrediction.ipynb)
- [View on GitHub](https://github.com/Timensider/churn-prediction-streaming-service/blob/main/notebook/ChurnPrediction.ipynb)


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
├── notebooks/                          # All Jupyter notebooks
│   └── ChurnPrediction.ipynb
│
├── data/                               # Not included – used locally
│   └── (Mentioned in README, ignored in repo)
│
├── assets/                             # Visual assets for README or analysis
│   └── video_streaming.png
│
├── .gitignore                          # Files and folders to exclude from Git
├── LICENSE                             # MIT License for code
├── README.md                           # Project overview + instructions
├── requirements.txt                    # Python package dependencies

```

---

## Running the Project

This notebook includes all outputs and results.  
It’s meant to showcase the full forecasting pipeline from data prep to deployment.  
You don’t need to run it — everything is already rendered for review.

If you have access to the original Coursera dataset:

```bash
pip install -r requirements.txt
```

Then open the notebook:
```
notebook/ChurnPrediction.ipynb
```

---

## Author’s Note

This version of the project was developed **after completing the original Coursera challenge**, and is intended for educational and portfolio purposes only.

All code, models, and evaluations were written independently to:
- Explore more robust modeling techniques
- Automate tuning with Optuna
- Improve interpretability using SHAP and other tools

⚠️ **Note**: This repository does **not** include the original Coursera datasets or any proprietary course materials, in compliance with Coursera's content policy.

AI tools were used to support research, code drafting, and documentation — reflecting a modern, real-world workflow.

---

## License

This project is open-source and released under the MIT License.  
See the [LICENSE](LICENSE) file for details.

