---
layout: archive
title: "Projets"
permalink: /projets/
author_profile: true
---

{% include base_path %}

{% for post in site.projets reversed %}
  {% include archive-single.html %}
  ___
{% endfor %}