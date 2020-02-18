---
title: Interpretación geométrica de la eliminación por método de Gauss
linktitle: Eliminación Gaussiana
toc: true
type: docs
date: "2020-02-18T00:05:00+01:00"
draft: true
menu:
  lineal:
    parent: Notas
    weight: 2

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

Recordemos que el proceso de Gauss aplicado a un sistema lineal de $m$ ecuaciones con $n$ incógnitas de la forma $(A|b)$ nos produce un sistema lineal equivalente $(U|c)$ donde $U$ es una matriz escalonada y $r$ el número de renglones no cero de la matriz $U$ es el rango de $A$.

En caso de tener $2$ o $3$ incógnitas podemos interpretar las ecuaciones y la solución como un objeto geométrico en $\mathbb{R}^2$ o $\mathbb{R}^3$. 

En caso de tener $2$ incógnitas y un sistema consistente con $r\leq m$, tenemos que 

  * El sistema tiene una única solución si $r=2$, es decir tenemos dos rectas que se intersecan en un solo punto (no son paralelas)
  * El sistema tiene una infinidad de soluciones si $r=1$, en este caso tenemos dos rectas idénticas y por tanto el conjunto solución es igual a estas rectas. 
    
Por ejemplo consideremos el sistema lineal $Ax=b$ donde $$(A|b)=\left(\begin{array}{cc|c} 1 & -1 & 2 \\\\ 2 & 2 & 1\end{array}\right)$$ Este sistema es consistente y tiene solución única $x_1=5/4$, $x_2=-3/4$. 
Y geometricamente esto significa que el punto $(5/4,-3/4)$ es el punto de intersección de las rectas $x-y=2$ y $2x+2y=1$:

<iframe scrolling="no" title="Sistemas lineales 2x2" src="https://www.geogebra.org/material/iframe/id/fsdzvjeu/width/1510/height/738/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="750px" height="550px" style="border:0px;" allowfullscreen> </iframe>
  
En caso de tener $3$ incógnitas y un sistema consistente tenemos más opciones:

  * El sistema tiene una única solución si $r=3$, entonces tenemos tres planos que se intersecan en un solo punto.
  * El sistema tiene infinitas soluciones si $r=2$, en este caso tenemos dos planos que se intersecan sobre una recta, por eso tenemos como solución una ecuación paramétrica de la forma $\mathbf{X}=\mathbf{U}+t\\,\mathbf{V}$.
  * El sistema tiene infinitas soluciones si $r=1$, en este caso tenemos un solo plano y por tanto la solución es ese plano, al final tenemos una ecuación paramétrica de la forma $\mathbf{X}=\mathbf{U}+t\\,\mathbf{V}+s\\,\mathbf{W}$.
    
Por ejemplo el sistema de 3 ecuaciones lineales 
$$\left(\begin{array}{ccc|c} 1 & 0 & -1 & 1\\\\ -2 & 3 & -1 & 0\\\\ -6 & 6 & 0 & -2\end{array}\right)$$
tiene como solución a la recta
$$
\begin{pmatrix}x \\\\ y \\\\ z \end{pmatrix} = \begin{pmatrix} 1 \\\\ 2/3 \\\\ 0 \end{pmatrix} + t\\,\begin{pmatrix} 1 \\\\ 1 \\\\ 1 \end{pmatrix}
$$
que geometricamente se puede observar aqui:

<iframe scrolling="no" title="EcuacionesR3" src="https://www.geogebra.org/material/iframe/id/g8tv5e8s/width/1240/height/780/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="750px" height="550px" style="border:0px;" allowfullscreen> </iframe>

    
