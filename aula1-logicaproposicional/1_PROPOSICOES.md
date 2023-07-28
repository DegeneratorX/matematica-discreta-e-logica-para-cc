https://unicode-table.com/en/sets/mathematical-signs/

# Proposição

É uma sentença declarativa que assume **Verdadeiro** ou **Falso**.

Exemplos:

- O morcego é um mamífero. *(Verdadeiro)*
- Rio de Janeiro é a capital do Brasil. *(Falso, mas já foi Verdadeiro um dia)*
- Há 36 macacos no zoológico de Londres. *(Não dá pra saber)*
- A taxa de juros do banco central vai subir amanhã. *(Não dá pra saber)*
- O trilionésimo algarismo decimal de pi é 7. *(Dá pra saber, mas precisa calcular)*

### O que não seria proposições?

Frases interrogativas **NÃO** são proposições:

- O que é isto?

Frases imperativas **NÃO** são proposições:

- Leia com cuidado.

Certas frases autoreferentes **NÃO** são proposições, pois podem gerar paradoxos:

- Essa sentença/frase é falsa.

Frases que contem elementos indefinidos não são proposições:

- $x$ é menor que 3. *(Não é proposição, pois x não foi definido. É uma fórmula)*

# Conectivos Lógicos, Proposições Compostas e Notações

Alguns conectivos podem negar uma proposição, ou juntar duas ou mais proposições em uma frase

- e;
- ou
- não;
- se...então.

Exemplos de conectivos e proposições compostas:

- [Brasília é a capital do Brasil] ou [Montevidéu é a capital da Argentina];
- Não [haverá sessão da meia-noite hoje neste cinema];
- Se [a taxa de juros cair amanhã], então [a inflação vai aumentar neste mês].

Tudo que está entre chaves são proposições. Podemos resumir elas em apenas letras para simplificar. Por convenção, se utiliza letras como $p$, $q$, $r$, $s$, por aí vai. Feita a conversão:

- $p$ ou $q$;
- Não $p$;
- Se $p$, então $q$.

## Notações

Os conectores também possuem suas notações na lógica matemática. 

- Definimos **e** como sendo $\wedge$, a operação de *conjunção*;
    - Exemplo: $p \wedge q$ *(p e q)*;
- Definimos **ou** como sendo $\vee$, a operação de *disjunção*;
    - Exemplo: $p \vee q$ *(p ou q)*;
- Definimos **não** como sendo $\neg$, a operação de *negação*;
    - Exemplo: $\neg p$ *(não p)*;
- Definimos **se...então (implica)** como sendo $\to$, a operação de *implicação*;
    - Exemplo: $p \to q$ *(se p então q / p implica q)*;
- Definimos **se e somente se (sse, equivale a)** como sendo $\leftrightarrow$, a operação de *equivalência*;
    - Exemplo: $p \leftrightarrow q$ *(p se, e somente se q / p equivale a q)*;
- Definimos **ou, e somente ou** como sendo $\bigoplus$, a operação de *ou exclusivo*.
    - Exemplo: $p \bigoplus q$ *(p ou, e somente ou q)*.

>Nota: é possível que em alguns casos se depare com o símbolo $\Rightarrow$ ou $\Leftrightarrow$. Esses símbolos significam **implicam logicamente** ou **se, e logicamente somente se**, e **NÃO** são operadores lógicos, mas sim afirmações tautológicas (ou seja, que são sempre verdadeiras, como se fosse um resultado óbvio). Exemplo: $2 + 2 = x \Rightarrow x = 4$. 

# Tabela Verdade

Uma tabela verdade é uma representação tabular que lista todas as possíveis combinações de valores de entrada para um conjunto de variáveis proposicionais em uma expressão lógica. Ela apresenta as saídas resultantes dessas combinações, indicando os valores verdadeiros *V ou 1* e falsos *F ou 0* para cada configuração de entradas. 

Essas tabelas são amplamente utilizadas em lógica booleana e são essenciais para analisar o comportamento de circuitos lógicos, funções booleanas e avaliar a validade de proposições lógicas.

Aqui estão as principais tabelas verdades para estudo.

### AND

| $p$ | $q$ | $p \land q$ |
|---|---|-----------|
| V | V |     V     |
| V | F |     F     |
| F | V |     F     |
| F | F |     F     |

### OR

| $p$ | $q$ | $p \lor q$ |
|---|---|----------|
| V | V |    V     |
| V | F |    V     |
| F | V |    V     |
| F | F |    F     |

### XOR

| $p$ | $q$ | $p \oplus q$ |
|---|---|-------------|
| V | V |      F      |
| V | F |      V      |
| F | V |      V      |
| F | F |      F      |

### SE ENTÃO

| $p$ | $q$ | $p \rightarrow q$ |
|---|---|------------------|
| V | V |        V         |
| V | F |        F         |
| F | V |        V         |
| F | F |        V         |

### SSE

| $p$ | $q$ | $p \leftrightarrow q$ |
|---|---|----------------------|
| V | V |          V           |
| V | F |          F           |
| F | V |          F           |
| F | F |          V           |

### NOT

| $p$ | $\neg p$ |
|---|--------|
| V |   F    |
| F |   V    |

