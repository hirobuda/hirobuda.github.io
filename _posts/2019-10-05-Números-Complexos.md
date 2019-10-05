---
layout: post
title: Números Complexos 
---

## Números Complexos I
 
## Álgebra Geométrica no plano
Hoje vou mostar como é possível encontrar os números complexos por meio do produto geométrico.

O produto geométrico entre dois vetores $$a$$ e $$b$$ é definido como $$ab ={a}\wedge{b} + {a}\cdot{b}$$, onde "$$\wedge$$" e "$$\cdot$$" são os produtos exterior e interno(farei um post detalhando essa álgebra algum dia).
Esse produto pega dois vetores e nos retorna um **multivetor**, que é a soma de **n-vetores**. Para entender o conceito de n-vetor é preciso antes compreender o significado geométrico do produto exterior: uma área orientada ou **bivetor**.

Assim como vetores são caracterizados por direção, sentido e magnitude, bivetores possuem direção(definida por dois vetores), orientação e área. A orientação define um sentido horário ou anti-horário para a região, que é denotado pelo sinal do produto, isto é, se $$a \wedge b$$ tem sentido anti-horário, então $$b \wedge a$$ tem sentido horário. Já a área nada mais é do que a área do paralelogramo definido pelos dois vetores.
Se extendermos esses conceitos, podemos então dizer que escalares são 0-vetores, vetores usuais são 1-vetores, bivetores são 2-vetores e assim por diante. Multivetores são, então, soma de "vetores de várias dimensões". Isso parece um pouco esquisito, mas reflita, por exemplo, sobre algo como $$a+bi$$.

Vamos começar definindo uma base ortonormal $$b=\{e_1,e_2\}$$ para o $$\mathbb{R}^2$$ e aplicando o produto geométrico nos vetores dessa base:

$$e_1e_2 ={e_1} \wedge {e_2} + {e_1}\cdot{e_2}$$

Como a base é ortonormal:

$$e_1 \wedge e_2= -e_2 \wedge e_1=1$$

$$e_1 \cdot e_2=e_2 \cdot e_1=0$$

Ou seja:

$$e_1e_2 ={e_1}\wedge{e_2}=1$$

Aqui é interessante ressaltar algumas coisas:
1. O produto geométrico **comuta** quando os vetores são paralelos e **anticomuta** quando os vetores são ortogonais.
2. O produto geométrico entre um vetor e ele mesmo é sempre um escalar.
3. Não seria possível fazer nada disso com o produto vetorial usual do $$\mathbb{R}^3$$.

## Números Complexos

Bem, mas e os números complexos?

Calma, já vamos chegar lá. Vamos continuar trabalhando com a nossa base:

Temos que  $$e_1e_2 ={e_1}\wedge{e_2}=1$$

Como, nesse caso, o produto geométrico resulta em escalares, é justo dizer:

$$(e_1e_2)^2=e_1e_2e_1e_2$$

aplicando a anticomutatividade:

$$(e_1e_2)^2=-e_1e_1e_2e_2$$

$$(e_1e_2)^2=-1$$

Temos aqui nosso equivalente da unidade imaginária $$i$$. Resta mostrar que existe uma subalgebra equivalente aos complexos nessa construção, mas antes, gostaria de pontuar o significado geométrico de $$e_1e_2$$: uma rotação de 90°.

Seja um vetor $$v=(x,y)$$ qualquer na base $$b$$. Podemos escrever $$v$$ como $$v=xe_1+ye_2$$. Multiplique esse vetor por $$e_1e_2$$:

$$v'=(xe_1+ye_2)e_1e_2$$

$$v'=xe_1e_1e_2+ye_2e_1e_2$$ *é possível demonstrar a distributividade pela definição, inclusive, você deveria tentar!

$$v'=xe_2-ye_1$$

Temos então que $$v'$$ é uma rotação de 90° de $$v$$!

![](/assets/rot.png)

### Números Complexos: uma subalgebra da Álgebra Geométrica do $$\mathbb{R}^2$$
Uma álgebra nada mais é do que um espaço vetorial com uma forma bilinear $$A \times A \rightarrow A$$ que faz $$(x,y) \mapsto xy$$. Uma subalgebra é um subespaço vetorial de uma álgebra que é fechada nas operações da álgebra.

Considere um elemento $$p=xe_1+xe_2$$ e tome o produto geométrico por $$e_1$$:

$$Z=e_1p=xe_1e_1+ye_1e_2$$ 

$$Z=e_1p=x+ye_1e_2$$

O elemento $$Z$$ é um **multivetor de grau par**. O subespaço gerado por $$Z$$ é uma subalgebra da álgebra geométrica do $$\mathbb{R}^2$$(ou $$\mathcal{G^2}$$). Vamos provar que existe um isormorfismo entre essa subalgebra e a álgebra dos números complexos.

A operação $$Z=e_1p$$ leva cada elemento $$xe_1+ye_2$$ de $$\mathcal{G^2}$$ para um elemento $$x+ye_1e_2$$ da álgebra complexa($$(e_1e_2)^2=i^2=-1$$). Além disso, podemos dizer que $$p =e_1Z$$, o que define um isomorfismo entre a subalgebra par de $$\mathcal{G^2}$$ e a álgebra dos números complexos.

E é isso que eu queria fazer nesse post! É possível fazer um processo parecido com quaternions, mas não pretendo postar isso tão logo. Não decidi qual vai ser o próximo tema, mas recentemente comecei a ler o livro "An introduction to Clifford algebras and spinors" dos professores Jayme Vaz(UNICAMP) e Roldão da Rocha(UFABC), então provavelmente vou ter mais material em breve. 

Obrigado pela atenção, volte sempre! 

## Referências
*Geometric Algebra* - Eric Chisolm

[Geometric Algebra](https://www.youtube.com/watch?v=PNlgMPzj-7Q&list=PLpzmRsG7u_gqaTo_vEseQ7U8KFvtiJY4K) - Mathoma
