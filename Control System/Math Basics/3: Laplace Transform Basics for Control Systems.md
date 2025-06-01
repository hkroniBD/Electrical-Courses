
# 📘 **Chapter 3: Laplace Transform Basics for Control Systems**

**Instructor**: *Md. Hassanul Karim Roni, EEE, HSTU, BD*
**Lecture Duration**: 50 minutes
**Objective**: Simplify analysis of control systems by transforming time-domain differential equations into algebraic equations in the Laplace domain.

---

## 🎯 Learning Goals

✅ Understand the Laplace transform and its use in solving differential equations
✅ Learn common Laplace pairs and properties
✅ Apply Laplace Transform to model dynamic systems
✅ Understand transfer functions and system response analysis

---

## 🧩 1. Why Laplace Transform?

📌 **Control systems** are governed by differential equations.
📌 Solving these in the **time domain** is hard.
✔️ Laplace Transform converts them to **algebraic equations**, which are easier to handle.

🧠 Think of it as:

$$
\text{Time domain} \xrightarrow{\mathcal{L}} \text{Frequency (s) domain}
$$

---

## 🧾 2. Laplace Transform Definition

$$
\mathcal{L}\{f(t)\} = F(s) = \int_0^{\infty} e^{-st} f(t) dt
$$

### Notation:

| Time Domain | Laplace Domain |
| ----------- | -------------- |
| $f(t)$      | $F(s)$         |
| $y(t)$      | $Y(s)$         |
| $u(t)$      | $U(s)$         |

✅ *Applicable for causal functions: $f(t) = 0$ for $t < 0$*

---

## 🧰 3. Common Laplace Transform Pairs

| $f(t)$      | $\mathcal{L}\{f(t)\}$ |
| ----------- | --------------------- |
| $1$         | $\frac{1}{s}$         |
| $t$         | $\frac{1}{s^2}$       |
| $e^{at}$    | $\frac{1}{s - a}$     |
| $\sin(at)$  | $\frac{a}{s^2 + a^2}$ |
| $\cos(at)$  | $\frac{s}{s^2 + a^2}$ |
| $\delta(t)$ | $1$                   |
| $u(t)$      | $\frac{1}{s}$         |

🎯 *These will be used often to solve ODEs or find system responses.*

---

## ⚙️ 4. Derivatives in Laplace Domain

| Time Function          | Laplace                   |
| ---------------------- | ------------------------- |
| $\frac{df(t)}{dt}$     | $sF(s) - f(0)$            |
| $\frac{d^2f(t)}{dt^2}$ | $s^2F(s) - sf(0) - f'(0)$ |

🛠️ **Example**:
Given: $\frac{dy}{dt} + 3y = 5$, with $y(0) = 2$

➡️ Take Laplace on both sides:

$$
sY(s) - 2 + 3Y(s) = \frac{5}{s}
\Rightarrow Y(s)(s + 3) = \frac{5}{s} + 2
$$

Solve for $Y(s)$, then take inverse Laplace to get $y(t)$

---

## 🧪 5. Solving ODE Using Laplace Transform

**Example**:

$$
\ddot{x} + 6\dot{x} + 8x = 0, \quad x(0) = 1, \quad \dot{x}(0) = 0
$$

➡️ Laplace Transform:

$$
s^2X(s) - sx(0) - \dot{x}(0) + 6(sX(s) - x(0)) + 8X(s) = 0
$$

Plug in values:

$$
s^2X(s) - s + 6sX(s) - 6 + 8X(s) = 0
\Rightarrow X(s)(s^2 + 6s + 8) = s + 6
$$

Solve for $X(s)$, then take inverse to find $x(t)$

---

## 🔁 6. Properties of Laplace Transform

