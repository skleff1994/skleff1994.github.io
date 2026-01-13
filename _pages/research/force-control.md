---
layout: default
title: Force Control
permalink: /research/force-control/
description: Research on force feedback in model-predictive control
---

<div class="container" style="max-width: 900px; margin: 0 auto; padding-left: 24px; padding-right: 24px; text-align: justify;">

<h1>Force Control</h1>

<p>
The performance of Model-Predictive Control is fundamentally limited in tasks involving contact with the environment.
In contrast, force control techniques are well-established in robotics, but they inherently lack planning capabilities.
During my PhD, I proposed explored different ways to explain and bridge this critical gap. I developed, tested and evaluated novel MPC formulations that allow to systematically include measured efforts into modern optimal control. 
</p>

<p>
The first idea I investigated during my PhD was to model the actuation dynamics in order to include joint torque measurement feedback <a href="#bib-KleffIROS22">[1]</a>. This formulation has the avantage of not requiring additional sensors on torque-controlled robots while increasing the force control performance in dynamic contact tasks w.r.t. the standard MPC formulation.
</p>

<p>
Another idea relied on direct force modeling as a visco-elastic phenomena. This led to a powerful formulation that showed state-of-the-art performance in a wide range of tasks including force/motion tracking, multi-contactand and hard nonlinear constraints <a href="#bib-KleffTRO">[2]</a>. Crucially, this work demonstrates experimentally that MPC and force control can combine within a single control architecture without impeding any of their individual benefits, and outperforming each of them taken individually.
</p>

<p>
I also investigated another solution in collaboration with <a href="https://scholar.google.com/citations?user=zLICCioAAAAJ&hl=en&oi=ao" target="_blank" rel="noopener noreferrer">Armand Jordana</a>, that relied on online estimation of the contact force modeling error in a disturbance-observer-like fashion <a href="#bib-JordanaICRA24">[3]</a>. This simple formulation allowed surprisingly good performance.
</p>


<p>
Formulating force tasks in arbiratry frames also required to derive contact dynamics derivatives in moving coordinates <a href="#bib-KleffHumanoids22">[4]</a>. This formulation was added to the <a href="https://github.com/loco-3d/crocoddyl">Crocoddyl</a> optimal control library.
</p>

<p>
The force feedback MPC formulation has also been used in combination with higher level planning to achieve challenging industrial tasks such as deburring <a href="#bib-WojciechowskiDeburring">[5]</a>.
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
    <li id="bib-KleffIROS22">
      <span class="bib-number">[1]</span>
      <div class="bib-content">
        <strong>S. Kleff</strong>, E. Dantec, G. Saurel, N. Mansard, L. Righetti,
        "Introducing Force Feedback in Model Predictive Control",
        <em>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</em>, 2022.
        <br>
        <a href="https://hal.science/hal-03594295/document" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://www.youtube.com/watch?v=EErwxOrCnnQ" class="btn_bib btn btn-sm" target="_blank">Video</a>
      </div>
    </li>
    <li id="bib-KleffTRO">
      <span class="bib-number">[2]</span>
      <div class="bib-content">
        <strong>S. Kleff</strong>, A. Jordana, N. Mansard, L. Righetti,
        "Force Feedback Model Predictive Control: A Soft Contact Approach",
        <em>Preprint</em>, 2025.
        <br>
        <a href="https://hal.science/hal-04572399v2/document" class="btn_bib btn btn-sm" target="_blank">Preprint</a>
        <a href="https://youtu.be/tRDU4Flo7Lg?si=x01E5S3qqQpRtQfQ" class="btn_bib btn btn-sm" target="_blank">Video</a>
      </div>
    </li>
    <li id="bib-JordanaICRA24">
      <span class="bib-number">[3]</span>
      <div class="bib-content">
        A. Jordana*, <strong>S. Kleff*</strong>, J. Carpentier, N. Mansard, L. Righetti,
        "Force Feedback Model-Predictive Control via Online Estimation",
        <em>IEEE International Conference on Robotics and Automation (ICRA)</em>, 2024.
        <br>
        <a href="https://hal.science/hal-04564888v1/document" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://www.youtube.com/watch?v=4A-766qsWHI" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/machines-in-motion/force_observer" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
    <li id="bib-KleffHumanoids22">
      <span class="bib-number">[4]</span>
      <div class="bib-content">
        <strong>S. Kleff</strong>, J. Carpentier, N. Mansard, L. Righetti,
        "On the Derivation of the Contact Dynamics in Arbitrary Frames (Application to Polishing with Talos)",
        <em>IEEE-RAS International Conference on Humanoid Robots (Humanoids)</em>, 2022.
        <br>
        <a href="https://hal.science/hal-03758989/file/HUMANOIDS_2022_FINAL.pdf" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://www.youtube.com/watch?v=5pMWWsgXKe0" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/MeMory-of-MOtion/sobec" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
    <li id="bib-WojciechowskiDeburring">
      <span class="bib-number">[5]</span>
      <div class="bib-content">
      K. Wojciechowski, E. Gursoy, A. Haffemayer, <strong>S. Kleff</strong>, V. Bonnet, F. Lamiraux, N. Mansard
        "Learning-Guided Force-Feedback Model Predictive Control with Obstacle Avoidance for Robotic Deburring",
        <em>Preprint</em>, 2025.
        <br>
        <a href="https://hal.science/hal-05320433v1/file/deburring_paper-4.pdf" class="btn_bib btn btn-sm" target="_blank">Paper</a>
        <a href="https://peertube.laas.fr/w/oY2KeZcjdsmfywg5aH3y34" class="btn_bib btn btn-sm" target="_blank">Video</a>
        <a href="https://github.com/agimus-project/agimus-demos/tree/humble-devel" class="btn_bib btn btn-sm" target="_blank">Code</a>
      </div>
    </li>
  </ol>
</div>

