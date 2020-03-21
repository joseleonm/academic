---
title: Tarea 1
linktitle: tarea 1
toc: true
type: docs
date: "2019-12-02T00:00:00+01:00"
draft: false
menu:
  analisis:
    parent: Tareas

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
# weight: 2
---

Resuelva los siguientes ejercicios

1. Calcule el error absoluto y el error relativo en las aproximaciones de $p$ mediante $p^\ast$.
    * $p=\pi$, $p^\ast=22/7$
    * $p=\pi$, $p^\ast=3.1416$
    * $p=e$, $p^\ast=2.718$
    * $p=\sqrt{2}$, $p^\ast=1.414$
    * $p=8!$, $p^\ast=39900$
2. Suponga que $p^\ast$ debe aproximar a $p$ con un error relativo a lo sumo $10^{-3}$. Determine el máximo intervalo en que debe estar $p^\ast$ para cada valor de $p$.
    * $150$
    * $900$
    * $1500$
    * $90$
3. Sea $f\in C[a,b]$ una función continua cuya derivada existe en $(a,b)$. Suponga que se evaluará a $f$ en $x_0$ en $(a,b)$, pero en vez de calcular el valor real $f(x_0)$, el valor aproximado $\overline{f}(x_0)$, es el valor real de $f$ en $x_0+\epsilon$, es decir, $\overline{f}(x_0)=f(x_0+\epsilon)$.
    * Use el teorema del valor medio para estimar el error absoluto $|f(x_0)-\overline{f}(x_0)|$ y el error relativo $|f(x_0)-\overline{f}(x_0)|/|f(x_0)|$, suponiendo que $f(x_0)\neq 0$
    * Si $\epsilon=5\times 10^{-6}$ y $x_0=1$, calcule las cotas de los errores absoluto y relativo para $f(x)=e^x$ y $g(x)=\operatorname{sen}x$.
4. El número $e$ se define como $e=\displaystyle \sum_{n=0}^\infty \frac{1}{n!}$ donde $n!=n(n-1)(n-2)\cdots 2\cdot 1$ para $n\neq 0$ y $0!=1$. Use la aritmética de truncamiento de cuatro cifras para calcular la siguiente aproximación de $e$ y determine los errores absoluto y relativo.
    * $e \approx \displaystyle \sum_{n=0}^5 \frac{1}{n!}$
    * $e \approx \displaystyle \sum_{k=0}^{10} \frac{1}{(10-j)!}$
5. Determine la rapidez de convergencia de las siguientes sucesiones cuando $n\to \infty$
    * $\displaystyle\lim_{n \to \infty} \operatorname{sen}\frac{1}{n} = 0$
    * $\displaystyle\lim_{n\to \infty} \operatorname{sen}\frac{1}{n^2}=0$
    * $\displaystyle\lim_{n\to \infty}\left(\operatorname{sen}\frac{1}{n}\right)^2 = 0$
    * $\displaystyle\lim_{n\to \infty} \big[\ln(n+1)-\ln(n)\big]=0$
6. Determine las razones de convergencia de las siguientes funciones cuando $h\to 0$.
    * $\displaystyle\lim_{h\to 0} \frac{\operatorname{sen}h}{h}=1$
    * $\displaystyle\lim_{h\to 0} \frac{1-\cos h}{h}=0$
    * $\displaystyle\lim_{h\to 0} \frac{\sin h-h\cosh}{h}=0$
    * $\displaystyle\lim_{h\to 0} \frac{1-e^h}{h}=1$
7. 
    * ¿Cuántas multiplicaciones y sumas se necesitan para determinar una suma de la siguiente forma? $$\sum_{i=1}^n\sum_{j=1}^i a_ib_j$$
    * Modifique la suma en una forma equivalente que reduzca el número de cálculos.
8. Suponga que se tiene el polinomio $P(x)=a_nx^n + a_{n-1}x^{n-1}+\cdots + a_1x+a_0$. Construya un algoritmo para evaluar $P(x_0)$ por medio de una multiplicación anidada.
    
    
