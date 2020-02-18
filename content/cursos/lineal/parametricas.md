---
title: Ecuaciones Paramétricas de la recta y el plano
linktitle: Ecuaciones paramétricas
toc: true
type: docs
date: "2019-12-02T00:00:00+01:00"
draft: false
#menu:
#  lineal:
#    name: Avisos
#    weight: 1
---

Un sistema de ecuaciones paramétricas permite representar una curva o superficie en el plano o en el espacio, mediante valores que recorren un intervalo de números reales, mediante una variable, llamada parámetro, considerando cada coordenada de un punto como una función dependiente del parámetro.

En particular estamos interesados en la ecuación paramétrica de la recta y el plano porque estas ecuaciones paramétricas ocurren a menudo en la solución de sistemas lineales.

{{% alert note %}}
La ecuación paramétrica de una recta es $$\mathbf{X}=\mathbf{U}+t\\,\mathbf{V}$$ donde $\mathbf{U}$ es un punto en la recta, $\mathbf{V}$ es el vector de dirección de la recta y $t$ es un parámetro $t\in(-\infty,\infty)$. 
{{% /alert %}}

Por ejemplo, consideremos en $\mathbb{R}^3$ (el espacio euclidiano de tres dimensiones) la recta 
$$\begin{pmatrix}x \\\\ y \\\\ z \end{pmatrix} = \begin{pmatrix} 2 \\\\ 0 \\\\ -3 \end{pmatrix} + t\\,\begin{pmatrix} 1 \\\\ -1 \\\\ 2 \end{pmatrix}$$

Esta ecuación se puede visualizar de la siguiente forma:

<iframe scrolling="no" title="RectaR3" src="https://www.geogebra.org/material/iframe/id/mvrsgtde/width/1240/height/780/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1240px" height="780px" style="border:0px;" allowfullscreen> </iframe>

Pueden cambiar los valores del punto en la recta y del vector de dirección para observar que recta genera por cada cambio de vectores así como el desplazamiento sobre la recta de los puntos de acuerdo al parámetro $t$.

Similarmente podemos definir la ecuación paramétrica de un plano de la siguiente forma:

{{% alert note %}}
La ecuación paramétrica de un plano es $$\mathbf{X}=\mathbf{U}+t\\,\mathbf{V}+s\\,\mathbf{W}$$ donde $\mathbf{U}$ es un punto en el plano, $\mathbf{V}$ y $\mathbf{W}$ son vectores de dirección (si uno no es múltiplo del otro entonces generan un plano que pasa por $\mathbf{U}$) y $t$ y $s$ son parámetros $t,s\in(-\infty,\infty)$. 
{{% /alert %}}

Entonces el plano 
$$\begin{pmatrix}x \\\\ y \\\\ z \end{pmatrix} = \begin{pmatrix} 2 \\\\ 0 \\\\ -3 \end{pmatrix} + t\\,\begin{pmatrix} 1 \\\\ -1 \\\\ 2 \end{pmatrix}+s\\,\begin{pmatrix} 0 \\\\ 2 \\\\ 1 \end{pmatrix}$$
tiene la siguiente representación geométrica:

<iframe scrolling="no" title="PlanoR3" src="https://www.geogebra.org/material/iframe/id/dyvngebh/width/1240/height/780/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="1240px" height="780px" style="border:0px;" allowfullscreen> </iframe>

Similarmente, puede editar los valores de los vectores de dirección y observar que plano se genera a partir de ellos y del punto inicial en el plano. 
