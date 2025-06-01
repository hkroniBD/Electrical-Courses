

### **Course Title:** Optimization with Python for Electrical Engineers  
**Duration:** 8–10 weeks  
**Prerequisites:**  
- Basic Python programming (NumPy, SciPy, Matplotlib).  
- Introductory knowledge of linear algebra and calculus.  
- Familiarity with electrical engineering concepts (e.g., circuits, power systems).  

---

### **Module 1: Introduction to Optimization in Electrical Engineering**  
**Topics:**  
- Why optimization matters in EE (e.g., power flow, control systems, circuit design).  
- Types of optimization problems: linear, nonlinear, convex, integer, and dynamic.  
- Python tools: `SciPy`, `CVXPY`, `PuLP`, `Pyomo`, `GEKKO`.  

**Lab:**  
- Solve simple EE problems (e.g., resistor network power minimization).  

---

### **Module 2: Linear and Mixed-Integer Programming (LP/MIP)**  
**Topics:**  
- Formulating LP/MIP problems (objective functions, constraints).  
- Solvers: `PuLP`, `SciPy.optimize.linprog`, `Gurobi` (academic licenses).  
- Applications:  
  - Optimal power dispatch in grids.  
  - Unit commitment problems.  
  - Resource allocation in communication networks.  

**Lab:**  
- Economic dispatch problem with generator constraints.  

---

### **Module 3: Nonlinear and Convex Optimization**  
**Topics:**  
- Unconstrained vs. constrained optimization.  
- Gradient-based methods (BFGS, Newton’s method).  
- Convex optimization with `CVXPY`.  
- Applications:  
  - Optimal power flow (OPF).  
  - Parameter tuning in control systems (PID controllers).  

**Lab:**  
- Solve a convex OPF problem using `CVXPY`.  

---

### **Module 4: Heuristic and Metaheuristic Methods**  
**Topics:**  
- Genetic algorithms (GA), particle swarm optimization (PSO).  
- Simulated annealing for combinatorial problems.  
- Libraries: `DEAP`, `PySwarms`.  
- Applications:  
  - Antenna array design.  
  - Machine learning hyperparameter tuning.  

**Lab:**  
- Optimize a wireless sensor network layout using PSO.  

---

### **Module 5: Dynamic Optimization and Optimal Control**  
**Topics:**  
- Discrete-time vs. continuous-time optimization.  
- Model Predictive Control (MPC) with `GEKKO`.  
- Applications:  
  - Battery energy management.  
  - Trajectory optimization for robotics.  

**Lab:**  
- MPC for a DC motor speed control system.  

---

### **Module 6: Stochastic and Robust Optimization**  
**Topics:**  
- Handling uncertainty in EE problems.  
- Chance constraints, scenario-based methods.  
- Applications:  
  - Renewable energy integration (wind/solar).  
  - Demand response under uncertainty.  

**Lab:**  
- Stochastic optimization for microgrid scheduling.  

---

### **Module 7: Optimization in Machine Learning for EE**  
**Topics:**  
- Neural network training as optimization.  
- AutoML for EE applications (e.g., fault detection).  
- Libraries: `TensorFlow`, `Optuna`.  

**Lab:**  
- Hyperparameter tuning for an LSTM-based load forecasting model.  

---

### **Module 8: Large-Scale and Distributed Optimization**  
**Topics:**  
- Decomposition methods (ADMM).  
- Parallel computing with `Dask` or `Ray`.  
- Applications:  
  - Distributed energy resource (DER) coordination.  
  - Smart grid optimization.  

**Lab:**  
- Decentralized optimization for a multi-agent microgrid.  

---

### **Final Project (Choose One):**  
1. **Design Optimization:** Minimize losses in a power distribution network.  
2. **Control Systems:** Tune a PID controller using GA.  
3. **Signal Processing:** Beamforming optimization for 5G antennas.  
4. **Machine Learning:** Optimal feature selection for fault detection.  

---

### **Assessment:**  
- Weekly coding assignments (50%).  
- Midterm project (20%).  
- Final project with report/presentation (30%).  

### **Tools/Resources:**  
- Textbooks: *Convex Optimization* (Boyd), *Python for Power System Analysis* (F. Milano).  
- Datasets: IEEE test cases (e.g., IEEE 14-bus system), open-source EE simulators (e.g., `Pandapower`).  

---
