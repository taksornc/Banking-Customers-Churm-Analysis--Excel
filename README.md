# Banking Customer Churn Analysis

An end-to-end data analytics project exploring customer retention and churn patterns for a retail banking dataset (10,000 customers). This repository includes dataset preprocessing, exploratory data analysis (EDA), statistical hypothesis testing, logistic regression modeling, and interactive dashboard preparation in Microsoft Excel.

---

## Project Overview

Customer churn poses a significant financial risk to retail banks. The primary objective of this project is to identify key risk drivers causing customers to close their accounts (`Exited = 1`) and build analytical models to predict potential churners, enabling proactive retention strategies.

### Key Objectives
* **Identify Churn Drivers:** Analyze demographic, behavioral, and transactional attributes influencing customer attrition.
* **Statistical Validation:** Perform $t$-tests and correlation analyses to confirm significant factors driving churn.
* **Predictive Modeling:** Build and evaluate Logistic Regression models (handling class imbalance via undersampling techniques).
* **Interactive Visualization:** Develop pivot tables and dashboard mockups for stakeholder reporting.

---

## Dataset Summary

The dataset consists of **10,000 customer records** across 21 features:

| Category | Features Included |
| :--- | :--- |
| **Demographics** | `Geography` (France, Spain, Germany), `Gender`, `Age`, `Age Group` |
| **Account Info** | `Tenure`, `Tenure group`, `Balance`, `NumOfProducts`, `HasCrCard` |
| **Customer Behavior** | `IsActiveMember`, `EstimatedSalary`, `Complain`, `Satisfaction Score`, `Point Earned` |
| **Credit Profile** | `CreditScore`, `Credit score Group`, `Card Type` (SILVER, GOLD, PLATINUM, DIAMOND) |
| **Target Variable** | `Exited` ($0 = \text{Retained}, 1 = \text{Churned}$) |

---

## Key Insights & Findings

* **Customer Complaints:** A strong correlation exists between logged complaints (`Complain = 1`) and churn rate.
* **Age Factor:** Older demographics (`Age Group` 46–60) show significantly higher churn propensity compared to younger age brackets.
* **Geographic Trends:** Customers in **Germany** exhibit a higher churn rate compared to those in France and Spain.
* **Product Engagement:** Customers holding **3 or 4 products** demonstrate higher churn risk, suggesting possible product mis-fit or over-bundling issues.
* **Activity Level:** Non-active members (`IsActiveMember = 0`) are substantially more likely to leave the bank.

---

## Project Structure & Workflow

The workbook `bank customer churn (update).xlsx` is structured into dedicated analysis stages:

```text
├── Bank_churn                  # Raw & Binned Dataset (10,000 rows)
├── Exploratory Data Analysis   # Summary Statistics & Feature Distributions
├── t test                      # Hypothesis Testing (Mean Comparisons)
├── correl                      # Correlation Matrix
├── Logistic Reg imbalance      # Initial Logistic Regression Model
├── Logist undersampling        # Balanced Logistic Regression (Undersampled)
├── pivot table                 # Cross-tabulations & Segment Summaries
├── pivot for dashboard         # Structured Aggregations for Charts
└── Dashboard(link)             # Executive Dashboard Layout
