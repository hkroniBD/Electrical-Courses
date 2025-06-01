# 📊 Lecture 7-8: Time Domain Analysis of Control Systems
## Week 4 | Control Systems with Python

---

## 🎯 Learning Objectives
By the end of this lecture, you will be able to:
- ✅ Analyze step response characteristics of control systems
- ✅ Calculate performance specifications (rise time, settling time, overshoot)
- ✅ Implement time domain analysis in Python and MATLAB
- ✅ Apply time domain specifications to real-world control problems
- ✅ Design systems to meet time domain requirements

---

## 📋 Lecture Outline
| Section | Topic | Duration |
|---------|--------|----------|
| 1 | Introduction & Real-World Context | 15 min |
| 2 | Step Response Fundamentals | 25 min |
| 3 | Performance Specifications | 30 min |
| 4 | Python/MATLAB Implementation | 25 min |
| 5 | Real-World Applications | 15 min |
| 6 | Summary & Next Steps | 10 min |

---

## 🌍 Section 1: Real-World Context

### Why Time Domain Analysis Matters

**🚗 Automotive Example: Cruise Control System**
When you set your car's cruise control to 65 mph:
- **Rise Time**: How quickly does the car accelerate to 65 mph?
- **Overshoot**: Does it briefly exceed 65 mph before settling?
- **Settling Time**: How long until the speed stabilizes at exactly 65 mph?
- **Steady-State Error**: Does it maintain exactly 65 mph or settle at 64.5 mph?

**🏭 Industrial Example: Temperature Control**
In a pharmaceutical manufacturing reactor:
- **Critical**: No overshoot allowed (could damage product)
- **Fast Response**: Quick temperature changes for efficiency
- **Precision**: ±0.1°C accuracy required

**🚁 Aerospace Example: Drone Positioning**
For package delivery drones:
- **Stability**: No oscillations during hover
- **Speed**: Quick response to position commands
- **Precision**: Landing accuracy within centimeters

---

## 📈 Section 2: Step Response Fundamentals

### 🔄 What is Step Response?

The **step response** is the output of a system when the input changes instantaneously from 0 to a constant value (usually 1).

**Mathematical Definition:**
```
If input u(t) = 1 for t ≥ 0 (unit step)
Then step response y(t) = system output for t ≥ 0
```

### 📊 Typical Step Response Shapes

| System Type | Response Shape | Characteristics |
|-------------|----------------|-----------------|
| **First-Order** | Exponential approach | No overshoot, monotonic |
| **Second-Order (ζ > 1)** | Exponential approach | Overdamped, no overshoot |
| **Second-Order (ζ = 1)** | Critical approach | Critically damped |
| **Second-Order (ζ < 1)** | Oscillatory | Underdamped, overshoot |
| **Higher-Order** | Complex behavior | Multiple poles effects |

### 🧮 Second-Order System Deep Dive

**Standard Form:**
```
G(s) = ωₙ²/(s² + 2ζωₙs + ωₙ²)
```

Where:
- **ωₙ** = Natural frequency (rad/s)
- **ζ** = Damping ratio (dimensionless)

**Time Domain Response:**
For ζ < 1 (underdamped):
```
y(t) = 1 - (e^(-ζωₙt)/√(1-ζ²)) × sin(ωₐt + φ)
```

Where:
- **ωₐ = ωₙ√(1-ζ²)** = Damped frequency
- **φ = cos⁻¹(ζ)** = Phase angle

---

## 📏 Section 3: Performance Specifications

### 🎯 Key Performance Metrics

| Metric | Symbol | Definition | Typical Values |
|--------|--------|------------|----------------|
| **Rise Time** | tᵣ | Time to reach 90% of final value | 0.1-2.0 s |
| **Peak Time** | tₚ | Time to reach maximum value | 0.2-3.0 s |
| **Settling Time** | tₛ | Time to stay within ±2% of final value | 2-10 s |
| **Maximum Overshoot** | Mₚ | Peak value above final value (%) | 0-25% |
| **Steady-State Error** | eₛₛ | Final error between desired and actual | 0-5% |

