# Aula 13 — 19/10/2026

## Coloração de Arestas

Uma **$k$-coloração de arestas** de um grafo $G$ é uma atribuição de cores às arestas de $G$.

Uma $k$-coloração é **própria** se arestas adjacentes recebem cores diferentes.

O **índice cromático**, denotado por

$$
\chi'(G),
$$

é o menor $k$ tal que $G$ admite uma $k$-coloração própria.

**Exemplo:**

Considere o caminho $P_5$.

Podemos obter:

- $1,2,3,1$ — $3$-coloração própria;
- $1,1,2,3$ — $3$-coloração;
- $1,2,3,4$ — $4$-coloração própria;
- $1,2,1,2$ — $2$-coloração própria.

Portanto,

$$
\chi'(P_5)=2.
$$

---

## Definição 13.1 — $k$-coloração como partição

Uma $k$-coloração é uma partição

$$
(E_1,E_2,\ldots,E_k)
$$

de $E$, onde $E_i$ é o conjunto de arestas de cor $i$.

Uma $k$-coloração própria particiona $E$ em emparelhamentos, onde cada cor $i$ define um emparelhamento.

**Exemplo:**
Considere o grafo,

![Exemplo de grafo](../assets/aula13_img1.svg)

Com $n=5$ e $m=7.$

$G$ não admite uma $3$-coloração própria.

Assim,

$$
3\leq\chi'(G)\leq7
$$

Além disso,

$$
\alpha'(G)=\left\lfloor\frac{n}{2}\right\rfloor=2
$$

---

## Teorema 13.1 — Vizing

Para todo grafo $G$, temos que

$$
\Delta(G)\leq\chi'(G)\leq\Delta(G)+1.
$$

Se

$$
\chi'(G)=\Delta(G),
$$

então $G$ é dito **classe 1**.

Se

$$
\chi'(G)=\Delta(G)+1,
$$

então $G$ é dito **classe 2**.

---

## Teorema 13.2 — König

Se $G$ é bipartido, então

$$
\chi'(G)=\Delta(G)
$$

### Prova

Temos

$$
\Delta(G)\leq\chi'(G)
$$

Segue do Teorema de Vizing.

Vamos provar

$$
\chi'(G)\leq\Delta(G)
$$

por indução em $m$.

**Base:** Se $m=0$, não há arestas para colorir; nenhuma cor será usada e

$$
\Delta(G)=0.
$$

Suponha que para todo grafo com menos de $m$ arestas possa ser colorido propriamente com, no máximo, seu grau de cor.

Vamos provar para um grafo bipartido com $m\geq1$ arestas.

Escolha uma aresta

$$
uv\in E(G)
$$

e considere

$$
G'=G-uv.
$$

O grafo $G'$ permanece bipartido.

Além disso,

$$
|E(G')|=m-1.
$$

Pela hipótese de indução, $G'$ admite uma coloração própria que usa no máximo

$$
\Delta(G')
$$

cores.

Como a remoção de arestas não aumenta o grau,

$$
\Delta(G')\leq\Delta(G).
$$

Assim, podemos considerar essa coloração como uma coloração cujas cores pertencem a

$$
C=\{1,2,\ldots,\Delta(G)\}.
$$

As cores de $C$ que não aparecem em $G'$ simplesmente ficam sem uso.

Uma cor está **livre em $x$** quando nenhuma aresta incidente a $x$ possui esta cor.

No grafo $G'$, o vértice $u$ tem

$$
d_{G'}(u)=d_G(u)-1
$$

arestas incidentes; todas têm cores diferentes.

Como

$$
d_G(u)-1\leq\Delta(G)-1,
$$

no máximo

$$
\Delta(G)-1
$$

cores de $C$ aparecem em $u$.

Assim, há pelo menos uma cor de $C$ que está livre em $u$.

O mesmo vale para $v$.

**Término da prova na próxima aula — 21/10/2026.**
