---
title: "ASCII Mandelbrot"
date: 2022-10-10
permalink: /posts/2022/ascii-mandelbrot/
excerpt: "Écrivez un programme pour calculer une image Mandelbrot, la stocker dans un tableau et l’afficher
sous forme de caractères ASCII. La largeur `w` et l’hauteur `h` de l’image (en caractères) sera définie par
les arguments de la ligne de commande. Procédez étape par étape, en suivant les indications données par
les questions ci-dessous."
tags:
  - Informatique
  - Mathématiques
---

L’ensemble Mandelbrot est un ensemble de points $(x, y)$ qui sont définis en utilisant le procédé itératif suivant. En partant des valeurs $a = 0$, $b = 0$, $c = 0$ et $k = 0$, on applique l'itération *Mandelbrot*

$$
\begin{align*}
  c &= ab \\
  a &= a^2 - b^2 + x \\
  b &= 2c + y \\
  k &= k + 1
\end{align*}
$$

tant que $a^2 + b^2 \leqslant 4$ est satisfait (sinon, on s'arrête). L'ensemble de Mandelbrot est constitué des points $(x, y)$ pour lesquels $k \to \infty$. Pour des raisons pratiques, on s'arrête aussi quand $k$ atteint la valeur $k_{\mathrm{max}} = 100$. Chaque pixel de l'image correspond à une valeur $(x, y)$. La "couleur" du pixel est la valeur $k$. Le coin en haut à gauche de l'image est à $(x_{\mathrm{left}}, y_\mathrm{top})$ et qui a une largeur de $x_\mathrm{width}$ et une hauteur de $y_\mathrm{height} = x_\mathrm{width} \times h / w$. 
Vous allez calculer l'ensemble Mandelbrot sur une image de taille $w \times h$ qui représente les valeurs sur un rectangle dont le coin en haut à gauche est à $(x_{\mathrm{left}}, y_\mathrm{top})$. Chaque "pixel" $(i,j)$ est associé par interpolation linéaire à une coordonnée $(x,y)$ où $i$ est le numéro de ligne et $j$ le numéro de colonne.
On attribuera au pixel $(0,0)$ la coordonnée $(x_{\mathrm{left}}, y_\mathrm{top})$ et au pixel $(w-1, h-1)$ la coordonnée $(x_{\mathrm{left}} + x_\mathrm{width}, y_\mathrm{top} - y_\mathrm{height})$.

Dans l’image Mandelbrot, chaque caractère affiché sera un des 16 caractères suivants (le permier est un espace) : ` .,:;-+uco*#&8%@`.

```c
#include <stdio.h>
#include <math.h>
#include "paint.h"

int compter_iterations(double x, double y, int max_iter) {
  int iter = 0;
  double a = 0.0;
  double b = 0.0;
  double ab = 0.0;
  while (a*a+b*b<4.0 && iter<max_iter) {
    ab = a*b;
    a = a*a - b*b + x;
    b = 2 * ab + y;
    ++iter;
  }
  return iter;
}

unsigned char map_R(double z) {
  return 255*pow(z,0.5);
}

unsigned char map_G(double z) {
  return 200*sin(M_PI*z);
}

unsigned char map_B(double z) {
  return 255-255*z;
}

int main ()
{
  int width = 1080;
  int height = 720;
  int max_iter = 100;
  double max_val = 4.0;

  double x_left = -2;
  double y_top = 1;
  double x_width = 3;
  double y_height = 2;
  
  // Creer les pixels pour dessiner
  unsigned char* pixels = create_pixels(width,height);

  char r,g,b;
  double x,y,z;
  int i,j;
  for (i=0;i<width;++i) {
    for (j=0;j<height;++j) {
      // Calculer (x,y) par interpolation
      // attention, y commence en haut, à y_max
      x = x_left+x_width*i/width;
      y = y_top-y_height*j/height;
      // Calculer iterations pour (x,y)
      int iter = compter_iterations(x,y,max_iter);
      z = (double)iter/max_iter;
      // Calculer la couleur
      if (iter==max_iter) {
        r = 0;
        g = 0;
        b = 0;
      } else {
        r = map_R(z);
        g = map_G(z);
        b = map_B(z);
      }
      // Colorier le pixel
      color_pixel(i,j,r,g,b,width,height,pixels);
    }
  }

  /* Ecrire vers un fichier BMP */
  save_BMP("mandelbrot.bmp", width, height, pixels);

  /* Détruire le canvas pour libérer la mémoire */
  destroy_pixels(pixels);

  return (0) ;
}
```