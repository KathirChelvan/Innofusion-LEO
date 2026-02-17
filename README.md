# 🧠 AI-Powered Credit Risk Underwriting System  
### 🚀 Hackathon Submission – Innofusion LEO  

<p align="center">
  <img src="https://img.shields.io/badge/Machine%20Learning-Random%20Forest-success">
  <img src="https://img.shields.io/badge/ROC--AUC-0.75-blue">
  <img src="https://img.shields.io/badge/Dataset-40K%20Loans-orange">
  <img src="https://img.shields.io/badge/Default%20Rate-10.8%25-red">
  <img src="https://img.shields.io/badge/Status-End--to--End%20Pipeline-brightgreen">
</p>

---

## 🔗 Live Notebook

👉 **Google Colab:**  
https://colab.research.google.com/drive/1LouZrCq95toclTv489ahio8EtVSZPwLM?usp=sharing  

Fully executable end-to-end underwriting simulation.
Load Notebook Manually into Colab
If you cloned the repository:
Go to:
https://colab.research.google.com
Click Upload
Upload:
leo.ipynb

Once opened, click:
Runtime → Run All
---

# 📌 Project Overview

This project builds a complete **AI-powered credit risk underwriting engine** that enables financial institutions to:

✔ Predict Probability of Default (PD)  
✔ Optimize loan approval strategies  
✔ Implement risk-based pricing  
✔ Estimate expected portfolio losses  
✔ Perform real-time applicant evaluation  

The solution transforms historical loan data into a deployable underwriting decision system.

---

# 🎯 Problem Statement

Financial institutions must balance:

- 📈 Loan approval growth  
- ⚠ Credit risk exposure  
- 💰 Profitability  
- 🏦 Capital allocation  

Traditional rule-based underwriting is inefficient and rigid.

This system introduces:

- Data-driven approval decisions  
- Risk-tier segmentation  
- Pricing optimization  
- Portfolio-level risk monitoring  

---

# 📊 Dataset Overview

**Total Records:** 40,000 loans  
**Default Rate:** ~10.8%

### Features Include:

- Loan Amount  
- Interest Rate  
- Annual Income  
- Debt-to-Income (DTI)  
- Employment Length  
- Delinquencies  
- Credit Limits  
- Loan Status (Target Variable)

### 🎯 Target Variable

| Value | Meaning |
|-------|---------|
| 0 | Fully Paid / Current |
| 1 | Default |

---

# ⚙️ Machine Learning Pipeline

## 1️⃣ Data Preprocessing

- Removed high-cardinality features  
- Stratified train-test split (80/20)  
- Missing value imputation  
- One-hot encoding  
- Feature alignment  

---

## 2️⃣ Models Implemented

| Model | Purpose | ROC-AUC |
|-------|---------|---------|
| Logistic Regression | Baseline | ~0.56 |
| **Random Forest (Final Model)** | Nonlinear risk capture | **~0.75** |

### Why Random Forest?

- Captures nonlinear relationships  
- Handles feature interactions  
- Class balancing enabled  
- Strong discrimination across risk tiers  

---

# 📈 Risk Segmentation Framework

Borrowers are segmented using **Predicted Probability of Default (PD):**

| Risk Tier | PD Range | Strategy |
|------------|----------|----------|
| 🟢 Low Risk | < 0.2 | Approve |
| 🟡 Medium Risk | 0.2 – 0.4 | Conditional Approval |
| 🔴 High Risk | > 0.4 | Reject / Manual Review |

Clear separation between risk bands enables smarter portfolio management.

---

# 💰 Approval Strategy Optimization

Using **decision threshold = 0.3**:

- Improves detection of high-risk borrowers  
- Reduces portfolio exposure  
- Maintains strong approval rate  

Dynamic thresholding can adapt to:

- Economic downturns  
- Regulatory requirements  
- Capital constraints  

---

# 💵 Risk-Based Pricing Engine

Where:

- **PD** → Predicted Probability of Default  
- **Exposure** → Loan Amount  
- **LGD** → Loss Given Default (Assumed 60%)  

### Pricing Strategy

| Risk Tier | Pricing Recommendation |
|------------|-----------------------|
| Low Risk | Standard Interest Rate |
| Medium Risk | +2% Risk Premium |
| High Risk | High Premium or Decline |

This ensures pricing is aligned with quantified borrower risk.

---

# 🛡 Risk Management Framework

✔ Risk-tier monitoring  
✔ Early-warning high PD flagging  
✔ Capital allocation via expected loss  
✔ Portfolio diversification strategy  
✔ Dynamic approval thresholds  

---

# 🤖 Real-Time Applicant Evaluation

The notebook includes:

```python
evaluate_applicant(applicant_dict)


### Expected Loss Formula

