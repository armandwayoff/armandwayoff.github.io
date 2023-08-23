---
layout: post
title: Chiffres capitaux
date: 2023-07-21
description: Pour des chiffres à la bonne taille ! Solutions avec \(\LaTeX\) et CSS
tags: typographie \(\LaTeX\) CSS
# categories: sample-posts
featured: false
---

```latex
\newcommand{\scnums}[1]{\ifmmode\mathsmaller{\newstylenums{#1}}\else\textsmaller{\newstylenums{#1}}\fi}
```

```css
.chiffres-capitaux {
  font-size: smaller;
  text-transform: uppercase;
}
```