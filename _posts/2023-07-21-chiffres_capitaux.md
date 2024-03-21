---
layout: post
title: Chiffres en capitales
date: 2023-07-21
description: Pour des chiffres à la bonne taille ! Solutions avec \(\LaTeX\) et CSS
# tags: typographie \(\LaTeX\) CSS
# categories: sample-posts
featured: false
---

## $$\LaTeX$$

#### Implémentation

```latex
\usepackage{relsize} 
\newcommand{\scnums}[1]{\ifmmode\mathsmaller{#1}\else\textsmaller{#1}\fi}
```

#### Illustration

<center>
    <img src="/assets/img/illustration_chiffres_capitaux.png" style="width: 100%;">
</center>
<a href="https://www.overleaf.com/read/zymhxxvpzcdd#f6d96a">Ouvrir dans Overleaf</a>

## **CSS**

#### Implémentation

```css
.chiffres-capitaux {
  font-size: smaller;
  text-transform: uppercase;
}
```

```css
<span class="chiffres-capitaux">11</span>
```

#### Illustration

Chiffres majuscules : 13 <br/>
Chiffres capitaux : <span class="chiffres-capitaux">13</span>


