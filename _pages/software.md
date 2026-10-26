---
layout: archive
title: "Software"
permalink: /software/
author_profile: true

nav_bar: true
nav_order: 6
---

{% include base_path %}

I am actively involved in developing open-source software for robotics research, with a focus on numerical optimization and Model Predictive Control (MPC).

<!-- ## Main Projects
======

### mim_solvers -->
I am one of the main developers and managers of the <a href="https://github.com/machines-in-motion/mim_solvers" target="_blank" rel="noopener noreferrer">mim_solvers</a> library, an efficient numerical optimization solver tailored for nonlinear Model-Predictive Control, compatible with the <a href="https://github.com/loco-3d/crocoddyl" target="_blank" rel="noopener noreferrer">Crocoddyl</a> library. It enables real-time constrained MPC on manipulators, quadrupeds, humanoids and drones, is used by 20+ researchers across several groups, and supported the EU project AGIMUS.

I am also the main developer of <a href="https://github.com/machines-in-motion/force_feedback_mpc" target="_blank" rel="noopener noreferrer">force_feedback_mpc</a>, the first experimentally validated implementation of force-feedback MPC on modern manipulators, interfaced with Crocoddyl and used in the EU project AGIMUS for industrial deburring and polishing tasks. The companion repository <a href="https://github.com/machines-in-motion/force_feedback_dgh" target="_blank" rel="noopener noreferrer">force_feedback_dgh</a> provides real-time deployment code for the Kuka iiwa.

<!-- **Key Features:**
* High-performance numerical optimization for MPC
* Integration with Crocoddyl for optimal control problem formulation
* Designed for real-time applications on robotic systems -->

<!-- ### croco_mpc_utils -->
I contributed to the <a href="https://github.com/loco-3d/crocoddyl" target="_blank" rel="noopener noreferrer">Crocoddyl</a> library by implementing constrained forward dynamics derivatives in moving coordinates, enhancing the library's capabilities for contact tasks. 

I also contributed to the development and democratization of nonlinear MPC in the robotics community through the <a href="https://github.com/machines-in-motion/croco_mpc_utils" target="_blank" rel="noopener noreferrer">croco_mpc_utils</a> plugin and introductory examples to Crocoddyl <a href="https://github.com/machines-in-motion/minimal_examples_crocoddyl" target="_blank" rel="noopener noreferrer">minimal_examples_crocoddyl</a>. These tools enable rapid prototyping of Optimal Control Problems in Crocoddyl through templated configuration files and provides visualization of solutions, effectively lowering the barrier of entry for new users. I also maintain a tutorial on MPC <a href="https://github.com/skleff1994/mpc_tutorial" target="_blank" rel="noopener noreferrer">mpc_tutorial</a>.

<!-- **Key Features:**
* Quick prototyping of Optimal Control Problems
* Template-based configuration files
* Solution visualization tools -->

<!-- ## Contributions
====== -->

<!-- ### Crocoddyl -->


<!-- ## Code Availability
====== -->

You can visit my <a href="https://github.com/skleff1994" target="_blank" rel="noopener noreferrer">GitHub page</a> to find more about my software activity. 
