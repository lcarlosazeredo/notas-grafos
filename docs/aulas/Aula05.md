# Aula 05 — 24/08/2026

## Teorema 4.2 — Caracterização dos grafos bipartidos

Um grafo $G$ é bipartido se, e somente se, $G$ não contém ciclo ímpar.

### Prova

$(\Leftarrow)$ Suponha que $G$ não contém ciclos ímpares.

Tome $u\in V$ arbitrário. Como $G$ é conexo, defina

$$
X=\{x\in V \mid d(x,u) \text{ é par}\}
$$

e

$$
Y=\{y\in V \mid d(y,u) \text{ é ímpar}\}.
$$

Resta mostrar que $X$ e $Y$ formam uma bipartição.

Com efeito, tome $v,w\in X$. Portanto,

$$
d(u,v)
$$

e

$$
d(u,w)
$$

são pares.

Considere $P$ um caminho de menor comprimento de $u$ até $v$ e $Q$ um caminho de menor comprimento de $u$ até $w$.

Considere $u'$ o último vértice comum que pertence tanto a $P$ quanto a $Q$. (note que eventualmente $u=u'$)

Como $P$ e $Q$ são caminhos de menor comprimento, os caminhos $P_{uu'}$ e $Q_{uu'}$ possuem o mesmo tamanho.

Além disso, temos que $P$ e $Q$ são de comprimento par. Logo, $P_{u'v}$ e $Q_{u'w}$ possuem a mesma paridade.

Implicando, então, que o caminho entre $v$ e $w$, utilizando as arestas de $P$ e $Q$, passando por $u'$, tem comprimento par.

Se $v$ e $w$ fossem vizinhos, este caminho juntamente com a aresta $vw$ formaria um ciclo ímpar.

Porém, $G$ não contém ciclo ímpar, por hipótese.

Como a prova é análoga se $v,w\in Y$, temos que $G$ é bipartido.

$\square$

---

## Definição 5.1 — Árvore

Uma **árvore** é um grafo conexo e acíclico.

---

## Teorema 5.1 — Caracterização das árvores

Um grafo é uma árvore se, e somente se, entre cada par de vértices existe um único caminho.

### Prova

$(\Leftarrow)$ Suponha que $G$ é um grafo tal que entre cada par de vértices existe um único caminho.

Pela existência do caminho, $G$ é conexo.

Além disso, como o caminho é único, $G$ é acíclico.

Logo, $G$ é uma árvore.

$(\Rightarrow)$ Seja $G$ uma árvore e suponha que, entre $u$ e $w$, existam dois caminhos distintos $P$ e $P'$.

Tome

$$
xy\in E(P)
$$

tal que

$$
xy\notin E(P').
$$

Considere o subgrafo induzido por

$$
P\cup P'
$$

e remova deste subgrafo a aresta $xy$.

Note que

$$
(P\cup P')\setminus\{xy\}
$$

é conexo.

Logo, existe um caminho $P''$ entre $x$ e $y$ neste subgrafo.

Portanto,

$$
P''+\{xy\}
$$

é um ciclo em $G$.

Absurdo, pois $G$ é uma árvore e, portanto, acíclico.

Logo, entre cada par de vértices existe um único caminho.

$\square$

---

## Teorema 5.2 — Número de arestas de uma árvore

Se $G$ é uma árvore de ordem $n$ e tamanho $m$, então

$$
m=n-1.
$$

### <span class="prova-exercicio">Prova (Exercício-Lista)</span>

<div class="prova-exercicio">

</div>

---

## Corolário 5.1 — Folhas de uma árvore

Em uma árvore com

$$
n\geq 2,
$$

sempre há pelo menos duas folhas.

### <span class="prova-exercicio">Prova (Exercício-Lista)</span>

<div class="prova-exercicio">

</div>

---

## Corolário 5.2 — Número de folhas e grau máximo

Se $T$ é uma árvore com $f$ folhas, então

$$
f\geq\Delta(T).
$$

### Prova

Considere $u\in V$ tal que

$$
d(u)=\Delta(T),
$$

e seja $F$ o conjunto de $f$ folhas de $T$.

Pelo Teorema do Aperto de Mãos, temos

$$
\sum_{v\in V}d(v)
=
f+\Delta+\sum_{v\in V\setminus(F\cup\{u\})}d(v).
$$

Como

$$
d(v)\geq 2,
\qquad
\forall v\in V\setminus(F\cup\{u\}),
$$

temos

$$
\sum_{v\in V}d(v)
\geq
f+\Delta+2(n-f-1).
$$

Logo,

$$
\sum_{v\in V}d(v)
\geq
-f+\Delta+2n-2.
$$

Por outro lado, como $T$ é uma árvore,

$$
m=n-1.
$$

Pelo Teorema do Aperto de Mãos,

$$
\sum_{v\in V}d(v)
=
2m
=
2(n-1)
=
2n-2.
$$

Assim,

$$
2n-2
\geq
-f+\Delta+2n-2.
$$

Portanto,

$$
f\geq\Delta.
$$

$\square$