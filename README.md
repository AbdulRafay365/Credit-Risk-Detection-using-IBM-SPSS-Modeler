# Credit Risk Detection using IBM SPSS Modeler  

---

## 📌 Executive Summary  
This project evaluates machine learning models for **credit risk prediction** using the German credit dataset.  

### 🔑 Key Findings  
| Model                  | Testing Accuracy | Risk Detection (Sensitivity) | No Risk Detection (Specificity) |  
|------------------------|------------------|------------------------------|---------------------------------|  
| **RF (No SMOTE)**      | 81.55%           | 85.4%                        | 21.8%                           |  
| **RF (SMOTE)**         | 79.07%           | 69.5%                        | 25.6%                           |  
| **DT (SMOTE)**         | 78.97%           | 71.0%                        | 24.1%                           |  

**Best Model**:  
- **Strict risk aversion** → Non-SMOTE RF (highest Risk detection).  
- **Balanced lending** → SMOTE-RF (better equilibrium).  

---

## 📂 Repository Structure  
```plaintext
Credit-Risk-Detection-using-IBM-SPSS-Modeler/  
├── exports/  
│   ├── Credit Card Fraud Detection/  
│   │   ├── Evaluations/  
│   │   │   ├── RF and DT, SMOTE/  
│   │   │   │   ├── Gains.png          # Cumulative gains chart  
│   │   │   │   ├── Lift.png           # Lift curve  
│   │   │   │   ├── Performance Evaluation.png  # Metric summary  
│   │   │   │   └── ROC.png            # ROC curve  
│   │   │   └── RF, No SMOTE/  
│   │   │       ├── Gains.png  
│   │   │       ├── Lift.png  
│   │   │       ├── Performance Evaluation.png  
│   │   │       └── ROC.png  
│   │   ├── Saved Models/  
│   │   └── Stream/  
├── Analysis Report.pdf  
└── README.md  
```

---

## Model Performance Analysis
Please read the analysis report in exports folder, and also review the evaluations folder for performance evaluation and comparision graphs. 
