# **Root Cause Analysis for Tear-offs on Aluminum Beverage Cans** 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vblP6z-EeI2WSIT2oHVoMe6NBybU6GoC?usp=sharing)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Completed-success)]()

> **Role:** Process Engineer / Data Science Intern Candidate
> **Domain:** Manufacturing & Quality Control (Aluminum Cans)

---

## ** Executive Summary**
In the aluminum beverage can manufacturing process, **"Tear-offs"** (cans tearing during the ironing process) are a critical defect that leads to machine downtime and material waste.

This project applies **Data Science techniques** to solve this engineering problem. By simulating sensor data from a Bodymaker machine, we identify the root causes of defects using **SQL for data extraction**, **Statistical Analysis**, and **Machine Learning**.

### ** Note on Data**
Due to the proprietary nature of industrial data (Thai Beverage Can Ltd.), this project utilizes **Synthetic Data** generated via Python. The data logic is designed to mimic real-world engineering behaviors.

---

## ** Project Roadmap & Methodology**

This project is divided into 3 strategic phases to mimic a real-world problem-solving workflow:

### **Phase 1: Data Extraction & Simulation (SQL)** 
* **Objective:** To replicate the factory environment and retrieve relevant sensor data.
* **Action:**
    * Generated **1,000 production logs** simulating a Bodymaker machine.
    * Utilized **SQL (SQLite)** to query and filter data specifically during high-pressure events.
* **Key Skill:** `SQL Querying`, `Data Simulation`, `Database Management`

### **Phase 2: Exploratory Data Analysis (EDA)** 
* **Objective:** To visualize anomalies and scientifically define "Normal" vs. "Abnormal" conditions.
* **Action:**
    * Calculated **Z-scores** and **3-Sigma Thresholds** based on Statistical Process Control (SPC).
    * Visualized data distributions to spot outliers.
* **Finding:** Defects significantly cluster when **Ironing Pressure > 135 Bar**.
* **Key Skill:** `Data Visualization` (Matplotlib/Seaborn), `Statistical Analysis`

### **Phase 3: Root Cause Analysis (Machine Learning)** 
* **Objective:** To automate the detection of critical factors causing the defects.
* **Action:**
    * Trained a **Decision Tree Classifier** to predict Tear-off events.
    * Analyzed **Feature Importance** to rank the most critical sensors.
* **Result:** The AI model identified **Coolant Temperature** and **Ironing Pressure** as the dominant root causes.
* **Key Skill:** `Scikit-learn`, `Decision Tree`, `Feature Engineering`

---

## ** Key Findings & Business Impact**

| Parameter | Critical Threshold | Engineering Insight |
| :--- | :--- | :--- |
| **Ironing Pressure** | **> 135 Bar** | Indicates excessive friction during the forming process. |
| **Coolant Temp** | **> 53.15°C** | Symptom of overheating, leading to material fatigue and tearing. |

### **Recommendations:**
1.  **Real-time Alarm:** Set an automated alert in the SCADA system when Coolant Temperature exceeds **53°C**.
2.  **Preventive Maintenance:** Inspect the ironing rings and coolant flow rate immediately if pressure spikes above **130 Bar**.

---

## ** Tools & Technologies Used**

<p align="left">
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" alt="numpy" width="40" height="40"/>
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/>
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="sql" width="40" height="40"/>
</p>

---

## ** How to Run This Project**

You can reproduce the entire analysis directly in your browser without installing anything:

1.  Click the **"Open in Colab"** badge at the top of this page.
2.  Run the notebook cells sequentially (Runtime > Run all).
3.  Observe the generated data, SQL queries, and ML model outputs.

---

## ** License**
Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">
  
**Developed by Tharika Puntlert**   
*Bridging the gap between Manufacturing Engineering and Data Science.*

</div>
