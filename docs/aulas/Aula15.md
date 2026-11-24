
# Aula 15 — 04/11/2026

## Número de Ramsey

$r(k,\ell)$ é o menor inteiro tal que todo grafo com $r(k,\ell)$ vértices possui uma clique de tamanho $k$ ou um conjunto independente de tamanho $\ell$.

---

## Teorema 15.1

Para $k\geq 2$ e $\ell\geq 2$,

$$
r(k,\ell)\leq r(k,\ell-1)+r(k-1,\ell).
$$

### Prova

Seja $G$ um grafo com

$$
r(k,\ell-1)+r(k-1,\ell)
$$

vértices.

Considere $v\in V$ e distingamos dois possíveis casos:

**I)** $v$ não é adjacente aos vértices de um conjunto $S\subseteq V-\{v\}$, tal que

$$
|S|\geq r(k,\ell-1).
$$

**II)** $v$ é adjacente aos vértices de um conjunto $T\subseteq V-\{v\}$, tal que

$$
|T|\geq r(k-1,\ell).
$$

Vamos demonstrar que I ou II ocorre.

Suponha a negação, ou seja, não ocorre I e não ocorre II.

Tomando

$$
S=N_{\overline{G}}(v)
$$

e

$$
T=N_G(v),
$$

temos

$$
|S|\leq r(k,\ell-1)-1
$$

e

$$
|T|\leq r(k-1,\ell)-1.
$$

O fato de $v$ não ser adjacente aos vértices de $S$ em $G$ significa que $v$ é adjacente aos vértices de $S$ em $\overline{G}$.

Assim,

$$
|N_{\overline{G}}(v)|=|S|.
$$

Logo,

$$
\begin{aligned}
|N_{\overline{G}}(v)|+|N_G(v)|
&\leq r(k,\ell-1)-1+r(k-1,\ell)-1\\
&=r(k,\ell-1)+r(k-1,\ell)-2.
\end{aligned}
$$

Note que

$$
V-\{v\}=N_G(v)\cup N_{\overline{G}}(v)
$$

e

$$
|V-\{v\}|=r(k,\ell-1)+r(k-1,\ell)-1.
$$

Como as duas vizinhanças são disjuntas, temos uma contradição.

Portanto, pelo menos um dos casos I ou II ocorre.

**Caso I.**

$G[S]$ contém uma clique de tamanho $k$ ou um conjunto independente de tamanho $\ell-1$.

Como $v$ não é adjacente aos vértices de $S$, podemos adicionar $v$ ao conjunto independente de tamanho $\ell-1$, caso ele exista.

Logo,

$$
G[S\cup\{v\}]
$$

contém uma clique de tamanho $k$ ou um conjunto independente de tamanho $\ell$.

**Caso II.**

$G[T]$ contém uma clique de tamanho $k-1$ ou um conjunto independente de tamanho $\ell$.

Como $v$ é adjacente a todos os vértices de $T$, podemos adicionar $v$ à clique de tamanho $k-1$, caso ela exista.

Logo,

$$
G[T\cup\{v\}]
$$

contém uma clique de tamanho $k$ ou um conjunto independente de tamanho $\ell$.

Portanto,

$$
r(k,\ell)\leq r(k,\ell-1)+r(k-1,\ell).
$$

$\square$

---

## Teorema 15.2 — Limite superior para os números de Ramsey

$$
r(k,\ell)\leq\binom{k+\ell-2}{k-1}.
$$

### Ideia da prova

Mostre por indução em $k+\ell$.

Verifique que o resultado vale para

$$
k+\ell\leq 5.
$$

Assuma que o resultado vale para todos os valores de $k$ e $\ell$ tais que

$$
5\leq k+\ell<m+n.
$$

Pelo teorema anterior, temos

$$
r(m,n)\leq r(m,n-1)+r(m-1,n).
$$

Pela hipótese de indução,

