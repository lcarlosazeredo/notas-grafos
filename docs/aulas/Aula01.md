# Aula 01 — 10/08/2026

## Ementa

- Conceitos básicos;
- Árvores;
- Conectividade;
- Grafos eulerianos e hamiltonianos;
- Emparelhamentos;
- Planaridade;
- Coloração de vértices e arestas;
- Problemas extremais em grafos.

---

## Bibliografia

- *Introduction to Graph Theory* — West;
- *Graph Theory* — Diestel;
- *Graph Theory* — Bondy and Murty, 2008;
  > mais completo;
- *Graphs and Digraphs* — Chartrand et al.;
  > mais intuitivo.

---

## Avaliação

**Graduação**

$$
\frac{P_1+P_2}{2} \geq 5,0
$$

**Pós-graduação**

$$
\frac{P_1+P_2+S}{3} \geq 5,0
$$

onde $S$ corresponde a um seminário.

- 75% de presença.

---

## Notações

Considere:

$$
\mathbb{N}=\{1,2,\ldots\}
$$

e

$$
[n]=\{1,2,\ldots,n\}.
$$

Dado um conjunto $V$ e um inteiro $k\geq 0$, definimos

$$
\binom{V}{k}
=
\{V'\subseteq V: |V'|=k\}.
$$

Se $|V|=n$, então

$$
\left|\binom{V}{k}\right|
=
\frac{n!}{k!(n-k)!}.
$$

Ou seja, $\binom{V}{k}$ representa os subconjuntos de $V$ que têm
exatamente tamanho $k$.

---

## Definição 1.1 — Parte de um conjunto

Uma **parte de $A$** é um subconjunto de $A$.

---

## Definição 1.2 — Partição

Uma **partição** de $V$ é uma família

$$
V_1,\ldots,V_k
$$

de subconjuntos de $V$ tal que cada elemento de $V$ está precisamente
em um membro da família.

Portanto,

$$
V=V_1\cup\cdots\cup V_k,
\qquad V_i\neq\varnothing,
$$

e

$$
V_i\cap V_j=\varnothing,
\qquad \forall\, V_i\neq V_j.
$$

**Exemplo:**

Considere

$$
V=\{1,2,3,4\}.
$$

Algumas famílias anotadas:

$$
\{\{2\},\{3,4\}\}
$$

e

$$
\{\{2\},\{1\},\{3,4\}\}.
$$

---

## Definição 1.3 — Coloração

Uma **coloração** de $V$ é uma função

$$
c:V\longrightarrow[k].
$$

> **Dica:** Teorema de Van der Waerden.

---

## Teorema 1.1 — Princípio da Casa dos Pombos

Se há $n+1$ pombos e $n$ casas, há ao menos dois pombos na mesma casa.

> A ideia pode ser demonstrada considerando os casos associados a uma
função e usando uma bijeção.

---

## Definição 1.4 — Conjunto livre de soma

Seja

$$
A\subseteq[k].
$$

Dizemos que $A$ é **livre de soma** se

$$
\forall x,y\in A
\quad\Longrightarrow\quad
x+y\notin A.
$$

**Exemplo:**

Considere o conjunto dos números ímpares em $[n]$:

$$
I=\{\text{números ímpares em }[n]\}.
$$

Então

$$
|I|=\left\lceil\frac{n}{2}\right\rceil.
$$

---

## Problema extremal

**Pergunta:** Qual é o tamanho máximo de um subconjunto

$$
A\subseteq[n]
$$

que seja livre de soma?

---

## Teorema 1.2

Seja $A\subseteq[n]$. Se $A$ é livre de soma, então

$$
|A|\leq\left\lceil\frac{n}{2}\right\rceil.
$$

### Prova

Vamos provar que, se

$$
|A|>
\left\lceil\frac{n}{2}\right\rceil,
$$

então $A\subseteq[n]$ **não é livre de soma**.

Seja

$$
m=\max A.
$$

Defina

$$
B=\{m-a:a\in A\}\setminus\{0\}.
$$

Note que

$$
B\subseteq[n]
$$

e

$$
|B|=|A|-1.
$$

Logo,

$$
|A|+|B|
\ge
2\left\lceil\frac{n}{2}\right\rceil+1
> n+1
> n.
$$

Pelo **Princípio da Casa dos Pombos**, existe

$$
b\in A\cap B.
$$

Como $b\in B$, existe $a\in A$ tal que

$$
b=m-a.
$$

Portanto,

$$
a+b=m.
$$

Como

$$
a,b,m\in A,
$$

temos dois elementos de $A$ cuja soma também pertence a $A$.

Logo, $A$ **não é livre de soma**.

$\square$