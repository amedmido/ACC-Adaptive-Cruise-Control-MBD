# Adaptive Cruise Control (ACC) System - Model-Based Design (MBD)

An automotive longitudinal control project developed in **MATLAB/Simulink** following Model-Based Design (MBD) principles. The system implements a safety distance headway and relative speed tracking controller coupled with a vehicle dynamics plant and automated ANSI C code generation.

---

## 🚗 System Architecture & Workflow

* **Driver & Environment:** Generates set speed references (`v_set`) and dynamic obstacle/lead vehicle trajectory (`v_lead`, `x_lead`).
* **ACC Controller:** Computes required acceleration/deceleration commands based on safety headway distance ($d_{safe} = d_0 + T_{gap} \cdot v$) and speed error.
* **Vehicle Dynamics Plant:** Models vehicle mass, aerodynamic drag, rolling resistance, and actuator response in closed-loop simulation.
* **Automated Code Generation:** Deployed Embedded Coder / Simulink Coder to produce production-grade ANSI C source files from the standalone atomic controller module.

---

## 📊 Key Highlights & Results

* **Closed-Loop Stability:** Verified smooth throttle and braking dynamics without control oscillations during rapid deceleration scenarios.
* **Production C Code:** Generated clean C functions (`step` and `initialize`) ready for automotive ECU integration.
* **Model-Based Verification:** Full Model-in-the-Loop (MIL) dynamic validation.

---

## 🛠️ Tech Stack & Tools

* **Modeling & Simulation:** MATLAB, Simulink
* **Embedded Software:** Simulink Coder, Embedded Coder, ANSI C
* **Automotive Standards:** Model-Based Design (MBD), ADAS, Longitudinal Vehicle Dynamics
