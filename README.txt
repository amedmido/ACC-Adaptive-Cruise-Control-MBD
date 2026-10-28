# Adaptive Cruise Control (ACC) System - Model-Based Design (MBD)

A comprehensive automotive control project developed in **MATLAB/Simulink** following Model-Based Design (MBD) principles. The system implements a longitudinal vehicle control algorithm (safe distance and relative speed regulation) coupled with a vehicle plant model and automated ANSI C code generation.

---

## 🚗 System Architecture & Workflow

* **Driver & Environment:** Generates set speed references (`v_set`) and dynamic obstacle/lead vehicle trajectory (`v_lead`, `x_lead`).
* **ACC Controller:** Computes required acceleration/deceleration commands based on safety distance headway ($d_{safe} = d_0 + T_{gap} \cdot v$) and speed error.
* **Vehicle Dynamics Plant:** Models vehicle mass, aerodynamic drag, rolling resistance, and actuator response in closed-loop simulation.
* **Automated Code Generation:** Deploys Simulink Coder / Embedded Coder to produce production-grade ANSI C source files from the standalone controller module.

---

## 📊 Key Highlights & Results

* **Closed-Loop Stability:** Verified smooth throttle and braking dynamics without control oscillations during rapid deceleration scenarios.
* **Production C Code:** Generated clean, MISRA-compliant C functions (`step` and `initialize`) for automotive target integration.
* **Model-Based Verification:** Full MIL (Model-in-the-Loop) dynamic validation.

---

## 🛠️ Tech Stack & Tools

* **Modeling & Simulation:** MATLAB, Simulink, Simscape
* **Embedded Software:** Simulink Coder, Embedded Coder, ANSI C/C++
* **Automotive Standards:** Model-Based Design (MBD), ADAS, V-Cycle Workflow