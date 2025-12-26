# Customer Churn Analysis: A Business Report

## Reducing Customer Loss in Telecommunications

---

## Executive Summary

**The Problem:** Our telecommunications company loses approximately 1 in 4 customers. This report identifies *why* customers leave and *who* is most likely to leave next—enabling proactive intervention before it's too late.

**Key Finding:** We can now identify which customers are at risk of leaving with 84% reliability (ROC-AUC), catching 78% of churners before they leave. This gives the business a powerful tool to reduce churn and protect revenue.

**Bottom Line:** By focusing retention efforts on the right customers with the right interventions, we estimate potential savings of **$370,000 to $740,000** in protected revenue (based on conservative assumptions).

---

## The Business Challenge

### What is Churn?

Customer churn occurs when a subscriber cancels their service. In telecommunications, industry research suggests acquiring a new customer costs significantly more than retaining an existing one. Every customer who leaves represents:

- Lost monthly recurring revenue
- Wasted acquisition costs
- Potential negative word-of-mouth
- Market share given to competitors

### Our Current Situation

We analyzed **7,043 customer records** to understand churn patterns:

| Metric | Value |
|--------|-------|
| Total Customers Analyzed | 7,043 |
| Customers Who Left | 1,869 |
| Customers Who Stayed | 5,174 |
| **Overall Churn Rate** | **26.54%** |

**This means more than 1 in 4 customers are leaving.**

---

## Who Is Leaving? Key Discoveries

Our analysis revealed clear patterns in customer departures. The findings below highlight the most significant factors affecting churn.

### 1. Contract Type: The #1 Factor

The type of contract a customer holds is the single strongest predictor of whether they will leave.

| Contract Length | Churn Rate | Risk Level |
|-----------------|------------|------------|
| Month-to-month | **42.7%** | 🔴 Very High |
| One-year | 11.3% | 🟡 Moderate |
| Two-year | **2.8%** | 🟢 Very Low |

**Insight:** Customers without long-term commitments are 15 times more likely to leave than those on two-year contracts.

### 2. Customer Tenure: The First Year Is Critical

How long a customer has been with us dramatically affects their likelihood of staying.

| Time with Company | Churn Rate | Risk Level |
|-------------------|------------|------------|
| 0-12 months | **47.4%** | 🔴 Very High |
| 12-24 months | 28.7% | 🟠 High |
| 24-48 months | 20.4% | 🟡 Moderate |
| 48-72 months | **9.5%** | 🟢 Low |

**Insight:** Nearly half of customers in their first year leave. If we can keep customers past the one-year mark, their loyalty increases significantly.

### 3. Service Add-ons: Security Services Retain Customers

Customers who subscribe to our security-related services stay much longer.

| Service | Without Service | With Service | Difference |
|---------|-----------------|--------------|------------|
| Online Security | 41.8% churn | 14.6% churn | -27.2% |
| Tech Support | 41.6% churn | 15.2% churn | -26.4% |

**Insight:** Customers who feel protected and supported are nearly 3 times less likely to leave.

### 4. Internet Service Type: Fiber Optic Concerns

Surprisingly, our premium fiber optic customers are leaving at higher rates than DSL customers.

| Internet Type | Churn Rate | Monthly Cost |
|---------------|------------|--------------|
| Fiber Optic | **41.9%** | $91.50 avg |
| DSL | 19.0% | $58.10 avg |
| No Internet | 7.4% | $21.08 avg |

**Insight:** Fiber optic customers pay more but leave more often—suggesting a potential service quality or value perception issue that warrants investigation.

### 5. Payment Method: Electronic Check Red Flag

How customers pay reveals risk patterns.

| Payment Method | Churn Rate |
|----------------|------------|
| Electronic Check | **45.3%** |
| Mailed Check | 19.1% |
| Bank Transfer (Auto) | 16.7% |
| Credit Card (Auto) | 15.2% |

**Insight:** Customers who pay manually via electronic check are 3 times more likely to churn than those on automatic payments. This may indicate lower engagement or intent to leave.

### 6. Monthly Charges: Price Sensitivity

Higher monthly bills correlate with higher churn risk.

| Monthly Bill Range | Churn Rate |
|--------------------|------------|
| $0-35 | 10.9% |
| $35-55 | 28.0% |
| $55-75 | 27.0% |
| $75-120 | **34.6%** |

**Insight:** Customers paying over $75/month churn at 3 times the rate of those paying under $35.

---

## The Solution: Predictive Modeling

### What We Built

We developed a system that analyzes customer characteristics and predicts who is likely to leave. This enables **proactive intervention** rather than reactive damage control.

### How Well Does It Work?

We tested three different approaches. Here's how they performed:

| Approach | Accuracy | Churn Detection Rate |
|----------|----------|---------------------|
| Logistic Regression | 73.8% | **78.3%** ✓ Best |
| Random Forest | **76.9%** | 70.3% |
| Gradient Boosting | 75.0% | 73.5% |

**What This Means:**
- **Accuracy** = How often the prediction is correct overall
- **Churn Detection Rate** = How many at-risk customers we successfully identify