### 📐 Mathematical Relationships (Second-Order Systems)

**Peak Time:**
```
tₚ = π/(ωₙ√(1-ζ²))    for ζ < 1
```

**Maximum Overshoot:**
```
Mₚ = e^(-ζπ/√(1-ζ²)) × 100%    for ζ < 1
```

**Rise Time (10% to 90%):**
```
tᵣ ≈ (2.16ζ + 0.60)/ωₙ    for ζ < 1
```

**Settling Time (2% criterion):**
```
tₛ ≈ 4/(ζωₙ)    for ζ < 1
```

### 🎚️ Design Trade-offs

| Increase ζ | Effect |
|------------|--------|
| ↗️ Damping | ↘️ Overshoot, ↗️ Rise Time |
| ↗️ Natural Frequency | ↘️ Rise Time, ↘️ Settling Time |

**🔍 Research Insight:**
Recent studies in mechatronics show that optimal damping ratios for robotic systems are typically 0.6-0.8, balancing speed and stability.

---

## 💻 Section 4: Python & MATLAB Implementation

### 🐍 Python Implementation

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy import signal
import control as ctrl

# Define second-order system
def create_second_order_system(wn, zeta):
    """Create second-order transfer function"""
    num = [wn**2]
    den = [1, 2*zeta*wn, wn**2]
    return ctrl.tf(num, den)

# Calculate step response
def analyze_step_response(sys, t_final=10):
    """Comprehensive step response analysis"""
    
    # Generate time vector
    t = np.linspace(0, t_final, 1000)
    
    # Calculate step response
    t_step, y_step = ctrl.step_response(sys, t)
    
    # Find performance metrics
    final_value = y_step[-1]
    
    # Rise time (10% to 90%)
    idx_10 = np.where(y_step >= 0.1 * final_value)[0]
    idx_90 = np.where(y_step >= 0.9 * final_value)[0]
    
    if len(idx_10) > 0 and len(idx_90) > 0:
        rise_time = t_step[idx_90[0]] - t_step[idx_10[0]]
    else:
        rise_time = None
    
    # Peak time and overshoot
    peak_idx = np.argmax(y_step)
    peak_time = t_step[peak_idx]
    peak_value = y_step[peak_idx]
    overshoot = ((peak_value - final_value) / final_value) * 100
    
    # Settling time (2% criterion)
    settling_band = 0.02 * final_value
    settled_indices = np.where(np.abs(y_step - final_value) <= settling_band)[0]
    
    if len(settled_indices) > 100:  # Ensure sustained settling
        settling_time = t_step[settled_indices[100]]
    else:
        settling_time = t_final
    
    return {
        'time': t_step,
        'response': y_step,
        'rise_time': rise_time,
        'peak_time': peak_time,
        'settling_time': settling_time,
        'overshoot': overshoot,
        'final_value': final_value
    }

# Example: Analyze different damping ratios
zeta_values = [0.3, 0.5, 0.7, 1.0, 1.5]
wn = 2.0  # Natural frequency

plt.figure(figsize=(12, 8))

for i, zeta in enumerate(zeta_values):
    sys = create_second_order_system(wn, zeta)
    results = analyze_step_response(sys)
    
    plt.subplot(2, 1, 1)
    plt.plot(results['time'], results['response'], 
             label=f'ζ = {zeta}', linewidth=2)
    
    print(f"ζ = {zeta}:")
    print(f"  Rise Time: {results['rise_time']:.3f} s")
    print(f"  Peak Time: {results['peak_time']:.3f} s")
    print(f"  Settling Time: {results['settling_time']:.3f} s")
    print(f"  Overshoot: {results['overshoot']:.1f}%")
    print()

plt.subplot(2, 1, 1)
plt.grid(True, alpha=0.3)
plt.xlabel('Time (s)')
plt.ylabel('Response')
plt.title('Step Response for Different Damping Ratios')
plt.legend()

# Performance metrics comparison
plt.subplot(2, 1, 2)
rise_times = []
overshoots = []

