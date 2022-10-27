---
title: "La spirale d'ULAM"
date: 2012-08-14
permalink: /posts/spirale-ulam
tags:
  - Informatique
  - Mathématiques
---

My codes are based on the [A063826 sequence](https://oeis.org/A063826):

let $n \in \mathbb{N}^\star$, we define the sequence $(a_n)$ as follows
$$a_n := \left \lfloor \sqrt{4n+1} \right \rfloor\ \mathrm{mod}[4].$$
For all $n \in \mathbb{N}^\star, a_n \in \\{ 1, 2, 3, 4 \\}$. 	Let $1, 2, 3, 4$ represent moves to the right, down, left and up; this sequence describes the movements in the clockwise square spiral.