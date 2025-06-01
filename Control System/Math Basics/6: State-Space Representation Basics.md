# 📘 Chapter 6: State-Space Representation Basics

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 Objective

To understand the fundamentals of state-space modeling and how matrix algebra is applied to describe dynamic systems in control theory.

---

## 📊 1. What is State-Space Representation?

A mathematical model of a system using **state variables** to describe a system with first-order differential equations.

### Standard Form:

$\dot{X}(t) = AX(t) + BU(t)$
$Y(t) = CX(t) + DU(t)$

Where:

* $X(t)$: State vector
* $U(t)$: Input vector
* $Y(t)$: Output vector
* $A, B, C, D$: System matrices

---

## 🔢 2. Why State-Space?

* Suitable for **MIMO** systems
* Works for **time-varying** systems
* Easier simulation and analysis in modern software
* Allows observer and controller design

---

## 📒 3. Example: Second-Order System

Given a system:
$\frac{d^2x}{dt^2} + 4\frac{dx}{dt} + 3x = u(t)$

Convert to state-space by defining:
$x_1 = x, \quad x_2 = \frac{dx}{dt}$
Then,
$\dot{x}_1 = x_2$
$\dot{x}_2 = -3x_1 - 4x_2 + u$

Thus,
$\dot{X} = \begin{bmatrix} 0 & 1 \\ -3 & -4 \end{bmatrix} X + \begin{bmatrix} 0 \\ 1 \end{bmatrix} u$
$Y = \begin{bmatrix} 1 & 0 \end{bmatrix} X$

---

## 📊 4. MATLAB Implementation

```matlab
A = [0 1; -3 -4];
B = [0; 1];
C = [1 0];
D = [0];
sys = ss(A, B, C, D)
```

---

## 📊 5. Python Implementation (Using Control Library)

```python
import numpy as np
import control as ctrl

A = np.array([[0, 1], [-3, -4]])
B = np.array([[0], [1]])
C = np.array([[1, 0]])
D = np.array([[0]])

sys = ctrl.ss(A, B, C, D)
print(sys)
```

---

## 📊 Summary Table

| Concept           | MATLAB Command | Python Equivalent     |
| ----------------- | -------------- | --------------------- |
| Define SS system  | `ss(A,B,C,D)`  | `ctrl.ss(A, B, C, D)` |
| Matrix Definition | `[ ]`          | `np.array([[]])`      |

---

## 👉 What’s Next

In the next chapter, we will discuss how to convert between **Transfer Function and State-Space** representations.

➡️ Proceed to **Chapter 7: Transfer Function <=> State-Space Conversion**