$$
\begin{aligned}
r(m,n)
&\leq r(m,n-1)+r(m-1,n)\\
&\leq\binom{m+n-3}{m-1}
+\binom{m+n-3}{m-2}\\
&=\binom{m+n-2}{m-1}.
\end{aligned}
$$

A última igualdade segue da Relação de Pascal.

Portanto,

$$
r(k,\ell)\leq\binom{k+\ell-2}{k-1}.
$$

$\square$

---

## Teorema 15.3 — Limite inferior para os números de Ramsey

Para $k\geq 2$,

$$
r(k,k)\geq 2^{\frac{k}{2}}.
$$

### Prova

Como

$$
r(2,2)=2,
$$

o resultado vale para $k=2$.

Tome $k\geq 3$.

Sejam:

- $G_n$: conjunto dos grafos sobre o conjunto de vértices $\{v_1,v_2,\ldots,v_n\}$;
- $G_n^k$: subconjunto de $G_n$ contendo os grafos que possuem uma clique de tamanho $k$.

Note que

$$
|G_n|=2^{\binom{n}{2}}.
$$

Pelo Princípio da Multiplicação, para cada par de vértices, podemos ter ou não uma aresta.

Assim,

$$
2^{\binom{n}{2}}
$$

é o número de grafos sobre um conjunto fixado de $n$ vértices.

O número de grafos de $G_n$ contendo uma clique de tamanho $k$ sobre um conjunto particular de $k$ vértices é

$$
2^{\binom{n}{2}-\binom{k}{2}}.
$$

Isso ocorre porque, dos

$$
\binom{n}{2}
$$

pares de vértices, os

$$
\binom{k}{2}
$$

pares que formam a clique devem ser arestas.

Para os demais

$$
\binom{n}{2}-\binom{k}{2}
$$

pares, podemos escolher se há ou não uma aresta.

Como temos

$$
\binom{n}{k}
$$

subconjuntos distintos com $k$ vértices, temos

$$
|G_n^k|
\leq
\binom{n}{k}
2^{\binom{n}{2}-\binom{k}{2}}.
$$

Dividindo a desigualdade por $|G_n|$, temos

$$
\begin{aligned}
\frac{|G_n^k|}{|G_n|}
&\leq
\frac{
\binom{n}{k}2^{\binom{n}{2}-\binom{k}{2}}
}{
2^{\binom{n}{2}}
}\\
&=\binom{n}{k}2^{-\binom{k}{2}}\\
&=\frac{n!}{(n-k)!k!}2^{-\binom{k}{2}}\\
&\leq\frac{n^k}{k!}2^{-\binom{k}{2}}.
\end{aligned}
$$

Queremos estabelecer que

$$
r(k,k)\geq 2^{\frac{k}{2}}.
$$

Suponha

$$
n\leq 2^{\frac{k}{2}}.
$$

Então,

$$
\begin{aligned}
\frac{|G_n^k|}{|G_n|}
&\leq\frac{n^k}{k!}2^{-\binom{k}{2}}\\
&\leq\frac{(2^{\frac{k}{2}})^k}{k!}
2^{-\binom{k}{2}}\\
&=\frac{2^{\frac{k^2}{2}}}{k!}
2^{-\frac{k(k-1)}{2}}\\
&=\frac{2^{\frac{k}{2}}}{k!}\\
&<\frac{1}{2},
\qquad k\geq 3.
\end{aligned}
$$

Note que menos da metade dos grafos de $G_n$ possui uma clique de tamanho $k$.

Como $G$ e $\overline{G}$ pertencem a $G_n$, e uma clique em $\overline{G}$ corresponde a um conjunto independente em $G$, menos da metade dos grafos de $G_n$ possui um conjunto independente de tamanho $k$.

Logo, existe algum grafo em $G_n$ que não possui clique de tamanho $k$ nem conjunto independente de tamanho $k$.

Assim, para $n\leq 2^{\frac{k}{2}}$, existe um grafo de ordem $n$ que não satisfaz a propriedade que define $r(k,k)$.

Portanto,

$$
r(k,k)\geq 2^{\frac{k}{2}}.
$$

$\square$
