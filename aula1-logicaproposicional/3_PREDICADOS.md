# Predicados, Quantificadores e mais provas

Quando a proposição é fechada, ela não depende de nenhuma variável, que é basicamente o que foi visto anteriormente, com símbolos lowercase $p, q, r, s, t$...

Uma proposição aberta é quando depende de uma ou mais variáveis. Por exemplo:

- $x+1$ é maior que $x$.
- o quadrado de $x$ é 16.
- $x$ é um número primo
- $x$ é maior que $y$.
- $x + y = 2x + z$.

Perceba que se tratam de proposições abertas, pois existe algo que varia que pode contribuir para que essa proposição seja verdadeira ou falsa. Um **predicado** é uma proposição aberta. Os **predicados** são funções que recebem um ou mais parâmetros que podem ou não variar, e retornam um booleano *Verdadeiro* ou *Falso*, e isso dependerá da proposição descrita.

>Nota: A lógica de predicados será amplamente abordada na parte de lógica para ciência da computação. 

A notação que se utiliza para diferenciar as proposições fechadas dos predicados são as letras uppercase $P, Q, R, S, T$... porém, com os parâmetros sendo passados ao predicado.

Pegando o exemplo "$x+1$ é maior que $x$", podemos resumir esse predicado na notação $P(x)$. E pegando o exemplo "$x$ é maior que $y$", podemos resumir esse predicado na notação $Q(x,y)$. Ambos podem retornar verdadeiro ou falso.

### Conversão de Aberta para Fechada

Para converter um predicado em proposição fechada, basta definir os valores das variáveis. Por exemplo, "$x$ é maior que $y$" possui notação $Q(x,y)$ e é um predicado, e portanto, uma proposição aberta. Basta eu declarar $x = 3$ e $y = 1$, e agora tenho uma proposição fechada $Q(3,1)$, que sempre será verdadeira, afinal, $3 > 1$.

# Quantificadores

Outra forma de converter predicados em proposições fechadas é utilizando **quantificadores**.

Os dois principais quantificadores são:

- **Para todo** ($\forall$)
- **Existe** ($\exists$)

Também chamados de **quantificador universal** e **quantificador existencial**, respectivamente.

O quantificador universal generaliza que todos os elementos de um conjunto específico validam um predicado. Já o quantificador existencial afirma que pelo menos um elemento de um conjunto específico valida um predicado. Por exemplo: "para todo $x$ no conjunto dos reais, $P(x)$. Isso pode ser escrito como $(\forall x \in \mathbb{R})P(x)$. Pode também ser resumido a $\forall xP(x)$ dependendo do contexto apresentado. E outro exemplo: "existe pelo menos um $x$ no conjunto dos reais, tal que $P(x)$. Isso pode ser escrito como $(\exists x \in \mathbb{R})P(x)$. Pode também ser resumido a $\exists xP(x)$ dependendo do contexto apresentado (domínio esteja implícito). 

## Quantificadores Universais

Se pegarmos a frase "$x+1$ é maior que $x$", então $(\forall x \in \mathbb{N})P(x)$ é verdade, pois se substituirmos $x$ por qualquer número inteiro, a afirmação $P(x)$ será sempre verdadeira. Por outro lado, se $P(x)$ for "$x$ é um número primo", então a frase não é mais válida, pois $P(6)$ seria falso, por exemplo.

Se o domínio $D$ é um conjunto finito com elementos $v_1, v_2,..., v_n$, então a frase $(\forall x \in D)P(x)$ é equivalente logicamente a $P(v_1) \land P(v_2) \land ... \land P(v_n)$. Ou seja:

$$(\forall x \in D)P(x) \Leftrightarrow P(v_1) \land P(v_2) \land ... \land P(v_n)$$

Isso significa que, por **definição**, a frase $(\forall x \in D)P(x)$ é verdadeira se, e somente se, a proposição $P(x)$ for sempre verdadeira quando substituímos a variável $x$ por qualquer elemento do conjunto $D$.

### Exemplo

$P(x)$ siginifcando "$x$ é par", $Q(x)$ significando "$x$ é divisível por 3" e $R(x)$ significando "$x$ é divisível por 4", temos:

