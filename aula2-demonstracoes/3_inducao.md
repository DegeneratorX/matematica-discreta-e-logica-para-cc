- Princípio da Indução Matemática
    - É a principal ferramenta pra demonstrar sentenças da forma (∀n ∈ ℕ)P(n).

    - Axioma: Seja P(n) uma sentença aberta sobre ℕ. Suponha que:

        - P(0) é verdade, e
        - Sempre que P(k) é verdade, para algum k ∈ ℕ, temos que P(k + 1) é verdade.
        - Então, P(n) é verdade ∀n ∈ ℕ.

    - Para demonstrar uma afirmação (∀n ∈ ℕ)P(n) usando o princípio da indução matemática, podemos então seguir este roteiro:
        
        - Base da Indução: PRovar que P(0) é verdade.
        - Hipótese de Indução: Supor que para algum k ∈ ℕ, P(k) é verdade.
        - Passo de Indução: Provar que P(k + 1) é verdade.


    - Teorema: Provar que para todo n ≥ 0, vale 1 + 3 + 5 + ... + (2n + 1) = (n + 1)²

    - Prova:
        - Base: P(0) é verdade, pois a expressão acima é trivialmente válida para n = 0.

        - Hip. de ind.: suponhamos que para algum k, P(k) é verdade, isto é, 1 + 3 + 5 + ... + (2k + 1) = (k +1)²

        - Passo de indução: temos que provar que P(k + 1) é verdade, isto é, temos que provar que 1 + 3 + 5 + ... + (2k + 1) + (2(k + 1) + 1) == ((k + 1) + 1)². P

        - Pela hipótese de indução, temos (1 + 3 + 5 + ... + (2k + 1)) + (2(k + 1) + 1) = ((k + 1)²) + (2(k + 1) + 1)

        - Por simples cálculos, verificamos que o lado direito é igual a ((k + 1) + 1)²

        - Isto mostra que P(k + 1) é verdade, toda vez que P(k) é verdade. Portanto, por indução, a fóruma é válida para todo número natural n.