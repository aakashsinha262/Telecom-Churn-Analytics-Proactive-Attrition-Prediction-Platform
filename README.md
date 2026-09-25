# 📡 Telecom Customer Churn Intelligence & Retention Platform

An end-to-end data analytics and predictive machine learning project built using **Microsoft SQL Server**, **Power BI**, **ML(Random Forest)** and **Python (Scikit-Learn)**. 

The project diagnoses historical attrition patterns across **6,418 telecom subscribers** (overall **27.0% churn rate**), identifies key demographic and operational risk factors, and deploys a **Random Forest classification pipeline** to forecast churn likelihood among newly onboarded customers.

---

## 📌 Executive Summary & Key Insights

* **Total Customer Base:** 6,418 customers with 1,732 total churned users (**27.0% churn rate**).
* **Demographic Exposure:** Female subscribers accounted for **64% of total churn**, heavily concentrated in the **>50 age group**.
* **Primary Attrition Driver:** **761 cancellations** were directly triggered by competitor pricing and offerings.
* **Contract Risk:** Month-to-month contracts demonstrated the highest attrition velocity, accounting for **355 anticipated churners** in prospective cohorts.
* **Payment Behavior Risk:** Customers paying via Credit Card accounted for the highest single payment segment at risk (**192 projected churners**).

---

## 🛠️ Tech Stack & Architecture

| Layer | Tools / Technologies | Key Implementations |
| :--- | :--- | :--- |
| **Data Cleaning & Extraction** | Microsoft SQL Server, T-SQL | Staging views (`vw_ChurnData`, `vw_JoinData`), missing value imputation, deduplication |
| **Predictive Modeling** | Python, Pandas, Scikit-Learn, Joblib | Random Forest Classifier, Label Encoding, Train/Test Split, Model Serialization |
| **Interactive BI & Analytics** | Power BI Desktop, DAX, Power Query | Star Schema modeling, automated KPI cards, multi-page drill-through reporting |

---

## 🏗️ Project Architecture & Workflow

```mermaid
flowchart LR
    A[Raw Telecom Data] --> B[Microsoft SQL Server]
    B -->|Cleaned Views| C[Python ML Pipeline]
    B -->|Direct Query / Import| D[Power BI Dashboard]
    C -->|Batch Predictions .CSV| D
    D --> E[Actionable Retention Insights]
