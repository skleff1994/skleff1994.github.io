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
Part of my research focuses on developing new tools to achieve this potential and push the limits of nonlinear MPC in practice on torque-controlled robots.
</p>

<p>
In particular during the early years of my PhD, I proposed the first implementation of high-frequency nonlinear MPC on a torque-controlled manipulator, thereby demonstrating experimentally those benefits and opening up new possibilities for the real-time motion generation and control of robots <a href="#bib-KleffICRA21">[3]</a>. 
</p>

<p>
Adding inequality constraints in the MPC problem has long been considered a challenging problem in robotics. With my colleagues (with <a href="https://scholar.google.com/citations?user=zLICCioAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Armand Jordana</a> and <a href="https://scholar.google.com/citations?user=DsGVfRwAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Avadesh Meduri</a>), we showed that it was possible to tackle this issue by tailoring standard numerical optimization algorithms to the MPC problem by exploiting its structure (a.k.a. sparsity). We developed a state-of-the-art Sequential Quadratic Programming (SQP) solver for nonlinear MPC <a href="#bib-JordanaSQP">[1]</a>, showing the first implementation of inequality constraints in MPC on torque-controlled robots. The solver is open-sourced in the <a href="https://github.com/machines-in-motion/mim_solvers" target="_blank" rel="noopener noreferrer">mim_solvers</a> library and is actively maintained.
<p>

<p> 
I also contributed to pushing the limits of MPC, by investigating how the Value Function (VF) can serve as a terminal cost. I collaborated with <a href="https://scholar.google.com/citations?user=wsRIfL4AAAAJ&hl=en" target="_blank" rel="noopener noreferrer">Amit Parag</a> to develop and validate a Sobolev learning framework that exploits derivatives of the value function to accelerate reinforcement learning<a href="#bib-Parag2022">[4]</a>. I also collaborated with <a href="https://scholar.google.com/citations?user=zLICCioAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Armand Jordana</a> to extend this idea to constrained problems by learning the infinite-horizon value functionm which enabled MPC to escape from local minima<a href="#bib-JordanaValue2025">[2]</a>.
</p>



<h2 style="padding-top: 20px;">Related Publications</h2>

<div class="bib_section" style="padding-top: 20px">
  <style>
    .manual-bib-list {
        list-style: none;
        padding-left: 0;
    }
    .manual-bib-list li {
        margin-bottom: 24px;
        display: flex;
        align-items: flex-start;
    }
    .manual-bib-list .bib-number {
        flex-shrink: 0;
        margin-right: 10px;
        font-weight: bold;
    }
    .manual-bib-list .bib-content {
        flex: 1;
    }
  </style>
  
  <ol class="manual-bib-list">
    <li id="bib-JordanaSQP">
      <span class="bib-number">[1]</span>
      <div class="bib-content">
        A. Jordana*, <strong>S. Kleff*</strong>, A. Meduri*, J. Carpentier, N. Mansard, L. Righetti,
        "Structure-Exploiting Sequential Quadratic Programming for Model-Predictive Control",
        <em>IEEE Transactions on Robotics</em>, 2025.
        <br>
        <a href="https://laas.hal.science/hal-04330251v2/file/SQP_OC_paper_final.pdf" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://www.youtube.com/watch?v=eXAQ10NDbbg" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/machines-in-motion/mim_solvers" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
    
    <li id="bib-JordanaValue2025">
      <span class="bib-number">[2]</span>
      <div class="bib-content">
        A. Jordana, <strong>S. Kleff</strong>, A. Haffemayer, J. Ortiz-Haro, J. Carpentier, N. Mansard, L. Righetti,
        "Infinite-Horizon Value Function Approximation for Model Predictive Control",
        <em>IEEE Robotics and Automation Letters</em>, 2025.
        <br>
        <a href="https://doi.org/10.1109/LRA.2025.3577875" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://youtu.be/CruTx2CvcFQ?si=45bWfp094Mx0v_WY" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/ajordana/value_function" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
    
    <li id="bib-KleffICRA21">
      <span class="bib-number">[3]</span>
      <div class="bib-content">
        <strong>S. Kleff</strong>, A. Meduri, R. Budhiraja, N. Mansard, L. Righetti,
        "High-Frequency Nonlinear Model Predictive Control of a Manipulator",
        <em>IEEE International Conference on Robotics and Automation (ICRA)</em>, 2021.
        <br>
        <a href="https://hal.science/hal-02993058v1/file/ICRA21_skleff.pdf" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://www.youtube.com/watch?v=5pMWWsgXKe0" class="btn_bib btn btn-sm" target="_blank">Video</a>
      </div>
    </li>
    
    <li id="bib-Parag2022">
      <span class="bib-number">[4]</span>
      <div class="bib-content">
        A. Parag, <strong>S. Kleff</strong>, L. Saci, N. Mansard, O. Stasse,
        "Value learning from trajectory optimization and Sobolev descent: A step toward reinforcement learning with superlinear convergence properties",
        <em>IEEE International Conference on Robotics and Automation (ICRA)</em>, 2022.
        <br>
        <a href="https://hal.science/hal-03356261v1/file/icra_2021.pdf" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://peertube.laas.fr/w/17uzneDe7QVAZs5ePc8WKM" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/amitparag/Kuka-arm-DvP" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
  </ol>
</div>
