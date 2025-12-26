# Capstone Project Proposal: Predicting Customer Churn in Telecommunications

## Research Question

What factors most strongly predict customer churn in a telecommunications company, and can we build a model to identify at-risk customers before they leave?

## Expected Data Source

Telco Customer Churn Dataset from Kaggle: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
Links to an external site.
This dataset contains 7,043 customer records with 21 features including demographics, account information, and service subscriptions, along with a binary churn indicator.

## Techniques Expected

* Exploratory Data Analysis: Examine distributions, correlations, and patterns across churned vs. retained customers
* Feature Engineering: Create meaningful variables from existing data (e.g., tenure groups, total services subscribed)
* Classification Models: Logistic Regression, Random Forest, and Gradient Boosting to predict churn probability
* Model Evaluation: Compare performance using accuracy, precision, recall, F1-score, and ROC-AUC
* Feature Importance Analysis: Identify which variables have the greatest impact on churn predictions

## Expected Results

I anticipate identifying 5-7 key factors that strongly influence churn, likely including contract type, tenure, monthly charges, and service combinations. The final model should achieve at least 75-80% accuracy in predicting which customers will leave, with particular emphasis on recall to minimize missed at-risk customers.

## Why This Question Matters

Losing a customer is expensive. Industry estimates suggest acquiring a new customer costs five to seven times more than retaining an existing one. For a telecom company, every churned customer represents not just lost monthly revenue but also wasted marketing dollars and potential negative word-of-mouth.

If this question goes unanswered, companies operate blindly, reacting to cancellations after they happen rather than preventing them. Marketing budgets get spread thin across all customers instead of targeting those who actually need attention.

The benefit of this analysis is straightforward: identify unhappy customers before they walk out the door. With a reliable prediction model, a retention team can proactively reach out with personalized offers, address service issues, or simply check in. Even preventing 10-15% of predicted churners from leaving could translate to significant annual revenue savings. Beyond the numbers, this approach shifts the business from reactive firefighting to proactive customer care, a competitive advantage in a crowded market.
