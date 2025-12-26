# Predicting Customer Churn in Telecommunications

## Project Overview
This project analyzes customer churn in a telecommunications company using machine learning to identify at-risk customers before they leave.

**Research Question:** What factors most strongly predict customer churn, and can we build a model to identify at-risk customers?

## Dataset
- **Source:** [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 customer records with 21 features
- **Features:** Demographics, account information, and service subscriptions

## Reports & Analysis
📊 **[Business Report (Nontechnical)](REPORT.md)** - Executive summary and recommendations for stakeholders  
📓 **[Technical Analysis Notebook](churn_analysis.ipynb)** - Full data science workflow with code

## Summary of Findings

### Model Performance
| Model | Accuracy | Recall (Churn) | ROC-AUC |
|-------|----------|----------------|---------|
| Logistic Regression | 73.81% | **78.34%** | **0.8415** |
| Random Forest | **76.86%** | 70.32% | 0.8367 |
| Gradient Boosting | 74.95% | 73.53% | 0.8353 |

Random Forest achieved the highest accuracy (76.86%), while Logistic Regression provides the best recall (78.34%) for identifying churners.

### Top 7 Key Factors Influencing Churn
1. **Contract Type** (importance: 0.2121) - Month-to-month: 42.7% churn vs Two-year: 2.8%
2. **Tenure** (importance: 0.1257) - 0-12 months: 47.4% churn vs 48-72 months: 9.5%
3. **Total Charges** (importance: 0.1138) - Lower total spend indicates higher churn risk
4. **Monthly Charges** (importance: 0.0869) - Higher bills correlate with churn
5. **Tech Support** (importance: 0.0681) - Without: 41.6% churn vs With: 15.2%
6. **Online Security** (importance: 0.0674) - Without: 41.8% churn vs With: 14.6%
7. **Internet Service** (importance: 0.0660) - Fiber optic: 41.9% churn vs DSL: 19.0%

### Business Recommendations
1. **Focus on New Customers** - The first 12 months are critical; implement onboarding programs
2. **Promote Long-term Contracts** - Offer incentives for annual or two-year commitments
3. **Bundle Security Services** - Customers with OnlineSecurity and TechSupport churn less
4. **Review Fiber Optic Service** - High churn despite premium pricing suggests dissatisfaction
5. **Flag Electronic Check Payments** - 45.3% churn rate for this payment method

### Recommended Model for Deployment
**Logistic Regression** is recommended for production due to:
- Highest recall (78.34%) - catches more at-risk customers
- Highest ROC-AUC (0.8415) - best overall discrimination
- Interpretable coefficients for business understanding
- Fast prediction times

## Project Structure
```
capstone_ai/
├── churn_analysis.ipynb    # Main technical analysis notebook
├── REPORT.md               # Nontechnical business report (with visuals)
├── README.md               # This file
├── INITIAL.md              # Original project proposal
├── requirements.txt        # Python dependencies
├── generate_images.py      # Script to regenerate report visualizations
└── images/                 # Visualizations for the report
    ├── CHURN_DISTRIBUTION.png
    ├── CHURN_BY_CATEGORICAL_FEATURES.png
    ├── CHURN_BY_TENURE.png
    ├── CONFUSION_MATRICES.png
    ├── ROC_CURVES.png
    └── FEATURE_IMPORTANCE_BY_CATEGORY.png
```

## Requirements
```
pandas>=2.0.0
numpy>=1.24.0
matplotlib>=3.7.0
seaborn>=0.12.0
scikit-learn>=1.3.0
kagglehub>=0.2.0
jupyter>=1.0.0
```

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook churn_analysis.ipynb
```

