# Diffusion & Flow Models — Programming Assignments

<div align="center">
  <h2>KAIST CS492(C): Diffusion and Flow Models (Fall 2025)</h2>
  <p>
    Instructor: <a href="https://mhsung.github.io" target="_blank"><b>Minhyuk Sung</b></a><br>
    TA: <a href="https://dvelopery0115.github.io" target="_blank"><b>Yunhong Min</b></a><br>
    Credit: <a href="https://63days.github.io" target="_blank"><b>Juil Koo</b></a> &amp;
    <a href="https://hieuristics.xyz/" target="_blank"><b>Nguyen Minh Hieu</b></a>
  </p>
  <img src="assets/ddpm_vis.gif" width="520" alt="DDPM visualization"/>
</div>

---

## Overview

This repository contains the programming assignments for the course **Diffusion and Flow Models (CS492C)** at **KAIST**.  
Each assignment introduces a new concept in generative modeling — from the basics of diffusion processes to more advanced numerical solvers — with hands-on implementation and visualization in Python and Google Colab.

You will progressively build an intuition for how diffusion models generate data, how they can be improved for faster sampling, and how mathematical solvers are applied to real generative systems.


## 🧩 Assignment 1 — DDPM & DDIM

### Abstract
The first project introduces **Diffusion Models**, one of the most powerful modern generative frameworks.  
You will learn how to:
- Add noise step-by-step to data (the *forward* process),
- Train a neural network to remove this noise (the *reverse* process),
- And finally, generate new samples starting from pure noise.

The project covers two versions:
- **DDPM (Denoising Diffusion Probabilistic Model)** — the original stochastic sampling approach.  
- **DDIM (Denoising Diffusion Implicit Model)** — a faster, deterministic variant that can produce similar results with fewer steps.

Through this assignment, you’ll visualize how points in a 2D dataset evolve under noise, and how the trained model can reverse this process to create new data from randomness.

---

## ⚙️ Assignment 2 — DPM-Solver

### Abstract
The second project focuses on improving the **efficiency** of diffusion sampling.  
You will explore the idea behind **DPM-Solver**, a method that views the diffusion process as an ordinary differential equation (ODE).  
Instead of relying on many small denoising steps, DPM-Solver computes a more direct path from noise to data using clever numerical approximations.

In simple terms:
- DDPM takes *many small steps* to generate one sample.  
- DPM-Solver tries to reach the same result with *just a few larger steps*, by solving the underlying equations more accurately.

You’ll experiment with **first-order** and **second-order** versions of the solver, compare their results, and see how increasing solver accuracy reduces the number of required sampling steps.

---

## 🧠 Learning Goals

Across the assignments, you will:
- Understand the connection between diffusion models and noise prediction.  
- Visualize the sampling trajectory of stochastic vs. deterministic models.  
- Implement numerical solvers that accelerate generation while keeping high sample quality.  
- Build a strong conceptual foundation for modern generative AI techniques such as Stable Diffusion and Flow Matching models.

---

## 🚀 How to Run

### Option 1 — Google Colab (recommended)
1. Open the notebook file (e.g. `A1_DDPM_DDIM/DDPM_DDIM.ipynb`) in Google Colab.  
2. Follow the setup cell at the top of the notebook.  
3. Run all cells in sequence and complete the `TODO` parts.

### Option 2 — Local environment
1. Use Python ≥ 3.10  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Launch Jupyter and open the desired notebook.
