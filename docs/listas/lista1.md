# Lista 1

## Questão 1

Seja $G=(V,E)$ um grafo, $|V|=n$ e $|E|=m$. Mostre que:

**(a)**

$$
m \leq \frac{n(n-1)}{2}.
$$

**(b)** Se $G$ é um grafo bipartido, então

$$
m \leq \frac{n^2}{4}.
$$

---

## Questão 2

Mostre que em uma festa com $n$ ($n\geq 2$) pessoas, existem pelo menos duas pessoas com o mesmo número de conhecidos.

---

## Questão 3

Um grafo é auto-complementar se

$$
G \cong \overline{G}.
$$

**(a)** Dê dois exemplos de grafos auto-complementares.

**(b)** Prove que um grafo auto-complementar tem $4k$ ou $4k+1$ vértices, para $k$ um inteiro não negativo.

---

## Questão 4

Mostre que dois caminhos quaisquer de comprimento máximo em um grafo $G$ conexo possuem necessariamente algum vértice em comum.

---

## Questão 5

A cintura de um grafo $G$ é o comprimento de seu menor ciclo. Se $G$ for acíclico, sua cintura é infinita.

Mostre que um grafo $k$-regular de cintura $4$ possui pelo menos $2k$ vértices.

---

## Questão 6

Mostre que

$$
\delta \leq \frac{2m}{n} \leq \Delta
$$

para qualquer grafo $G=(V,E)$, onde $|V|=n$, $|E|=m$, $\delta$ é o menor grau de $G$ e $\Delta$ é o maior grau de $G$.

---

## Questão 7

Seja $G$ um grafo com $n$ vértices e $n-1$ arestas. Prove que as seguintes afirmações são equivalentes:

**(a)** $G$ é conexo;

**(b)** $G$ é acíclico;

**(c)** $G$ é uma árvore.

---

## Questão 8

Mostre que uma árvore com exatamente dois vértices de grau $1$ é um caminho.

---

## Questão 9

Prove o seguinte teorema:

Seja $T$ uma árvore geradora para um grafo $G$ e seja $e$ uma aresta que pertence a $G$, mas não a $T$. Então, o grafo $T+e$ possui exatamente um ciclo.

---

## Questão 10

O $k$-cubo ($Q_k$) é um grafo cujos vértices são $k$-uplas ordenadas de $0$'s e $1$'s, e tal que dois vértices são adjacentes se e somente se diferem em exatamente uma coordenada.

**(a)** Desenhe $Q_1$, $Q_2$, $Q_3$ e $Q_4$.

**(b)** Qual é o número de vértices e arestas de cada um desses grafos?

**(c)** Qual o número de vértices e arestas de $Q_k$?

**(d)** Prove que $Q_k$ é bipartido.

---

## Questão 11

Mostre que qualquer grafo $G=(V,E)$ contém pelo menos

$$
m-n+w
$$

ciclos distintos, onde $|V|=n$, $|E|=m$ e $w=$ número de componentes conexos de $G$.

---

## Questão 12

Prove ou dê contra-exemplo (considere $G$ não trivial).

**(a)** Se $v$ é uma articulação de $G$, então $v$ é articulação de todo subgrafo induzido que o contém (i.e. ser articulação é propriedade hereditária).

**(b)** Se $G$ contém uma ponte, então $G$ contém uma articulação.

**(c)** Se $G$ contém uma articulação, então $G$ contém uma ponte.

---

## Questão 13

Seja $G$ um grafo conexo e $S$ um subconjunto próprio não vazio de $V$. Mostre que o corte

$$
[S,\overline{S}]
$$

é minimal se e somente se $G[S]$ e $G[\overline{S}]$ forem ambos conexos.

---

## Questão 14

Dê exemplo de um grafo com

$$
\kappa=3,\qquad \kappa'=4
\qquad\text{e}\qquad
\delta=5.
$$

---

## Questão 15

Mostre que se $G$ é cúbico (i.e. regular de grau $3$), então

$$
\kappa=\kappa'.
$$