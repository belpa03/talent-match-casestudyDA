# 🧠 Talent Match Intelligence – AI-Powered Talent Matching System  
A three-stage analytics project combining Success Pattern Discovery, SQL logic design, and an interactive AI-driven Streamlit dashboard.

This repository contains the full end-to-end workflow for the **Talent Match Intelligence Case Study (Data Analyst 2025)**.  
The goal is to simulate how Company X identifies the drivers of employee success and computes talent–role match scores for succession and hiring.

---

## 📌 Project Overview  
This project follows the official case-study flow:

### **1️⃣ Success Pattern Discovery (Exploration & Insights)**  
Analyze what differentiates high performers (rating 5) using:  
- Competency pillars (10-pillar model)  
- Psychometric assessments (PAPI, MBTI, DISC, IQ, GTQ, TIKI, Pauli, Faxtor)  
- Behavioral themes (CliftonStrengths)  
- Organizational context (grade, tenure, education, position, department)

This phase produces:
- Storytelling visuals (heatmaps, radar charts, correlation grids)  
- Insights explaining *why* employees succeed  
- A **Success Formula**: weighted structure of Talent Variables (TV) and Talent Group Variables (TGV)

---

### **2️⃣ SQL Logic Design (Operationalizing Success Formula)**  
SQL is used to compute Talent Match Scores for every employee based on user-selected benchmark employees.

The query implements:
- Dynamic baseline aggregation (median scores of chosen benchmarks)  
- TV Match Rate (numeric, categorical, directional scoring)  
- TGV Match Rate (group-level averages)  
- Final Match Rate (weighted across TGVs)

Expected output includes:
- `employee_id`, `fullname`, `directorate`, `position`, `grade`  
- `tgv_name`, `tv_name`, `baseline_score`, `user_score`  
- `tv_match_rate`, `tgv_match_rate`, `final_match_rate`

All SQL is documented, modular, and built with clean CTE structure.

---

### **3️⃣ AI Talent App & Dashboard (Streamlit Application)**  
A lightweight Streamlit dashboard that dynamically:

- Accepts runtime user inputs:
  - Role name  
  - Job level  
  - Role purpose  
  - Benchmark employee IDs  
- Regenerates the SQL logic  
- Recomputes baselines and match rates  
- Generates job requirements using an LLM  
- Visualizes match results and strengths/gaps

Output includes:
- Ranked employee list  
- Radar + bar + heatmap comparisons  
- AI-generated job profile  
- Clear insights for non-technical stakeholders  

The app is deployed publicly for review.

---

## 📁 Repository Structure  

