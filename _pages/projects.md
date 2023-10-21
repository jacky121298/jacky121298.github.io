---
layout: barebone
title: Projs & Leisure
permalink: /projects/
description:
nav: true
nav_order: 2
display_categories:
horizontal: false
---

<!-- pages/projects.md -->
<article>

<h1 class="post-title">Projects</h1>
<p class="post-description">
other interesting computer science-related projects🧑🏻‍💻
</p>
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>

<h1 class="post-title">Leisure</h1>
<p class="post-description">
Badminton🏸 / Competition🏅 / Travel🚀
</p>
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.leisure | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  <div class="img-slides">
  {% include image_slides.html %}
  </div>
</div>
</article>