| Property        | Formula                                                            |
| --------------- | ------------------------------------------------------------------ |
| Linearity       | $\mathcal{L}\{af(t) + bg(t)\} = aF(s) + bG(s)$                     |
| Time Shift      | $\mathcal{L}\{f(t-a)u(t-a)\} = e^{-as}F(s)$                        |
| Frequency Shift | $\mathcal{L}\{e^{at}f(t)\} = F(s - a)$                             |
| Differentiation | $\mathcal{L}\{f'(t)\} = sF(s) - f(0)$                              |
| Integration     | $\mathcal{L}\left\{\int_0^t f(\tau)d\tau\right\} = \frac{F(s)}{s}$ |

---

## 🔄 7. Inverse Laplace Transform

**Find $f(t)$ given $F(s)$:**
Use partial fractions and known inverse pairs.

### Example:

$$
F(s) = \frac{2}{s(s+2)} \Rightarrow \frac{2}{s(s+2)} = \frac{A}{s} + \frac{B}{s+2}
$$

Find $A = 1, B = -1$, so:

$$
f(t) = \mathcal{L}^{-1}\left\{ \frac{1}{s} - \frac{1}{s+2} \right\} = 1 - e^{-2t}
$$

---

## 📊 8. Transfer Function Concept

**Definition**:
The **transfer function** is the Laplace transform of the output over the Laplace transform of the input, assuming zero initial conditions:

$$
G(s) = \frac{Y(s)}{U(s)}
$$

🛠️ **Example**:
Given:

$$
\ddot{y} + 5\dot{y} + 6y = u(t)
$$

Take Laplace:

$$
(s^2Y(s) + 5sY(s) + 6Y(s)) = U(s) \Rightarrow Y(s) = \frac{1}{s^2 + 5s + 6} U(s)
$$

So:

$$
G(s) = \frac{1}{s^2 + 5s + 6}
$$

---

## 💻 9. MATLAB Example

```matlab
syms s t
f = ilaplace(1/(s^2 + 4*s + 3))
pretty(f)
```

✅ Try `step()` and `impulse()` functions for plotting system responses:

```matlab
num = [1];
den = [1 5 6];
sys = tf(num, den);
step(sys)
```




## 🧪 10. Python Code Equivalent

### ✅ Example 1: Laplace Transform

```python
from sympy import symbols, laplace_transform, exp, Heaviside, simplify
t, s = symbols('t s')
f = exp(-2*t) * Heaviside(t)
F = laplace_transform(f, t, s, noconds=True)
print("Laplace Transform:", simplify(F))
```

### ✅ Example 2: Solving Differential Equation Using Laplace

```python
from sympy import Function, dsolve, Eq, Derivative, laplace_transform, inverse_laplace_transform

y = Function('y')
t, s = symbols('t s')
ode = Eq(Derivative(y(t), t) + 3*y(t), 5)
sol = dsolve(ode, y(t), ics={y(0): 2})
print("Solution:", sol)
```

### ✅ Example 3: Transfer Function and Step Response

```python
import matplotlib.pyplot as plt
import control as ctrl

# Define transfer function: G(s) = 1 / (s^2 + 5s + 6)
num = [1]
den = [1, 5, 6]
sys = ctrl.TransferFunction(num, den)

# Step response
t, y = ctrl.step_response(sys)
plt.plot(t, y)
plt.title('Step Response')
plt.xlabel('Time [s]')
plt.ylabel('Output')
plt.grid(True)
plt.show()
```

---

## 🧰 Installation Tips for Students

If you're preparing this for student use, ask them to install the following:

```bash
pip install numpy scipy sympy matplotlib control
```

Alternatively, you can use **Google Colab** so students can run everything without installing Python locally.

---



---

## 🧠 Summary Table

| Topic               | Application in Control                        |
| ------------------- | --------------------------------------------- |
| Laplace Transform   | Converts ODEs to algebraic form               |
| Derivative Property | Handles initial conditions easily             |
| Inverse Laplace     | Gets time-domain response                     |
| Transfer Function   | Describes system behavior in frequency domain |

---

## ✅ Homework / Practice

1. Take Laplace of:

   $$
   \frac{dy}{dt} + 4y = \sin(t), \quad y(0) = 0
   $$
2. Find inverse Laplace of:

   $$
   \frac{3s + 5}{s^2 + 2s + 1}
   $$
3. Find the transfer function of:

   $$
   \ddot{y} + 3\dot{y} + 2y = u(t)
   $$

---
