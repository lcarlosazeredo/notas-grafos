# Aula 03 — 17/08/2026

## Definição 3.1 — Complemento de um grafo

O **complemento** de um grafo $G$, denotado por $\overline{G}$, é dado por

$$
V(G)=V(\overline{G})
$$

e

$$
E(\overline{G})
=
\{uv \mid u,v\in V(G) \text{ e } uv\notin E(G)\}.
$$

---

## Definição 3.2 — Subgrafo

Seja

$$
G=(V,E)
$$

um grafo.

Um grafo

$$
H=(V(H),E(H))
$$

é dito **subgrafo** de $G$ se

$$
V(H)\subseteq V
$$

e

$$
E(H)\subseteq E.
$$

---

## Definição 3.3 — Subgrafo gerador

Um subgrafo

$$
H=(V(H),E(H))
$$

é um **subgrafo gerador** de $G$ se $H$ é subgrafo de $G$ e

$$
V(H)=V.
$$

---

## Definição 3.4 — Subgrafo induzido

Seja

$$
X\subseteq V.
$$

Um subgrafo $H$ é um **subgrafo induzido** de $G$ por $X$, denotado por

$$
H=G[X],
$$

se

$$
V(H)=X
$$

e

$$
E(H)=\{uv\in E(G)\mid u,v\in X\}.
$$

**Exemplo:**

Na figura da aula, tomando

$$
X=\{v_3,v_4,v_5\},
$$

o grafo $G[X]$ é o subgrafo de $G$ induzido pelos vértices de $X$.

---

## Problema NP-completo

> Clique e Conjunto Independente

---

## Definição 3.5 — Clique

Uma **clique** de $G$ é um conjunto de vértices

$$
V'\subseteq V
$$

tal que

$$
G[V']
$$

é um grafo completo.

> Uma clique pode ser **maximal**, mas não necessariamente **máxima**.

---

## Definição 3.6 — Conjunto independente

Um **conjunto independente** de $G$ é um conjunto de vértices

$$
V'\subseteq V
$$

tal que

$$
G[V']
$$

é um grafo nulo.

---

## Definição 3.7 — Maximal e minimal

Um subgrafo $H$ de $G$ é **maximal** (respectivamente, **minimal**) com relação a uma propriedade $P$ se $H$ satisfaz $P$ e não existe $H'$ satisfazendo $P$ tal que

$$
H\subset H'
$$

(respectivamente,

$$
H'\subset H
$$

).

---

## Definição 3.8 — Máximo e mínimo

Um subgrafo $H$ de $G$ é **máximo** (respectivamente, **mínimo**) com relação a uma propriedade $P$, em relação a vértices, se, dentre todos os subgrafos $H'$ de $G$ maximais (respectivamente, minimais) com relação à propriedade $P$,

$$
|V(H)|\geq |V(H')|
$$

(respectivamente,

$$
|V(H)|\leq |V(H')|
$$

).

> **Observação:** "máximo" e "mínimo" podem se referir ao número de vértices ou ao número de arestas, dependendo da propriedade considerada.

---

## Emparelhamento

> Conjunto independente de arestas

---

## Problema de Isomorfismo

Dois grafos

$$
G_1=(V_1,E_1)
$$

e

$$
G_2=(V_2,E_2)
$$

são **isomorfos**, e denotamos por

$$
G_1\cong G_2,
$$

se existe uma função bijetiva

$$
f:V_1\longrightarrow V_2
$$

que satisfaz

$$
ab\in E_1
$$

se, e somente se,

$$
f(a)f(b)\in E_2.
$$

---

## Exercício — Isomorfismo

Determine se os grafos apresentados na figura da aula são isomorfos.

### <span class="prova-exercicio">Resolução (Exercício)</span>

<div class="prova-exercicio">

</div>
