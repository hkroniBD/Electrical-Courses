# 📘 Chapter 2: Differential Equations Refresher

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 **Objective**

To recall and practice solving differential equations that describe the dynamic behavior of physical systems in control engineering.

---

## 🔍 1. What is a Differential Equation?

A **differential equation** relates a function with its derivatives. In control systems, they model how system states evolve over time.

### General Form:

$\frac{dy(t)}{dt} + ay(t) = bu(t)$
Where:

* $y(t)$: system response
* $u(t)$: input (forcing function)
* $a, b$: constants

---

## 🧪 2. First-Order Linear DE: Tank Model

### Example: Water Tank Filling

$\frac{dh(t)}{dt} + 2h(t) = 10$

* This represents a tank where water flows in at a constant rate, and leaks are proportional to height.

---

### 📊 MATLAB Solution

```matlab
syms h(t)
Dh = diff(h, t);
ode = Dh + 2*h == 10;
cond = h(0) == 0;
hSol = dsolve(ode, cond)
fplot(hSol, [0 10])
```

### 📊 Python Symbolic Solution

```python
from sympy import symbols, Function, Eq, dsolve

# Define variable
t = symbols('t')
h = Function('h')

# Differential Equation
ode = Eq(h(t).diff(t) + 2*h(t), 10)
sol = dsolve(ode, h(t), ics={h(0): 0})
print(sol)
```

---

### 📊 Python Numerical Plot

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.integrate import solve_ivp

def tank_ode(t, h):
    return 10 - 2*h

sol = solve_ivp(tank_ode, [0, 10], [0], t_eval=np.linspace(0, 10, 200))
plt.plot(sol.t, sol.y[0], label='h(t)')
plt.title('Solution to dh/dt + 2h = 10')
plt.xlabel('Time (s)')
plt.ylabel('Water Height h(t)')
plt.grid(True)
plt.legend()
plt.show()
```

---

## 🎓 3. Second-Order DE: Mass-Spring-Damper

### Equation:

$m \frac{d^2x}{dt^2} + c \frac{dx}{dt} + kx = F(t)$

* **m**: mass
* **c**: damping constant
* **k**: spring constant
* **F(t)**: applied force

Let $m = 1, c = 3, k = 2, F(t) = 0$

---

### 📊 MATLAB Code

```matlab
syms x(t)
Dx = diff(x, t);
D2x = diff(x, t, 2);
ode = D2x + 3*Dx + 2*x == 0;
cond1 = x(0) == 1;
cond2 = Dx(0) == 0;
xSol = dsolve(ode, [cond1, cond2])
fplot(xSol, [0 10])
```

### 📊 Python Symbolic Solution

```python
from sympy import dsolve, Derivative as D
x = Function('x')

de = Eq(D(D(x(t), t), t) + 3*D(x(t), t) + 2*x(t), 0)
sol = dsolve(de, x(t), ics={x(0): 1, x(t).diff(t).subs(t,0): 0})
print(sol)
```

---

### 📊 Python Numerical Plot

```python
from scipy.integrate import solve_ivp

def mass_spring_damper(t, y):
    x, v = y
    dxdt = v
    dvdt = -3*v - 2*x
    return [dxdt, dvdt]

sol = solve_ivp(mass_spring_damper, [0, 10], [1, 0], t_eval=np.linspace(0, 10, 200))
plt.plot(sol.t, sol.y[0], label='x(t)')
plt.title('Mass-Spring-Damper Response')
plt.xlabel('Time (s)')
plt.ylabel('Displacement x(t)')
plt.grid(True)
plt.legend()
plt.show()
```

---

## 📝 Summary Table

| Type of Equation    | General Form                       | Use in Control | Solved Using          |
| ------------------- | ---------------------------------- | -------------- | --------------------- |
| First-Order Linear  | $\frac{dy}{dt} + ay = b$           | Tank, RC       | `dsolve`, `solve_ivp` |
| Second-Order Linear | $m\ddot{x} + c\dot{x} + kx = F(t)$ | Mechanical Sys | `dsolve`, `solve_ivp` |

---

## 👉 What’s Next

Next, we explore the **Laplace Transform** to convert time-domain differential equations into simpler algebraic equations.

➡️ Proceed to **Chapter 3: Laplace Transform Essentials**
