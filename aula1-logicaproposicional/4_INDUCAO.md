# Método (ou princípio) da Indução Matemática

O princípio da indução matemática é a principal ferramenta para demonstrar sentenças da forma

$$\boxed{\Large(\forall n \in \mathbb{N})P(n)}$$

Ou seja, demonstrar que uma afirmação vale para todo número $n$ nos conjuntos dos naturais.

## Como fazer

Separamos em etapas:

- Base da Indução: Provar que $P(0)$ é verdade.
- Hipótese de Indução: Supor que para algum $k \in \mathbb{N}$, $P(k)$ é verdade.
- Passo da Indução: Provar que $P(k + 1)$ é verdade.

### Teorema: Para todo $n \ge 0$, é verdade que $1 + 3 + 5 +...+ (2n + 1) = (n+1)$.

### Prova:

- Base: $P(0)$ é verdade, pois a expressão acima é trivialmente válida para $n = 0$.

- Hipótese de indução: Suponhamos que para algum $k$, $P(k)$ é verdade, isto é,
$$1 + 3 + 5 + \ldots + (2k + 1) = (k + 1)^2$$

- Passo de indução: Temos de provar que $P(k + 1)$ é verdade, isto é, temos que provar
que:
$$1 + 3 + 5 + \ldots + (2k + 1) + (2(k + 1) + 1) = ((k + 1) + 1)^2$$

Pela hipótese de indução, temos
$$\left[1 + 3 + 5 + \ldots + (2k + 1)\right] + (2(k + 1) + 1) = \left[(k + 1)^2\right] + (2(k + 1) + 1)$$

Por simples cálculos, verificamos que o lado direito é igual a
$$((k + 1) + 1)^2$$

Isto mostra que $P(k + 1)$ é verdade, toda vez que $P(k)$ é verdade. Portanto, por indução,
a fórmula é válida para todo número natural $n$.

# Indução Forte