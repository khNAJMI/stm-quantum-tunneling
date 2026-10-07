STM: Quantum Tunneling Through a Potential Barrier
Simulation of the tunneling current that powers the Scanning TunnelingMicroscope (STM). Modern Physics project — UM6P, January 2026.

Authors: Khawla Najmi · Alex Lankoande · Yssouf Sana École de Physique Appliquée et d'Ingénierie, UM6P
Physics Background
In an STM, electrons tunnel quantum-mechanically across the vacuum gapbetween a sharp tip and a conducting sample. Solving the 1D Schrödingerequation for a rectangular barrier (WKB approximation) gives a transmissionprobability T(d) ≈ exp(−2κd), leading to the exponential current–distance law:

I(d) = I0 · exp[−k (d − d0)]     with k ≈ 20 nm⁻¹, I0 = 1.0 nA, d0 = 0.30 nm
Why It Matters
This exponential dependence is why the STM sees atoms:

Displacement Δd	Current change
0.05 nm (half an atom)	÷ 2.7
0.10 nm (one atom)	÷ 7.4
0.20 nm (atomic step)	÷ 55
A displacement the size of one atom changes the current by a factor of ~7 —easily measurable, giving atomic resolution.

What the Code Does
Implements the I(d) exponential model
Prints the sensitivity table (current vs. displacement)
Reproduces both presentation plots: linear-scale decay and semi-logvalidation (straight line ⇒ exponential law confirmed)
How to Run
Requires Python 3 with numpy and matplotlib:

pip install numpy matplotlibpython stm_tunneling.py
Results
See tunneling_current.png — generated output matching our analysis.

Presentation
slides.pdf (in French) contains the full 16-slide walkthrough: WKBderivation, bias-dependent tunneling mechanism, and STM spectroscopy(dI/dV ∝ local density of states).

📤 What to upload to the repo stm-quantum-tunneling
stm_tunneling.py
README.md
slides.pdf — your presentation (fine to include since you're a listed author; if you want, rename it slides-um6p-2026.pdf)
tunneling_current.png — run the script once, and upload the output
⚠️ One etiquette point: it's a group project with Alex and Yssouf. Listing them in the README (as I did) is the right move — and quickly ask them if they're okay with it being public.

🔗 Then update your CV (2 places)
Header: add your GitHub URL under your email.

STM project bullet — upgraded:

Modern Physics Research — STM Quantum Tunneling | UM6P | Jan 2026

Modeled tunneling current I(d) = I₀exp[−k(d−d₀)], k ≈ 20 nm⁻¹; demonstrated ×7 current change per 0.1 nm displacement — the physical origin of atomic resolution
Validated the exponential law via semi-log analysis; co-presented a 16-slide talk
Code & slides: github.com/username/stm-quantum-tunneling
🚀 Optional stretch goal (this would really impress)
Right now the repo shows the analytical model. Later, we could add a second script that numerically solves the Schrödinger equation (transfer-matrix method) for a rectangular barrier and plots real transmission T(E) — going from "used a formula" to "solved the physics." Say the word and I'll write it.

Quick questions:

Have you created the GitHub account yet? Which username did you pick?
Are Alex and Yssouf okay with the public repo?
Want the Schrödinger solver script now, or after the first upload is done?
