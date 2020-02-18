---
title: Resumen Eliminación Gaussiana
linktitle: Eliminación Gaussiana
toc: true
type: docs
date: "2019-12-02T00:00:00+01:00"
draft: false
#menu:
#  lineal:
#    name: Avisos
#    weight: 1
---

Consideramos sistemas de ecuaciones lineales de la forma $Ax=b$ donde:
  - $A$ es una matriz $m\times n$ con coficientes reales de $m$ ecuaciones con $n$ incógnitas.
  - $x$ es un vector $n\times 1$ con incógnitas $x_1$, $x_2$, $\dots$, $x_n$
  - $b$ es un vector $m \times 1$ de números reales, los "números a la derecha" de las ecuaciones.
  
Las condiciones generales de solución son las siguientes:
  - El sistema es *consistente* (tiene solución) si $r(A|b)=r(A)$
      - La solución es única si $r(A|b)=r(A)=n$
      - Tiene infinitas soluciones si $r(A|b)=r(A)<n$
  - El sistema es *inconsistente* (no tiene solución) si $r(A|b)>r(A)$
  
### Ecuaciones con dos incógnitas

#### Dos ecuaciones consistentes

Consideremos el sistema lineal $Ax=b$ donde $$(A|b)=\left(\begin{array}{cc|c} 1 & -1 & 2 \\\\ 2 & 2 & 1\end{array}\right)$$ Este sistema es consistente y tiene solución única $x_1=5/4$, $x_2=-3/4$. Compruébenlo!

Y geometricamente esto significa que el punto $(5/4,-3/4)$ es el punto de intersección de las rectas $x-y=2$ y $2x+2y=1$:

{{< figure library="true" src="ec1.png" title="Intersección de las rectas" lightbox="true" height="500px" width="500px">}}

<iframe scrolling="no" title="Sistemas lineales 2x2" src="https://www.geogebra.org/material/iframe/id/fsdzvjeu/width/1510/height/738/border/888888/sfsb/true/smb/false/stb/false/stbh/false/ai/false/asb/false/sri/false/rc/false/ld/false/sdz/false/ctl/false" width="800px" height="588px" style="border:0px;" allowfullscreen> </iframe>
