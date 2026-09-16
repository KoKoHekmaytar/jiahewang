---
layout: page
title: Data-Driven Modeling and Control of Soft Robotic Systems
description: "2025: PDE+KOT+MPC+PIKO"
img: assets/img/publication_preview/RAL2026.png
importance: 1
category: research
related_publications: true
---

## Overview

<div class="embed-responsive embed-responsive-16by9 mb-4">
  <iframe
    class="embed-responsive-item"
    src="https://www.youtube.com/embed/v68kZcnB4Fk"
    title="Data-Driven Modeling and Control of Soft Robotic Systems video"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowfullscreen
  ></iframe>
</div>

This project presents a unified framework for **modeling and control of soft robotic systems**, combining physics-based modeling with data-driven methods.

The work integrates:

- A **muscle–rod PDE model** for soft actuator dynamics
- **Koopman operator learning** using EDMDc
- A control framework based on **PIKO (Physics-Informed Koopman Operator)**

📄 **Paper:**  
[Read on IEEE Xplore](https://ieeexplore.ieee.org/document/11417449)

---

## 1. Muscle–Rod PDE Model

We model the soft robotic actuator using a **continuum mechanics formulation**, where the system is described by a set of nonlinear partial differential equations (PDEs).

Key features:

- Captures **continuous deformation dynamics**
- Incorporates **actuation forces and material properties**
- Provides a **physics-consistent baseline model**

This model serves as the foundation for generating simulation data and understanding system behavior.

---

## 2. Koopman Operator Learning (EDMDc)

To enable efficient control, we approximate the nonlinear system using a **Koopman operator framework**.

We use:

- **EDMDc (Extended Dynamic Mode Decomposition with control)**
- Learned linear dynamics in a lifted space

Advantages:

- Converts nonlinear dynamics → **linear representation**
- Enables **model predictive control (MPC)**
- Efficient for real-time applications

---

## 3. PIKO Framework

We propose a **Physics-Informed Koopman Operator (PIKO)** approach that integrates:

- Physics-based structure from the PDE model
- Data-driven learning from system trajectories

This hybrid approach improves:

- Model accuracy
- Generalization across operating conditions
- Stability in control tasks

---

## Results

The proposed framework demonstrates:

- Accurate prediction of soft robot dynamics
- Improved control performance compared to baseline models
- Real-time feasibility for robotic applications

---

## Code & Reproducibility

https://github.com/KoKoHekmaytar/PIKO-Continuum-Robot-MPC-2025

---
