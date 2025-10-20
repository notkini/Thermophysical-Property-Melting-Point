📘 Overview

This project was built for the Melting Point Prediction Challenge, a Kaggle-style regression competition where the goal is to predict the melting points (Tm) of organic molecules using group contribution features that represent chemical substructures.

Melting point prediction is crucial in drug design, materials engineering, and process safety, yet experimental measurements can be expensive or unavailable.
This project applies machine learning to learn the nonlinear relationship between molecular structure and melting behavior.

📂 Dataset

Source: Provided via the Machine Learning for Engineers – Thermophysical Properties page

Total compounds: 3328

🧠 Model Pipeline

Environment: Google Colab

Libraries: pandas, scikit-learn, lightgbm

Workflow:

Mount Google Drive and load the dataset

Drop non-numeric columns (id, SMILES)

Split training data into train/validation sets

Train LightGBM Regressor with early stopping

Evaluate model performance using Mean Absolute Error (MAE)

Retrain on full data and generate predictions for test set

Export submission.csv for Kaggle upload

📊 Results

| Metric         | Score         |
| -------------- | ------------- |
| Validation MAE | **≈ 42.03 K** |

A lower MAE indicates better predictive accuracy.
The model achieved good generalization using only group contribution features.

🧰 Future Improvements

Feature engineering from SMILES (e.g., RDKit molecular descriptors)

Hyperparameter tuning via Optuna or GridSearchCV

Ensemble learning (LightGBM + XGBoost + CatBoost)

SHAP feature importance analysis

👨‍💻 Author

Aditya Kinikar
B.Tech in ECS | SIES GST
Passionate about ML, AI, and full-stack projects 🚀
