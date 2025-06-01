# 📘 Chapter 8: Time Domain Analysis of First and Second Order Differential Equations

**Instructor:** Md. Hassanul Karim Roni, EEE, HSTU, BD

---

## 🎯 Objective

To understand the behavior of first- and second-order differential equations in the time domain under various standard inputs. This knowledge is essential before diving into full control system analysis.

---

## 📊 1. First-Order Differential Equation

General form:
$\frac{dy(t)}{dt} + a y(t) = b u(t)$

### ✅ Homogeneous Case (u(t) = 0):

$y(t) = y(0) e^{-a t}$
Exponential decay depending on the constant $a$.

### ✅ Step Response (u(t) = 1):

Solution:
$y(t) = \left( y(0) - \frac{b}{a} \right) e^{-a t} + \frac{b}{a}$

---

## 📊 2. Second-Order Differential Equation

General form:
$\frac{d^2x}{dt^2} + 2\zeta\omega_n \frac{dx}{dt} + \omega_n^2 x = \omega_n^2 u(t)$
Where:

* $\omega_n$: natural frequency
* $\zeta$: damping ratio

### 🔢 Case 1: Underdamped ($0 < \zeta < 1$)

$x(t) = 1 - \frac{1}{\sqrt{1-\zeta^2}} e^{-\zeta \omega_n t} \sin(\omega_d t + \phi)$
Where $\omega_d = \omega_n \sqrt{1 - \zeta^2}$

### 🔢 Case 2: Critically Damped ($\zeta = 1$)

$x(t) = (A + Bt) e^{-\omega_n t}$

### 🔢 Case 3: Overdamped ($\zeta > 1$)

$x(t) = C_1 e^{s_1 t} + C_2 e^{s_2 t} \quad \text{where } s_1, s_2 < 0$

---

## 🔄 3. Responses to Standard Inputs

| Input Type            | First Order Output             | Second Order Output ($\zeta < 1$) |
| --------------------- | ------------------------------ | --------------------------------- |
| Step (1)              | $1 - e^{-at}$                  | Oscillatory rise to 1             |
| Ramp (t)              | $t - \frac{1}{a}(1 - e^{-at})$ | Complex expression                |
| Impulse ($\delta(t)$) | $b e^{-at}$                    | Sharp initial response            |

---

## 👨‍💻 4. MATLAB Examples

### ✅ First Order Step Response

```matlab
num = [1]; den = [1 2];
sys = tf(num, den);
step(sys)
```

### ✅ Second Order Ramp Response

```matlab
num = [1]; den = [1 2 2];
sys = tf(num, den);
ramp = tf([1 0], [1 0]);
lsim(sys, ramp.input, ramp.time)
```

---

## 👨‍💻 5. Python Examples (Using `control` Library)

### ✅ First Order Step Response

```python
from control import tf, step_response
import matplotlib.pyplot as plt

sys = tf([1], [1, 2])
t, y = step_response(sys)
plt.plot(t, y)
plt.title("Step Response: First Order")
plt.grid(True)
plt.show()
```

### ✅ Second Order Impulse Response

```python
from control import tf, impulse_response
sys2 = tf([1], [1, 2, 2])
t2, y2 = impulse_response(sys2)
plt.plot(t2, y2)
plt.title("Impulse Response: Second Order")
plt.grid(True)
plt.show()
```

---

## 📅 6. Summary Table: Key Time-Domain Parameters

| Parameter     | Description                                 |
| ------------- | ------------------------------------------- |
| Rise Time     | Time to rise from 10% to 90% of final value |
| Settling Time | Time to stay within ±2% of final value      |
| Overshoot     | Max amount above steady-state               |
| Steady-State  | Final value as $t \to \infty$               |

---

## 👉 What’s Next

In the next chapter, we will cover **Convolution Integral**, which is fundamental for time-domain system response using input-output relationships.

➡️ Proceed to **Chapter 9: Convolution Integral and Applications**
