---
layout: archive
title: "Figures"
permalink: /figures/
author_profile: true
---

{% include base_path %}

{% for post in site.figures reversed %}
  {% include archive-single.html %}
  ___
{% endfor %}