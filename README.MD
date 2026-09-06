# Student Academic Performance Analysis & Prediction System

An end-to-end data analytics and predictive modeling system built with Python, Pandas, and NumPy to analyze multi-semester engineering cohorts across multiple institutions, identify curriculum bottlenecks, detect at-risk students, and forecast future academic outcomes.


## 📌 Project Overview
* **Dataset Scope:** 178 student records spanning 5 semesters across 4 colleges and 2 curriculum codes.
* **Core Goal:** Unify fragmented academic schemas, diagnose batch-level trajectory patterns, build a closed-form multivariate regression model without external ML libraries, and generate institutional diagnostic reports.


## ⚙️ Architecture & Pipeline
1. **Schema Unification & Cleaning:** Merged fragmented identifier columns (`Roll` and `Roll no.`) into nullable integer types (`Int64`), resolved label inconsistencies, and handled missing examination data.
2. **Exploratory Data Analysis:** Extracted cohort metrics, identified curriculum difficulty shifts (notable 3rd-semester drop), and analyzed inter-semester correlation matrices.
3. **Predictive Modeling:** Solved Ordinary Least Squares (OLS) multivariate linear regression via `np.linalg.lstsq` using semesters 1–4 to predict semester 5 SGPA.
4. **Early Warning Engine:** Categorized students into actionable operational tiers (`High Achiever`, `Academic Probation`, `Critical Drop`, `Missing Exams`).
5. **Interactive Diagnostic Card:** Built an on-demand profile lookup utility plotting individual student trajectories against predicted benchmarks.
6. **Institutional Export:** Automated batch export of enriched student records and college-level executive summaries.


## 📊 Key Findings
* **Curriculum Dip:** A cohort-wide performance drop occurs in Semester 3 (mean SGPA: 6.62) followed by recovery in Semester 4 and a peak in Semester 5 (mean SGPA: 7.43).
* **Predictive Drivers:** Semester 4 performance exhibits the strongest regression weight ($+0.628$) in forecasting final-semester SGPA.
* **Early Warning:** Identified 24 students requiring academic intervention (13 on probation with CGPA < 6.0, 11 with steep negative deltas $\le -1.0$).


## 🚀 Setup & Usage

### 1. Clone the repository
```bash
git clone https://github.com/SneJ2703/Student-performance-analytics
cd Student-performance-analytics