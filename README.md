# Predicting Diabetes Care Gaps Using Machine Learning

### 2026 ASA DataFest | Team Mangaussian

**Team Members:** Seyoung Yoo, Zihang Peng  
**Project:** The Journey Navigation Flag: Turning Diabetes Encounters into Action

---

## Project Overview

This project analyzes longitudinal healthcare data from **Stormont Vail Health (SVH)** to identify gaps in follow-up care among patients with Type 2 diabetes and develop a machine learning-based risk screening tool.

Rather than analyzing individual healthcare visits in isolation, we reconstructed patient journeys to understand patterns in follow-up frequency, care continuity, and potential barriers to accessing healthcare.

**Objective:** Identify patients at risk of insufficient follow-up and help healthcare providers prioritize early interventions.

---

## Methodology

### 1. Data Processing & Feature Engineering

- Integrated patient demographics, diagnoses, encounters, healthcare providers, departments, social determinants of health, and census data.
- Constructed patient-level longitudinal journeys to track diabetes-related healthcare utilization.
- Engineered features related to:
  - Follow-up intervals
  - Prior healthcare utilization
  - First-visit characteristics
  - MyChart access
  - Social risk indicators

### 2. Exploratory Data Analysis

- Analyzed follow-up patterns across **22,155 Type 2 diabetes patient journeys**.
- Classified patients into distinct journey types based on healthcare utilization and continuity.
- Evaluated annual monitoring patterns across **50,070 patient-year records**.

### 3. Predictive Modeling

- Developed and evaluated classification models to identify patients at risk of not meeting regular diabetes follow-up benchmarks.
- Defined regular annual follow-up as **at least four diabetes-related encounters per year**.
- Evaluated model performance using:
  - ROC-AUC
  - Average Precision (AP)
  - Precision
  - Recall
- Developed a risk-based screening approach to prioritize patients for targeted outreach.

---

## Key Findings

| Finding | Result |
|---|---|
| Type 2 Diabetes Journeys Analyzed | 22,155 |
| No Timely Follow-Up Within 4 Months | 61% |
| Median Time to First Follow-Up | 91 days |
| Annual Diabetes Care Records | 50,070 |
| Records Meeting Regular Follow-Up Benchmark | ~26% |

**Main Insights:**

1. A majority of observed diabetes journeys experienced delayed follow-up or disconnection.
2. Follow-up gaps were concentrated among patients with limited or disconnected healthcare journeys.
3. Patients with more connected healthcare pathways were more likely to maintain regular follow-up.

---

## Predictive Model Performance

| Metric | Result |
|---|---|
| ROC-AUC | **0.799** |
| Average Precision (AP) | **0.917** |
| Precision (Top 30% Risk Group) | **94.9%** |
| Recall (Top 30% Risk Group) | **38.2%** |

By targeting the **30% of patients with the highest predicted risk**, the model identified approximately **38.2% of observed care-gap cases**, while maintaining **94.9% precision**.

These results suggest that predictive modeling could help healthcare organizations prioritize outreach resources more effectively.

---

## Proposed Solution: Journey Navigation Flag

We proposed a machine learning-based screening tool that uses early patient information to identify individuals who may require additional follow-up support.

### Proposed Workflow

1. **Patient Encounter:** Collect information from a patient's initial diabetes-related encounter.
2. **Risk Prediction:** Estimate the patient's risk of insufficient regular follow-up.
3. **Risk Flag:** Identify patients with elevated predicted risk.
4. **Targeted Intervention:** Prioritize flagged patients for proactive outreach.

### Potential Interventions

- Follow-up appointment scheduling and reminders
- Transportation assistance
- MyChart and digital healthcare access support
- Social service referrals
- Nurse navigator or care coordinator support

The goal is to shift healthcare delivery from **reactive care to proactive patient outreach**.

---

## Tools & Technologies

| Category | Tools |
|---|---|
| Programming Language | Python |
| Data Manipulation | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Visualization | Matplotlib, Seaborn |
| Development Environment | Jupyter Notebook |

---

## Limitations

- Follow-up encounters outside Stormont Vail Health may not be captured.
- Patient journeys may be incomplete because of limited observation windows.
- Missing social determinant information does not necessarily indicate an absence of social needs.
- The screening tool requires additional validation before real-world clinical deployment.

**Note:** The model is intended to support healthcare outreach and resource allocation, not replace clinical judgment.

---

## Project Impact

This project demonstrates how **longitudinal healthcare analytics and machine learning** can support chronic disease management by:

- Identifying patients at risk of insufficient follow-up.
- Detecting patterns in healthcare utilization.
- Prioritizing targeted outreach and care coordination.
- Supporting more proactive and data-driven healthcare decisions.

**Overall Goal:** Transform historical patient encounter data into actionable insights that can improve continuity of care.
