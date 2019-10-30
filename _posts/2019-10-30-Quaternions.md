---
layout: post
title: Quaternions
---

# Quaternions

Hoje vou abordar a Álgebra Geométrica sobre o  $$\mathbb{R}^{3}$$. Mas antes, algumas considerações. Vou mudar um pouco a notação usada, além de possívelmente começar a escrever "Álgebras de Clifford" mais do que "Álgebra Geométrica", ficando mais próximo dos livros que tenho lido. Quando me referir a uma álgebra de clifford no $$R^3$$ , por exemplo, vou usar $$\mathbb{Cl_{3}}$$, além de definir $$e_{i}e_{j}=e_{ij}$$ quando estivermos falando sobre os vetores da base ortonormal. Dito isso, vamos começar.

## A Álgebra $$\mathbb{Cl_3}$$

Considere a boa e velha base ortonormal do $$R^3$$, $$b=\{e_1,e_2,e_3\}$$. Podemos gerar alguns elementos com essa base e o produto geométrico:

| elemento                             | grau           |
| :----------------------------------- | :------------- |
| 1                                    | **escalar**    |
| **$$e_1,$$$$e_2,$$$$e_3$$**          | **vetores**    |
| **$$e_{12},$$$$e_{23},$$$$e_{13}$$** | **bivetores**  |
| **$$e_{123}$$**                      | **trivetores** |

Estes 8 elementos geram a **Álgebra de Clifford do $$\mathbb{R^3}$$**. Essa álgebra é a soma direta de duas partes: a parte par(formada por elemento de grau par) e a parte ímpar(formada por elementos de grau ímpar). 

$$\mathbb{Cl_{3}} = \mathbb{R} \bigoplus \mathbb{R^3} \bigoplus \bigwedge^2\mathbb{R^3}\bigoplus \bigwedge^3 \mathbb{R^3}$$

$$\mathbb{Cl_3^+}=\mathbb{R} \bigoplus \bigwedge^2\mathbb{R^3}, \text{a parte par}$$

$$\mathbb{Cl_3^-}=\mathbb{R^3}\bigoplus \bigwedge^3 \mathbb{R^3},\text{a parte ímpar}$$

*O conjunto $$\bigwedge^{i}\mathbb{R^3}$$ é o conjunto dos **multivetores de grau $$i$$**. 

Assim como no $$\mathbb{R^2}$$, a parte par, $$\mathbb{Cl_3}$$, forma uma subalgebra que merece nossa atenção.

## A subalgebra $$\mathbb{Cl_3^+}$$
Os elementos dessa subalgebra geram o subespaço $$\{a+be_{12}+ce_{23}+de_{13} | a,b,c,d \in \mathbb{R}\}$$, de forma que:

$$
\begin{align*}
{e_{12}}^2&={e_{23}}^2={e_{13}}^{2}=-1 \\
 e_{12}e_{23}&=e_{13}\\
 e_{23}e_{13}&=e_{12}\\
 e_{13}e_{12}&=e_{23}
\end{align*}
$$

Guarde isso no seu coração.

Antes de chegar nos Quaternions(que já estão batendo na porta), vamos analisar rapidamente outra subalgebra do $$\mathbb{Cl_{3}}$$.

### O centro do $$\mathbb{Cl_3}$$
O centro de um espaço é o subconjunto dos elementos que comutam com quaisquer outros elementos. No nosso caso, temos os subconjuntos $$\mathbb{R}$$ e $$\bigwedge^3\mathbb{R^3}$$. Ou seja, temos o subespaço {$$x+ye_{123}|x,y\in\mathbb{R}$$}, onde $${e_{123}}^2=-1$$, isto é **o centro do $\mathbb{Cl_3}$ é isomorfo ao $$\mathbb{C}$$ !**

## Enfim, os Quaternions
Os Quaternions são definidos pelo conjunto $$\mathbb{H}=\{a+bi+cj+dk|a,b,c,d\in \mathbb{R}\}$$ onde vale que $$ij=k=-ji$$, $$jk = i=-kj$$ e $$ki=j=-ik$$  e $$i^2=j^2=k^2=ijk=-1$$. Leitores razoavelmente atentos perceberão que existe uma correspondência entre $$\mathbb{H}$$ e $$\mathbb{Cl_3}$$.

| $$\mathbb{H}$$ | $$\mathbb{Cl_3}$$ |
| -------------- | ----------------- |
| 1              | 1                 |
| $$i$$          | $$e_{12}$$        |
| $$j$$          | $$e_{23}$$        |
| $$k$$          | $$e_{13}$$        |

Pois bem, temos aqui que $$\mathbb{Cl}_3$$ é isomorfo ao $$\mathbb{H}$$!

