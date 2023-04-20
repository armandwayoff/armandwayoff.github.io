---
layout: archive
title: "Articles"
permalink: /articles/
author_profile: true
---

{% include base_path %}

{% for post in site.articles reversed %}
  {% include archive-single.html %}
  ___
{% endfor %}
