---
layout: barebone
title: Projs & more
permalink: /projects/
description: A growing collection of cool projects.
nav: true
nav_order: 2
display_categories:
horizontal: false
cv_pdf: CV_Shih-Lun_Wu_Oct24.pdf
---

<!-- pages/projects.md -->
<article>

<h1 class="post-title">Projects</h1>
<p class="post-description">
other cool stuff built together with my colleagues
</p>
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects_work | sort: "importance" -%}
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
travel / hiking / dessert baking🍰 / table tennis🏓 / classical music (piano🎹 & viola🎻)
</p>
<div class="projects">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects_leisure | sort: "importance" -%}
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
