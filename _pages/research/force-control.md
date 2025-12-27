---
layout: default
title: Force Control
permalink: /research/force-control/
description: Research on force feedback in model-predictive control
---

<div class="container" style="max-width: 900px; margin: 0 auto; padding-left: 24px; padding-right: 24px; text-align: justify;">

<h1>Force Control</h1>

<p>
Force control techniques are well-established in robotics, however they operate in perfectly known environments under closely monitored conditions (e.g. factory setting). The recent development of Model Predictive Control (MPC) opens up the possibility for robots to optimize their behavior online based on sensor measurements. However, in MPC, contact forces are typically _planned_ rather than _controlled_ in MPC. My research aims at bridging this gap between traditional force control and modern optimal control by developing new formulations that allow to integrate directly effort measurements into MPC.

</p>

<h2 style="padding-top: 20px;">Related Publications</h2>

<div class="bib_section" style="padding-top: 20px">
  {% bibliography --query @*[key=KleffTRO || key=JordanaICRA24 || key=KleffHumanoids22 || key=KleffIROS22] %}
</div>

</div>