- $(\forall x \in \mathbb{N})P(x)$ é falso. Lê-se "para todo natural $x$, $x$ é par".
- $(\forall x \in \mathbb{N})P(x) \lor Q(x)$ é falso. Lê-se "para todo natural $x$, $x$ é par ou divisível por 3".
- $(\forall x \in \mathbb{N})R(x) \rightarrow P(x)$ é verdadeiro. Lê-se "para todo natural $x$, se $x$ é divisível por 4, então $x$ é par.

## Quantificadores Existenciais

Se pegarmos a frase "$x$ é um número primo", então $(\exists x \in \mathbb{N})P(x)$ é verdade, pois se substituirmos $x$ por um 7, a afirmação $P(x)$ será verdadeira. Por outro lado, se $P(x)$ for "$y$ é igual a $y+1$", então a frase não é válida, pois não existe nenhum número natural que satisfaça essa sentença.

Se o domínio $D$ é um conjunto finito com elementos $v_1, v_2,..., v_n$, então a frase $(\exists x \in D)P(x)$ é equivalente logicamente a $P(v_1) \lor P(v_2) \lor ... \lor P(v_n)$. Ou seja:

$$(\exists x \in D)P(x) \Leftrightarrow P(v_1) \lor P(v_2) \lor ... \lor P(v_n)$$

Isso significa que, por **definição**, a frase $(\exists x \in D)P(x)$ é verdadeira se, e somente se, existir pelo menos um elemento de $D$ que, atribuído a variável $x$, torna a afirmação $P(x)$ verdadeira, e $P(x)$ é falso se, e somente se, não existe nenhum elemento de $D$ com essa propriedade.

### Exemplo

$P(x)$ siginifcando "$x$ é par", $Q(x)$ significando "$x$ é divisível por 3" e $R(x)$ significando "$x$ é divisível por 4", temos:

- $(\exists x \in \mathbb{N})R(x)$ é verdadeiro. Lê-se "existe um natural $x$ (tal que $x$ é) divisível por 4". O proprio 4 é um exemplo que já torna a sentença verdadeira.
- $(\exists x \in \mathbb{N})P(x) \lor Q(x)$ é verdadeiro. Lê-se "existe um natural $x$ (tal que $x$ é) par ou divisível por 3.
- $(\exists x \in \mathbb{N})Q(x) \rightarrow Q(x+1)$ é verdadeiro. Lê-se "existe um natural $x$ tal que se ele for divisível por 3, então ele incrementado é divisível por 4". O 2 é um exemplo, pois $Q(2)$ é falso, e na tabela-verdade, se a condicional é falsa, a proposição composta toda é verdadeira, não importando a conclusão.

## Equivalências Lógicas de Predicados

Algumas equivalências são importantes para a lógica de predicados.

### Negação do Para Todo

- $\neg[(\forall x  \in D)P(x)]$ equivale a $(\exists x \in D)\neg P(x)$.

Ao negar essa proposição universal, obtemos a afirmação de que nem todas as instâncias de $P(x)$ são verdadeiras, ou seja, existe pelo menos um elemento $x$ no conjunto $D$ para o qual $P(x)$ é falso.

Isso é muito lógico até no cotidiano. A negação de algo que generaliza tudo é provar que pelo menos 1 caso não cai nessa afirmação inteira. Por exemplo. se eu digo que todo chocolate no mundo é doce $(\forall \text{choco}  \in \text{Mundo})P(\text{choco})$, mas uma pessoa diz que essa afirmação toda é falsa $\neg[(\forall \text{choco} \in \text{Mundo})P(\text{choco})]$, então para contrariar meu argumento, basta ela mostrar um caso que torna essa frase falsa, um chocolate amargo por exemplo. Portanto, $(\exists \text{choco} \in \text{Mundo})\neg P(\text{choco})$, onde "choco" seria um chocolate amargo dessa vez.

Resumindo, a negação do "para todo" se resume a "nem todo". Exemplo: "nem todo $x$ em $D$ satisfaz $P(x)$" equivale a "existe um $x$ em $D$ que não satisfaz $P(x)$. Ou seja, $\neg\forall x:P(x) \Leftrightarrow \exists x : \neg P(x)$.

