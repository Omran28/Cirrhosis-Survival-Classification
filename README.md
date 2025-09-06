# 🫀 Cirrhosis Survival Prediction

[![Python](https://img.shields.io/badge/Python-3.11-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.1-red)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/cirrhosis-survival-prediction)](https://github.com/yourusername/cirrhosis-survival-prediction/issues)

---

## 📌 Project Overview
This project leverages **machine learning and deep learning techniques** to predict survival outcomes for patients with cirrhosis. By analyzing clinical and demographic data, it provides actionable insights to assist healthcare professionals in **prognosis, risk stratification, and clinical decision-making**.

> “Transforming patient data into actionable insights with precision and reliability.”

---

## 🧰 Key Features
- **Data Preprocessing:**  
  - Handling missing values with imputation strategies.  
  - Scaling continuous features using standardization.  
  - One-hot encoding categorical variables like Gender and Comorbidities.  
  - Splitting data into **training, validation, and test sets**.  

- **Modeling:**  
  - Implements a **custom Neural Network architecture** using PyTorch.  
  - Comparison with classical ML models like Random Forest and XGBoost for benchmarking.  
  - Implements **stochastic depth and dropout** to reduce overfitting.  

- **Evaluation:**  
  - Metrics include **accuracy, precision, recall, F1-score, and ROC-AUC**.  
  - Confusion matrix and feature importance visualization.  

- **Visualization:**  
  - Survival curves, prediction distributions, and feature importance plots for clinical interpretability.  

---

## 🗂 Project Workflow

1. **Data Collection:**  
   - Source: [Specify source or indicate proprietary data]  
   - Data includes clinical parameters such as Age, Bilirubin, Albumin, Platelets, Gender, and Survival Status.  

2. **Data Cleaning & Preprocessing:**  
   - Remove irrelevant columns (e.g., patient ID).  
   - Impute missing values using median or mean strategies.  
   - One-hot encode categorical variables.  
   - Scale numeric features using `StandardScaler`.  
   - Split into training (70%), validation (15%), and test sets (15%).  

3. **Model Architecture (Neural Network):**  
   - **Input Layer:** Number of features after preprocessing.  
   - **Hidden Layers:**  
     - Layer 1: 256 neurons + ReLU + LayerNorm + Dropout  
     - Layer 2: 128 neurons + ReLU + LayerNorm + Dropout  
     - Layer 3: 64 neurons + ReLU + LayerNorm + Dropout  
   - **Output Layer:** 2 neurons (for survival vs non-survival) + Softmax.  
   - **Regularization:** Dropout rate of 0.2–0.3 and stochastic depth to prevent overfitting.  
   - **Optimizer:** Adam with learning rate scheduler.  
   - **Loss Function:** Cross-Entropy Loss with optional class weighting for imbalance.  

4. **Model Training:**  
   - Trained for 100 epochs with early stopping based on validation loss.  
   - Uses **mini-batch gradient descent** (batch size = 32–64).  
   - Monitors training and validation loss/accuracy to prevent overfitting.  

5. **Evaluation & Interpretation:**  
   - Evaluate metrics on validation and test sets.  
   - Plot confusion matrix and ROC curve.  
   - Analyze feature importance from classical models for interpretability.  

---

## ⚙️ Installation
Clone the repo and install dependencies:

```bash
git clone https://github.com/yourusername/cirrhosis-survival-prediction.git
cd cirrhosis-survival-prediction
pip install -r requirements.txt
