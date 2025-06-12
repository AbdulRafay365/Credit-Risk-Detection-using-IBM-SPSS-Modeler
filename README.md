# Credit-Risk-Detection-using-IBM-SPSS-Modeler

<div align="center">
  <img src="https://github.com/user-attachments/assets/fd8cd037-1e29-4260-92ba-e4aa9b41563c" alt="Image">
</div>

---

## 📌 Executive Summary  
This project evaluates machine learning models for **credit risk prediction** (Risk vs. No Risk) using the German credit dataset.  

### 🔑 Key Findings  
| Model                  | Testing Accuracy | Risk Detection (Sensitivity) | No Risk Detection (Specificity) |  
|------------------------|------------------|------------------------------|---------------------------------|  
| **RF (No SMOTE)**      | 81.55%           | 85.4%                        | 21.8%                           |  
| **RF (SMOTE)**         | 79.07%           | 69.5%                        | 25.6%                           |  
| **DT (SMOTE+Boosting)**| 78.97%           | 71.0%                        | 24.1%                           |  

**Best Model**:  
- **Strict risk aversion** → Non-SMOTE RF (highest Risk detection).  
- **Balanced lending** → SMOTE-RF (better equilibrium).  

---

## 📂 Repository Structure  
```plaintext
Credit-Risk-Detection-using-IBM-SPSS-Modeler/  
├── exports/  
│   ├── Credit Card Fraud Detection/  
│   │   ├── Evaluations/                # Contains ROC curves & performance graphs  
│   │   │   ├── roc_rf_no_smote.png     # [PLACEHOLDER: RF Non-SMOTE ROC]  
│   │   │   ├── roc_rf_smote.png        # [PLACEHOLDER: RF SMOTE ROC]  
│   │   │   └── dt_smote_boosting.png   # [PLACEHOLDER: DT ROC]  
│   │   ├── Saved Models/               # .gen files for deployed models  
│   │   └── Stream/                     # SPSS Modeler workflow  
│   │       └── Data/                   # Dataset used in the stream  
├── Analysis Report.pdf                 # Detailed performance analysis  
└── README.md                           # This file  
