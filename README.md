# 🧑‍⚕️ Optimizing Nurse Workforce Scheduling in a Healthcare Call Centre

## 📋 Project Overview

This project presents an **Integer Linear Programming (ILP)** and **Discrete Event Simulation** model to optimize nurse workforce scheduling in a healthcare call centre. The goal is to **minimize total staffing cost** while meeting varying hourly patient demand and complying with operational constraints. The model is implemented in **Excel Solver** and simulated in **SIMUL8** to evaluate queue performance and nurse utilization.

---

## 🧮 ILP Model Highlights

* **Objective**: Minimize total cost = £80 × full-time nurses + £64 × part-time nurses
* **Decision Variables**:

  * `F`: Full-time nurses (9am–5pm, with 1-hour lunch break)
  * `P1`–`P5`: Part-time nurses starting between 9am and 1pm for 4-hour shifts
* **Constraints**:

  * Cover patient demand (5 patients/hour/nurse)
  * Minimum 4 and max 20 full-time nurses
  * Max 20 part-time nurses
* **Optimal Solution**:

  * 10 full-time nurses
  * 14 part-time nurses (1 at 9am, 9 at 11am, 2 at 12pm, 2 at 1pm)
  * **Total cost: £1,696/day**

---

## 🧪 Simulation Model (SIMUL8)

* **Arrival Rate**: Based on hourly patient demand (exponential distribution)
* **Service Time**: Normally distributed (mean: 12 mins, std dev: 4 mins)
* **Performance Metrics**:

  * Nurse utilization: **80.70%**
  * Avg queue time: **2.01 mins**
  * Max queue time: **9.16 mins**
  * Avg queue size: **2.23 patients**

---

## 📈 Key Insights

* ILP successfully identifies cost-effective staffing while covering all time periods
* Simulation reveals moderate wait times and high nurse efficiency
* System can be fine-tuned to further reduce peak-time delays
* Future improvements could target **more balanced break scheduling** to improve service continuity during lunch hours

---

## 📁 Repository Structure

```
nurse-scheduling-callcentre/
1. ilp-model/              # Excel Solver files for optimization
2. sim-model/              # SIMUL8 files and simulation screenshots
3. report/                 # Full project write-up and charts
4. README.md               # Project overview (this file)
```
