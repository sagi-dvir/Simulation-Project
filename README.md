# 🏥 Data-Driven Simulation Model for Emergency Department Optimization

## 👥 Authors
**Sagi Dvir**  

---

## 📌 Project Description

This project presents a **Discrete Event Simulation (DES)** model designed to improve **logistics in hospital emergency departments (EDs)**. The model evaluates how adding a **Support-Release Department (SR)** — designated for patients who have completed their treatment but require additional monitoring — impacts patient flow, bed utilization, and average length of stay (LOS) in the ED.

---

## 📚 Background

Inspired by a research article, the simulation addresses the question:

> *How can patient flow and resource usage in emergency departments be improved?*

The original article proposed adding an **ADA unit** for complex patients and expanding **intermediate care (35C)**. This project explores an **additional solution**: introducing a **Support-Release (SR)** department.

---

## 🧪 Objectives

- Evaluate the effect of adding an SR unit on:
  - **Average Length of Stay (LOS)** for different patient types.
  - **Bed utilization rates** in both ED and SR.
- Simulate patient arrival, treatment, and flow using discrete-event modeling.
- Identify optimal allocation of beds between ED and SR to minimize delays.

---

## 🏥 Patient Categories

Patients are divided into four types:
1. **Critical**
2. **Non-Critical**
3. **Complex** (may need CT)
4. **Simple** (can be handled by SR)

---

## 🧾 Model Assumptions

- **Arrival Process:** Non-homogeneous Poisson process; peak hours: 11:00–16:00.
- **Treatment Times:** Exponential distribution in ED and SR.
- **No patient abandonment.**
- **SR Eligibility:** Only simple patients.
- **Post-SR return probability:** Based on historical forecasts.
- **Initial Configuration:** 50 ED beds, 5 SR beds (beds reallocated during experiments).

---

## 🔄 Simulation Design

- **Simulation Horizon:** 2 months
- **Entities:** Four patient types
- **Resources:** ED & SR beds
- **Queues:** FIFO (First-In-First-Out) for both departments
- **Metrics Tracked:**
  - Average wait & treatment time by patient type
  - Bed utilization in ED and SR

---

## 📊 Key Findings

- **Optimal configuration found:** 35 ED beds and 20 SR beds
- This balance:
  - Reduced average LOS for all patient types.
  - Improved flow and resource utilization.
  - Handled increased arrival and treatment times better than the baseline.
- Bed utilization improved, though ED beds remained underutilized in some cases due to cross-source data inconsistencies.

---

## 🧠 Sensitivity Analysis

- Simulated stress tests:
  - **1.5× longer treatment durations**
  - **10× higher arrival rates**
- Results confirmed robustness of SR unit in handling variability.

---

## 🚀 Future Directions

- Integrate predictive tools for patient triage and prioritization.
- Study impact of **human resources** (doctors, nurses) on flow.
- Extend the simulation to include the **entire hospital system**.
- Use **AI-based demand forecasting** for dynamic resource reallocation.
- Include **patient satisfaction metrics**.

---

## 💻 Technologies Used

- **Python**
- **SimPy** (for discrete event simulation)
- **Matplotlib / Seaborn** (for visualization)
- **Jupyter Notebook**

---

## 📁 Files

- `Project_Medical_Healthcare.ipynb`: Simulation code and results
- `Medical Healthcare.pptx`: Presentation slides with visual summary and explanations

---

## 🙏 Acknowledgements

Based on data and insights from:
- NHAMCS, AHRQ, HCUP
- Israeli Ministry of Health (2019 Patient Experience Survey)
- Peer-reviewed literature on emergency department simulation

---

## 📬 Contact

For questions or collaborations, reach out to:  
📧 sagi.dvir@gmail.com  
