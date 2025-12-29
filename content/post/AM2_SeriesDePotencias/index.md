+++
author = "Marcos Strauss"
title = "Análisis Matemático II - Series de potencias"
date = "2025-08-19"
description = "Notas de series de potencias"
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

### Series funcionales: Series de potencias

#### Definicion
Una `serie funcional de potencias` es la que puede escribirse de la forma:

$\displaystyle\sum_{n=0}^{+\infin}a_n(x-x_0)^n$

Siendo $\Set{a_n}_{n\in\N}\medspace$ una `sucesion de numeros reales` y $\thinspace x_0\in\R\thinspace$.
> Observamos que en $x=x_0\medspace$ $\textcolor{lightgreen}{converge\medspace siempre}$..

#### Teorema
Sea $\medspace\displaystyle\sum_{n=0}^{+\infin}a_n(x-x_0)^n\quad\land\quad R=sup\thinspace\set{r\in\R\ge 0: la\medspace serie\medspace converge\medspace\forall x\in\R\medspace /|x-x_0|<r}$

> $R\thinspace$ puede ser infinito y se llama `radio de convergencia`.
1. $\medspace$ Si $\thinspace$ $x\in\R\medspace /\medspace|x-x_0|<R\Longrightarrow\medspace$ la serie `converge absolutamente`.
2. $\medspace$ Si $\thinspace$ $x\in\R\medspace /\medspace|x-x_0|>R\Longrightarrow\medspace$ la serie `diverge`.
3. $\medspace$ Si $\thinspace$ $x\in\R\medspace /\medspace|x-x_0|=R\Longrightarrow\medspace$ no sabemos que pasa con la serie.

> * Si solo `converge absolutamente` en $\medspace x=x_0\iff R=0$
> * Si  `converge absolutamente` $\medspace\forall x\in\R\iff R=+\infin$


> * Si la serie `converge absolutamente` $\Longrightarrow$ la serie `converge`
> * Si la serie `diverge` $\Longrightarrow$ la serie `no converge absolutamente`

### Teorema (Calculo del radio)
Sea $\displaystyle\sum_{n=0}^{+\infin}a_n(x-x_0)^n$, el `radio` se puede calcular como:

1. $R = \begin{cases}
   0 &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\frac{|a_{n+1}|}{|a_n|} = \infin \\\
   \infin &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\frac{|a_{n+1}|}{|a_n|} = 0 \\\
   \frac{1}{L} &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\frac{|a_{n+1}|}{|a_n|} = L
\end{cases}$

2. $R = \begin{cases}
   0 &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\sqrt[n]{|a_n|} = \infin \\\
   \infin &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\sqrt[n]{|a_n|} = 0 \\\
   \frac{1}{L} &\text{si } \lim\limits_{n\medspace\to \scriptsize + \infin}\sqrt[n]{|a_n|} = L
\end{cases}$