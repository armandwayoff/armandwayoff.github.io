---
layout: post
title: "Dessiner des figures mathématiques avec <i>Inkscape</i>"
date: 2024-02-21
description: Prise en main du logiciel <i>Inkscape</i>, insertion de symboles mathématiques et autres fonctionnalités avancées
tags: Inkscape \(\LaTeX\) 
# categories: sample-posts
featured: false
thumbnail: /assets/img/figures/mouvements_possibles_systeme_commande.png
# toc:
#   sidebar: left
---

Apprenons par l'exemple en dessinant étape par étape la figure suivante
{% include figure.html path="/assets/img/figures/mouvements_possibles_systeme_commande.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="Système commandé sur une variété différentiable"%}

Cette figure illustre un système commandé sur une variété différentiable et vous pouvez la retrouver dans le <a href='https://ensta-paris.hal.science/hal-03243924v3/document'>polycopié du cours <span class='capitales'>aot</span><span class='chiffres-capitaux'>13</span> de l'<span class='capitales'>ensta</span> <span class='capitales'>p</span>aris - <i>Géométrie Différentielle et Application au Contrôle Géométrique</i> de Frédéric <span class='capitales'>Jean</span></a>.

Apprendre à dessiner cette figure va nous permettre de nous familiariser avec les **outils incontournables** du logiciel *[Inkscape](https://inkscape.org/fr/)* ainsi qu'avec certaines de ses **fonctionnalités avancées** comme:
* la différence entre objet, contour et chemin,
* la déformation par grille,
* l'insertion de symboles mathématiques,
* la déformation des flèches,
* les contours autour de symboles.

La puissance d'*Inkscape* va nous permettre de créer des perspectives et de dessiner des surfaces courbes, ce qui serait nettement plus difficile à faire avec Ti*k*Z par exemple. 

# Outils

Pour dessiner nos figures, nous allons utiliser *[Inkscape](https://inkscape.org/fr/)*, un logiciel de dessin vectoriel libre, avec l'extensition *[TexText](https://textext.github.io/textext/)* qui permet d'ajouter et de rééditer des éléments <span class="capitales">svg</span> générés par <span style='position:relative;'>L</span><span style='position:relative; font-size:0.7em; top:-0.25em; right:0.33em;'>A</span><span style='position:relative; right:0.335em'>T</span><span style='position:relative; top:0.15em; right:0.51em;'>E</span><span style='position:relative; top:0em; right:0.685em;'>X</span> <span style='position:relative; top:0em; right:0.685em;'>et *Typst*.</span>

# Démarche

Avant de dessiner une figure sur ordinateur, il faut tout d'abord la **dessiner à la main**, avec une feuille et un crayon. Ce dessin *à la main* nous servira de référence pour la suite, l'idée étant de ne se mettre à son ordinateur que lorsque l'on a une vision très claire de ce que l'on souhaite dessiner. Il demande également une attention particulière, car il nécessite d'être **précis** et **rigoureux** afin d'être le plus lisible et compréhensible possible et exempt de toutes ambiguïtés.
Nous verrons par la suite que la couleur sera d'une grande utilité pour améliorer la lisibilité de la figure. 

# Démonstration étape par étape

La figure est composée de trois éléments principaux : *la variété*, *le plan tangent* et *les flèches*.


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="/assets/img/tuto_inkscape/1.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="La variété"%}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="/assets/img/tuto_inkscape/2.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="Le plan tangent"%}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="/assets/img/tuto_inkscape/3.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="Les flèches"%}
    </div>
</div>

## Perspective et déformation par grille

<div class="row mt-2">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.html path="/assets/img/tuto_inkscape/4.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="Perspective"%}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.html path="/assets/img/tuto_inkscape/5.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption="Déformation par grille"%}
    </div>
</div>

## Insérer des symboles mathématiques

{% include figure.html path="/assets/img/tuto_inkscape/6.png" width="300px" class="img-fluid rounded z-depth-1" zoomable=true caption=""%}

# Ressource
<a href="https://castel.dev/post/lecture-notes-2/" target="_blank">How I draw figures for my mathematical lecture notes using Inkscape</a> - Gilles <span class="capitales">Castel</span>