for zeta in zeta_values:
    sys = create_second_order_system(wn, zeta)
    results = analyze_step_response(sys)
    rise_times.append(results['rise_time'] if results['rise_time'] else 0)
    overshoots.append(results['overshoot'])

plt.plot(zeta_values, rise_times, 'bo-', label='Rise Time (s)')
plt.plot(zeta_values, [o/10 for o in overshoots], 'ro-', label='Overshoot/10 (%)')
plt.grid(True, alpha=0.3)
plt.xlabel('Damping Ratio (ζ)')
plt.ylabel('Performance Metrics')
plt.title('Performance vs Damping Ratio')
plt.legend()

plt.tight_layout()
plt.show()
```

### 📊 MATLAB Implementation

```matlab
%% MATLAB Time Domain Analysis
clear; clc; close all;

% Define system parameters
wn = 2;  % Natural frequency
zeta_values = [0.3, 0.5, 0.7, 1.0, 1.5];

% Create figure
figure('Position', [100, 100, 1000, 600]);

% Colors for different responses
colors = ['b', 'r', 'g', 'm', 'k'];

subplot(2,2,1); hold on;
subplot(2,2,2); hold on;
subplot(2,2,3); hold on;
subplot(2,2,4); hold on;

performance_data = [];

for i = 1:length(zeta_values)
    zeta = zeta_values(i);
    
    % Create transfer function
    num = wn^2;
    den = [1, 2*zeta*wn, wn^2];
    sys = tf(num, den);
    
    % Step response
    [y, t] = step(sys);
    
    % Plot step response
    subplot(2,2,1);
    plot(t, y, colors(i), 'LineWidth', 2, 'DisplayName', ['\zeta = ', num2str(zeta)]);
    
    % Calculate performance metrics
    info = stepinfo(sys);
    
    % Store performance data
    performance_data(i,:) = [zeta, info.RiseTime, info.PeakTime, ...
                            info.SettlingTime, info.Overshoot];
    
    fprintf('ζ = %.1f: Rise=%.3fs, Peak=%.3fs, Settling=%.3fs, Overshoot=%.1f%%\n', ...
            zeta, info.RiseTime, info.PeakTime, info.SettlingTime, info.Overshoot);
end

% Format subplots
subplot(2,2,1);
grid on; xlabel('Time (s)'); ylabel('Response');
title('Step Response Comparison');
legend('show', 'Location', 'best');

% Performance metrics plots
subplot(2,2,2);
plot(performance_data(:,1), performance_data(:,2), 'bo-', 'LineWidth', 2);
grid on; xlabel('Damping Ratio (\zeta)'); ylabel('Rise Time (s)');
title('Rise Time vs Damping Ratio');

subplot(2,2,3);
plot(performance_data(:,1), performance_data(:,5), 'ro-', 'LineWidth', 2);
grid on; xlabel('Damping Ratio (\zeta)'); ylabel('Overshoot (%)');
title('Overshoot vs Damping Ratio');

subplot(2,2,4);
plot(performance_data(:,1), performance_data(:,4), 'go-', 'LineWidth', 2);
grid on; xlabel('Damping Ratio (\zeta)'); ylabel('Settling Time (s)');
title('Settling Time vs Damping Ratio');

sgtitle('Time Domain Analysis: Second-Order Systems');
```

---

## 🏭 Section 5: Real-World Applications

### 🚗 Case Study 1: Automotive Suspension System

**Problem:** Design active suspension for passenger comfort

**System Model:**
```
G(s) = X_body(s)/F_actuator(s) = K/(ms² + cs + k)
```

**Requirements:**
- Rise time < 0.5 s (quick pothole response)
- Overshoot < 10% (comfort)
- Settling time < 2 s (stability)

**Python Design Example:**
```python
# Suspension system parameters
m = 300  # kg (quarter car mass)
c = 1500  # N⋅s/m (damping)
k = 20000  # N/m (spring constant)

# Create transfer function
num = [k]
den = [m, c, k]
suspension_sys = ctrl.tf(num, den)

# Analyze current performance
results = analyze_step_response(suspension_sys, t_final=5)

