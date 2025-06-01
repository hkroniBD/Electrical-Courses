# 📘 **Chapter 1: Linear Algebra Essentials for Control Systems**

**Lecture Duration**: 45 minutes
**Audience**: Undergraduate students preparing to study control systems
**Lecture Format**: Handnote-style with examples, tables, and control relevance

---

## 🎯 Lecture Objectives:

* Understand the core linear algebra concepts used in control theory
* Apply matrix operations to system equations
* Learn how eigenvalues relate to system stability and dynamics

---

## 🧮 1. Scalars, Vectors, and Matrices

| Concept    | Description                                                          |
| ---------- | -------------------------------------------------------------------- |
| **Scalar** | A single number (e.g., 2, -5, 3.7)                                   |
| **Vector** | A one-dimensional array: $\begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}$ |
| **Matrix** | A rectangular array: $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}$  |

💡 *Application*: In control systems, vectors represent **states** and matrices represent **system behavior**.

---

## 🧾 2. Matrix Operations

### A. Addition & Subtraction

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad B = \begin{bmatrix} 2 & 1 \\ 0 & 5 \end{bmatrix}
$$

$$
A + B = \begin{bmatrix} 3 & 3 \\ 3 & 9 \end{bmatrix}
$$

### B. Matrix Multiplication

$$
AB = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \cdot \begin{bmatrix} 2 & 0 \\ 1 & 5 \end{bmatrix} = \begin{bmatrix} 4 & 10 \\ 10 & 20 \end{bmatrix}
$$

> 💬 Rule: Number of columns in **A** = Number of rows in **B**

---

## 🔁 3. Transpose, Identity, and Inverse

| Operation        | Example                                                                                         |
| ---------------- | ----------------------------------------------------------------------------------------------- |
| Transpose $A^T$  | $\begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}^T = \begin{bmatrix} 1 & 3 \\ 2 & 4 \end{bmatrix}$ |
| Identity $I$     | $\begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}$                                                  |
| Inverse $A^{-1}$ | Only exists if $\text{det}(A) \ne 0$                                                            |

$$
A^{-1} = \frac{1}{\text{det}(A)} \text{adj}(A)
$$

💡 *Application*: Used to solve system equations and decouple state-space representations.

---

## 📐 4. Determinant and Rank

### A. Determinant

$$
\text{det} \begin{bmatrix} a & b \\ c & d \end{bmatrix} = ad - bc
$$

* If $\text{det}(A) = 0$: Matrix is **singular** (not invertible)
* If $\text{det}(A) \ne 0$: Invertible system matrix

### B. Rank

* Number of linearly independent rows or columns
* Rank = Number of states a system can control or observe

---

## 🧪 5. Eigenvalues and Eigenvectors

### A. Definition:

For matrix $A$, $\lambda$ is an eigenvalue if:

$$
A v = \lambda v
$$

Where:

* $v$ is the eigenvector
* $\lambda$ is the eigenvalue

### B. Finding Eigenvalues

Solve:

$$
\det(A - \lambda I) = 0
$$

**Example**:
Let

$$
A = \begin{bmatrix} 4 & -2 \\ 1 & 1 \end{bmatrix}
$$

Then

$$
\det\left(\begin{bmatrix} 4-\lambda & -2 \\ 1 & 1-\lambda \end{bmatrix}\right) = 0
\Rightarrow (4-\lambda)(1-\lambda) + 2 = 0
$$

### C. Interpretation in Control Systems:

* Real negative eigenvalues → stable system
* Real positive eigenvalues → unstable
* Complex conjugate pairs → oscillatory behavior

---

## ⚙️ 6. Application in Control Systems

### State-Space Representation:

$$
\dot{x} = Ax + Bu, \quad y = Cx + Du
$$

* **A**: system matrix (defines behavior)
* Eigenvalues of **A** determine **stability**
* Inverse operations help with **controllability** and **observability** analysis

---

## 💻 7. MATLAB Practice

```matlab
A = [1 2; 3 4];
eig(A)           % Eigenvalues
inv(A)           % Inverse of A
det(A)           % Determinant
```

---

## 🧠 Quick Summary Table

| Concept     | Symbol    | Role in Control |
| ----------- | --------- | --------------- |
| Matrix      | $A$       | System dynamics |
| Inverse     | $A^{-1}$  | Solving systems |
| Determinant | $\det(A)$ | Invertibility   |
| Eigenvalues | $\lambda$ | Stability check |

---

## ✅ Homework/Practice

1. Find eigenvalues and eigenvectors of:

   $$  A = \begin{bmatrix} 2 & 1 \\ 1 & 2 \end{bmatrix}
   $$
2. Verify whether this matrix is invertible:

   $$
   B = \begin{bmatrix} 3 & 6 \\ 1 & 2 \end{bmatrix}
   $$
3. In MATLAB, plot the direction field of a 2-state system using eigenvectors.

---
