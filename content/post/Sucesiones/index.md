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
* $\lim\limits_{n\medspace\to \scriptsize + \infin} = L \quad si \quad
\colorbox{grey}{
    $\forall\varepsilon > 0 \quad \exist\thinspace n_0\in\N \thinspace / \thinspace |a_n - L|<\varepsilon\quad si\quad n \ge n_0$
    }$ 
> En este caso diremos que $\Set{a_n}_{n\in\N}$ `converge` a $L.\thinspace$ En cualquier otro caso, diremos que `diverge`.

* $\lim\limits_{n\medspace\to \scriptsize + \infin}a_n = +\infin \quad si \quad
\colorbox{grey}{
    $\forall\thinspace n>0\quad\exist\thinspace n_0\in\N\thinspace/\thinspace a_n > n\quad si\quad n\ge n_0$
    }$

* $\lim\limits_{n\medspace\to \scriptsize + \infin}a_n = -\infin \quad si \quad
\colorbox{grey}{
    $\forall\thinspace n>0\quad\exist\thinspace n_0\in\N\thinspace/\thinspace a_n < -n\quad si\quad n\ge n_0$
    }$

* $\lim\limits_{n\medspace\to \scriptsize + \infin}a_n = \infin \quad si\quad\lim\limits_{n\medspace\to \scriptsize + \infin}|a_n| = +\infin$

#### Definicion (Monotonia)
* Sea $\Set{a_n}_{n\in\N}\medspace$ una sucesion, diremos que es `creciente` si $\medspace a_n\le a\_{n+1}$.
* Si $\medspace a_n\ge a\_{n+1}$, diremos que es `decreciente`.
* En cualquiera de los dos casos diremos que es `monotona`.

#### Definicion (Sucesion acotada)
* Sea $\Set{a_n}_{n\in\N}\medspace$ una sucesion, diremos que esta `acotada inferiormente` si $\thinspace\colorbox{grey}{
    $\exist\thinspace k\in\R\thinspace/\thinspace k<a_n\quad,\thinspace \forall\thinspace n\in\N$
    }$

* Diremos que esta `acotada superiormente` si $\thinspace\colorbox{grey}{
    $\exist\thinspace k\in\R\thinspace/\thinspace a_n<k\quad,\thinspace \forall\thinspace n\in\N$
    }$

* Diremos que esta `acotada` si $\thinspace\colorbox{grey}{
    $\exist\thinspace k\in\R\thinspace/\thinspace |a_n|<k\quad,\thinspace \forall\thinspace n\in\N$
    }$

#### Teorema
Sea $\Set{a_n}_{n\in\N}\medspace$ una sucesion `convergente` $\Longrightarrow$ es `acotada`.

#### Teorema
Si $\Set{a_n}_{n\in\N}\medspace$ es `monotona` y `acotada` $\Longrightarrow$ la sucesion $\thinspace\textcolor{lightgreen}{converge}$.

#### Observaciones
1. $\thinspace$ Sea $\thinspace F\negthinspace :I\sub\R\to\R\thinspace/\lim\limits_{x\medspace\to \scriptsize + \infin}F(x)=L\quad\land\quad a_n=F(n)\quad n\in\N\quad\Longrightarrow\quad\thinspace\colorbox{grey}{
    $\lim\limits_{n\medspace\to \scriptsize + \infin}a_n=L$
}$  
> A esto se lo llama $\thinspace\textcolor{lightblue}{paso\medspace a\medspace variable\medspace real}$.

2. $\thinspace$ Sea $\Set{a_n}_{n\in\N}\medspace$ `acotada` $\thinspace\land$ $\Set{b_n}\_{n\in\N}\medspace/\thinspace b_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}0\quad\Longrightarrow\quad\thinspace\colorbox{grey}{
    $a_n\thinspace .\thinspace b_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}0$
}$
> A esto se lo llama $\thinspace\textcolor{lightblue}{cero\medspace por\medspace acotada}$.

3. $\quad a_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}a\quad\Longrightarrow\quad |a_n|\xrightarrow[n\medspace\to\scriptsize +\infin]{}|a|$

4. $\quad a_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}0\quad\xLeftrightarrow \quad\quad |a_n|\xrightarrow[n\medspace\to\scriptsize +\infin]{}0$ 

5. $\thinspace$ Sean $\Set{a_n}_{n\in\N}\medspace\land\medspace\Set{b_n}\_{n\in\N}\thinspace/\thinspace a_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}a\medspace\land\medspace b_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}b\medspace\medspace\land\medspace\alpha,\thinspace\beta\in\R$
    * $\alpha\thinspace .\thinspace a_n + \beta\thinspace .\thinspace b_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}\alpha\thinspace .\thinspace a+\beta\thinspace .\thinspace b$
    * $a_n\thinspace .\thinspace b_n\xrightarrow[n\medspace\to\scriptsize +\infin]{}a\thinspace .\thinspace b$
    * Si $b\ne 0\thinspace,\quad\frac{a_n}{b_n}\xrightarrow[n\medspace\to\scriptsize +\infin]{}\frac{a}{b}$

### Criterios de convergencia

#### Teorema
