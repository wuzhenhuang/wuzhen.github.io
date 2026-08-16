---
layout: page
title: research
permalink: /research/
description: Selected research in X-ray imaging, advanced manufacturing, process monitoring, and materials characterization.
nav: true
nav_order: 2
horizontal: true
---

My research is organized into two complementary tracks. The first focuses on **X-ray imaging and computational CT**, from imaging physics and simulation to reconstruction and quantitative measurement. The second focuses on **manufacturing and process monitoring**, combining experiments, sensing, signal analysis, modelling, and materials characterization.

<div class="projects">

## X-ray Imaging

{% assign xray_projects = site.projects | where: "category", "xray-imaging" | sort: "importance" %}
<div class="container">
  <div class="row row-cols-1 row-cols-md-2">
  {% for project in xray_projects %}
    {% include projects_horizontal.liquid %}
  {% endfor %}
  </div>
</div>

## Manufacturing & Monitoring

{% assign manufacturing_projects = site.projects | where: "category", "manufacturing-monitoring" | sort: "importance" %}
<div class="container">
  <div class="row row-cols-1 row-cols-md-2">
  {% for project in manufacturing_projects %}
    {% include projects_horizontal.liquid %}
  {% endfor %}
  </div>
</div>

</div>
