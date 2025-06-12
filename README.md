# Credit Risk Detection using IBM SPSS Modeler  
**Author**: AbdulRafay365  

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

📊 Model Performance Analysis
1. Random Forest (No SMOTE)
Testing Metrics:

Accuracy: 81.55%

Risk Detection: 85.4%

No Risk Detection: 21.8%

Graphical Evidence:
https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF,%2520No%2520SMOTE/ROC.png
Figure 1: High AUC (0.82) confirms strong Risk class identification but flat No Risk curve (specificity 21.8%).

https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF,%2520No%2520SMOTE/Gains.png
Figure 2: Top 20% of predictions capture 45% of actual Risk cases (ideal for strict screening).

2. Random Forest (With SMOTE)
Testing Metrics:

Accuracy: 79.07%

Risk Detection: 69.5%

No Risk Detection: 25.6%

Graphical Evidence:
https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF%2520and%2520DT,%2520SMOTE/ROC.png
*Figure 3: Balanced ROC curves (AUC 0.78) show improved No Risk detection vs. Non-SMOTE.*

https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF%2520and%2520DT,%2520SMOTE/Lift.png
*Figure 4: Lift of 2.5x in top decile - better than random for both classes.*

3. Decision Tree (SMOTE) ❌ Not Recommended
Testing Metrics:

Accuracy: 78.97%

Overfitting Gap: 96.15% (train) vs. 78.97% (test)

Graphical Evidence:
https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF%2520and%2520DT,%2520SMOTE/Performance%2520Evaluation.png
Figure 5: Severe overfitting visible in accuracy disparity (training vs testing).

🎯 Business Case Alignment
A. Fraud Prevention Priority
Graph Support:
https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF,%2520No%2520SMOTE/Lift.png
*Figure 6: Non-SMOTE RF achieves 3x lift for Risk class in top 30% predictions.*

B. Fair Lending Priority
Graph Support:
https://exports/Credit%2520Card%2520Fraud%2520Detection/Evaluations/RF%2520and%2520DT,%2520SMOTE/Gains.png
*Figure 7: SMOTE-RF shows smoother gains distribution across both classes.*

🚀 Recommendations
Use Case	Model	Supporting Evidence
Minimize defaults	Non-SMOTE RF	Fig 1, 2, 6
Reduce false rejections	SMOTE-RF	Fig 3, 4, 7
Avoid	SMOTE-DT	Fig 5 (Overfitting)
Next Steps:

Deploy selected model in SPSS Modeler stream

Monitor quarterly using Performance Evaluation.png metrics

Adjust probability thresholds based on Fig 2/7 gains curves

🔗 References
Dataset: German Credit Dataset (SPSS Modeler Sample)

Tools: IBM SPSS Modeler 18.2

Technique: SMOTE (50-50 class balance)
