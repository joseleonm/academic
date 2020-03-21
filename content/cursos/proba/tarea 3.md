---
title: Tarea 3
linktitle: tarea 3
toc: false
type: docs
date: "2019-12-02T00:00:00+01:00"
draft: false
menu:
  proba:
    parent: Tareas
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

Resuelva los siguientes ejercicios

1. Sean $E$, $F$ y $G$ tres eventos. Exprese en término de operaciones de conjuntos los siguientes eventos:
    * Solo $E$ ocurre,
    * $E$ y $G$ ocurren, pero $F$ no ocurre,
    * Al menos uno de los eventos ocurre,
    * Al menos dos de los eventos ocurre,
    * Los tres eventos ocurren,
    * Ninguno de los eventos ocurre,
    * A lo más uno de los eventos ocurre,
    * A lo más dos de los eventos ocurre,
    * Exactamente dos de los eventos ocurren,
    * A lo más tres de los eventos ocurren.
1. Supóngase que $A$ y $B$ son eventos ajenos para los cuales $P(A)=0.3$ y $P(B)=0.5$. ¿Cuál es la probabilidad de que
    * $A$ o $B$ ocurra? **$R:0.8$**
    * $A$ ocurre pero $B$ no? **$R:0.3$**
    * $A$ y $B$ ocurren? **$R:0$**
2. En una cierta población de 100,000 personas se publican diaramente 3 periódicos: I, II y III. Las proporciones de personas que leen estos periódicos es como sigue
    I: 10%,  II: 30%, III: 5%, I y II: 8%, I y III: 2%, II y III: 4%, I, II y III: 1%.
Esto nos dice, por ejemplo, que 8000 personas leen los periódicos I y II.
    * Encuentre el número de personas que lee sólo un periódico **$R:20, 000$**
    * ¿Cuántas personas leen por lo menos dos periódicos? **$R:12, 000$**
    * Si I y III son periódicos matutinos y II es un periódico vespertino, ¿Cuántas personas leen un periódico matutino más un periódico vespertino? **$R:11, 000$**
    * ¿Cuántas personas no leen ningún periódico? **$R:68, 000$**
    * ¿Cuántas personas leen solo un periódico matutino y un periódico vespertino? **$R:10, 000$**
3. Un hombre tiene $n$ llaves, de las cuales solo una abre una cerradura. Si el hombre intenta abrir con cada llave, una a la vez, seleccionada de forma aleatoria de las llaves que no se probaron antes. Encuentre la probabilidad de que la $r$-ésima llave sea la llave correcta. **$R:1/n$**
4. Recuerden que un baraja de póquer está dividida en 4 palos, espadas, corazones, rombos y diamantes. Cada palo tiene 13 cartas numeradas como: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A. Una mano de póquer consta de 5 cartas seleccionadas aleatoriamente sin reemplazo.
Calcule las probabilidades de que ocurra cada una de las siguientes manos:
    * **Escalera real**; 10, J, Q, K, A del mismo palo; **$R:1/\binom{52}{5}$**
    * **Escalera de color**; 5 cartas consecutivas del mismo palo; **$R:36/\binom{52}{5}$**
    * **Póker**; cartas con valores de la forma $(x,x,x,x,y)$ donde $x$ y $y$ son diferentes; **$R:624/\binom{52}{5}$**
    * **Full**; cartas con valores de la forma $(x,x,x,y,y)$ donde $x$ y $y$ son diferentes; **$R:3744/\binom{52}{5}$**
    * **Color**; Cinco cartas del mismo palo; **$R:5108/\binom{52}{5}$**
    * **Escalera**; Cinco cartas consecutivas sin importar el palo; **$R:10200/\binom{52}{5}$**
    * **Trío**; cartas con valores de la forma $(x,x,x,y,z)$, donde $x$, $y$ y $z$ son diferentes; **$R:54912/\binom{52}{5}$**
    * **Dos pares**; cartas con valores de la forma $(x,x,y,y,z)$, donde $x$, $y$ y $z$ son diferentes; **$R:123552/\binom{52}{5}$**
    * **Par**; cartas con valores de la forma $(x,x,y,z,w)$ donde $x,y,z$ y $w$ son diferentes. **$R:1098240/\binom{52}{5}$**
5. Una caja tiene 40 fusibles buenos y 10 defectuosos. Si se seleccionan 10 fusibles. ¿Cuál es la probabilidad de que los 10 seleccionados sean buenos? **$R:38530024/466921735$**
6. Un par de dados son lanzados. ¿Cuál es la probabilidad de que el segundo dado caiga en un valor mayor que el primero? **$R:5/12$**
7. Una caja tiene 10 bolas numeradas, 1, 2, $...$, 10. Suponga que una muestra aleatoria de tamaño 3 es seleccionada. Encuentre la probabilidad de que las bolas 1 y 6 se encuentren entre las 3 seleccionadas. **$R:1/15$**
8. Se barajean las cartas de una baraja de póquer y se revisan una a una hasta que el primer rey salga. Encuentre la probabilidad de que esto ocurra con la $n$-ésima carta.
**$R:\dfrac{4(52-n)(51-n)\cdots (50-n)}{52\cdot 51 \cdot 50 \cdot 49}$** 
9. Un par de dados son lanzados hasta que su suma de 5 o 7. Encuentre la probabilidad de que 5 ocurra primero. *Consejo:* Sea $A_n$ el evento en el que 5 ocurre en el $n$-ésimo lanzamiento y no ocurre un 5 o 7 en los $n-1$ anteriores. Calcule $P(A_n)$ y argumente que $\sum_{n=1}^\infty P(A_n)$ es la probabilidad deseada. $R:2/5$