## Precedência de operadores

As precedência de operadores (prioridade nas operações) são:

| Símbolo | Ordem |
|---------|-------|
|   $\neg$  |   1°  |
|   $\land$ |   2°  |
|   $\lor$  |   3°  |
|   $\rightarrow$, $\leftrightarrow$ |   4°  |

O motivo para essa ordem de precedência é baseado em convenções matemáticas e lógicas, visando garantir uma avaliação consistente e eficiente de expressões. A negação tem a maior precedência, pois é a operação mais simples e deve ser aplicada antes de outras. Em seguida, a conjunção tem precedência sobre a disjunção, uma vez que o "AND" geralmente é considerado mais restritivo do que o "OR".

## Outras tabelas verdades

Existem algumas tabelas verdades definidas pela obviedade das operações lógicas. São elas:

### TAUTOLOGIA

| $p$ | $¬p$ | $p \lor \neg p$ |
|---|----|---------------|
| V |  F |       V       |
| F |  V |       V       |

Isso sempre é verdadeiro. Afinal, sempre que uma proposição for verdadeira, a negação dela é falsa (lei da não-contradição). Tautologia é quando toda a proposição composta resulta em verdadeira.

### CONTRADIÇÃO

| $p$ | $¬p$ | $p \land \neg p$ |
|---|----|----------------|
| V |  F |       F        |
| F |  V |       F        |

Isso sempre é falso. Afinal, sempre que uma proposição for verdadeira, a negação dela é falsa (lei da não-contradição). Contradição é quando toda a proposição composta resulta em falsa.

>Nota: a contradição é uma negação da tautologia e vice-versa.

# Equivalências Lógicas Tautológicas

Algumas equivalências são importantes para simplificação de proposições e sentenças.

### De Morgan

- $\neg (p \land q)$ equivale a $(\neg p \lor \neg q)$;
- $\neg (p \lor q)$ equivale a $(\neg p \land \neg q)$;

### Implicação e Negação da Implicação

- $(p \rightarrow q)$ equivale a $(\neg p \lor q)$;
- $\neg (p \rightarrow q)$ equivale a $(p \land \neg q)$;

### Equivalência e Negação da Equivalência

- $(p \Leftrightarrow q)$ equivale a $(p \rightarrow q) \land (q \rightarrow p)$;
- $(p \Leftrightarrow q)$ equivale a $\neg (p \oplus q)$;

### Contrapositiva e Absurdo

- $(p \rightarrow q)$ equivale a $(\neg q \rightarrow \neg p)$;
- $(p \rightarrow q)$ equivale a $(p \land \neg q) \rightarrow \text{ Falso}$.

>Nota: nesse caso é perfeitamente possível substituir "equivale a" por $\Leftrightarrow$, pois é uma equivalência tautológica.

# Implicações Lógicas Tautológicas 

Uma implicação lógica tautológica é uma proposição que é sempre verdadeira, independentemente dos valores lógicos de suas premissas. Em outras palavras, é uma afirmação que não pode ser falsa sob nenhuma circunstância.

Lembrar que a implicação lógica é representada pelo símbolo $\rightarrow$. A tautologia ($\Rightarrow$) ocorre quando a conclusão $q$ é verdadeira para todas as situações em que a premissa $p$ é verdadeira.

Um exemplo clássico de implicação lógica tautológica é a seguinte afirmação:

Se está chovendo ($p$), então o chão está molhado ($q$).

Essa implicação é tautológica porque, sempre que está chovendo ($p$ é verdadeiro), o chão está molhado ($q$ também é verdadeiro). Não importa quais outras condições estejam presentes, a conclusão ainda é verdadeira quando a premissa é verdadeira.

Tautologias são fundamentais na lógica e na matemática, pois representam relações lógicas absolutas e incontestáveis, fornecendo bases sólidas para o raciocínio dedutivo.

As tautologias principais são:

### Tautologia Clássica 1

- $p \Rightarrow p \lor q$

Ou seja, $p \rightarrow (p \lor q)$ SEMPRE será verdade, independente de $p$ ou $q$. Se fizer a tabela verdade baseada nessa operação, verá que não tem como evitar a tautologia.

### Tautologia Clássica 2

- $p \land q \Rightarrow p$

Ou seja, $(p \land q) \rightarrow p$ SEMPRE será verdade, independente de $p$ ou $q$. Se fizer a tabela verdade baseada nessa operação, verá que não tem como evitar a tautologia.

### Modus Ponens

- $p \land (p \rightarrow q) \Rightarrow q$

### Modus Tollens (contrapositiva do Modus Ponens)

- $(p \rightarrow q) \land \neg q \Rightarrow \neg p$

### Silogismo Hipotético

- $p \rightarrow q \land q \rightarrow r \Rightarrow p \rightarrow r$

### Silogismo Disjuntivo

- $(p \lor q) \land \neg p \Rightarrow q$

### Demonstração por Absurdo

- $p \rightarrow \text{ Falso } \Rightarrow \neg p$ 

Assume um certo $p$ e chega numa conclusão falsa, logo $p$ é falso, ou seja, $\neg p$ é verdadeiro.