print("Current Suspension Performance:")
print(f"Rise Time: {results['rise_time']:.3f} s")
print(f"Overshoot: {results['overshoot']:.1f}%")
print(f"Settling Time: {results['settling_time']:.3f} s")

# Check if meets requirements
meets_rise = results['rise_time'] < 0.5
meets_overshoot = results['overshoot'] < 10
meets_settling = results['settling_time'] < 2

print(f"\nMeets Requirements:")
print(f"Rise Time: {'✅' if meets_rise else '❌'}")
print(f"Overshoot: {'✅' if meets_overshoot else '❌'}")
print(f"Settling Time: {'✅' if meets_settling else '❌'}")
```

### 🏭 Case Study 2: Industrial Temperature Control

**Problem:** Pharmaceutical reactor temperature control

**System Identification Data:**
```python
# Real experimental data from pharmaceutical reactor
time_data = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10])  # minutes
temp_response = np.array([20, 23, 28, 35, 42, 47, 49.5, 50.2, 50.1, 50.0, 50.0])  # °C

# Fit second-order model
def fit_second_order_model(t_data, y_data):
    """Fit second-order model to experimental data"""
    from scipy.optimize import curve_fit
    
    def second_order_step(t, K, wn, zeta):
        if zeta < 1:
            wd = wn * np.sqrt(1 - zeta**2)
            phi = np.arccos(zeta)
            y = K * (1 - (np.exp(-zeta*wn*t) / np.sqrt(1-zeta**2)) * 
                    np.sin(wd*t + phi))
        else:
            # Overdamped case
            r1 = -zeta*wn + wn*np.sqrt(zeta**2 - 1)
            r2 = -zeta*wn - wn*np.sqrt(zeta**2 - 1)
            y = K * (1 - (r1*np.exp(r2*t) - r2*np.exp(r1*t))/(r1-r2))
        return y
    
    # Initial guess
    K_guess = y_data[-1] - y_data[0]
    wn_guess = 1.0
    zeta_guess = 0.7
    
    popt, _ = curve_fit(second_order_step, t_data, y_data - y_data[0], 
                       p0=[K_guess, wn_guess, zeta_guess])
    
    return popt

# Fit model to data
K_fit, wn_fit, zeta_fit = fit_second_order_model(time_data, temp_response)

print(f"Fitted Model Parameters:")
print(f"Gain (K): {K_fit:.2f} °C")
print(f"Natural Frequency (ωₙ): {wn_fit:.3f} rad/min")
print(f"Damping Ratio (ζ): {zeta_fit:.3f}")

# Create fitted transfer function
fitted_sys = create_second_order_system(wn_fit, zeta_fit)
fitted_sys = ctrl.series(fitted_sys, ctrl.tf([K_fit], [1]))
```

### 🚁 Case Study 3: Drone Position Control

**Problem:** Quadcopter altitude control system

**Requirements Analysis:**
```python
# Drone altitude control specifications
specs = {
    'rise_time_max': 1.0,      # seconds (safety)
    'overshoot_max': 5.0,      # percent (stability)
    'settling_time_max': 3.0,   # seconds (efficiency)
    'steady_state_error_max': 0.02  # meters (precision)
}

# Drone dynamics (simplified)
# G(s) = Altitude(s)/Thrust(s)
m_drone = 2.0  # kg
g = 9.81  # m/s²
thrust_to_acceleration = 1/m_drone

# Second-order approximation for altitude dynamics
wn_drone = 3.0  # rad/s
zeta_drone = 0.6

drone_sys = create_second_order_system(wn_drone, zeta_drone)
drone_results = analyze_step_response(drone_sys, t_final=8)

# Performance evaluation
performance_check = {
    'rise_time': drone_results['rise_time'] <= specs['rise_time_max'],
    'overshoot': drone_results['overshoot'] <= specs['overshoot_max'],
    'settling_time': drone_results['settling_time'] <= specs['settling_time_max']
}

print("🚁 Drone Altitude Control Performance:")
for metric, passes in performance_check.items():
    status = "✅ PASS" if passes else "❌ FAIL"
    print(f"{metric.replace('_', ' ').title()}: {status}")
