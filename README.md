Recoverability Band in Delayed Dissipative Systems

This repository contains the code used to generate all numerical results and figures in the manuscript
“Recoverability as a Band-Limited Property in Delayed Dissipative Systems”.

Overview

We study recoverability in a minimal delayed stochastic dynamical system, defined as the probability that the system returns to and remains near a reference state after a finite perturbation.
All results are obtained by direct numerical simulation and Monte Carlo sampling.

Main script

run_recoverability_analysis.py
Runs all simulations, saves numerical results (CSV), and generates all figures used in the manuscript.

Model

The system is governed by the delayed stochastic differential equation

dx/dt = −γ x(t) + k tanh(x(t−τ)) + β x(t)³ + σ ξ(t)

with fixed parameters:

k = 2.0 (feedback gain)

σ = 0.02 (noise intensity)

A = 1.0 (perturbation amplitude)

Unless stated otherwise, β = 0.

Numerical settings

Time steps: Δt = 1×10⁻³ and 5×10⁻⁴

Total simulation time: T = 20

Integration: Euler–Maruyama scheme

Delay implemented via circular buffer

Random seed fixed for reproducibility

Outputs
Figures (used in the manuscript)

Figure 1a,b: Recoverability phase diagrams R(τ, γ)

Figure 2: Difference map ΔR between temporal resolutions

Figure 3a,b: Thresholded recoverability maps

Figure 4a,b: Effect of weak cubic nonlinearity and ΔR

Band-edge plots with recovery time statistics

Data files

Recoverability tables R(τ, γ)

Difference maps ΔR

Band-edge locations (γ_min, γ_max)

Median recovery times T_rec

All numerical values reported in the Results section are directly computed from these files.

Reproducibility

Running the main script reproduces:

All figures

All numerical values reported in the manuscript

No supplemental material is required

Dependencies

Python ≥ 3.9

numpy

scipy

matplotlib

pandas
