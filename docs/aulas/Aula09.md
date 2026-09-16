# Aula 09 — 14/09/2026

## Grafos Eulerianos

## Definição 9.1 — Ciclo de Euler

Um **ciclo de Euler** é um passeio fechado que visita cada aresta do grafo exatamente uma vez.

---

## Teorema 9.1 — Caracterização dos grafos eulerianos

Um grafo conexo não trivial é euleriano se, e somente se, o grau de cada um de seus vértices é par.

### Prova

$(\Rightarrow)$ Suponha que $G$ seja um grafo conexo não trivial e euleriano.

Seja $C$ um passeio de Euler com início e fim no vértice $u$.

Cada vez que um vértice $v$ aparece no passeio $C$, duas arestas incidentes a $v$ são contadas.

Como um passeio euleriano passa por cada aresta exatamente uma vez, para todo

$$
v\neq u,
$$

temos que

$$
d(v)
$$

é par.

Similarmente,

$$
d(u)
$$

é par, pois $C$ começa e termina em $u$.

Logo, todo vértice de $G$ possui grau par.

$(\Leftarrow)$ Suponha que $G$ seja um grafo conexo não trivial em que todo vértice possui grau par.

Vamos construir um passeio de Euler em duas etapas.

**Passo 1:** Decompor as arestas de $G$ em ciclos.

**Passo 2:** Compor o passeio de Euler a partir dos ciclos obtidos no Passo 1.

No Passo 1, começamos identificando um ciclo

$$
C^1
$$

no grafo.

Esse ciclo existe porque todos os vértices possuem grau par.

Podemos então repetir a operação em relação a uma componente não trivial deste grafo.

Assim, obtemos a decomposição.

No Passo 2, começando por $C^1$, compomos $C^1$ com um ciclo $C^j$ que tenha um vértice em comum com $C^1$.

O ciclo $C^j$ existe porque o grafo é conexo.

A composição é realizada enquanto houver ciclos do Passo 1 que ainda não pertençam a esta etapa.

Tomando, portanto, vértice $a$ e $v$ em $C^1$, tal que $v$ também pertença a $C^j$, percorremos $C^1$ até $a$, percorremos todo o ciclo $C^j$ e retornamos a $a$, continuando então o percurso de $C^1$.

Note que este é um passeio de Euler associado a $C^1$ e $C^j$.

Caso exista outro ciclo

$$
C^k,
$$

fazemos o mesmo procedimento, compondo $C^k$ ao $C^1C^j$.

Repetindo o procedimento até que todos os ciclos da decomposição tenham sido incorporados, obtemos um passeio fechado que utiliza cada aresta de $G$ exatamente uma vez.

Logo, $G$ é euleriano.

$\square$

---

## Grafos Hamiltonianos

## Definição 9.2 — Ciclo de Hamilton

Um **ciclo de Hamilton** é um ciclo gerador para o grafo.

---

## Definição 9.3 — Grafo hamiltoniano

Um grafo que admite um ciclo de Hamilton é dito **hamiltoniano**.

---

## Teorema 9.2

Todo grafo hamiltoniano é 2-conexo.

### Prova

Considere $G$ hamiltoniano e seja $C$ um ciclo hamiltoniano de $G$.

Como a remoção de qualquer vértice de $C$ não desconecta $C$, então não desconecta $G$.

Logo, $G$ não possui vértice de articulação e, portanto, é 2-conexo.

$\square$

---

## Teorema 9.3 — Condição necessária para Hamiltonicidade

Se $G$ é hamiltoniano e

$$
S\subset V(G)
$$

é qualquer subconjunto próprio não vazio de vértices, então

$$
W(G-S)\leq |S|
$$

Ou seja, $G-S$ possui, no máximo,

$$
|S|
$$

componentes conexas.

### <span class="prova-exercicio">Prova (Próxima aula)</span>

<div class="prova-exercicio">

</div>