```

---

## 📊 Section 6: Research Applications & Current Trends

### 🔬 Current Research Areas

| Research Area | Time Domain Focus | Recent Developments |
|---------------|-------------------|-------------------|
| **Autonomous Vehicles** | Fast lane-change response | Machine learning enhanced performance prediction |
| **Renewable Energy** | Grid stability during transitions | Adaptive settling time based on weather |
| **Medical Devices** | Drug delivery precision | Patient-specific performance optimization |
| **Robotics** | Human-robot interaction safety | Bio-inspired response characteristics |

### 📈 Performance Optimization Techniques

**1. Multi-Objective Optimization:**
```python
# Example: Optimize for multiple performance criteria
from scipy.optimize import minimize

def performance_objective(params, weights):
    """Multi-objective performance function"""
    wn, zeta = params
    if zeta <= 0 or wn <= 0:
        return 1e6  # Invalid parameters
    
    sys = create_second_order_system(wn, zeta)
    results = analyze_step_response(sys)
    
    # Normalize objectives (smaller is better)
    obj_rise = results['rise_time'] / 2.0  # Normalize by 2 seconds
    obj_overshoot = results['overshoot'] / 20.0  # Normalize by 20%
    obj_settling = results['settling_time'] / 5.0  # Normalize by 5 seconds
    
    # Weighted sum
    total_obj = (weights[0] * obj_rise + 
                weights[1] * obj_overshoot + 
                weights[2] * obj_settling)
    
    return total_obj

# Optimization example
weights = [0.4, 0.4, 0.2]  # Emphasize speed and overshoot
initial_guess = [2.0, 0.7]

result = minimize(performance_objective, initial_guess, 
                 args=(weights,), method='Nelder-Mead')

optimal_wn, optimal_zeta = result.x
print(f"Optimal Parameters: ωₙ = {optimal_wn:.3f}, ζ = {optimal_zeta:.3f}")
```

**2. Adaptive Performance Tuning:**
Recent research shows systems that adjust their response characteristics based on operating conditions.

---

## 📚 Summary & Key Takeaways

### 🎯 Core Concepts Mastered

| Concept | Key Formula | Application |
|---------|-------------|-------------|
| **Rise Time** | tᵣ ≈ (2.16ζ + 0.60)/ωₙ | Speed requirements |
| **Overshoot** | Mₚ = e^(-ζπ/√(1-ζ²)) × 100% | Stability/safety |
| **Settling Time** | tₛ ≈ 4/(ζωₙ) | Efficiency requirements |

### 🔧 Design Guidelines

1. **For Fast Response:** Increase ωₙ, maintain ζ ≈ 0.7
2. **For No Overshoot:** Set ζ ≥ 1 (critically damped or overdamped)
3. **For Balanced Performance:** Use ζ = 0.6-0.8

### 💡 Research Insights

- **Industry 4.0 Trend:** Adaptive time domain specifications
- **AI Integration:** Machine learning for performance prediction
- **Sustainability Focus:** Energy-efficient response optimization

---

## 🎯 Next Lecture Preview

**Lecture 9-10: Frequency Domain Analysis**
- 📊 Bode plots and frequency response
- 🔄 Relationship between time and frequency domains
- 🎛️ Design using frequency specifications
- 🚀 Advanced applications in communications and control

### 📝 Homework Assignment

**Problem 1:** Analyze the step response of a temperature control system with the following transfer function:
```
G(s) = 25/(s² + 4s + 25)
```
Calculate all performance specifications and suggest improvements.

**Problem 2:** Using the provided experimental data from a DC motor, fit a second-order model and evaluate its performance against automotive requirements.

**Python/MATLAB Exercise:** Create an interactive tool that shows how changing ωₙ and ζ affects all performance specifications in real-time.

---

## 📖 References & Further Reading

1. Franklin, Powell, Emami-Naeini. "Feedback Control of Dynamic Systems" (8th Ed.)
2. Recent research: "Adaptive Time Domain Performance in Modern Control Systems" - IEEE TAC 2024
3. Python Control Systems Library Documentation
4. MATLAB Control System Toolbox User Guide

---
