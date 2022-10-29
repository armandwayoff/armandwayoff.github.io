---
title: "ASCII Mandelbrot"
date: 2022-10-10
permalink: /posts/2022/ascii-mandelbrot/
tags:
  - Informatique
  - Mathématiques
---

L’ensemble MANDELBROT est un ensemble de points $(x, y)$ qui sont définis en utilisant le procédé itératif suivant. En partant des valeurs $a = 0$, $b = 0$, $c = 0$ et $k = 0$, on applique l'itération *MANDELBROT*
$$
\begin{align}
  c &= ab \\
  a &= a^2 - b^2 + x \\
  b &= 2c + y \\
  k &= k + 1
\end{align}
$$
tant que $a^2 + b^2 \leqslant 4$ est satisfait (sinon, on s'arrête). L'ensemble de MANDELBROT est constitué des points $(x, y)$ pour lesquels $k \to \infty$. Pour des raisons pratiques, on s'arrête aussi quand $k$ atteint la valeur $k_{\mathrm{max}} = 100$. Chaque pixel de l'image correspond à une valeur $(x, y)$. La "couleur" du pixel est la valeur $k$. Le coin en haut à gauche de l'image est à $(x_{\mathrm{left}}, y_\mathrm{top})$ et qui a une largeur de $x_\mathrm{width}$ et une hauteur de $y_\mathrm{height} = x_\mathrm{width} \times h / w$. 
Vous allez calculer l'ensemble MANDELBROT sur une image de taille $w \times h$ qui représente les valeurs sur un rectangle dont le coin en haut à gauche est à $(x_{\mathrm{left}}, y_\mathrm{top})$. Chaque "pixel" $(i,j)$ est associé par interpolation linéaire à une coordonnée $(x,y)$ où $i$ est le numéro de ligne et $j$ le numéro de colonne.
On attribuera au pixel $(0,0)$ la coordonnée $(x_{\mathrm{left}}, y_\mathrm{top})$ et au pixel $(w-1, h-1)$ la coordonnée $(x_{\mathrm{left}} + x_\mathrm{width}, y_\mathrm{top} - y_\mathrm{height})$.