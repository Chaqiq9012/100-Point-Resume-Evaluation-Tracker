# Talent Intelligence Hub: Candidate Scoring Matrix

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-0078D4?style=for-the-badge&logo=windows&logoColor=white)

<img width="1324" height="742" alt="Screenshot 2026-03-17 165254" src="https://github.com/user-attachments/assets/4ee91f9c-adbf-402e-9125-ecf7bd45e2d6" />

## 📌 Project Overview
In high-volume recruitment, Applicant Tracking Systems (ATS) often struggle to surface the best candidates efficiently. This project tackles that challenge by analyzing a dataset of **200,000 synthetic resume records**. 

The goal of this project was to design a **100-Point Candidate Scoring System** based on historical hiring data and build an interactive Power BI dashboard to help HR teams and technical recruiters instantly identify top-tier talent.

## 🛠️ Tech Stack & Workflow
* **Exploratory Data Analysis (EDA):** `MySQL` 
* **Data Cleaning & ETL:** `Power Query` (M Code)
* **Data Visualization & UI Design:** `Power BI` (DAX)

---

## ⚙️ The 100-Point Scoring System
Rather than relying on basic keyword matching, I engineered a custom scoring algorithm within Power Query to evaluate candidates objectively across four main pillars:
1. **Experience & Internships (40%)** - Prioritizing proven track records.
2. **Technical Capabilities (30%)** - Evaluating hard skills and programming language breadth.
3. **Proof of Application (15%)** - Rewarding proactive building (Projects, Hackathons).
4. **Baseline Requirements (15%)** - Factoring in soft skills, education, and certifications.

Candidates were then segmented into actionable tiers: **Top Tier (Must Interview)**, **Mid Tier (Backup Pool)**, and **Low Tier (Reject)**.

---

## 🚀 Project Workflow

### Phase 1: Data Exploration (MySQL)
Before importing 200K rows into Power BI, I utilized **MySQL** to understand the dataset's architecture and uncover initial patterns:
* Queried the database to find the baseline historical hire rate (~70%).
* Identified the variables with the highest correlation to successful hires (Experience, Skills Score, and Project counts).
* Discovered data anomalies (e.g., negative word counts in the resume length column) that needed to be addressed in the ETL phase.

### Phase 2: Data Cleaning & Transformation (Power BI / Power Query)
Data transformation was handled entirely within **Power Query** to ensure a repeatable ETL pipeline:

<img width="1915" height="968" alt="Screenshot 2026-03-17 154144" src="https://github.com/user-attachments/assets/6b94fcaf-cd99-40fa-8cad-e56eb3600dde" />

* **Data Quality Fixes:** Applied Absolute Value transformations to correct negative values in the `resume_length_words` column.
* **Feature Engineering:** Built a complex Custom Column using conditional logic to generate the `Total_Candidate_Score` (out of 100) for every row, automating the resume evaluation process.
* **Categorization:** Created the `Candidate_Tier` grouping to allow for high-level dashboard filtering.

### Phase 3: Dashboard Design (Power BI)
I designed the dashboard using a "Deep Trust & High Tech" brand identity (Navy Blue & Electric Teal) to mimic a premium enterprise application. 

**Key Dashboard Features:**
* **Macro KPI Banner:** Instantly tracks Total Candidates, Average Score, and Historical Hire Rates.
* **Candidate Tier Slicers:** Allows recruiters to instantly filter out noise and focus only on the "Top Tier" segment.
* **Experience vs. Quality Scatter Plot:** Helps recruiters spot "Hidden Gems"—candidates with lower years of experience but exceptionally high technical scores.
* **The "Call List" Matrix:** A bottom-line table sorted by Candidate Score, giving recruiters the exact IDs to contact immediately.

---

## 💡 Key Business Insights
1. **Experience is King, but Projects matter:** While years of experience had the highest correlation to getting hired, candidates with low experience but 3+ projects scored significantly higher than their peers.
2. **Education is just a baseline:** The data revealed that having a Master's or PhD did not significantly alter the hire rate compared to a Bachelor's degree, indicating that technical skills heavily outweigh academic pedigree in this dataset.

## 📂 Repository Structure
* `resume_dataset_200k_enhanced.csv`: The raw dataset used for this project.
* `Talent_Intelligence_Hub.pbix`: The final Power BI dashboard file.

---
*Developed by [Your Name/GitHub Profile]*
