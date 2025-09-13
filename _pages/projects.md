---
layout: page
title: projects
permalink: /projects/
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
_styles: |
  .post-title {
    display: none;
  }
---

<!-- pages/projects.md -->
<div class="projects">

<!-- Research Projects Section -->
<h2 class="category">Research Projects</h2>
{% assign sorted_projects = site.projects | sort: "importance" %}
<div class="row row-cols-1 row-cols-md-3">
  {% for project in sorted_projects %}
    {% include projects.liquid %}
  {% endfor %}
</div>

<!-- Course Projects Section -->
<h2 class="category">Course Projects</h2>
{% assign sorted_course_projects = site.courseprojects | sort: "importance" %}
<div class="row row-cols-1 row-cols-md-3">
  {% for project in sorted_course_projects %}
    {% include projects.liquid %}
  {% endfor %}
</div>

</div>

