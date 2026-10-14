# Aula 12 — 14/10/2026

## Definição 12.1 — Diferença Simétrica

Sejam $G$ e $H$ grafos com o mesmo conjunto de vértices $V$.

A **diferença simétrica** $G\triangle H$ é o grafo com conjunto de vértices $V$ cujas arestas são aquelas que pertencem a exatamente um dos grafos.

Considerando conjuntos de arestas, em particular, emparelhamentos $M$ e $M'$,

$$
M\triangle M'=(M-M')\cup(M'-M)
$$

---

## Lema 12.1

Cada componente conexa da diferença simétrica de dois emparelhamentos é ou um ciclo par ou um caminho.

---

## Teorema 11.1 — Berge

Seja $G$ um grafo. $M$ é um emparelhamento máximo de $G$ se, e somente se, $G$ não contém um caminho $M$-aumentante.

### Prova

$(\Leftarrow)$ Vamos provar por contrapositiva.

Suponha que $G$ tenha um emparelhamento $M'$ de cardinalidade maior do que $M$.

Pelo lema anterior,

$$
F=M\triangle M'
$$

é constituído de ciclos pares ou caminhos.

Note que isso implica, como

$$
|M'|>|M|,
$$

que $F$ tenha uma componente conexa que é um caminho.

Além disso, esse caminho deve iniciar e terminar com arestas de

$$
M'-M,
$$

pois

$$
|M'|>|M|.
$$

Assim, ele é um caminho $M$-aumentante.

---

## Corolário 12.1

Uma árvore admite, no máximo, um emparelhamento perfeito.

---

## Teorema 12.1 — Hall

Seja $G$ um grafo bipartido com

$$
V=X\cup Y.
$$

$G$ contém um emparelhamento que satura todo vértice de $X$ se, e somente se,

$$
|N(S)|\geq |S|
$$

para todo

$$
S\subseteq X.
$$