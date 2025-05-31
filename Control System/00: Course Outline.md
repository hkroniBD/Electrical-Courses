## **Module 1: Foundations of Control Systems & Python Basics**  
### **Lecture 1: Introduction to Control Systems & Python Setup**  
- Overview of control systems in research  
- Python libraries for control (`numpy`, `scipy`, `matplotlib`, `control`)  
- Setting up a Python environment (Jupyter, Google Colab, VS Code)  
- **Practical:** Simulating a first-order system step response  

### **Lecture 2: Linear Time-Invariant (LTI) Systems & Transfer Functions**  
- State-space vs. transfer function representations  
- System interconnections (series, parallel, feedback)  
- **Practical:** Modeling a DC motor with `control` library  
- **Research Reference:** Ogata’s *Modern Control Engineering*  

---

## **Module 2: Time & Frequency Domain Analysis**  
### **Lecture 3: Time Response Analysis**  
- Step, impulse, and ramp responses  
- Stability analysis (poles, zeros, Routh-Hurwitz)  
- **Practical:** Simulating a second-order system with varying damping  

### **Lecture 4: Frequency Response & Bode Plots**  
- Bode, Nyquist, and Nichols plots  
- Gain and phase margins  
- **Practical:** Stability analysis of a PID-controlled system  
- **Research Reference:** Franklin’s *Feedback Control of Dynamic Systems*  

---

## **Module 3: Controller Design & Optimization**  
### **Lecture 5: PID Control & Tuning Methods**  
- Ziegler-Nichols, Cohen-Coon, and optimization-based tuning  
- **Practical:** Auto-tuning a temperature control system  

### **Lecture 6: State-Space Control (LQR, Pole Placement)**  
- Controllability & observability  
- LQR design with `scipy.linalg.solve_continuous_are`  
- **Practical:** Balancing an inverted pendulum  

### **Lecture 7: Robust Control (H∞, μ-Synthesis)**  
- Introduction to robust control theory  
- **Practical:** Sensitivity minimization with `slycot` (if available)  
- **Research Reference:** Skogestad’s *Multivariable Feedback Control*  

---

## **Module 4: Advanced Topics in Control Research**  
### **Lecture 8: Nonlinear Control (Sliding Mode, Feedback Linearization)**  
- Lyapunov stability analysis  
- **Practical:** Simulating a sliding mode controller for a nonlinear system  

### **Lecture 9: Adaptive & Learning-Based Control**  
- Model Reference Adaptive Control (MRAC)  
- Reinforcement Learning (RL) for control (using `gym` or `PyTorch`)  
- **Research Reference:** Sutton & Barto’s *Reinforcement Learning*  

### **Lecture 10: Model Predictive Control (MPC)**  
- Linear and nonlinear MPC formulations  
- **Practical:** MPC for a quadrotor (using `do-mpc` or `cvxpy`)  

---

## **Module 5: Research Applications & Case Studies**  
### **Lecture 11: Control in Robotics (ROS & Python Integration)**  
- Trajectory tracking for robotic arms  
- **Practical:** Simulating a robotic manipulator with `PyBullet`  

### **Lecture 12: Control in Power Systems & Smart Grids**  
- Frequency regulation in microgrids  
- **Research Reference:** Kundur’s *Power System Stability and Control*  

### **Lecture 13: Emerging Topics (AI-Based Control, Neuromorphic Control)**  
- Neural network-based controllers  
- **Practical:** Differentiable control with `PyTorch`  

---

## **Final Project (Research-Oriented)**  
- Students implement a control strategy on a real-world problem (e.g., drone control, HVAC optimization)  
- Peer-reviewed presentation & report  

---

### **References & Tools**  
- **Books:**  
  - Astrom & Murray (*Feedback Systems*)  
  - Khalil (*Nonlinear Systems*)  
- **Python Libraries:**  
  - `control` (for classical control)  
  - `cvxpy` (for MPC)  
  - `PyTorch` (for learning-based control)  
- **Datasets/Simulators:**  
  - OpenAI Gym  
  - Webots/PyBullet for robotics  
