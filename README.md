# Credit Risk Detection using IBM SPSS Modeler  

---
## Stream Overview

<div align="center">
  <img src="https://github.com/user-attachments/assets/fd8cd037-1e29-4260-92ba-e4aa9b41563c" alt="Image">
</div>

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
## 🚀 How to Run the Stream

### Prerequisites
- IBM SPSS Modeler installed (Version 18.2+)
- Stream file: `exports/Credit Card Fraud Detection/Stream/*.str`
- Dataset in: `exports/Credit Card Fraud Detection/Stream/Data/`

### Steps
1. **Open the Stream**:
   - Launch SPSS Modeler
   - `File > Open Stream` > Navigate to:
     ```
     exports/Credit Card Fraud Detection/Stream/Your_Stream_Name.str
     ```

2. **Verify Data Source**:
   - Edit the Source Node
   - Confirm path points to:
     ```
     exports/Credit Card Fraud Detection/Stream/Data/Your_Dataset.csv
     ```

3. **Execute**:
   - ▶️ Run button (full stream)
   - OR right-click any node > "Run from Here"

4. **View Results**:
   - Check Table nodes for outputs
   - Browse Model nodes for trained models
   - Evaluation nodes auto-generate graphs

### Troubleshooting
| Issue | Solution |
|-------|----------|
| Missing Data | Verify dataset path in Source node |
| Model Errors | Check license requirements |
| SMOTE Issues | Validate Balance node settings |

> 💡 **Tip**: Use Turbo Mode (⚡) for faster execution on large datasets

---

## Model Performance Analysis
Please read the analysis report in exports folder, and also review the evaluations folder for performance evaluation and comparision graphs. 
