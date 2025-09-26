# Diabetes-Patient-Data-Analysis-Dashboard-US-130-Hospital-Dataset

# Project Overview
This project analyzes hospital patient data from 130 US hospitals to provide insights into diabetes management, readmissions, and medication patterns. Using Python for Exploratory Data Analysis (EDA) and Power BI for visualization, this dashboard highlights trends in diagnoses, hospital stays, medications, and patient demographics. The goal is to create a comprehensive, interactive dashboard for healthcare stakeholders to quickly understand key metrics and identify areas for clinical focus.

# Dataset
 - Source: US 130 Hospitals Diabetes Dataset
 - Content: Patient encounter records with the following columns (not exhaustive):
 - encounter_id, patient_nbr, race, gender, age, weight, admission_type_id, discharge_disposition_id, admission_source_id, time_in_hospital, payer_code, medical_specialty, num_lab_procedures, num_procedures, num_medications, number_outpatient, number_emergency, number_inpatient, diag_1, diag_2, diag_3, number_diagnoses, max_glu_serum, A1Cresult, Medication columns: metformin, repaglinide, nateglinide, …, insulin, glipizide-metformin, etc., change, diabetesMed, readmitted
 - Size: ~100k+ patient encounters

# Project Phases

 # Phase 1: Data Collection & Cleaning
   - Imported the dataset in Python using Pandas.
   - Handled missing values:
   - Replaced None in lab test columns (max_glu_serum, A1Cresult) with “Not Tested”.
   - Filled missing medical_specialty with Unknown.
   - Unpivoted medication columns to create a Medication table for interactive analysis in Power BI.

 # Phase 2: Exploratory Data Analysis (EDA)
   - Performed EDA in Python and Excel to uncover insights:
   - Distribution of diagnoses (diag_1, diag_2, diag_3)
   - Readmission trends by age, gender, and diagnosis
   - Hospital stay patterns (time_in_hospital)
   -  prescribed medications and combinations
   - Correlation analysis between hospital stay, readmission, and lab tests

# Phase 3: Dashboard Development in Power BI
   - Key features of the dashboard:
   - Overview Page
   - KPI cards: Total Admissions, Average Hospital Stay, Readmission Rate, Average number of Diagnosis per Patient
   - Bar charts: Top Diagnoses, Top Medications
   - Age and Gender distributions
   - Heatmap: Diagnosis Category vs Readmission Rate
   - Drill-through Pages
   - Detailed patient data for Diagnosis and Medication
   - Filtered automatically when user drills through from Overview page
   - Slicers & Interactivity
   - Filter by medications, diagnosis, age group, and gender
   - Back buttons implemented on drill-through pages
   - Design Highlights:
   - Clean layout: KPIs on top, trends in the middle, detailed tables at the bottom
   - Color-coded heatmaps for quick insights

 # Key Insights
   - Mental disorders are the most prevalent diagnosis category.
   - Pioglitazone and Rosiglitazone are the top prescribed medications.
   - Elderly patients have higher hospital admissions and longer hospital stays.
   - Readmission rates increase with age and the number of medications administered.

# How to Use
   - Open Diabetes_Dashboard.pbix in Power BI Desktop.
   - Navigate the Overview page for KPIs and high-level charts.
   - Right-click on a Diagnosis or Medication data point to drill through into detailed patient information.
   - Use slicers to filter data interactively by medications, diagnosis, age, or gender.

# Technologies & Tools
   - Python (Pandas, NumPy, Matplotlib, Seaborn) – EDA & data cleaning
   - Excel – basic charts and quick summaries
   - Power BI – interactive dashboard creation, drill-through pages, KPIs, and heatmaps
