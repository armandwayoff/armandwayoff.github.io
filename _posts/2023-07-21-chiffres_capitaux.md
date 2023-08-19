---
layout: post
title: Chiffres capitaux avec \(\LaTeX\)
date: 2023-07-21
description: Pour des chiffres à la bonne taille !
tags: typographie \(\LaTeX\)
# categories: sample-posts
featured: false
---
```latex
\newcommand{\scnums}[1]{\ifmmode\mathsmaller{\newstylenums{#1}}\else\textsmaller{\newstylenums{#1}}\fi}
```