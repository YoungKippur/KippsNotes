+++
author = "Marcos Strauss"
title = "Sucesiones - Análisis Matemático II"
date = "2025-08-13"
description = "Notas de sucesiones"
math = "true"
tags = [
    "Análisis Matemático II"
]
+++

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css" integrity="sha384-n8MVd4RsNIU0tAv4ct0nTaAbDJwPJzDEaqSD1odI+WdtXRGWt2kTvGFasHpSy3SV" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js" integrity="sha384-XjKyOOlGwcjNTAIQHIpgOno0Hl1YQqzUOEleOLALmuqehneUG+vnGctmUb0ZY0l8" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js" integrity="sha384-+VBxd3r6XgURycqtZ117nYw44OOcIax56Z4dCRWbxyPt0Koah1uHoK0o4+/RRE05" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

#### Definicion (Sucesiones)
Una sucesion de elementos en $\Alpha$ es una funcion $F \negthinspace : \N\to\R\quad (\Alpha\in\R)$.

$\Set{a_n}_{n\in\N}\medspace$ siendo $\medspace a_n = F(n)$

$\colorbox{grey}{
    ($F$ no es una funcion continua)
    }$

#### Definicion (Limite de una sucesion)
* $\lim\limits_{n\to \scriptsize + \infin} = L \quad si \quad
\colorbox{grey}{
    $\forall\varepsilon > 0 \quad \exist\thinspace n_0\in\N \thinspace / \thinspace |a_n - L|<\varepsilon\quad si\quad n \ge n_0$
    }$ 
> En este caso diremos que $\Set{a_n}_{n\in\N}$ `converge` a $L.\thinspace$ En cualquier otro caso, diremos que `diverge`.

* $\lim\limits_{n\to \scriptsize + \infin}a_n = +\infin \quad si \quad
\colorbox{grey}{
    $\forall n>0\quad\exist\thinspace n_0\in\N\thinspace/\thinspace a_n > n\quad si\quad n\ge n_0$
    }$

* $\lim\limits_{n\to \scriptsize + \infin}a_n = -\infin \quad si \quad
\colorbox{grey}{
    $\forall n>0\quad\exist\thinspace n_0\in\N\thinspace/\thinspace a_n < -n\quad si\quad n\ge n_0$
    }$

* $\lim\limits_{n\to \scriptsize + \infin}a_n = \infin \quad si\quad\lim\limits_{n\to \scriptsize + \infin}|a_n| = +\infin$