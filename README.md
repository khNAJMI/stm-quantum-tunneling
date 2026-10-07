# STM: Quantum Tunneling Through a Potential Barrier

Simulation of the tunneling current that powers the Scanning Tunneling Microscope (STM).

**Modern Physics project — UM6P, January 2026**

**Authors:** Khawla Najmi · Alex Lankoande · Yssouf Sana
*École de Physique Appliquée et d'Ingénierie, UM6P*

---

## Physics Background

In an STM, electrons tunnel quantum-mechanically across the vacuum gap between a sharp tip and a conducting sample. Solving the 1D Schrödinger equation for a rectangular barrier (WKB approximation) gives a transmission probability:

$$T(d) \approx \exp(-2\kappa d)$$

leading to the exponential current–distance law:

$$I(d) = I_0 \cdot \exp[-k(d - d_0)]$$

with $k \approx 20 \text{ nm}^{-1}$, $I_0 = 1.0 \text{ nA}$, $d_0 = 0.30 \text{ nm}$



## Why It Matters

This exponential dependence is why the STM sees atoms:

| Displacement Δd | Current change |
|-----------------|----------------|
| 0.05 nm (half an atom) | ÷ 2.7 |
| 0.10 nm (one atom) | ÷ 7.4 |
| 0.20 nm (atomic step) |  ÷ 55 |

A displacement the size of one atom changes the current by a factor of ~7 — easily measurable, giving **atomic resolution**.



## What the Code Does

- Implements the $I(d)$ exponential model
- Prints the sensitivity table (current vs. displacement)
- Reproduces both presentation plots:
  - Linear-scale decay
  - Semi-log validation (straight line → exponential law confirmed)



## How to Run

Requires Python 3 with `numpy` and `matplotlib`:

```bash
pip install numpy matplotlib
python stm_tunneling.py
