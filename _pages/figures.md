---
layout: page
title: Galerie de figures
permalink: /figures/
soustitre: "Quelques figures mathématiques réalisées avec Ti<span style='font-style:italic;'>k</span>Z et <span style='font-style:italic;'>Inkscape</span>"
description: "Vous trouverez un grand nombre de mes figures dans le <a href='https://ensta-paris.hal.science/hal-03243924v3/document'>polycopié du cours <span class='capitales'>aot</span><span class='chiffres-capitaux'>13</span> de l'<span class='capitales'>ensta</span> <span class='capitales'>p</span>aris - <i>Géométrie Différentielle
et Application au Contrôle Géométrique</i> de Frédéric <span class='capitales'>Jean</span></a>."
nav: true
nav_order: 2
horizontal: false
---

<script>
    // This function will run once the DOM is fully loaded
    document.addEventListener("DOMContentLoaded", function() {
        // Get all h2 elements in the document
        const h2Elements = document.querySelectorAll("h2");

        // Loop through each h2 element and remove it
        h2Elements.forEach(function(h2) {
            h2.remove();
        });
    });
</script>

<div class="publications projects">
    <div class="grid">
        {% bibliography -f figures.bib --template bibfigures %}
    </div>
</div>