# 📘 **Chapter 2: Ordinary Differential Equations (ODEs) Essentials for Control Systems**

**Lecture Duration**: 45 minutes
**Target Audience**: Undergraduate students preparing for control systems
**Lecture Style**: Visual, example-focused, and connected to control system modeling

---

## 🎯 Lecture Objectives:

* Understand how physical systems are modeled using ODEs
* Learn to solve first and second-order ODEs
* Connect differential equations with system response and transfer functions

---

## 🔧 1. What is an ODE?

An **Ordinary Differential Equation (ODE)** expresses a relationship between a function and its derivatives.

### General form:

$$
\frac{d^n y}{dt^n} + a_{n-1} \frac{d^{n-1}y}{dt^{n-1}} + \dots + a_1 \frac{dy}{dt} + a_0 y = f(t)
$$

* If $f(t) = 0$, the system is **homogeneous**
* If $f(t) \neq 0$, the system is **non-homogeneous**

---

## 🛠️ 2. First-Order ODEs

### General Form:

$$
\frac{dy}{dt} + ay = b
$$

### Example:

$$
\frac{dy}{dt} + 3y = 6, \quad y(0) = 2
$$

### Solution:

1. Homogeneous solution: $y_h = Ce^{-3t}$
2. Particular solution: $y_p = 2$
3. General solution:

$$
y(t) = Ce^{-3t} + 2
$$

Apply $y(0) = 2$:

$$
2 = C + 2 \Rightarrow C = 0 \Rightarrow y(t) = 2
$$

### MATLAB Code:

```matlab
syms y(t)
Dy = diff(y,t);
ode = Dy + 3*y == 6;
cond = y(0) == 2;
sol = dsolve(ode, cond)
fplot(sol, [0 5])
```

---

## 🧰 3. Second-Order ODEs

### General Form:

$$
\frac{d^2x}{dt^2} + a_1\frac{dx}{dt} + a_0x = f(t)
$$

### Example:

$$
\ddot{x} + 5\dot{x} + 6x = 0, \quad x(0) = 2, \quad \dot{x}(0) = 0
$$

#### Step 1: Characteristic equation

$$
s^2 + 5s + 6 = 0 \Rightarrow s = -2, -3
$$

#### Step 2: General solution

$$
x(t) = C_1 e^{-2t} + C_2 e^{-3t}
$$

#### Step 3: Use initial conditions

$$
x(0) = C_1 + C_2 = 2 \\
\dot{x}(t) = -2C_1 e^{-2t} -3C_2 e^{-3t}, \quad \dot{x}(0) = -2C_1 -3C_2 = 0
$$

Solve the system:

$$
\begin{cases}
C_1 + C_2 = 2 \\
-2C_1 - 3C_2 = 0
\end{cases}
\Rightarrow C_1 = 6, \quad C_2 = -4
$$

Final solution:

$$
x(t) = 6e^{-2t} - 4e^{-3t}
$$

---

## 🔁 4. Homogeneous vs. Non-Homogeneous

| Type            | ODE                                 | Behavior                     |
| --------------- | ----------------------------------- | ---------------------------- |
| Homogeneous     | $\ddot{x} + 2\dot{x} + x = 0$       | Free response (no input)     |
| Non-Homogeneous | $\ddot{x} + 2\dot{x} + x = 5\sin t$ | Forced response due to input |

---

## ⚙️ 5. Connection to Control Systems

* Mechanical and electrical systems modeled as ODEs
* Transfer functions are derived from **linear time-invariant ODEs**
* Second-order systems define rise time, overshoot, and damping ratio

### Example: Mass-Spring-Damper System

$$
m\ddot{x} + b\dot{x} + kx = F(t)
$$

→ Standard second-order ODE in control systems

---

## 💡 6. Numerical Solution of ODEs (Euler's Method)

### Euler's Approximation:

$$
y_{n+1} = y_n + h f(t_n, y_n)
$$

**Given**: $\frac{dy}{dt} = -2y, \quad y(0) = 1, \quad h = 0.1$

Compute a few steps using:

```python
y = 1
h = 0.1
for t in range(10):
    y = y - 2 * y * h
    print(y)
```

Use when analytic solution is hard or system is complex.

---

## 🧠 Quick Summary Table

| Concept         | Purpose in Control Systems                  |
| --------------- | ------------------------------------------- |
| 1st Order ODE   | Models RC circuits, fluid systems           |
| 2nd Order ODE   | Common in mechanical and electrical systems |
| Homogeneous     | Describes natural/free response             |
| Non-Homogeneous | Input-driven response                       |
| Euler Method    | Numerical simulation of system response     |

---

## ✅ Homework / Practice Problems

1. Solve:

   $$
   \frac{dy}{dt} + 4y = 8, \quad y(0) = 0
   $$
2. Use Euler method to solve:

   $$
   \frac{dy}{dt} = y - t^2 + 1, \quad y(0) = 0.5, \quad h = 0.2
   $$
3. MATLAB/Simulink: Simulate an RLC circuit and plot output voltage over time.

---
