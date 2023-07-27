- Método direto (p → q)

    - Supomos que a hipótese p é verdadeira, e usamos uma sequência de proposições que são consequências lógicas das anteriores, até obter a tese q. Esta sequẽncia de passos prova a implicação p → q.

    - Teorema: Se m e n são inteiros pares, então m + n é par.

    - Prova:
        - Suponha que m é par (hipótese)
        - Suponha que n é par (hipótese)
        - Existe um inteiro r tal que m = 2r (Definição de par)
        - Existe um inteiro s tal que n = 2s (Definição de par)
        - m + n = 2r + 2s = 2(r + s)
        - Seja t = r + s (introdução de viariável)
        - Existe um inteiro t tal que m + n = 2t
        - Portanto, m + n é par, por definição de par.

    - Prova abreviada:
        - Suponha que m e n são inteiros pares. Por definição de número "par", existem inteiros r e s tais que m = 2r e n = 2s. Logo, m + n = 2r + 2s = 2(r + s). Como r + s é inteiro, concluímos que o inteiro m + n é par, pela definição. Isto prova que, se m e n são pares, m + n é par.

    - Prova super abreviada:
        - m, n pares → m = 2r, n = 2s para r e s inteiros. Isso implica m + n = 2(r + s). Logo, m + n é par, pois r + s é inteiro.

    - Conclusão: uso implícito de modus ponens (se p e p → q são verdadeiros, então q é verdadeiro).  


- Método da Contrapositiva

    - Para provar a afirmação p → q, supomos que a negação da tese ¬q é verdadeira, e procuramos uma sequência de deduções lógicas que termina com a negação da hipótese ¬p. Esta sequência de passos prova que (¬q) → (¬p), afinal isso é equivalente a p → q, que também está provada.

    - Teorema: Se n² é um inteiro par, então n é par

    - Prova: Suponha que n é ímpar. Pela definição de ímpar, existe um inteiro k tal que n = 2k + 1. Portanto, n² = (2k + 1)² = 4k² + 4k + 1 = 2(2k² + 2k) + 1. Como 2k² + 2k é um inteiro, pela definição de ímpar, concluimos que n² é ímpar. Pela contrapositiva, se n² é um inteiro par, então n é um inteiro par.


- Método da Redução ao Absurdo (Contradição ou Prova Indireta)

    - Baseia-se na equivalência lógica entre p → q e a fórmula (p ∧ ¬q) → F, e, portanto, a afirmação equivale a p → q.

    - Teorema: Se m e n são inteiros pares, então m + n é um inteiro par.

    - Prova: Suponha que m e n são inteiros pares e m + n é um inteiro ímpar. Vamos mostrar que estas suposições levam a uma contradição. Pela def de par, existem r e s inteiros tais que m = 2r e n = 2s. Pela def de ímpar, existe um inteiro j tal que m + n = 2j + 1. Logo, 2r + 2s = 2j + 1, ou seja, r + s - j = 1/2. Isto é um absurdo (falso), pois r + s - j é um inteiro. Portanto, se m e n são intieors pares, então m + n é um inteiro par.


- Generalização Universal
    
    - Se o objetivo é provar uma afirmação do tipo ∀xP(x), podemos começar supondo que x é um elemento de D escolhido arbitrariamente, e omitir o quantificador no restante da prova. Se, com essa suposição, conseguirmos provar a afirmação P(x), podemos concluir que o teorema original (com o quantificador) é verdadeiro. Esse último passo é chamado de generalização universal.

    - Teorema: Para quaisquer números reais x e y, (x + y)² - (x - y)² = 4xy

    - Prova: Sejam x e y dois números reais quaisquer. Pelo teorema do binômio, temos (x + y)² = x² + 2xy + y², e (x - y)² = x² - 2xy + y². Portanto, (x + y)² - (x - y)² = (x² + 2xy + y²) - (x² - 2xy + y²) = 4xy.


- Demonstração por Vacuidade

    - Se E é o conjunto vazio, a afirmação ∀x pertencente a E, Q(x) é verdadeira, qualquer que seja o predicado Q.

    - Teorema: Todos os pares primos maiores que dois são quadrados perfeitos.

    - Prova: Essa afirmação é verdadeira por vacuidade, pois não existem primos pares maiores que dois.


- Demonstração por Contra-Exemplo

    - Se o elemento x de D comprovadamente não satisfaz P(x), mostra falsidade da conjetura, e portanto, é um conra-exemplo.

    - Teorema: Para todo primo n, o inteiro (2 elevado a n) - 1 é primo.

    - Prova: Esta afirmação é falsa, basta ver que o número n = 11 é um contra-exemplo, pois P(11) = (2 elevado a 11) - 1 = 2047 = 23 x 89.