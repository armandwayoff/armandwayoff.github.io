---
layout: page
title: Galerie de figures
permalink: /figures/
soustitre: "Quelques figures mathématiques réalisées avec Ti<span style='font-style:italic;'>k</span>Z et <span style='font-style:italic;'>Inkscape</span>"
description: "Vous trouverez un grand nombre de mes figures dans le <a href='https://ensta-paris.hal.science/hal-03243924v3/document'>polycopié du cours <span class='capitales'>aot</span><span class='chiffres-capitaux'>13</span> de l'<span class='capitales'>ensta</span> <span class='capitales'>p</span>aris - <i>Géométrie Différentielle
et Application au Contrôle Géométrique</i> de Frédéric <span class='capitales'>Jean</span></a>."
nav: true
nav_order: 3
horizontal: false
---

<!-- pages/figures.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized figures -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.figures | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each figure -->
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
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.figures | sort: "importance" -%}
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
{%- endif -%}
</div>
