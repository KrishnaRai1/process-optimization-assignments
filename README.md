# Process Optimization (CH62001) - Assignments 1 & 2
### Department of Chemical Engineering, Indian Institute of Technology (IIT) Kharagpur
**Instructor:** Dr. Amandeep Jindal  
**Student:** Krishna Rai  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/KrishnaRai1/process-optimization-assignments/blob/main/GPU_Thermal_Optimization_Assignment_1_and_2.ipynb)

---

## Project Title
**Data-Driven Optimization of GPU Thermal Operating Point in HPC Data Centers: From Single-Variable to Multi-Variable System Co-Optimization**

## Overview
This repository contains the complete, consolidated Google Colab notebook for **Assignment 1** and **Assignment 2**:

1. **Assignment 1 (Single-Variable Optimization):**
   - Telemetry data ingestion from NREL HPC Eagle supercomputer.
   - Cubic power model regression: $P(T) = aT^3 + bT^2 + cT + d$ ($R^2 = 0.9755$).
   - Single-variable Newton-Raphson optimization of GPU operating temperature setpoint $T_{GPU}$ with fixed ambient $T_a = 25^\circ\text{C}$.
   - Convergence to $T^* = 52.29^\circ\text{C}$ with second derivative verification $J''(x^*) = 0.5103 > 0$.
   - Sensitivity analysis on cooling priority weight $\lambda_c \in [0.1, 10.0]$.

2. **Assignment 2 (Multi-Variable Optimization Extension):**
   - Extension to coupled 2-variable decision vector: $\mathbf{T} = [T_{GPU}, T_{supply}]^T$ (GPU operating temperature setpoint and facility chilled supply temperature).
   - Coupled thermodynamic objective balancing silicon leakage power, fan convective airflow, Carnot chiller refrigeration lift, and thermal stress risk.
   - Multi-variable Newton-Raphson method with Levenberg-Marquardt spectral modification and Armijo backtracking line search.
   - Comparative benchmark with Multi-variable Gradient Descent (Cauchy Steepest Descent).
   - Optimality verification via Hessian eigensystem analysis (strictly positive definite: $\lambda_1, \lambda_2 > 0$, $\det(\mathbf{H}) > 0$).
   - 3D objective landscape mesh and 2D contour maps with optimization trajectories.
   - Seasonal sensitivity analysis across outdoor design temperatures $T_{outdoor} \in [25^\circ\text{C}, 45^\circ\text{C}]$.

3. **Presentation & Course Reflection:**
   - Personalization and engineering context.
   - Detailed quantitative and algorithmic comparison: *"How Easy/Difficult It Became to Solve When It Became Multi-Variable"*.
   - Student reflection and feedback note for Dr. Amandeep Jindal.

---

## Colab Access Link
Click below to open the complete interactive notebook directly in Google Colab:  
👉 **[Open in Google Colab](https://colab.research.google.com/github/KrishnaRai1/process-optimization-assignments/blob/main/GPU_Thermal_Optimization_Assignment_1_and_2.ipynb)**
