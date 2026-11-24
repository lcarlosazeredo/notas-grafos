
# Aula 14 — 21/10/2026

## Teorema 13.2 — König (Continuação)

Se $G$ é um grafo bipartido, então

$$
\chi'(G)=\Delta(G).
$$

### Prova (Continuação)

Já sabemos que

$$
\chi'(G)\geq\Delta(G)
$$

Resta provar que

$$
\chi'(G)\leq\Delta(G)
$$

Seja

$$
G'=G-uv
$$

Temos:

- $\Delta(G')\leq\Delta(G)$;
- $d_{G'}(u)=d_G(u)-1\leq\Delta(G)-1$;
- analogamente para $v$.

Considere o conjunto de cores

$$
C=\{1,2,\ldots,\Delta(G)\}
$$

Escolha uma cor $\alpha$ livre em $u$ e uma cor $\beta$ livre em $v$.

Se alguma cor estiver livre simultaneamente em $u$ e em $v$, atribua-a à aresta $uv$.

Suponha, então, que

$$
\alpha\neq\beta.
$$

Assim, a cor $\beta$ aparece em alguma aresta incidente a $u$, e a cor $\alpha$ aparece em alguma aresta incidente a $v$.

Como a coloração de $G'$ é própria, cada cor aparece no máximo uma vez nas arestas incidentes a um dado vértice.

Logo, há exatamente uma aresta de cor $\beta$ incidente a $u$ e uma aresta de cor $\alpha$ incidente a $v$.

Seja $H$ o subgrafo gerador de $G'$ que contém exatamente as arestas coloridas por $\alpha$ ou $\beta$.

Temos

$$
V(H)=V(G)
$$

e

$$
E(H)=\{e\in E(G'):c(e)\in\{\alpha,\beta\}\}\subseteq E(G').
$$

Como em cada vértice há, no máximo, uma aresta de cor $\alpha$ e, no máximo, uma aresta de cor $\beta$, temos

$$
d_H(x)\leq 2,
\qquad \forall x\in V(H).
$$

A cor $\alpha$ está livre em $u$. Assim,

$$
d_H(u)=1.
$$

A componente de $H$ que contém $u$ não pode ser um ciclo nem um vértice isolado.

Logo, ela é um caminho $P$ que possui $u$ como uma de suas extremidades.

Sua primeira aresta, ao sair de $u$, tem a cor $\beta$.

Queremos provar que

$$
v\notin V(P)
$$

por contradição.

Note que

$$
d_H(v)=1.
$$

Assim, se $v$ pertencesse a $P$, ele teria de ser a outra extremidade de $P$.

Percorrendo $P$ de $u$ até $v$, teríamos a sequência de cores

$$
\underbrace{\beta,\alpha,\beta,\alpha,\ldots,\beta,\alpha}_{\text{número par de arestas}}
$$

Mas $uv$ é uma aresta de $G$.

Como $G$ é bipartido, $u$ e $v$ pertencem a partições diferentes.

Note que todo caminho de $u$ para $v$ deve ter comprimento ímpar.

Logo,

$$
v\notin V(P).
$$

### <span class="prova-exercicio">Continuação da prova (Exercício)</span>

<div class="prova-exercicio">

</div>

---

## Teorema 14.1 — Ramsey

Para todo par de inteiros positivos $k$ e $\ell$, existe um menor inteiro

$$
r(k,\ell)
$$

tal que todo grafo com $r(k,\ell)$ vértices possui:

- uma clique de tamanho $k$; ou
- um conjunto independente de tamanho $\ell$.

O número $r(k,\ell)$ é chamado de **número de Ramsey**.

---

## Exemplo — Número de Ramsey $r(3,3)$

Qual é o número mínimo de pessoas em uma festa de modo que existam:

- três pessoas que se conhecem mutuamente; ou
- três pessoas que não se conhecem mutuamente?

Em termos de grafos, queremos determinar

$$
r(3,3).
$$

Nas figuras apresentadas em aula, são considerados os ciclos $C_5$ e $C_6$.

O ciclo $C_5$ não possui triângulos nem conjuntos independentes de tamanho $3$.

Portanto,

$$
r(3,3)>5.
$$

De fato,

$$
r(3,3)=6.
$$

### Prova

Considere um grafo $G$ com $6$ vértices.

Vamos mostrar que $G$ possui uma clique de tamanho $3$ ou um conjunto independente de tamanho $3$.

#### Caso 1 — Grafos desconexos

Há, ao menos, um vértice em cada componente conexa que podemos escolher para formar um conjunto independente.

Se houver pelo menos três componentes conexas, então temos o que queremos.

Se houver duas componentes conexas, então uma das componentes possui pelo menos três vértices.

Dentre esses vértices, ou três formam uma clique, ou existem dois vértices não vizinhos.

Nesse último caso, escolhendo também um vértice da outra componente, obtemos um conjunto independente de tamanho $3$.

#### Caso 2 — Grafos conexos

Se há uma clique de tamanho $3$, temos o que queremos.

Se não houver, então o tamanho da maior clique é $2$.

Tome um vértice $u$.

Se $u$ for vizinho de pelo menos três vértices, então três desses vértices formam um conjunto independente.

Se não houver vértice de grau pelo menos $3$, então todo vértice tem grau $1$ ou $2$.

Como $G$ é conexo, então

$$
G\cong C_6
$$

ou

$$
G\cong P_6.
$$

Em cada caso, há um conjunto independente de tamanho $3$.

Assim,

$$
r(3,3)=6.
$$

$\square$

---

## Alguns Números de Ramsey

| $r(k,\ell)$ | 1 | 2 | 3 | 4 | 5 | 6 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **1** | 1 | 1 | 1 | 1 | 1 | 1 |
| **2** | 1 | 2 | 3 | 4 | 5 | 6 |
| **3** | 1 | 3 | 6 | 9 | 14 | 18 |
| **4** | 1 | 4 | 9 | 18 | 25 | ? |
| **5** | 1 | 5 | 14 | 25 | ? | ? |
| **6** | 1 | 6 | 18 | ? | ? | ? |

**Casos particulares:**

$$
r(2,k)
$$

e

$$
r(k,2).
$$

---

## Propriedades dos Números de Ramsey

### Simetria

$$
r(k,\ell)=r(\ell,k)
$$

Todo grafo $G$ com $r(k,\ell)$ vértices possui uma clique de tamanho $k$ ou um conjunto independente de tamanho $\ell$.

Assim, seu complementar $\overline{G}$ possui um conjunto independente de tamanho $k$ ou uma clique de tamanho $\ell$.

---

### Monotonicidade

$$
r(k+1,\ell)\geq r(k,\ell)
$$

---

### Limite inferior

$$
r(k,\ell)\geq\min\{k,\ell\}
$$
