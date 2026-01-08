# Four-bar-linkage
# Four-Bar Linkage Modeling and Simulation in Python

This project presents a complete workflow for modeling, solving, and
simulating a planar four-bar linkage mechanism using numerical methods
in Python.

The focus is on problem formulation, nonlinear equation solving,
and numerical validation rather than purely analytical solutions.

---

## Motivation

Mechanical systems are governed by nonlinear constraints that often
do not admit closed-form solutions. Accurately modeling such systems
requires translating physical laws into mathematical equations and
solving them numerically.

This project demonstrates foundational skills that are also critical
in applied AI and model-based machine learning:
- Mathematical modeling
- Nonlinear optimization
- Numerical stability and validation

---

## Problem Formulation

A planar four-bar linkage consists of four rigid links connected by
revolute joints.

Given:
- Link lengths \( l_1, l_2, l_3, l_4 \)
- Input joint angle \( \theta_2 \)

Find:
- Unknown joint angles \( \theta_3 \) and \( \theta_4 \)
- The corresponding mechanism configuration

The kinematic loop-closure equation is written in vector form and
separated into real and imaginary components, resulting in a system
of two nonlinear equations.

---

## Methodology

1. Derive the kinematic loop-closure equations.
2. Formulate the problem as a system of nonlinear equations.
3. Solve the system using `scipy.optimize.fsolve`.
4. Validate solutions through geometric reconstruction.
5. Simulate continuous motion by sweeping the input angle and
   reusing previous solutions for numerical stability.
6. Visualize both static configurations and dynamic motion.

---

## Results

- Successful convergence of joint angles for valid input ranges.
- Geometrically consistent closed-loop configurations.
- Smooth motion during dynamic simulation.

Static visualization and animation are used to verify the correctness
of numerical solutions.

---

## How to Run

```bash
pip install numpy scipy matplotlib
