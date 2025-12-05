save
# Fraud Prediction Model Development

This repository contains the full workflow for developing a machine learning model to detect credit card fraud.  
It includes data exploration, preprocessing, feature engineering, model training, threshold tuning, and saving the final deployment-ready model assets.

---

##  Dataset Overview

- **Total Rows:** 1,296,675  
- **Total Columns:** 23  
- **Fraud Cases:** 7,506  
- **Non-Fraud Cases:** 1,289,169  
- **Imbalance:**  
  - **99.42% Non-Fraud**  
  - **0.58% Fraud**

### **Dataset Source**  
Publicly available credit card fraud dataset used for machine-learning training and experimentation.

---

## Project Workflow

### **1. Exploratory Data Analysis (EDA)**
- Understanding distributions  
- Fraud vs non-fraud insights  
- Checking missing values  
- Summary statistics  

### **2. Preprocessing & Feature Engineering**
- Cleaning columns  
- Creating new fields  
- Handling imbalance  
- Encoding features  

### **3. Model Training**
Multiple ML models were trained and evaluated.  
The **Tuned Decision Tree** was selected as the best model due to its balance of:

- Precision  
- Recall  
- F1 Score (Fraud class)  
- Practical fraud detection performance  

### **4. Threshold Tuning**
A custom probability cutoff was calculated to maximize fraud detection performance.  
This optimized threshold is saved for deployment.

### **5. Saving Deployment Files**
The following assets are generated:

- `final_decision_tree_model.pkl`  
- `fraud_best_threshold.pkl`  
- `selected_features.pkl`  

These are consumed by the deployment API.

---

## Repository Structure

```
fraud-prediction-model-development/
│
├── fraud_model_development.ipynb   # Main notebook (EDA → Training → Best Model)
├── fraudTrain.csv                  # Dataset (optional to include)
├── models/                         # Saved model files (optional)
├── scripts/                        # Python training scripts (optional)
├── requirements.txt
└── README.md
```

---

## 🛠 Installation

```bash
pip install -r requirements.txt
```

---

## How to Run

### Run the Notebook
```bash
jupyter notebook fraud_model_development.ipynb
```

### Or run training script
```bash
python train_model.py
```

---

## Output Files for Deployment

- `final_decision_tree_model.pkl`  
- `fraud_best_threshold.pkl`  
- `selected_features.pkl`  

These should be copied into the Deployment Repository.

---

## Author
Completed as part of the **DerpTech Upskilling Programme (3MTT Initiative)** machine learning capstone project.
