# 📘 Chapter 7: Transfer Function ⇄ State-Space Conversion

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 Objective

To learn how to convert between transfer function and state-space models for dynamic systems using both analytical and software-based approaches.

---

## 📊 1. Transfer Function to State-Space

Given a transfer function:
$G(s) = \frac{Y(s)}{U(s)} = \frac{b_0s^n + \dots + b_n}{s^n + a_1s^{n-1} + \dots + a_n}$

### ✅ Canonical State-Space Form (Controllable Form):

Let:
$x_1 = y, \quad x_2 = \dot{y}, \quad \dots, \quad x_n = y^{(n-1)}$

Then,
$\dot{X} = A X + B U$
$Y = C X + D U$
Where:

$$
A = \begin{bmatrix} 0 & 1 & 0 & \cdots & 0 \\ 0 & 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \vdots & \ddots & \vdots \\ -a_n & -a_{n-1} & \cdots & -a_1 \end{bmatrix},
B = \begin{bmatrix} 0 \\ 0 \\ \vdots \\ 1 \end{bmatrix},
C = \begin{bmatrix} b_n - a_1b_{n-1} + \cdots \end{bmatrix},
D = [0]
$$

---

## 📊 2. State-Space to Transfer Function

From:
$\dot{X}(t) = AX(t) + BU(t), \quad Y(t) = CX(t) + DU(t)$

Apply Laplace Transform (zero initial conditions):
$sX(s) = AX(s) + BU(s) \Rightarrow X(s) = (sI - A)^{-1} BU(s)$
$Y(s) = C(sI - A)^{-1}B U(s) + D U(s) \Rightarrow G(s) = \frac{Y(s)}{U(s)} = C(sI - A)^{-1}B + D$

---

## 📈 3. MATLAB Examples

### ✅ Transfer Function to State-Space

```matlab
num = [1]; den = [1 4 3];
sys_tf = tf(num, den);
sys_ss = ss(sys_tf)
```

### ✅ State-Space to Transfer Function

```matlab
A = [0 1; -3 -4];
B = [0; 1];
C = [1 0];
D = [0];
sys_ss = ss(A, B, C, D);
sys_tf = tf(sys_ss)
```

---

## 📈 4. Python Examples (Using `control` Library)

### ✅ Transfer Function to State-Space

```python
from control import tf, ss
num = [1]
den = [1, 4, 3]
sys_tf = tf(num, den)
sys_ss = ss(sys_tf)
print(sys_ss)
```

### ✅ State-Space to Transfer Function

```python
import numpy as np
from control import ss, tf
A = np.array([[0, 1], [-3, -4]])
B = np.array([[0], [1]])
C = np.array([[1, 0]])
D = np.array([[0]])
sys_ss = ss(A, B, C, D)
sys_tf = tf(sys_ss)
print(sys_tf)
```

---

## 📊 Summary Table

| Conversion Type | MATLAB        | Python (Control Lib) |
| --------------- | ------------- | -------------------- |
| TF → SS         | `ss(tf(...))` | `ss(tf(...))`        |
| SS → TF         | `tf(ss(...))` | `tf(ss(...))`        |

---

## 👉 What’s Next

In the next chapter, we will learn how to analyze the **Time Response of Control Systems** using state-space and transfer function approaches.

➡️ Proceed to **Chapter 8: Time Response Analysis**
