# Prova

A necessidade de provar matematicamente as coisas decorre da busca pela validade, confiabilidade e fundamentação do conhecimento matemático. 

As provas matemáticas garantem a precisão das afirmações, permitem verificação de resultados, eliminam suposições, possibilitam a descoberta de novos resultados e estruturam o raciocínio lógico.

Existem alguns tipos de afirmações na matemática que se usa para chegar a resultados maiores. São eles:

- Definição
- Axioma ou Postulado
- Teorema
- Lema
- Corolário
- Lei
- Conjetura

## Definição

Uma definição é uma afirmação precisa e clara que atribui um significado específico a um conceito, termo ou objeto matemático. 

Ela estabelece o sentido de um termo dentro de um contexto matemático, permitindo que seja utilizado de forma consistente em toda a área de estudo.

Ou seja, é algo estabelecido por uma pessoa, sem necessidade de provar. Normalmente é o ponto inicial.

## Axioma ou Postulado

Um axioma ou postulado é uma proposição fundamental e autoevidente, considerada verdadeira sem a necessidade de prova. 

Eles servem como bases iniciais sobre as quais se constrói um sistema matemático, formando os princípios básicos aceitos como verdadeiros e indiscutíveis em uma teoria.

É basicamente um fato não questionado, mas uma regra inquebrável para formular um teorema mais pra frente.

## Teorema

Um teorema é uma afirmação matemática que é comprovadamente verdadeira a partir de provas lógicas e dedutivas, baseadas em axiomas, definições e teoremas previamente estabelecidos.

Os teoremas são resultados fundamentais da matemática e têm implicações importantes para diversas áreas do conhecimento.

Resumindo, é uma afirmação previamente demonstrada.

## Lema

Um lema é um teorema auxiliar, geralmente utilizado como um passo intermediário na prova de um teorema mais significativo. 

Apesar de ser importante e interessante, o lema é usado principalmente como uma ferramenta para estabelecer resultados mais abrangentes.

Portanto, um lema é um teorema necessário para ajudar a estabelecer outro teorema.

## Corolário

Um corolário é uma proposição que é uma consequência direta de um teorema previamente demonstrado. Ele se segue imediatamente do teorema sem necessidade de novas provas, pois é uma extensão lógica do resultado principal.

Concisamente, o colorário é um teorema que é consequência de um teorema anterior.

## Lei

Uma lei matemática refere-se a uma relação regular ou princípio que descreve padrões ou comportamentos observados em fenômenos matemáticos. 

Essas "leis" são frequentemente usadas para descrever comportamentos consistentes em certos contextos, como as leis dos expoentes ou as leis da álgebra.

Basicamente leis são regras universais irrefutáveis aplicada para um sistema onde a lei descreve.

## Conjetura

Uma conjetura é uma afirmação ou suposição que se acredita ser verdadeira, mas ainda não foi comprovada ou refutada por meio de uma prova matemática sólida. 

Conjeturas são frequentemente propostas com base em evidências ou padrões observados, mas exigem uma demonstração formal para serem consideradas verdadeiras.

Um exemplo famoso foi a conjetura de Fermat, que afirmava que não existem números inteiros positivos $x$, $y$ e $z$ que satisfaçam a equação $x^n + y^n = z^n$, onde $n$ é um inteiro maior que 2. Esta conjetura ficou famosa devido a uma margem proposital na obra do matemático Pierre de Fermat (ele não provou propositalmente e deixou para futuros matemáticos provarem), mas foi finalmente provada em 1994 por Andrew Wiles, se transformando assim no teorema de Fermat.

Outro exemplo, dessa vez em teoria dos grafos, é a conjetura de Four Color (Conjetura das Quatro Cores). Ela afirma que é possível colorir qualquer mapa planar usando apenas quatro cores de forma que nenhum par de regiões adjacentes tenha a mesma cor. Essa conjetura foi amplamente estudada e, em 1976, foi finalmente provada verdadeira por meio de computação assistida.

# Tipos de provas

Existem várias formas de provar afirmações matemáticas e teoremas, e todas elas utilizam as proposições e notações de forma implícita.

Os teoremas podem possuir muitas demonstrações diferentes. Qual a melhor é, até certo ponto, uma questão de gosto, e depende para quem a demonstração é dirigida. Em geral, quanto mais curta a prova, melhor; mas há outros critérios, como a facilidade de compreensão, a simplicidade dos passos, etc.. De modo geral, quando não sabemos se uma afirmação é verdadeira, nossa primeira preocupação é encontrar uma demonstração que nos convença. Para convencer outras pessoas, entretanto, devemos cuidar para que a demonstração seja, além de correta, também simples, clara e objetiva.

## Método direto

Supomos que a hipótese $p$ é verdadeira, e usamos uma sequência de proposições que são consequências lógicas das anteriores, até obter a tese $q$. Esta sequência de passos prova a implicação $p \rightarrow q$.

### Teorema: Se $m$ e $n$ são inteiros pares, então $m + n$ é par.

### Prova

- Suponha que $m$ é par (hipótese)
- Suponha que $n$ é par (hipótese)
- Existe um inteiro $r$ tal que $m = 2r$ (Definição de par)
- Existe um inteiro $s$ tal que $n = 2s$ (Definição de par)
- $m + n = 2r + 2s = 2(r + s)$
- Seja $t = r + s$ (introdução de variável)
- Existe um inteiro $t$ tal que $m + n = 2t$
- Portanto, $m + n$ é par, por definição de par.