### Our Recommendation: Logistic Regression Model

We recommend deploying the **Logistic Regression** approach because:

1. **Catches More At-Risk Customers** – Identifies 78.3% of customers who will churn (highest recall)
2. **Highly Reliable** – 84.15% ROC-AUC, meaning strong ability to distinguish churners from loyal customers
3. **Transparent** – We can explain *why* each customer is flagged as at-risk
4. **Fast** – Can score thousands of customers instantly for marketing campaigns

---

## Business Recommendations

Based on our findings, we recommend the following strategic initiatives:

### Immediate Actions (0-3 Months)

#### 1. Launch a "New Customer Success" Program
- **Target:** All customers in their first 12 months
- **Why:** 47.4% churn rate in this period
- **Actions:**
  - Personalized onboarding calls at 30/60/90 days
  - Early detection of service issues
  - Exclusive first-year loyalty benefits

#### 2. Promote Long-Term Contract Conversions
- **Target:** Month-to-month customers
- **Why:** 42.7% churn vs 2.8% for two-year contracts
- **Actions:**
  - Offer meaningful discounts for 1-2 year commitments
  - Bundle with premium features as incentive
  - Time offers around the 6-month mark before peak churn

#### 3. Flag High-Risk Payment Patterns
- **Target:** Customers using electronic check payments
- **Why:** 45.3% churn rate
- **Actions:**
  - Proactively reach out with autopay incentives
  - Offer small discounts for switching to automatic payments
  - Include these customers in retention campaigns

### Medium-Term Actions (3-6 Months)

#### 4. Bundle Security Services
- **Target:** Customers without Online Security or Tech Support
- **Why:** These services reduce churn by 27%
- **Actions:**
  - Promote security bundle packages
  - Offer free trials of security services
  - Position as "peace of mind" value add

#### 5. Investigate Fiber Optic Customer Satisfaction
- **Target:** Fiber optic subscribers
- **Why:** 41.9% churn despite premium pricing
- **Actions:**
  - Survey fiber customers on service quality
  - Review technical support tickets for patterns
  - Assess competitive pricing and value proposition

### Long-Term Strategy (6-12 Months)

#### 6. Implement Predictive Churn Scoring
- **What:** Deploy the predictive model to score all customers monthly
- **How:** 
  - Generate "churn risk scores" for each customer
  - Automatically flag high-risk customers for outreach
  - Measure intervention effectiveness
- **Expected Impact:** Reduce churn by 10-15% through proactive retention

---

## Expected Business Impact

### Conservative Estimate

If we reduce churn by just **10%** (from 26.54% to 23.89%):

| Metric | Current | After 10% Reduction |
|--------|---------|---------------------|
| Expected Churners (of 7,000) | 1,858 | 1,672 |
| Customers Saved | — | **186** |
| Avg. Customer Lifetime Value | $2,000* | $2,000 |
| **Revenue Protected** | — | **$372,000** |

*Illustrative estimate. Actual CLV should be calculated from your company's financial data. Based on ~32 months average tenure × $65 avg monthly charge ≈ $2,080.

### Optimistic Estimate

If targeted interventions reduce churn by **20%**:

| Metric | Value |
|--------|-------|
| Customers Saved | 372 |
| **Revenue Protected** | **$744,000** |

---

## How to Read the Risk

### Customer Risk Profile Summary

A customer is **HIGH RISK** if they have 3+ of these characteristics:

- ☐ Month-to-month contract
- ☐ Less than 12 months tenure
- ☐ No Online Security subscription
- ☐ No Tech Support subscription
- ☐ Fiber optic internet
- ☐ Pays by electronic check
- ☐ Monthly charges over $75

**Example High-Risk Customer:**
> "John has been with us for 4 months on a month-to-month contract. He has fiber optic internet, pays $89/month via electronic check, and has no security services."
> 
> **Risk Score: Very High** – This customer matches all 7 risk factors.

**Recommended Action:** Proactive outreach with a personalized retention offer.

---

## Conclusion

Customer churn is not random—it follows predictable patterns. Our analysis shows that:

1. **We can identify at-risk customers** with 84% reliability (ROC-AUC) before they decide to leave
2. **Contract type and tenure are the strongest predictors** of whether a customer stays
3. **Security services and automatic payments** are associated with loyal customers
4. **The first 12 months are critical** for building customer loyalty

By implementing the recommended actions and deploying our predictive model, we can transform our approach from **reactive** (responding after customers leave) to **proactive** (intervening before they decide to go).

**The cost of inaction is clear:** Without intervention, we continue to lose more than 1 in 4 customers—many of whom could have been retained with proactive engagement.

---

## Appendix: Data Quality Notes

- **Data Source:** Telco Customer Churn Dataset (7,043 records)
- **Data Quality:** 99.84% complete (11 records with minor data issues, appropriately handled)
- **Analysis Period:** Point-in-time snapshot of customer base
- **Validation:** Model tested on held-out data to ensure real-world reliability

---

*Report prepared by the Data Analytics Team*  
*For questions, contact: [Analytics Team]*

