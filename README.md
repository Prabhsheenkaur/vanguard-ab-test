# 📊 Vanguard A/B Test — CX Team
This repository contains an end-to-end analysis of a Vanguard UX A/B test, using Python for data cleaning and Tableau for exploration and dashboards to evaluate whether a redesigned interface improves client funnel completion and engagement.

The project covers client demographics, behavioral activity (logins and calls), and step-by-step funnel progression to assess whether the new interface encourages more users to complete the process.


## 🎯 Project Objective
To evaluate whether a redesigned customer interface improves completion of a multi-step client process.

Specifically, we aimed to:
- Measure funnel completion from Start → Confirmed
- Compare Test vs Control performance
- Identify drop-off points and usability friction
- Validate whether the experiment groups are comparable
- Provide evidence-based recommendations for a rollout decision

## 📈 Key Insights
Funnel Performance
- Test group shows higher overall completion rates
- Largest drop-off occurs early: Start → Step 1
- Step 1 is the primary friction point

Engagement Trends
- Logins decline month-over-month in both groups
- Test drops more sharply in May, suggesting possible usability issues
- Higher logins correlate with higher support calls

Demographics
- Majority of clients aged 26–65
- Older users complete less frequently, indicating accessibility gaps

Financial & Membership
- Account balances increase with more accounts, but extreme values are unstable
- Both groups show similar tenure distributions (5–6 years peak)

Experiment Reliability
- Test group is 14% larger
- Partial months (March & June)
- Null/missing segments
  → Results are directional, not definitive


## ⭐ Executive Summary

The redesigned interface shows promising signs, with higher completion rates in the Test group. However, engagement trends and experiment design limitations reduce confidence in the results.

While the new UI may reduce friction for many users, the larger Test group, partial-month data, and inconsistent account distributions introduce bias. Because of these issues, the findings should be treated as indicative rather than conclusive.

A controlled rerun with balanced groups and a consistent timeframe is recommended before making a production decision.


## 🚀 Business Impact

For Product & UX Teams
- Identify critical friction points (especially Step 1)
- Prioritize usability improvements early in the journey
- Design accessibility enhancements for senior clients

For Operations / Support
- Understand relationship between logins and support calls
- Reduce unnecessary calls through clearer flows

For Leadership
- Make rollout decisions based on measurable funnel performance
- Validate product changes through structured experimentation


## ⚠️ Limitations

This analysis has several constraints:
- Unequal Test vs Control group sizes (+14% Test)
- Partial months included (March & June)
- Null segment with missing demographic data
- Small samples for high-account clients (unstable averages)
- Observational rather than fully controlled experimental conditions
As a result, conclusions are directional and not statistically definitive.


## 📁 Repository Structure

vanguard-ab-test/
│
├── data raw/                     # Raw text datasets (ignored via .gitignore)
├── data clean/                   # Cleaned/processed datasets
│
├── vanguard_data_raw_cleaning.ipynb   # Python/Pandas data preparation
│
├── vanguard_ab_test_MAIN_FILE.twbx    # Final Tableau dashboards & story
├── vanguard_ab_test_START_FILE.twbx   # Initial Tableau version
│
└── README.md


## 🛠️ Data Overview

The dataset consists of four raw text exports:
- Demographics
   https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_demo.txt
- Experiment assignment (Control/Test labels)
   https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_experiment_clients.txt
- Web activity (Part 1)
   https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_web_data_pt_1.txt
- Web activity (Part 2)
   https://github.com/data-bootcamp-v4/lessons/blob/main/5_6_eda_inf_stats_tableau/project/files_for_project/df_final_web_data_pt_2.txt

Data includes:
- Client demographics (age, gender, tenure)
- Experiment group assignment
- Logins and calls
- Step-by-step funnel behavior
- Account and financial metrics

~70,000 total clients analyzed.


## 🧹 Data Cleaning Workflow

Performed using Python (Pandas):
- Merge multiple raw datasets
- Remove duplicates
- Handle missing values and Null segments
- Create age groups and behavioral features
- Aggregate activity per client
- Prepare structured datasets for Tableau
All analysis and visualization were then conducted in Tableau.


## 📊 Methods & Tools

Python (Pandas)
- Data cleaning and preprocessing

Tableau Public/Desktop
- Exploratory data analysis
- Dashboards & visualizations
- Funnel analysis
- Month-over-Month comparisons
- Story presentation

Git/GitHub
Version control and collaboration


## 🔗 Dashboard & Presentation

Tableau Public Story:
https://public.tableau.com/app/profile/sana.aarsman/viz/vanguard_ab_test_MAIN_FILE_17695015283890/Presentation?publish=yes



