---
layout: default
title: Robust Motion Planning
permalink: /research/robust-planning/
description: Research on robust motion planning using reachability analysis
---

<div class="container" style="max-width: 900px; margin: 0 auto; padding-left: 24px; padding-right: 24px; text-align: justify;">

<h1>Robust Motion Planning</h1>

<p>
Traditional motion planning methods often fail to provide formal robust safety and performance guarantees. My research leverages Hamilton-Jacobi reachability analysis and differential games to compute provably safe motion plans in time-varying and adversarial environments under parametric uncertainty. This work also addresses stochastic trajectory optimization for handling uncertainties in contact interactions.
</p>

<h2 style="padding-top: 20px;">Related Publications</h2>

<div class="bib_section" style="padding-top: 20px">
  <style>
    ol.bib-numbered {
        list-style: none;
        padding-left: 0;
    }
    ol.bib-numbered li {
        margin-bottom: 24px;
    }
    ol.bib-numbered li .bib-entry-container {
        display: flex;
        align-items: flex-start;
    }
    /* Hide icons on research pages */
    ol.bib-numbered li .bib-icon {
        display: none;
    }
    ol.bib-numbered li .bib-number {
        flex-shrink: 0;
        margin-right: 10px;
        font-weight: bold;
    }
    ol.bib-numbered li .bib-text {
        flex: 1;
    }
  </style>
  <ol class="bib-numbered">
  {% bibliography --query @*[key=KleffRobotica20 || key=KleffCCDC2018 || key=Gazar22] %}
  </ol>
</div>

</div>
