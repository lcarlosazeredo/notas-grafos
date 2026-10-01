# Aula 11 — 30/09/2026

## Emparelhamentos

Um **emparelhamento** $M\subseteq E(G)$ é um subconjunto das arestas tal que quaisquer par de arestas em $M$ são não adjacentes.

> Ou seja, quaisquer duas arestas de $M$ não possuem um vértice em comum.

**Exemplo:**

Considere o grafo apresentado em aula.

Alguns emparelhamentos possíveis são

$$
M_1=\{fg\}
$$

$$
M_2=\{fg,ah,cd\}
$$

$$
M_3=\{eh,cd,ag\}
$$

$$
M_4=\{eh,fg\}
$$

---

Um emparelhamento é **maximal** se não está contido propriamente em nenhum outro emparelhamento.

Um emparelhamento é **máximo** se possui a maior cardinalidade entre todos os emparelhamentos.

Um emparelhamento é **perfeito** se tem cardinalidade $\frac{n}{2}$.

---

## Definição 11.1 — Vértice $M$-saturado/insaturado

Dada uma aresta

$$
xy\in M,
$$

dizemos que os extremos $x$ e $y$ são **$M$-emparelhados**.

Se existe uma aresta

$$
e\in M
$$

incidente em um vértice $x$, dizemos que $x$ está **$M$-saturado**.

Caso contrário, dizemos que $x$ é **$M$-insaturado**.

---

## Definição 11.2 — Caminho $M$-alternante

Um caminho $M$-alternante em $G$ é um caminho cujas arestas estão alternadamente em

$$
M
$$

e em

$$
E(G)\setminus M.
$$

---

## Definição 11.3 — Caminho $M$-aumentante

Um caminho $M$-alternante é chamado de **$M$-aumentante** se sua origem e seu término são vértices $M$-insaturados.

---

## Teorema 11.1 — Berge

Seja $G$ um grafo.

$M$ é um emparelhamento se, e somente se, $G$ não contém caminho aumentante.

### Prova

$(\Rightarrow)$ (Contrapositiva)

Suponha que $G$ possua um caminho $M$-aumentante.  
Obtemos um emparelhamento $M'$ tal que

$$
|M'|=|M|+1:
$$

- Mantenha as arestas de $M$ que não pertencem a $P$, seja $x$ esse número de arestas;
- remova $M\cap E(P)$, ou seja, remova de $M$ as arestas de $P$;
- adicione $E(P)-M$, ou seja, adicione as arestas de $P$ que não pertencem a $M$.

O caminho $M$-aumentante tem, necessariamente, quantidade par de vértices, pois as arestas alternam entre não pertence e pertence a $M$.

Seja

$$
P=v_1-v_2-\cdots-v_{2k}
$$

Temos:

$$
P=v_1-v_{2} \overset{M}{-}\cdots{-}v_{2k-2}\overset{M}{-}v_{2k-1}-v_{2k}
$$

Note que

$$
|M|=x+k-1
$$

e

$$
|M'|=x+k.
$$

Assim,

$$
|M'|=|M|+1
$$

Logo, $M$ não é máximo.
