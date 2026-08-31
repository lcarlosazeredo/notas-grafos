# Aula 07 — 31/08/2026

## Cortes de Arestas

Denotamos por

$$
[S, S']
$$

o conjunto das arestas com um extremo em $S$ e outro extremo em $S'$.

---

## Definição 7.1 — Corte de arestas

Um **corte de arestas** de um grafo $G$ é um conjunto $E$ da forma

$$
[S,\overline{S}],
$$

onde $S$ é um subconjunto próprio e não vazio de $V$ e

$$
\overline{S}=V\setminus S.
$$

**Exemplo:**

Para

$$
S=\{a,b\}
$$

e

$$
\overline{S}=\{c,d,e\},
$$

temos, no exemplo da aula,

$$
[S,\overline{S}]=\{bc,ac,ae\}.
$$

---

## Definição 7.2 — Ligação

Uma **ligação** é um corte de arestas minimal não vazio.

> **Observação:** Cada aresta que é uma ponte é uma ligação.

---

## Conteúdo da P1

**P1: 23/09**

Conteúdos:

- Conceitos básicos;
- Árvores;
- Conectividade;
- Grafos Eulerianos e Hamiltonianos.

---

## Conjunto desconectante de arestas

Se $G$ é conexo, então uma ligação de $G$ é um subconjunto minimal $B$ de $E$ tal que

$$
G-B
$$

é um grafo desconexo.

**Exemplo:**

Nos exemplos apresentados em aula, alguns conjuntos de arestas desconectam o grafo, mas não são necessariamente cortes de arestas minimais.

---

## Problema — Corte mínimo de arestas

**Pergunta:** Quantas arestas precisamos remover, no mínimo, para desconectar um grafo?

Os exemplos apresentados mostram que essa quantidade depende da estrutura do grafo.

> Não necessariamente, se o grafo for grande, será muito difícil de desconectar. Depende da estrutura.

---

## Minimal e mínimo

Um conjunto é **minimal** quando não pode ser diminuído mantendo uma determinada propriedade.

Um conjunto é **mínimo** quando possui o menor tamanho entre os conjuntos que satisfazem uma determinada propriedade.

---

## Articulação

## Definição 7.3 — Vértice de articulação

Um vértice $v$ é um **vértice de articulação** se, e somente se,

$$
W(G-\{v\})>W(G).
$$

Ou seja, a remoção de $v$ aumenta o número de componentes conexas do grafo.

**Exemplo:**

No grafo apresentado em aula, os vértices $c$ e $e$ são vértices de articulação.

Os vértices $a$, $b$ e $d$ não são vértices de articulação.

---

## Definição 7.4 — Corte de vértices

Um **corte de vértices** é um conjunto

$$
S\subseteq V
$$

tal que

$$
W(G-S)>W(G),
$$

ou tal que $G-S$ é isomorfo a $K_1$.

> **Observação:** Se $v$ é uma articulação de $G$, então $\{v\}$ é um corte de vértices de tamanho mínimo.

---

## Problema do corte de vértices

O problema de corte é um problema de **minimização**.

Queremos determinar o menor número de vértices cuja remoção desconecta o grafo.

---

## Definição 7.5 — Conectividade de vértices

O parâmetro

$$
\kappa(G)
$$

denota o tamanho do menor corte de vértices de $G$.

**Exemplo:**

Se $G = K_n$ (grafo completo) , então

$$
\kappa(G)=n-1.
$$

---

## Definição 7.6 — Conectividade de arestas

O parâmetro

$$
\kappa'(G)
$$

denota o tamanho do menor corte de arestas de $G$.

**Exemplo:**

Se $G = K_1$, então

$$
\kappa'(G)=0.
$$

---

## Definição 7.7 — Grafo $k$-conexo

Um grafo é **$k$-conexo** se

$$
\kappa(G)\geq k.
$$

---

## Definição 7.8 — Grafo $r$-aresta-conexo

Um grafo é **$r$-aresta-conexo** se

$$
\kappa'(G)\geq r.
$$