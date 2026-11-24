
# Aula 16 — 09/11/2026

## Coloração de Vértices

---

## Definição 16.1 — $k$-coloração de vértices

Uma **$k$-coloração de vértices** é uma atribuição de cores aos vértices de um grafo utilizando um conjunto de $k$ cores distintas disponíveis.

---

## Definição 16.2 — Coloração própria

Uma coloração é **própria** quando vértices adjacentes recebem cores distintas.

---

## Definição 16.3 — Grafo $k$-colorível

Um grafo é **$k$-colorível** se admite uma $k$-coloração própria.

---

## Definição 16.4 — Grafo $k$-cromático e número cromático

Um grafo é **$k$-cromático** se $k$ é o menor inteiro para o qual o grafo é $k$-colorível.

O **número cromático** de um grafo $G$ é denotado por

$$
\chi(G).
$$

Assim, se $G$ é $k$-cromático, então

$$
\chi(G)=k.
$$

---

## Teorema 16.1

Um grafo $G$ é 2-colorível se, e somente se, $G$ é bipartido.

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Definição 16.5 — Grafo crítico

Um grafo $G$ é **crítico** se

$$
\chi(H)<\chi(G)
$$

para todo subgrafo próprio $H$ de $G$.

---

## Definição 16.6 — Grafo $k$-crítico

Um grafo é **$k$-crítico** quando é crítico e $k$-cromático.

---

## Teorema 16.2

Se $G$ é um grafo $k$-crítico, então

$$
\delta(G)\geq k-1.
$$

### Prova

Suponha, por absurdo, que $G$ possua um vértice $v$ com menos do que $k-1$ vizinhos.

Seja

$$
H=G-v.
$$

Como $G$ é $k$-crítico, então $H$ é $(k-1)$-colorível.

Como

$$
N_G(v)\subseteq V(H)
$$

e

$$
|N_G(v)|<k-1,
$$

existe uma das $k-1$ cores que não foi atribuída a nenhum vizinho de $v$.

Então, $v$ pode receber tal cor e obtemos uma $(k-1)$-coloração própria para $G$.

Isso contradiz o fato de $G$ ser $k$-cromático.

Logo,

$$
\delta(G)\geq k-1.
$$

$\square$

---

## Corolário 16.1

Todo grafo $k$-cromático tem pelo menos $k$ vértices de grau pelo menos $k-1$.

### Prova

Como $G$ é $k$-cromático, existe um subgrafo $k$-crítico $H$ de $G$.

De fato, basta tomar um subgrafo minimal de $G$ cujo número cromático seja $k$.

Como $H$ é $k$-cromático,

$$
|V(H)|\geq k.
$$

Assim, pelo teorema anterior,

$$
\delta(H)\geq k-1.
$$

Portanto, cada vértice de $H$ tem grau pelo menos $k-1$.

Como $H$ é um subgrafo de $G$, temos

$$
d_G(v)\geq d_H(v)\geq k-1,
\qquad \forall v\in V(H).
$$

Logo, $G$ possui pelo menos $k$ vértices de grau pelo menos $k-1$.

$\square$

---

## Corolário 16.2

Para todo grafo $G$,

$$
\chi(G)\leq\Delta(G)+1.
$$

### Prova

Assuma que $G$ não seja $(\Delta(G)+1)$-colorível.

Então, $G$ possui número cromático pelo menos

$$
\Delta(G)+2.
$$

Isso implica, pelo corolário anterior, a existência de um vértice de grau pelo menos

$$
\Delta(G)+1.
$$

Mas isso contradiz a definição de grau máximo de $G$.

Logo,

$$
\chi(G)\leq\Delta(G)+1.
$$

$\square$

---

## Definição 16.7 — Corte de vértices (Revisão)

Um **corte de vértices** de $G$ é um conjunto

$$
S\subseteq V
$$

tal que

$$
W(G-S)>W(G).
$$

---

## Definição 16.8 — $S$-componentes

Seja $S$ um corte de vértices de $G$.

Sejam $V_1,V_2,\ldots,V_p$ os conjuntos de vértices das componentes conexas de $G-S$.

As **$S$-componentes** de $G$ são os subgrafos

$$
G_i:=G[V_i\cup S],
\qquad 1\leq i\leq p.
$$

**Exemplo:**

Considere o grafo apresentado em aula, no qual a remoção de $S$ resulta em três componentes conexas, com conjuntos de vértices

$$
V_1,\quad V_2,\quad V_3.
$$

As respectivas $S$-componentes são

$$
G_1=G[V_1\cup S],
$$

$$
G_2=G[V_2\cup S]
$$

e

$$
G_3=G[V_3\cup S].
$$

---

## Teorema 16.3

Se $G$ é um grafo crítico, nenhum corte de vértices é uma clique.

### Prova

Suponha, por contradição, que $G$ seja crítico e possua um corte de vértices $S$ que induz uma clique.

Seja

$$
k=\chi(G).
$$

Denote por

$$
G_i:=G[V_i\cup S],
\qquad 1\leq i\leq p,
$$

as $S$-componentes de $G$.

Como cada $G_i$ é um subgrafo próprio de $G$ e $G$ é crítico, cada $G_i$ é $(k-1)$-colorível.

Além disso,

$$
|S|\leq k-1,
$$

pois, caso contrário, cada $G_i$ teria número cromático pelo menos $k$.

Como $S$ induz uma clique, seus vértices recebem cores distintas em cada uma das colorações próprias dos subgrafos $G_i$.

Podemos, então, permutar as cores utilizadas em cada $G_i$ de modo que os vértices de $S$ recebam as mesmas cores em todas as $S$-componentes.

Como cada $G_i$ é $(k-1)$-colorível e $S$ está contido em todas as $S$-componentes de $G$, obtemos uma $(k-1)$-coloração própria de $G$.

Logo,

$$
\chi(G)\leq k-1,
$$

o que contradiz

$$
\chi(G)=k.
$$

Portanto, nenhum corte de vértices de um grafo crítico é uma clique.

$\square$

---

## Observação — Blocos

Lembre-se de que um bloco é um grafo conexo que não possui articulação.

Ou seja, não existe corte de vértices de tamanho 1.

---

## Corolário 16.3

Todo grafo crítico é um bloco.

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Teorema 16.4 — Brooks

Se $G$ é um grafo conexo que não é um ciclo ímpar e não é um grafo completo, então

$$
\chi(G)\leq\Delta(G).
$$

### <span class="prova-exercicio">Prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Observações sobre resultados matemáticos

- **Corolário:** uma consequência de um teorema. O teorema não é necessariamente estritamente mais forte que o corolário.

- **Lema:** resultado matemático demonstrado, geralmente utilizado como auxílio na demonstração de outro resultado.

- **Conjectura**: uma afirmação que se acredita ser verdadeira, mas que ainda não foi demonstrada e para a qual não se conhece um contraexemplo.
