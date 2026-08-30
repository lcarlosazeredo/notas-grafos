# Aula 02 — 12/08/2026

## Contagem Dupla

Queremos mostrar que

$$
\sum_{k=0}^{n}\binom{n}{k}=2^n.
$$

Podemos contar o número de subconjuntos de $[n]$ de duas formas.

### I)

Para cada $i\in[n]$, cada $i$ está ou não está em um subconjunto $A$.

Pelo P.M. (Princípio da Multiplicação),

$$
\underbrace{2\times\cdots\times2}_{n\text{ vezes}}=2^n.
$$

### II)

Existem exatamente

$$
\binom{n}{k}
$$

subconjuntos de $[n]$ de tamanho $k$.

Como cada subconjunto de $[n]$ tem tamanho $k$, para algum

$$
0\leq k\leq n,
$$

o número de subconjuntos de $[n]$ é

$$
\sum_{k=0}^{n}\binom{n}{k}.
$$

Portanto,

$$
\sum_{k=0}^{n}\binom{n}{k}=2^n.
$$

---

## Definição 2.1 — Grafo simples

Um **grafo simples**, ou simplesmente um **grafo**, é um par

$$
G=(V,E),
$$

em que $V$ é um conjunto finito não vazio, chamado **conjunto de vértices de $G$**, e

$$
E\subseteq\binom{V}{2}
$$

é chamado **conjunto de arestas de $G$**.

Denotamos esses conjuntos também por

$$
V(G)
$$

e

$$
E(G).
$$

Como

$$
E(G)\subseteq\binom{V(G)}{2},
$$

as arestas são formadas por pares de vértices distintos.

Em particular, um grafo simples não possui laços.

Além disso, denotamos uma aresta de $G$ como $\{u,v\}$, ou simplesmente por

$$
uv,
$$

se,

$$
uv\in E
$$

e $u,v\in V$, $u\neq v$.

---

## Definição 2.2 — Adjacência e incidência

Sejam $u,v\in V$ tais que $u\neq v$.

Dizemos que $u$ e $v$ são **adjacentes** se

$$
uv\in E.
$$

Além disso, dizemos que a aresta $uv$ **incide** em $u$ e $v$.

Os vértices $u$ e $v$ são chamados de **extremos** da aresta $uv$.

---

## Definição 2.3 — Ordem e tamanho de um grafo

A **ordem** de um grafo $G$ é denotada por $n$ e corresponde ao número de vértices:

$$
|V(G)|=n.
$$

O **tamanho** de um grafo $G$ é denotado por $m$ e corresponde ao número de arestas:

$$
|E(G)|=m.
$$

---

## Definição 2.4 — Vizinhança aberta

Seja $v\in V$.

A **vizinhança de $v$ em $G$** é definida por

$$
N(v)=\{u\in V:uv\in E(G)\}.
$$

---

## Definição 2.5 — Vizinhança fechada

A **vizinhança fechada** de $v$ em $G$ é definida por

$$
N[v]=N(v)\cup\{v\}.
$$

---

## Definição 2.6 — Grau de um vértice

O **grau** de um vértice $v$ é dado por

$$
d(v)=|N(v)|.
$$

Ou seja, $d(v)$ é o número de vizinhos de $v$.

Como $G$ é simples e possui $n$ vértices,

$$
0\leq d(v)\leq n-1,
\qquad \forall v\in V.
$$

Um vértice $v\in V$ é dito **isolado** se

$$
d(v)=0.
$$

Um vértice $v\in V$ é dito **universal** se

$$
d(v)=n-1.
$$

---

## Exemplo

Considere o grafo da figura apresentada em aula, com vértices

$$
V=\{v_1,v_2,v_3,v_4,v_5\}.
$$

Os graus dos vértices são

$$
d(v_1)=3,
$$

$$
d(v_2)=2,
$$

$$
d(v_3)=3,
$$

$$
d(v_4)=4,
$$

$$
d(v_5)=2.
$$

As respectivas vizinhanças são

$$
N(v_1)=\{v_2,v_3,v_4\},
$$

$$
N(v_2)=\{v_1,v_4\},
$$

$$
N(v_3)=\{v_1,v_4,v_5\},
$$

$$
N(v_4)=\{v_1,v_2,v_3,v_5\},
$$

$$
N(v_5)=\{v_3,v_4\}.
$$

---

## Definição 2.7 — Grau mínimo

O **grau mínimo** de um grafo $G$ é denotado por

$$
\delta(G):=\min_{v\in V}d(v).
$$

---

## Definição 2.8 — Grau máximo

O **grau máximo** de um grafo $G$ é denotado por

$$
\Delta(G):=\max_{v\in V}d(v).
$$

---

## Definição 2.9 — Grafo regular

Um grafo é **$k$-regular** se

$$
d(v)=k,
\qquad \forall v\in V.
$$

---

## Proposição 2.1

Se $G$ é um grafo de ordem $n$, então

$$
|E(G)|\leq\binom{n}{2}.
$$

### Prova

Como, por definição,

$$
E\subseteq\binom{V}{2},
$$

temos

$$
|E|\leq\left|\binom{V}{2}\right|.
$$

Como

$$
|V|=n,
$$

segue que

$$
\left|\binom{V}{2}\right|=\binom{n}{2}.
$$

Portanto,

$$
|E|\leq\binom{n}{2}.
$$

$\square$

---

## Teorema 2.1 — Teorema do Aperto de Mãos

Seja $G$ um grafo e seja

$$
m:=|E(G)|.
$$

Então

$$
\sum_{v\in V}d(v)=2m.
$$

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>
---

## Corolário 2.1

Em todo grafo, o número de vértices de grau ímpar é par.

### <span class="prova-exercicio">Prova (Exercício)</span>

!!! info "Exercício"
