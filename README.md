<h1 align="center">JPMorgan Chase & Co. — Quantitative Research</h1>
<h3 align="center">Virtual Job Simulation · The Forage · 2026</h3>

<p align="center">
  <img src="https://img.shields.io/badge/JPMorgan%20Chase-Quantitative%20Research-003087?style=for-the-badge&logo=jpmorgan&logoColor=white" alt="JPMorgan"/>
  <img src="https://img.shields.io/badge/The%20Forage-Verified%20Simulation-0A66C2?style=for-the-badge" alt="Forage"/>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Status-Completed-28a745?style=for-the-badge" alt="Completed"/>
  <img src="https://img.shields.io/badge/Duration-6--7%20Hours-FF6B35?style=for-the-badge" alt="Duration"/>
</p>

<p align="center">
  <em>A hands-on simulation replicating real quantitative research work at one of the world's largest investment banks — covering commodity pricing, time-series forecasting, credit risk modelling, and dynamic programming.</em>
</p>

---

## 📋 Table of Contents

- [About This Simulation](#-about-this-simulation)
- [Simulation at a Glance](#-simulation-at-a-glance)
- [Tasks Completed](#-tasks-completed)
- [Technical Skills Used](#-technical-skills-used)
- [Business Problems Solved](#-business-problems-solved)
- [Simulation-to-Real-World Mapping](#-simulation-to-real-world-mapping)
- [Repository Structure](#-repository-structure)
- [Key Achievements (Resume-Ready)](#-key-achievements-resume-ready)
- [How My Thinking Changed](#-how-my-thinking-changed)
- [Industry Insights Gained](#-industry-insights-gained)
- [Connect With Me](#-connect-with-me)

---

## 🏦 About This Simulation

This repository documents my completion of the **JPMorgan Chase & Co. Quantitative Research Virtual Job Simulation** hosted on [The Forage](https://www.theforage.com/simulations/jpmorgan/quantitative-research-11oc).

The **Quantitative Research (QR)** group at JPMorgan Chase is an expert modelling team that partners with traders, risk managers, and portfolio managers across all products and regions. This simulation replicates the actual day-to-day work of a junior Quant — from raw data processing and price forecasting to derivatives pricing and credit risk classification.

> _"Not a course. Not a tutorial. A simulation of real work, with real data, and real business stakes."_

---

## 📊 Simulation at a Glance

| Attribute | Details |
|---|---|
| **Company** | JPMorgan Chase & Co. |
| **Division** | Quantitative Research (QR) |
| **Platform** | The Forage |
| **Total Duration** | 6–7 hours |
| **Completed** | May 2026 |
| **Location** | Bengaluru, India |
| **Tasks** | 4 |
| **Primary Language** | Python |
| **Domain** | Quantitative Finance / Data Science |

---

## ✅ Tasks Completed

### Task 1 — Investigate & Analyze Natural Gas Price Data
> **Domain:** Time Series Analysis · Data Forecasting

**Objective:** A VP on the commodity trading desk wants to begin trading natural gas storage contracts, but the available market data has gaps and lacks granularity. The task is to build a tool that takes any date as input and returns a reliable price estimate — for both past and future dates.

**What I did:**
- Loaded and explored historical natural gas price data (`Nat_Gas.csv`)
- Performed trend analysis and identified seasonal price patterns
- Implemented interpolation for historical gap-filling and extrapolation for 1-year price forecasting
- Wrote a Python function: `get_price(date) → estimated_price`

**Key Techniques:** Linear/polynomial interpolation, time series extrapolation, data visualisation with matplotlib, pandas datetime handling

---

### Task 2 — Price a Commodity Storage Contract
> **Domain:** Financial Derivatives · Contract Valuation

**Objective:** Using the price model from Task 1, calculate the fair value of a natural gas storage contract — factoring in all real-world costs a trader on the desk would face.

**The core financial logic:**
```
Contract Value = (Sell Price − Buy Price) × Volume
               − Injection/Withdrawal Costs
               − Monthly Storage Fees
               − Transport Costs
```

**What I did:**
- Built a `contract_value(inject_dates, withdraw_dates, prices, rate, storage_cost_rate, transport_cost)` function
- Handled multiple injection/withdrawal date pairs
- Validated model logic against real-world commodity trading scenarios

**Key Techniques:** Financial derivatives pricing, Python function design, cost modelling, business logic implementation

---

### Task 3 — Credit Risk Analysis (Probability of Default)
> **Domain:** Machine Learning · Credit Risk · Loan Analytics

**Objective:** Analyse a real book of loan data to estimate each customer's **Probability of Default (PD)** — a core function of JPMorgan's credit risk desk.

**What I did:**
- Explored and cleaned customer loan data (income, loan value, payment history, FICO score)
- Trained a **Logistic Regression** model to predict default probability
- Evaluated model performance using classification metrics (accuracy, AUC-ROC)
- Produced a per-customer PD score for the loan book

**Key Techniques:** Logistic regression, scikit-learn, feature engineering, binary classification, model evaluation

---

### Task 4 — FICO Score Bucketing via Dynamic Programming
> **Domain:** Statistical Optimisation · Algorithm Design

**Objective:** Convert continuous FICO credit scores into discrete categorical buckets to maximise the predictive power of the credit risk model — a common challenge in quantitative risk management.

**What I did:**
- Designed a **dynamic programming** algorithm to find the optimal bucket boundaries
- Maximised log-likelihood (information value) of the buckets for default prediction
- Implemented a generalised solution that accepts any number of desired buckets `n`

**Key Techniques:** Dynamic programming, optimisation, FICO/credit scoring, Python algorithm design

---

## 🛠 Technical Skills Used

### Languages & Libraries

| Category | Tools |
|---|---|
| **Language** | Python 3.x |
| **Data Manipulation** | pandas, NumPy |
| **Machine Learning** | scikit-learn |
| **Time Series** | statsmodels, manual interpolation/extrapolation |
| **Visualisation** | matplotlib |
| **Environment** | Jupyter Notebook / Google Colab |

### Quantitative & Financial Concepts

`Time Series Forecasting` · `Derivatives Pricing` · `Contract Valuation` · `Probability of Default` · `Logistic Regression` · `Dynamic Programming` · `FICO Score Analysis` · `Credit Risk` · `Commodity Markets`

---

## 💼 Business Problems Solved

| # | Business Problem | My Solution |
|---|---|---|
| 1 | Trading desk lacks granular price data for gas contracts | Built a date-input price estimator using interpolation and forecasting |
| 2 | Traders need to know the fair value of a storage contract before signing | Developed a multi-variable pricing function covering all real cost components |
| 3 | Risk team needs per-customer default probabilities across the loan book | Trained and deployed a logistic regression PD classifier |
| 4 | Continuous FICO scores are not directly useful for risk categorisation | Implemented dynamic programming to find statistically optimal risk buckets |

---

## 🔗 Simulation-to-Real-World Mapping

| Simulation Task | Real JPMorgan QR Work |
|---|---|
| Natural gas price estimation | Commodity desk quants build price curves daily for trading decisions |
| Storage contract pricing | Derivatives pricing models underpin every structured commodity trade |
| Probability of Default modelling | PD models are core to Basel III/IV regulatory capital calculations |
| FICO score bucketing | Risk stratification is standard in consumer and corporate lending desks |

---

## 📁 Repository Structure

```plaintext
JPmorgan-Chase-Quantitative-Research/
│
├── analysis.ipynb         ← task 1 & task 2 code file
│
├── loan_analysis.ipynb         ← task 3 & task 4 code file
│
└── README.md                        ← This file
```

---

## 🏆 Key Achievements (Resume-Ready)

- **Developed** a natural gas price forecasting model that estimates prices for any given date, by engineering a time-series interpolation and extrapolation pipeline in Python on historical commodity market data.

- **Delivered** a commodity storage contract pricing engine that calculates net contract value accounting for injection, withdrawal, storage, and transport costs — by implementing a multi-variable financial model aligned with real derivatives desk logic.

- **Built** a credit risk classification model producing probability-of-default predictions across a full loan book, by applying logistic regression on customer financial attributes including income, outstanding debt, and credit history.

- **Optimised** FICO score bucketing for maximum default-prediction accuracy, by designing a dynamic programming algorithm that converts continuous credit scores into statistically meaningful categorical risk tiers.

---

## 🧠 How My Thinking Changed

> _Authentic reflections — not filler._

**Before the simulation**, I understood machine learning and Python as standalone technical skills.

**After the simulation**, I understand that in quantitative finance:

- Models are only valuable if they solve a specific business problem. A forecast that can't be queried by date is useless to a trader.
- Every financial model has a cost structure. Pricing is not just about the upside — it's about rigorously accounting for every fee, every risk, every edge case.
- Credit risk is deeply human. Behind every probability of default is a real person's financial life — that makes the modelling work matter.
- Optimisation is everywhere. Even something as "simple" as grouping credit scores into buckets is a non-trivial mathematical problem when accuracy is at stake.

---

## 💡 Industry Insights Gained

- **Commodity markets** operate on price curves, not single prices. A quant's job is to build the entire curve — not just the today price.
- **Storage contracts** are derivatives in disguise. Their value is entirely driven by the spread between future buy and sell prices, minus all carry costs.
- **PD modelling** is central to how banks comply with Basel capital requirements. Inaccurate models mean either over- or under-reserving capital — both costly to the bank.
- **Dynamic programming** is not just a CS concept — it is actively used in risk stratification, portfolio optimisation, and pricing across quantitative finance.

---

## 🤝 Connect With Me

<p>
  <a href="https://www.linkedin.com/in/manjunathareddyn/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin" alt="LinkedIn">
  </a>
  &nbsp;
  <a href="https://github.com/MrBeastGamerZz">
    <img src="https://img.shields.io/badge/GitHub-MrBeastGamerZz-181717?style=flat-square&logo=github" alt="GitHub">
  </a>
</p>

---

<p align="center">
  <sub>Completed as part of a self-directed professional development program via <a href="https://www.theforage.com">The Forage</a> · May 2026</sub>
</p>

