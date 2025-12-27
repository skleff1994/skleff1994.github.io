---
layout: default
title: Publications
permalink: /publications/

description: selected publications

nav_bar: true
nav_order: 5
---

<div class="container" style="max-width: 900px; margin: 0 auto; padding-left: 24px; padding-right: 24px; text-align: justify;">

My up-to-date publications list is also available on <a href="https://scholar.google.com/citations?user=yBs28hUAAAAJ&hl=en">Google Scholar</a>.

<div class="bib_section" style="padding-top: 20px">
  <style>
    ol.bibliography-list {
        list-style: none;
        padding-left: 0;
    }
    ol.bibliography-list li {
        margin-bottom: 24px;
    }
    ol.bibliography-list li .bib-entry-container {
        display: flex;
        align-items: flex-start;
    }
    ol.bibliography-list li .bib-icon {
        flex-shrink: 0;
        margin-right: 15px;
    }
    /* Hide numbers on publications page */
    ol.bibliography-list li .bib-number {
        display: none;
    }
    ol.bibliography-list li .bib-text {
        flex: 1;
    }
  </style>
  <ol class="bibliography-list">
    {% bibliography %}
  </ol>
</div>

  <div class="alert alert-info" style="margin-bottom: 24px;">
    <span style="font-size: 1.1em;">Authors marked with <strong>*</strong> contributed equally to this work.</span>
  </div>
</div>