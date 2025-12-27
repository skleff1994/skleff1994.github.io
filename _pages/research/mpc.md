---
layout: default
title: Model Predictive Control
permalink: /research/mpc/
description: Research on nonlinear model-predictive control for robotics
---

<div class="container" style="max-width: 900px; margin: 0 auto; padding-left: 24px; padding-right: 24px; text-align: justify;">

<h1>Model Predictive Control</h1>

<p>
Model-Predictive Control (MPC) is an appealing framework to control robots due to its ability to reason over the future and to update decisions online based on sensory information. 
<!-- Its effectiveness in generating automatically complex motions is now well recognized by the community. -->
Part of my research focuses on developing efficient numerical tools for nonlinear MPC on torque-controlled robots.
</p>

<p>
In particular during the early years of my PhD, I proposed the first implementation of high-frequency nonlinear MPC on a torque-controlled manipulator, thereby demonstrating experimentally those benefits and opening up new possibilities for the real-time motion generation and control of robots {% cite KleffICRA21 %}. 
</p>

<p>
Adding inequality constraints in the MPC problem has long been considered a challenging problem in robotics. With my colleagues (with <a href="https://scholar.google.com/citations?user=zLICCioAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Armand Jordana</a> and <a href="https://scholar.google.com/citations?user=DsGVfRwAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Avadesh Meduri</a>), we showed that it is possible to address this issue by tailoring standard numerical optimization tools to the MPC problem by exploiting its structure (a.k.a. sparsity). We developed a state-of-the-art Sequential Quadratic Programming (SQP) solver for nonlinear MPC {% cite JordanaSQP %}, showing the first implementation of inequality constraints in MPC on torque-controlled robots. The solver is open-sourced in the <a href="https://github.com/machines-in-motion/mim_solvers" target="_blank" rel="noopener noreferrer">mim_solvers</a> library and is actively maintained.
<p>

<p>
During my PhD, I also collaborated with Armand Jordana
Part of my research also focused onthe limitations of finite-horizon MPC related to local minima and short-sighted behavior. In <i>Infinite-Horizon Value Function Approximation for Model Predictive Control</i>, we showed that learning an approximation of the infinite-horizon value function and embedding it as a terminal cost in MPC effectively mitigates local minima issues and improves long-term decision making. In complementary work, we demonstrated how value functions and their derivatives can be leveraged to significantly accelerate learning in MPC-based control, bridging optimal control and learning while retaining strong performance guarantees on torque-controlled robots.
</p>



<h2 style="padding-top: 20px;">Related Publications</h2>

<div class="bib_section" style="padding-top: 20px">
  {% bibliography --query @*[key=JordanaSQP || key=JordanaValue2025 || key=KleffICRA21 || key=Parag2022] %}
</div>

</div>