### Prova abreviada

- Suponha que $m$ e $n$ são inteiros pares. Por definição de número "par", existem inteiros $r$ e $s$ tais que $m = 2r$ e $n = 2s$. Logo, $m + n = 2r + 2s = 2(r + s)$. Como $r + s$ é inteiro, concluímos que o inteiro $m + n$ é par, pela definição. Isto prova que, se $m$ e $n$ são pares, $m + n$ é par.

### Prova super abreviada

- $m, n$ pares $\rightarrow m = 2r, n = 2s$ para $r$ e $s$ inteiros. Isso implica $m + n = 2(r + s)$. Logo, $m + n$ é par, pois $r + s$ é inteiro.


>Nota: observe que existe o uso implícito de modus ponens (se $p$ e $p \rightarrow q$ são verdadeiros, então $q$ é verdadeiro).

## Método da Contrapositiva

Para provar a afirmação $p \rightarrow q$, supomos que a negação da tese $\neg q$ é verdadeira, e procuramos uma sequência de deduções lógicas que termina com a negação da hipótese $\neg p$. Esta sequência de passos prova que $(\neg q) \rightarrow (\neg p)$, afinal isso é equivalente a $p \rightarrow q$, que também está provada.

### Teorema: Se $n^2$ é um inteiro par, então $n$ é par.

### Prova

- Suponha que $n$ é ímpar. Pela definição de ímpar, existe um inteiro $k$ tal que $n = 2k + 1$. Portanto, $n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$. Como $2k^2 + 2k$ é um inteiro, pela definição de ímpar, concluímos que $n^2$ é ímpar. Pela contrapositiva, se $n^2$ é um inteiro par, então $n$ é um inteiro par.

>Nota: observe que existe o uso implícito da equivalência lógica de contrapositiva $(p \rightarrow q) \Leftrightarrow (\neg q \rightarrow \neg p)$.

## Método da Redução ao Absurdo (Contradição ou Prova Indireta)

Baseia-se na equivalência lógica entre $p \rightarrow q$ e a fórmula $(p \land \neg q) \rightarrow F$, e, portanto, a afirmação equivale a $p \rightarrow q$.

### Teorema: Se $m$ e $n$ são inteiros pares, então $m + n$ é um inteiro par.

### Prova

- Suponha que $m$ e $n$ são inteiros pares e $m + n$ é um inteiro ímpar. Vamos mostrar que estas suposições levam a uma contradição. Pela definição de par, existem $r$ e $s$ inteiros tais que $m = 2r$ e $n = 2s$. Pela definição de ímpar, existe um inteiro $j$ tal que $m + n = 2j + 1$. Logo, $2r + 2s = 2j + 1$, ou seja, $r + s - j = \frac{1}{2}$. Isto é um absurdo (falso), pois $r + s - j$ é um inteiro. Portanto, se $m$ e $n$ são inteiros pares, então $m + n$ é um inteiro par.

>Nota: observe que existe o uso implícito da equivalência lógica de absurdo $(p \rightarrow q) \Leftrightarrow (p \land \neg q) \rightarrow \text{ Falso}$

## Método da Implicação com Tese Conjuntiva

Para provar uma conjunção de duas afirmações $p \land q$, basta provar cada uma das afirmações separadamente.

Em particular, para provar uma implicação da forma $p \rightarrow (q \land r)$, podemos observar que ela equivale logicamente à afirmação “$(p \rightarrow q) \land (p \rightarrow r)$”. Portanto, basta provar cada uma destas duas implicacões separadamente. Se usarmos o método direto para provar cada implicação, supomos que $p$ é verdadeira; provamos então $q$; e provamos em seguida $r$.


### Teorema: Se 6 divide um inteiro $n$, então 2 divide $n$ e 3 divide $n$.

### Prova:

Se 6 divide $n$ então existe um inteiro $k$ tal que $n = 6k$. Então, $n = 2(3k)$, logo 2 divide $n$.
Temos também que $n = 3(2k)$, logo 3 divide $n$. Portanto 2 divide $n$ e 3 divide $n$.

## Método da Implicação com Hipótese Disjuntiva

Para provar uma implicação da forma $(p \lor q) \rightarrow r$, podemos observar que ela equivale logicamente à afirmação “$(p \rightarrow r) \land (q \rightarrow r)$”. Portanto, basta provar cada uma destas duas implicacões separadamente.

### Teorema: Para quaisquer inteiros $m$ e $n$, se $m$ for par ou $n$ for par, então $mn$ é par.

### Prova:

Sejam $m$ e $n$ inteiros quaisquer. Temos dois casos (não exclusivos):

- Caso 1: $m$ é par. Pela definição, existe um inteiro $q$ tal que $m = 2q$. Nesse caso,
$mn = (2q)n = 2(nq)$, e portanto $mn$ é par.

- Caso 2: $n$ é par. Pela definição, existe um inteiro $r$ tal que $n = 2r$. Nesse caso,
$mn = m(2r) = 2(mr)$, e portanto $mn$ é par.

Portanto, se $m$ é par ou $n$ não é par, $mn$ é par.
