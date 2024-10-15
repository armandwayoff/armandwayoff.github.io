---
layout: post
title: Chiffres en capitales, une coquetterie typographique
date: 2023-07-21
description: Pour des chiffres à la bonne taille ! Solutions avec \(\LaTeX\) 
tags: typographie \(\LaTeX\)
# categories: sample-posts
thumbnail: /assets/img/thumbnails/thumbnail_chiffres_en_capitales.png
featured: false
---

```latex
\usepackage{relsize} 
\newcommand{\scnums}[1]{\ifmmode\mathsmaller{#1}\else\textsmaller{#1}\fi}
```
{% include figure.html path="/assets/img/illustration_chiffres_capitaux.png" width="50%" class="img-fluid rounded z-depth-1" zoomable=true caption="<a href='https://www.overleaf.com/read/zymhxxvpzcdd#f6d96a'>Ouvrir dans Overleaf</a>"%}


