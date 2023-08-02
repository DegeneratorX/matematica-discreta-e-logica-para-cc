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

Também chamada de Indução Completa, é uma alternativa da indução, e serve para demonstrar sentenças da forma $(\forall n \in \mathbb{N})P(n)$, e alguns casos essa técnica torna a demonstração da sentença mais fácil que a técnica padrão.

## Como fazer

- Base da Indução: Primeiro, você prova que a afirmação é verdadeira para o menor valor inteiro positivo (geralmente, o número 1). Essa etapa é semelhante à base da indução normal.

- Hipótese de Indução Forte: Em vez de assumir apenas que a afirmação é verdadeira para um valor arbitrário k e, em seguida, provar para k + 1, na indução forte, você assume que a afirmação é verdadeira para todos os valores de 1 até k. Em outras palavras, a hipótese de indução forte é mais forte, pois assume que a afirmação é verdadeira para todos os valores menores ou iguais a k.

Em seguida, usando a hipótese de indução forte, você demonstra que a afirmação é verdadeira para k + 1.

### Teorema: Para todo $ n \geq 1$, a sequência de Fibonacci satisfaz $F_n \geq 2^n$.

### Prova:

A sequência de Fibonacci é definida como: $F_0 = 0, F_1 = 1$, e $F_n = F_{n-1} + F_{n-2}$ para $n \geq 2$.

**Base da Indução:** Vamos verificar a afirmação para $n = 1$:
$F_1 = 1 \geq 2^1 = 2$
A base da indução é verdadeira.

**Hipótese de Indução Forte:** Suponhamos que a afirmação é verdadeira para todos os valores de $k$, onde $1 \leq k \leq n$, ou seja, $F_k \geq 2^k$.

**Passo Indutivo:** Precisamos mostrar que a afirmação é verdadeira para $n+1$. Usando a definição da sequência de Fibonacci, temos:
$$F_{n+1} = F_n + F_{n-1}$$

Pela hipótese de indução forte, sabemos que $F_n \geq 2^n$ e $F_{n-1} \geq 2^{n-1}$. Portanto:
$$F_{n+1} = F_n + F_{n-1} \geq 2^n + 2^{n-1}$$

Podemos simplificar $2^n + 2^{n-1}$:
$$2^n + 2^{n-1} = 2^n + \frac{2^n}{2} = 2^n + 2^n = 2 \cdot 2^n = 2^{n+1}$$

Assim, concluímos que $F_{n+1} \geq 2^{n+1}$.

Portanto, a afirmação é verdadeira para $n+1$.