# 📘 Chapter 5: Matrix Algebra for Control Systems

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 Objective

To provide foundational understanding of matrix operations necessary for modeling and analyzing state-space representations in control systems.

---

## 📊 1. Why Matrix Algebra?

* Compact representation of multiple equations
* Essential for state-space modeling
* Enables solution of multi-variable systems

---

## 📊 2. Basic Matrix Operations

### ✅ Addition & Subtraction

Two matrices of the same dimension:
$A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}$
$A + B = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix}$

### ✅ Scalar Multiplication

$2A = \begin{bmatrix} 2 & 4 \\ 6 & 8 \end{bmatrix}$

### ✅ Matrix Multiplication

$AB = \begin{bmatrix} 1*5+2*7 & 1*6+2*8 \\ 3*5+4*7 & 3*6+4*8 \end{bmatrix} = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix}$

---

## 🔢 3. Special Matrices

| Matrix Type     | Symbol / Example                                   | Description                       |
| --------------- | -------------------------------------------------- | --------------------------------- |
| Identity Matrix | $I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$ | $AI = IA = A$                     |
| Zero Matrix     | $0 = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}$ | All elements are zero             |
| Diagonal Matrix | $D = \begin{bmatrix} 3 & 0 \\ 0 & 7 \end{bmatrix}$ | Non-zero entries only on diagonal |

---

## 📉 4. Determinant & Inverse

### ✔ Determinant

$\text{det}(A) = ad - bc \text{ for } A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}$

### ✔ Inverse (if $\det(A) \ne 0$)

$A^{-1} = \frac{1}{\text{det}(A)} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}$

---

## 🔢 5. Example: Solving Linear System

Given: $AX = B$

$A = \begin{bmatrix} 2 & 1 \\ 5 & 7 \end{bmatrix}, \quad B = \begin{bmatrix} 11 \\ 13 \end{bmatrix}$

Find $X$.

### 📊 MATLAB Code

```matlab
A = [2 1; 5 7];
B = [11; 13];
X = inv(A) * B
```

### 📊 Python Code

```python
import numpy as np
A = np.array([[2, 1], [5, 7]])
B = np.array([[11], [13]])
X = np.linalg.inv(A).dot(B)
print(X)
```

---

## 📊 Summary Table

| Operation             | Python Function   | MATLAB Command |
| --------------------- | ----------------- | -------------- |
| Matrix Multiplication | `dot()` or `@`    | `*`            |
| Inverse               | `np.linalg.inv()` | `inv()`        |
| Determinant           | `np.linalg.det()` | `det()`        |

---

## 👉 What’s Next

In the next chapter, we will apply matrix algebra to **State-Space Modeling**, the foundation of modern control systems.

➡️ Proceed to **Chapter 6: State-Space Representation Basics**
