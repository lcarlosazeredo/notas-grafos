# Aula 04 — 19/08/2026

## Definição 4.1 — Grafo bipartido

Um grafo $G=(V,E)$ é **bipartido** se $V$ admite uma partição em dois subconjuntos $X$ e $Y$ tal que toda aresta em $E$ possui um extremo em $X$ e outro em $Y$.

Essa partição de $V$ é chamada **bipartição** de $V$.

---

## Definição 4.2 — Grafo bipartido completo

Um grafo é **bipartido completo**, denotado por

$$
K_{p,q},
$$

se é um grafo bipartido com

$$
|X|=p
$$

e

$$
|Y|=q,
$$

e

$$
|E|=pq.
$$

**Exemplo:**

$$
K_{3,3}.
$$

---

## Teorema 4.1

Um grafo bipartido $r$-regular, com $r>0$, satisfaz

$$
|X|=|Y|.
$$

### Prova

Pelo Teorema do Aperto de Mãos, como $G$ é bipartido, temos

$$
m=\sum_{v\in X}d(v)
=
\sum_{v\in Y}d(v).
$$

Além disso, $G$ é $r$-regular. Assim,

$$
m=r|X|=r|Y|.
$$

Como

$$
r>0,
$$

segue que

$$
|X|=|Y|.
$$

$\square$

---

## Passeio, Trilha e Caminho

### Definição 4.3 — Passeio

Um **passeio** é uma sequência

$$
v_1,v_2,\ldots,v_k
$$

de vértices de $V$ tal que

$$
v_iv_{i+1}\in E,
\qquad i=1,\ldots,k-1.
$$

### Definição 4.4 — Trilha

Uma **trilha** é um passeio em que as arestas são distintas.

### Definição 4.5 — Caminho

Um **caminho** é um passeio em que os vértices são distintos.

### Definição 4.6 — Ciclo

Um **ciclo** é um passeio fechado

$$
v_1,v_2,\ldots,v_k=v_1,
$$

em que

$$
v_1,v_2,\ldots,v_{k-1}
$$

é um caminho.

A **cintura** é o tamanho do menor ciclo de $G$.

---

## Exemplo — Passeio, trilha e caminho

No grafo apresentado em aula:

$$
a,b,c,d,c,e
$$

é um **passeio**.

$$
a,b,c,e,f,b,g
$$

é uma **trilha**.

$$
h,b,c,d
$$

é um **caminho**.

---
## Conexidade

## Definição 4.7 — Grafo conexo

Um grafo $G$ é **conexo** se existe um caminho entre quaisquer dois vértices de $G$.

Um grafo é **desconexo** quando não é conexo.

---

## Definição 4.8 — Componente conexa

Uma **componente conexa** de um grafo $G$ é um subgrafo conexo maximal.

O número de componentes conexas de $G$ é denotado por

$$
W(G).
$$

---

## Distância, Excentricidade, Diâmetro e Centro

## Definição 4.9 — Distância

A **distância** entre dois vértices $u,v\in V$, denotada por

$$
d(u,v),
$$

é o tamanho do menor caminho entre $u$ e $v$ em $G$.

---

## Definição 4.10 — Excentricidade

A **excentricidade** de um vértice $v\in V$, denotada por

$$
e(v),
$$

é o valor da maior distância entre $v$ e os demais vértices de $V$.

---

## Definição 4.11 — Diâmetro

O **diâmetro** de um grafo $G$, denotado por

$$
\operatorname{diam}(G),
$$

é o valor da maior excentricidade dos vértices de $G$.

---

## Definição 4.12 — Centro

O **centro** de um grafo $G$, denotado por

$$
C(G),
$$

é o conjunto dos vértices de menor excentricidade do grafo.

### <span class="prova-exercicio">Exemplo (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Tipos importantes de grafos

## Definição 4.13 — Grafo ciclo

Um grafo é um **grafo ciclo** de tamanho $n$, denotado por

$$
C_n,
\qquad n\geq 3,
$$

se $G$ consiste de um único ciclo.

---

## Definição 4.14 — Grafo caminho

Um grafo é um **grafo caminho** de tamanho $n-1$, denotado por

$$
P_n,
\qquad n\geq 2,
$$

se $G$ consiste de um único caminho com $n$ vértices.

---

## Teorema 4.2 — Caracterização dos grafos bipartidos

Um grafo $G$ é bipartido se, e somente se, $G$ não contém ciclo ímpar.

### <span class="prova-exercicio">Prova$(\Rightarrow)$: (Exercício)</span>

<div class="prova-exercicio">

</div>