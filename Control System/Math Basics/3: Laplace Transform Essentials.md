# 📘 Chapter 3: Laplace Transform Essentials

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 **Objective**

To understand and apply the Laplace Transform to solve linear time-invariant differential equations in control system analysis.

---

## 📊 1. What is the Laplace Transform?

The **Laplace Transform** converts time-domain functions into the **s-domain** (complex frequency domain), making differential equations easier to solve.

### General Definition:

$$
\mathcal{L}\{f(t)\} = F(s) = \int_0^\infty e^{-st}f(t)\,dt
$$

---

## ✅ 2. Why Use Laplace in Control Systems?

* Transforms differential equations into algebraic equations
* Makes system analysis simpler
* Allows use of transfer functions
* Facilitates initial condition handling

---

## 📄 3. Common Laplace Pairs

| Time Domain $f(t)$ | Laplace Domain $F(s)$           |
| ------------------ | ------------------------------- |
| $1$                | $\frac{1}{s}$                   |
| $t$                | $\frac{1}{s^2}$                 |
| $e^{at}$           | $\frac{1}{s-a}$                 |
| $\sin(\omega t)$   | $\frac{\omega}{s^2 + \omega^2}$ |
| $\cos(\omega t)$   | $\frac{s}{s^2 + \omega^2}$      |

---

## 🔢 4. Example 1: Solve First-Order DE Using Laplace

### Problem:

$\frac{dy(t)}{dt} + 3y(t) = 6, \quad y(0) = 0$

### 📊 MATLAB Solution

```matlab
syms s Y
Y = solve(s*Y + 3*Y == 6, Y);
y = ilaplace(Y)
```

### 📊 Python Solution

```python
from sympy import symbols, Function, Eq, LaplaceTransform, inverse_laplace_transform
s, t = symbols('s t')
Y = symbols('Y')

# Laplace-domain algebraic equation
eqn = Eq(s*Y + 3*Y, 6)
Ysol = solve(eqn, Y)[0]
y_t = inverse_laplace_transform(Ysol, s, t)
print(y_t)
```

---

## 🔢 5. Example 2: Second-Order System

### Problem:

$\frac{d^2x}{dt^2} + 4 \frac{dx}{dt} + 3x = 0, \quad x(0)=1, \; x'(0)=0$

### 📊 MATLAB Code

```matlab
syms s X
X = solve(s^2*X + 4*s*X + 3*X == s, X);
x = ilaplace(X)
```

### 📊 Python Code

```python
from sympy import solve
X = symbols('X')
eqn2 = Eq(s**2 * X + 4*s*X + 3*X, s)
Xsol = solve(eqn2, X)[0]
x_t = inverse_laplace_transform(Xsol, s, t)
print(x_t)
```

---

## 📝 Summary Table

| Concept                    | Laplace Operation           | Python/MATLAB Tool             |
| -------------------------- | --------------------------- | ------------------------------ |
| Derivative $\frac{df}{dt}$ | $sF(s) - f(0)$              | `LaplaceTransform`, `ilaplace` |
| Integration $\int f(t)dt$  | $\frac{F(s)}{s}$            | `LaplaceTransform`, `ilaplace` |
| Solving DEs                | Convert to algebraic in $s$ | Symbolic math tools            |

---

## 👉 What’s Next

In the next chapter, we will cover **Partial Fractions**, which are essential for simplifying complex Laplace expressions before inverse transformation.

➡️ Proceed to **Chapter 4: Partial Fraction Expansion and Applications**
