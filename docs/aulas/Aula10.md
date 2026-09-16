# Aula 10 — 16/09/2026

## Teorema 9.3 — Condição necessária para Hamiltonicidade

Se $G$ é hamiltoniano e $S$ é qualquer subconjunto próprio não vazio de vértices, então $G-S$ tem, no máximo,

$$
|S|
$$

componentes conexas.

### Prova

Sejam $C$ um ciclo hamiltoniano e $S$ um subconjunto próprio não vazio de $V(G)$.

Então, o número de componentes conexas em $G-S$ é, no máximo,

$$
|S|.
$$

Pois $C-S$ é a união de, no máximo, $|S|$ caminhos disjuntos.

Como $G-S$ e $C-S$ têm o mesmo conjunto de vértices e $G-S$ tem possivelmente mais arestas que $C-S$, então $G-S$ tem, no máximo,

$$
|S|
$$

componentes conexas.

$\square$

**Exemplo.**

Considere

$$
S=\{v_2,v_4,v_6\}.
$$

Como $C$ é um ciclo hamiltoniano,

$$
|V(G)|=|V(C)|
$$

e

$$
|E(G)|\geq |E(C)|.
$$

---

## Teorema 10.1 — Teorema de Dirac

Se $G$ é um grafo com pelo menos $3$ vértices e

$$
\delta(G)\geq\frac{n}{2},
$$

então $G$ é hamiltoniano.

### Prova

Suponha que $G$ satisfaça

$$
n\geq 3
$$

e

$$
\delta(G)\geq\frac{n}{2}
$$

Considere

$$
P=v_1,v_2,\ldots,v_k
$$

um maior caminho em $G$.

Note que

$$
N(v_1)\cup N(v_k)\subseteq V(P),
$$

pois, caso contrário, teríamos um caminho maior que $P$, iniciando por algum

$$
v\in N(v_1)\cup N(v_k)
$$

Chame

$$
u=v_1
\qquad\text{e}\qquad
w=v_k
$$

### Caso 1 — $u$ e $w$ são vizinhos

Se $u$ e $w$ são vizinhos, então já temos um ciclo contendo todos os vértices de $P$.

### Caso 2 — $u$ e $w$ não são vizinhos

Queremos encontrar um índice $j$ tal que

$$
uv_{j+1}\in E
$$

e

$$
wv_j\in E
$$

Vamos mostrar que tal índice existe.

Defina

$$
S=\{i\mid uv_{i+1}\in E\}
$$

e

$$
T=\{i\mid wv_i\in E\}
$$

Pelo Princípio da Inclusão-Exclusão,

$$
|S\cup T|
=
|S|+|T|-|S\cap T|
$$

Equivalentemente,

$$
|S\cup T|+|S\cap T|
=
|S|+|T|
$$

Como

$$
|S|=d(u)
$$

e

$$
|T|=d(w),
$$

temos

$$
|S\cup T|+|S\cap T|
=
d(u)+d(w)
$$

Pela hipótese do Teorema de Dirac,

$$
d(u)+d(w)
\geq
\frac{n}{2}+\frac{n}{2}
=
n
$$

Note que

$$
|S\cup T|<n
$$

Logo,

$$
|S\cap T|\geq 1
$$

Assim, existe $j$ tal que

$$
wv_j\in E
$$

e

$$
uv_{j+1}\in E
$$

Portanto, podemos formar o ciclo

$$
C=
v_1v_{j+1}\ldots v_{k-1}v_kv_j\ldots v_3v_2v_1
$$

Vamos mostrar que $C$ contém todos os vértices de $G$.

Suponha que $C$ não contenha todos os vértices de $G$.

Como $G$ é conexo, tome um vértice

$$
z\notin V(C)
$$

que seja vizinho de algum vértice

$$
v_l\in V(C).
$$

Então, utilizando a aresta $zv_l$ e percorrendo $C$ a partir de $v_l$, obtemos um caminho em $G$ maior que $P$.

Isso contradiz a escolha de $P$ como um maior caminho.

Logo, $C$ contém todos os vértices de $G$.

Portanto, $C$ é um ciclo hamiltoniano e $G$ é hamiltoniano.

$\square$
