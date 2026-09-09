# Aula 08 — 02/09/2026

## Exemplos — Conectividade

Nos exemplos apresentados em aula, são comparadas a conectividade de vértices

$$
\kappa(G)
$$

e a conectividade de arestas

$$
\kappa'(G).
$$

Os exemplos ilustram diferentes valores possíveis para esses parâmetros.

---

## Teorema 8.1 — Caracterização das articulações em árvores

Um vértice $v$ de uma árvore é uma articulação se, e somente se,

$$
d(v)>1.
$$

### Ideia da prova

Se

$$
d(v)=0,
$$

então $G$ é o grafo trivial.

Se

$$
d(v)=1,
$$

o grafo $G-v$ não tem ciclos e tem

$$
m(G-v)=m(G)-1
$$

e

$$
n(G-v)=n(G)-1.
$$

Logo, $G-v$ é uma árvore.

Por outro lado, se

$$
d(v)>1,
$$

então existem $u,z$ adjacentes a $v$.

Como

$$
u,v,z
$$

é o único caminho entre $u$ e $z$, temos

$$
W(G-v)>W(G).
$$

Portanto, $v$ é uma articulação.

$\square$

---

## Corolário 8.1

Num grafo não trivial conexo, sempre existem pelo menos dois vértices que não são articulações.

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Teorema 8.2 — Relação entre conectividade, conectividade de arestas e grau mínimo

Para um grafo $G$,

$$
\kappa(G)\leq\kappa'(G)\leq\delta(G).
$$

### Ideia da prova

#### $\kappa'(G)\leq\delta(G)$

Seja $v$ um vértice tal que

$$
d(v)=\delta(G).
$$

As arestas incidentes a $v$ definem um corte de arestas para $G$.

Assim,

$$
\kappa'(G)\leq\delta(G).
$$

#### $\kappa(G)\leq\kappa'(G)$

Vimos que

$$
\kappa(G)\leq n-1.
$$

Considere o menor corte de arestas

$$
[S,\overline{S}]
$$

de $G$.

**Caso 1.** Se todo vértice de $S$ é adjacente a todo vértice de $\overline{S}$, então

$$
|[S,\overline{S}]|
=
|S||\overline{S}|
\geq n-1
\geq\kappa(G).
$$

**Caso 2.** Sejam

$$
x\in S
$$

e

$$
y\in\overline{S}
$$

tais que

$$
xy\notin E(G).
$$

Considere

$$
T=N_{\overline{S}}(x)
\cup
\{v\in S\mid v\neq x,\; N_{\overline{S}}(v)\neq\varnothing\}.
$$

Observe que todo caminho de $x$ para $y$ passa por $T$.

Logo, $T$ é um corte de vértices.

Note que, tomando as arestas de $x$ para os vértices de

$$
T\cap\overline{S}
$$

e uma aresta dos vértices de

$$
T\cap S
$$

para cada vértice de $\overline{S}$, temos $|T|$ arestas distintas que pertencem a

$$
[S,\overline{S}].
$$

Assim,

$$
\kappa'(G)
=
|[S,\overline{S}]|
\geq
|T|
\geq
\kappa(G).
$$

Portanto,

$$
\kappa(G)\leq\kappa'(G)\leq\delta(G).
$$

$\square$

---

## Definição 8.1 — Bloco

Um **bloco** é um grafo conexo que não possui articulação.

---

## Definição 8.2 — Bloco de um grafo

Um **bloco** de um grafo $G$ é um subgrafo maximal com relação à propriedade de ser um bloco.

---

## Fatos sobre blocos

**Fato 1.** Dois blocos diferentes em um grafo têm, no máximo, um vértice em comum.

**Fato 2.** Cada aresta de $G$ está em um único bloco.

Portanto, os blocos formam uma partição de

$$
E(G).
$$

---

## Caracterização de grafos $r$-conexos

- $G$ é **1-conexo** se, e somente se, para qualquer par de vértices $u,v$, existe pelo menos um caminho entre eles.

- $G$ é **2-conexo** se, e somente se, para qualquer par de vértices $u,v$, existem pelo menos dois caminhos sem vértices em comum, exceto $u$ e $v$.

> $\hookrightarrow$ **Teorema de Whitney**

- $G$ é **$r$-conexo** se, e somente se, para qualquer par de vértices $u,v$, existem pelo menos $r$ caminhos sem vértices em comum, exceto $u$ e $v$.

> $\hookrightarrow$ **Teorema de Menger**

---

## Teorema 8.3 — Whitney

### Ideia da prova

$(\Leftarrow)$ Direto.

<span class="prova-exercicio">$(\Rightarrow)$ (Lista)</span>

<div class="prova-exercicio">

</div>