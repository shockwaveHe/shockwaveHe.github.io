---
layout: page
title: robots
permalink: /robots/
description: Here are all the robots that I have been working with!
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/projects.md -->

<div class="projects">
<!-- Display service -->
  {%- assign sorted_service = site.robots | sort: "importance" -%}
  <!-- Generate cards for each service -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for service in sorted_service -%}
      {% include service_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for service in sorted_service -%}
      {% include service.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>