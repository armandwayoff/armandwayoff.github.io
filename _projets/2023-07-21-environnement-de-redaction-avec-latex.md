---
title: "Environnement de rédaction avec $\LaTeX$"
date: 2023-07-21
permalink: /projets/environnement-de-redaction-avec-latex
---

| Fichier      | Description | Lien     |
|  ---        |    ----     |          ---  |
| notations.tex      | Pour des notations mathématiques correctes et uniformes  | [Overleaf](https://www.overleaf.com/read/krwsfvqqybth)   |
| packages.tex   | Ensemble des packages        | [Overleaf](https://www.overleaf.com/read/txtwcfppyxxj)      |
| env.tex   | Environnements mathématiques (Théorème, Proposition, Démonstration, ...)        | [Overleaf](https://www.overleaf.com/read/ywbvsdfrftjs)      |
| style.tex   |         | [Overleaf](https://www.overleaf.com/read/jpjmrhmdgvvt)     |


```latex
\documentclass{article}

\input{packages}
\input{notations}
\input{env}
\input{style}

\begin{document}
    % ...
\end{document}
```

## Ressources

- [Règles françaises de typographie mathématique - Alexandre ANDRÉ](http://sgalex.free.fr/typo-maths_fr.pdf)
- [LaTeX... pour le prof de maths ! - Arnaud GAZAGNES](https://math.univ-lyon1.fr/irem/IMG/pdf/LatexPourLeProfDeMaths.pdf)
- [Package pas-math - Stéphane PASQUET](https://www.mathweb.fr/euclide/wp-content/uploads/2018/08/pas-math.pdf)