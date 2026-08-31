# Aula 06 — 26/08/2026

## Definição 6.1 — Ponte

Uma **ponte** em um grafo $G$ é uma aresta $e$ que satisfaz

$$
W(G)<W(G-e),
$$

isto é, a remoção de $e$ aumenta o número de componentes conexas do grafo.

> Se $G$ é conexo, então $W(G)=1$.

---

## Teorema 6.1 — Caracterização de pontes

Uma aresta $e$ é uma ponte se, e somente se, $e$ não pertence a um ciclo.

### Prova

$(\Rightarrow)$ Suponha que

$$
e=xy
$$

é uma ponte em $G$.

Logo,

$$
W(G)<W(G-e).
$$

Como $e$ é uma ponte, ao ser removida, temos que $x$ e $y$ pertencem a componentes distintas de $G-e$.

Caso a aresta $e$ pertencesse a um ciclo $C$ de $G$, então, após a remoção de $e$, ainda haveria um caminho entre $x$ e $y$.

Portanto, $e$ não seria uma ponte.

Logo, $e$ não pertence a nenhum ciclo de $G$.

$(\Leftarrow)$ Suponha que

$$
e=xy
$$

não pertence a um ciclo $C$ de $G$ e que $e$ não é uma ponte.

Assim,

$$
W(G)=W(G-e).
$$

A igualdade garante que existe um caminho entre $x$ e $y$ em $G-e$, isto é, um caminho que não utiliza $e$.

Logo, há mais de um caminho em $G$ entre $x$ e $y$ e, assim, $e$ pertence a um ciclo.

Contradição.

Portanto, $e$ é uma ponte.

$\square$

---

## Teorema 6.2 — Caracterização de árvores por pontes

Um grafo conexo é uma árvore se, e somente se, toda aresta é uma ponte.

### Prova

$(\Rightarrow)$ Seja $G$ uma árvore e seja $e$ uma aresta de $G$.

Como $G$ é acíclico, $e$ não pertence a nenhum ciclo de $G$.

Pelo Teorema 6.1, $e$ é uma ponte em $G$.

$(\Leftarrow)$ Suponha que $G$ seja conexo e não seja uma árvore.

Logo, $G$ possui um ciclo $C$.

Assim, pelo Teorema 6.1, nenhuma aresta de $C$ é uma ponte.

Portanto, nem toda aresta de $G$ é uma ponte.

$\square$

---

## Definição 6.2 — Árvore geradora

Uma **árvore geradora** de um grafo $G$ é um subgrafo gerador de $G$ que é uma árvore.

Ou seja, se $T$ é uma árvore geradora de $G$, então

$$
V(T)=V(G)
$$

e $T$ é conexo e acíclico.

---

## Teorema 6.3 — Existência de árvore geradora

Todo grafo conexo admite uma árvore geradora, isto é, um subgrafo gerador que é uma árvore.

### Prova

Seja $G$ um grafo conexo.

Considere um subgrafo gerador $H$ de $G$ que seja **minimalmente conexo**, isto é, para toda aresta

$$
e\in E(H),
$$

o grafo

$$
H-e
$$

é desconexo.

Cada aresta $e$ de $H$ é, portanto, uma ponte.

Pelo Teorema 6.1, temos que $e$ não está em nenhum ciclo.

Logo, $H$ é conexo e acíclico.

Portanto, $H$ é uma árvore geradora de $G$.

$\square$

---

## Corolário 6.1

Se $G$ é conexo, de ordem $n$ e tamanho $m$, então

$$
m\geq n-1.
$$

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Teorema 6.4 — Adição de uma aresta a uma árvore geradora

Seja $T$ uma árvore geradora de um grafo $G$ e seja $e$ uma aresta que pertence a $G$, mas não a $T$.

Então o grafo

$$
T+e
$$

possui exatamente um ciclo.

### <span class="prova-exercicio">Prova (Exercício-Lista)</span>

<div class="prova-exercicio">

</div>