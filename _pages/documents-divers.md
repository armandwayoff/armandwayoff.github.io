---
layout: archive
title: "Documents"
permalink: /documents/
author_profile: true
---

{% include base_path %}

La plupart des documents ci-dessous sont encore en cours de rédaction. Néanmoins, vous pouvez les consulter sur le site Overleaf. Les documents finalisés sont directement téléchargeables sous format PDF.

{% for post in site.documents reversed %}
  {% include archive-single.html %}
  ___
{% endfor %}