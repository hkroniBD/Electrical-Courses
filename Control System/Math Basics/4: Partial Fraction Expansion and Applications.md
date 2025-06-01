# 📘 Chapter 4: Partial Fraction Expansion and Applications

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 Objective

To learn how to break down complex Laplace expressions into simpler terms using partial fraction expansion, which simplifies inverse Laplace Transform calculations.

---

## 📊 1. What is Partial Fraction Expansion?

Partial Fraction Expansion (PFE) is a technique to decompose a complex rational function into a sum of simpler fractions, making it easier to invert using known Laplace pairs.

---

## ✅ 2. Why Use It in Control Systems?

* Simplifies inverse Laplace Transform
* Helps in finding time-domain responses
* Essential for hand-calculations and understanding system behavior

---

## 📄 3. Basic Forms

| Type                  | Example                 | Expanded Form                       |
| --------------------- | ----------------------- | ----------------------------------- |
| Simple Poles          | $\frac{5}{(s+1)(s+2)}$  | $\frac{A}{s+1} + \frac{B}{s+2}$     |
| Repeated Poles        | $\frac{6}{(s+1)^2}$     | $\frac{A}{s+1} + \frac{B}{(s+1)^2}$ |
| Irreducible Quadratic | $\frac{3s+5}{s^2+4s+5}$ | $\frac{As+B}{s^2+4s+5}$             |

---

## 🔢 4. Example 1: Simple Poles

### Problem:

$\frac{10}{s^2 + 5s + 6}$
Factor the denominator:
$\frac{10}{(s+2)(s+3)} = \frac{A}{s+2} + \frac{B}{s+3}$

### 📊 MATLAB Code

```matlab
[num, den] = numden(sym('10/(s^2 + 5*s + 6)'));
[A, B] = residue([10], [1 5 6])
```

### 📊 Python Code

```python
from sympy import apart, symbols
s = symbols('s')
f = 10 / (s**2 + 5*s + 6)
print(apart(f, s))
```

---

## 🔢 5. Example 2: Repeated Poles

### Problem:

$\frac{4s + 5}{(s+1)^2}$
Decompose as:
$\frac{A}{s+1} + \frac{B}{(s+1)^2}$

### 📊 MATLAB Code

```matlab
[A, B] = residue([4 5], [1 2 1])
```

### 📊 Python Code

```python
f2 = (4*s + 5)/((s+1)**2)
print(apart(f2, s))
```

---

## 🔢 6. Example 3: Inverse Laplace After Expansion

### Problem:

Find the inverse Laplace of:
$\frac{10}{(s+2)(s+3)}$

### 📊 MATLAB Code

```matlab
syms s t
f = 10/((s+2)*(s+3));
ilaplace(f)
```

### 📊 Python Code

```python
from sympy import inverse_laplace_transform
f = 10 / ((s + 2)*(s + 3))
inverse_laplace_transform(f, s, t)
```

---

## 📊 Summary Table

| Expression Type     | Method                             | Tool Used               |
| ------------------- | ---------------------------------- | ----------------------- |
| Rational Polynomial | Decompose into simpler fractions   | `apart()` / `residue()` |
| Inverse Laplace     | Use known pairs on simplified form | `ilaplace()`            |

---

## 👉 What’s Next

In the next chapter, we will study **Matrix Algebra** and its importance in state-space modeling and system equations.

➡️ Proceed to **Chapter 5: Matrix Algebra for Control Systems**