### Negação do Existe

- $\neg[(\exists x  \in D)P(x)]$ equivale a $(\forall x \in D)\neg P(x)$.

Ao negar essa proposição existencial, obtemos a afirmação de que para todos os elementos $x$ no conjunto $D$, a proposição $P(x)$ é falsa.

Ainda no cotidiano, se eu digo que existe pelo menos um chocolate salgado no mundo $(\exists \text{choco} \in \text{Mundo})P(\text{choco})$, mas uma pessoa diz que essa afirmação toda é falsa $\neg(\exists \text{choco} \in \text{Mundo})P(\text{choco})$, então para contrariar meu argumento, basta ela mostrar que todos os chocolates possíveis do mundo não são salgados $(\forall \text{choco} \in \text{Mundo})\neg P(\text{choco})$.

Resumindo, a negação do "existe" se resume a "nenhum", ou "não existe". Exemplo: "nenhum $x$ em $D$ satisfaz $P(x)$" equivale a "para todo $x$ em $D$ não satisfaz $P(x)$. Ou seja, $\neg\exists x:P(x) \Leftrightarrow \forall x : \neg P(x)$.

### Distribuição do Para Todo

- $(\forall x \in D)(P(x) \land Q(x))$ equivale a $[(\forall x \in D)P(x)] \land [(\forall x \in D)Q(x)]$.

### Distribuição do Existe

- $(\exists x \in D)(P(x) \lor Q(x))$ equivale a $[(\exists x \in D)P(x)] \lor [(\exists x \in D)Q(x)]$.

# Provas com quantificadores

Existem outros tipos de provas importantes utilizando o básico da lógica de predicados.

Aqui são as provas que utilizam bem mais os conceitos de lógica de predicados.

## Método da Generalização Universal

É um tipo de prova que estabelece a validade de uma afirmação para todos os elementos de um conjunto, utilizando uma notação matemática geral. Em vez de considerar casos individuais, ela usa quantificadores universais (como o "para todo" - $\forall$) para mostrar que a afirmação é verdadeira para cada elemento dentro do conjunto em questão.

### Teorema: Para quaisquer números reais $x$ e $y$, $(x + y)^2 - (x - y)^2 = 4xy$

### Prova

- Sejam $x$ e $y$ dois números reais quaisquer. Pelo teorema do binômio, temos $(x + y)^2 = x^2 + 2xy + y^2$, e $(x - y)^2 = x^2 - 2xy + y^2$. Portanto, $(x + y)^2 - (x - y)^2 = (x^2 + 2xy + y^2) - (x^2 - 2xy + y^2) = 4xy$.

## Método da Vacuidade

A prova por vacuidade é um tipo de prova que se baseia na ausência de elementos em um conjunto ou condição. Ela é concisa porque não há elementos para serem considerados, portanto, qualquer afirmação feita sobre o conjunto vazio é automaticamente verdadeira.

Por exemplo, se temos a afirmação "Para todo $x$ no conjunto vazio, $P(x)$ é verdadeiro", a prova por vacuidade mostra que a afirmação é verdadeira, simplesmente porque não existem elementos no conjunto vazio para contradizer a proposição $P(x)$.

### Teorema: Todos os pares primos maiores que dois são quadrados perfeitos.

### Prova

- Essa afirmação é verdadeira por vacuidade, pois não existem primos pares maiores que dois.

## Método do Contra-Exemplo

A prova por contraexemplo é um tipo de prova que refuta uma afirmação rapidamente mostrando um exemplo específico em que ela é falsa. Em vez de mostrar que a afirmação é verdadeira para todos os casos possíveis, basta encontrar um único exemplo que contradiga a afirmação para provar que ela não é válida universalmente. Se parar para pensar, é a forma que os seres humanos mais provam algo durante sua vida, pois basta um exemplo que quebre a generalização de algo.

### Teorema: Para todo primo $n$, o inteiro $(2^n) - 1$ é primo.

### Prova

- Esta afirmação é falsa, basta ver que o número $n = 11$ é um contra-exemplo, pois $P(11) = (2^{11}) - 1 = 2047 = 23 \times 89$.