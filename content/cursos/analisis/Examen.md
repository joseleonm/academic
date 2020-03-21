---
title: Examen 1er Parcial
linktitle: Examen
toc: false
type: docs
date: "2020-02-14T00:00:00+01:00"
draft: true
menu:
  analisis:
    name: Examen
weight: 1
    
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
# weight: 2
---

Instrucciones: Contestar las siguientes preguntas y enviarlas a mi correo en foto o escaneadas. Verificar que en la pregunta 4 el número de iteraciones sea el correcto asumiendo que p0 es la iteración 0 (el método de la secante inicia en iteración 2 por ejemplo).

1. 
    * ¿Cuántas multiplicaciones y sumas se necesitan para determinar una suma de la siguiente forma?
$$
\sum_{i=1}^n \sum_{j=1}^i a_i b_j
$$
    * Modifique la suma en una forma equivalente que reduzca el número de cálculos.
2. Usando que $\sin x \leq x$ para valores pequeños de $x$, $0\leq x <1$, calcule la rapidez de convergencia de las siguientes sucesiones cuando $n\to \infty$
  * $\displaystyle\lim_{n\to \infty} \sin \dfrac{1}{n}=0$
  * $\displaystyle\lim_{n\to \infty} \sin \dfrac{1}{n^2}=0$
3. Considere la función $g(x)=\dfrac{\pi}{2}+0.5\sin\left(\dfrac{x}{3}\right)$. Demuestre que esta función tiene un único punto fijo en $[0,2\pi]$ y calcule teóricamente el número de iteraciones necesarias para obtener el valor de punto fijo con un error menor a $10^{-5}$, considere $p_0=\pi$.
4. Encuentre el número de iteraciones necesarias para obtener una aproximación precisa a 5 digitos decimales del punto fijo de $g$ (el punto fijo es $1.86151\dots$) usando el método de bisección, de punto fijo, de Newton-Raphson y de la secante. Use $\pi=3.14159$, $p_0=\pi$ para el método de Newton y $p_0=0$, $p_1=2\pi$ para el método de la secante.
*Consejo:* Para el método de bisección, Newton-Raphson y de la secante considerar el problema de encontrar la raíz para la función $f(x)=g(x)-x$.
