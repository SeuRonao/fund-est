---
title: Medidas de Tendência Central
order: 3
header:
  teaser: /assets/images/teasers/numbers-500x300.jpg
---
São medidas para resumir o *miolo* de uma distribuição de frequência em apenas um número.

Para simplificar a notação, todo somatório na forma $\sum_{i=1}^n$ será escrito como $\sum$ quando o contexto dos itens a serem somados ficar claro.

## Somatórios

Um somatório é uma forma de resumir uma sequencia de somas.
O símbolo que representa é o sigma maiúsculo $\sum$.
Existem algumas formas diferentes de dizer o que vai ser somado, ou resumido, a mais comum é:

$$\sum_{i = k}^n f(i)$$

A fórmula acima é um resumo para a soma de todos os valores de $i$ variando de $k$ até $n$.
Ou seja, o somatório acima pode ser lido como:
Some o resultado de $f(i)$ para cada valor de $i$ de $k$ até $n$.
No caso seria, $f(k) + f(k + 1) + f(k + 2) + \cdots + f(n)$.

### Exemplo 1: Somatório Simples

$$\sum_{i = 2}^5 2i$$

Esse somatório pode ser lido como:

> O somatório de $i$ variando de $2$ até $5$ de $2i$.

A expansão do somatório seria:

$$\sum_{i = 2}^5 2i = 2 \cdot (2) + 2 \cdot (3) + 2 \cdot (4) + 2 \cdot (5)$$

$$\sum_{i = 2}^5 2i = 4 + 6 + 8 + 10$$

$$\sum_{i = 2}^5 2i = 28$$

### Exemplo 2: Somatório de Conjunto

Dado um conjunto $S$ de valores numericos, outra notação é da seguinte forma:

$$\sum_{i \in S} f(i)$$

Suponha que $S = \{-3, 2, 4, 8\}$, e que $f(i) = 2^i$.

$$\sum_{i \in S} 2^i$$

> Somatório de $i$ pertencente à $S$ de $2^i$.

A expansão do somatório fica:

$$\sum_{i \in S} 2^i = 2^{-3} + 2^2 + 2^4 + 2^8$$

$$\sum_{i \in S} 2^i = 1/8 + 4 + 16 + 256$$

$$\sum_{i \in S} 2^i = 276.125$$

### Exemplo 3: Somatório com Variável

Dada uma variável com valores observados $x_1, x_2, \dots, x_n$.
Note que, são todos os valores observados, inclusive se tiver repetição, vai aparecer repetido alguns valores de $x_i$.

$$\sum_{i = 1}^n f(x_i)$$

Suponha que os valores observados para $x$ são:

$$-2, 2, 3, 3, 5, 7$$

E que $f(x_i) = 2x_i + 3$.

$$\sum_{i = 1}^6 2x_i + 3$$

A expansão fica:

$$\sum_{i = 1}^6 2x_i + 3 = (2x_1 + 3) + (2x_2 + 3) + (2x_3 + 3) + (2x_4 + 3) + (2x_5 + 3) + (2x_6 + 3)$$

$$\sum_{i = 1}^6 2x_i + 3 = (2 \cdot -2 + 3) + (2 \cdot 2 + 3) + (2 \cdot 3 + 3) + (2 \cdot 3 + 3) + (2 \cdot 5 + 3) + (2 \cdot 7 + 3)$$

$$\sum_{i = 1}^6 2x_i + 3 = (-4 + 3) + (4 + 3) + (6 + 3) + (6 + 3) + (10 + 3) + (14 + 3)$$

$$\sum_{i = 1}^6 2x_i + 3 = -4 + 4 + 6 + 6 + 10 + 14 + 6 \cdot 3$$

$$\sum_{i = 1}^6 2x_i + 3 = 54$$

### Exercícios de Somatório

Vamos calcular:

1. $\sum_{i = 1}^6 3$
2. $\sum_{i = 4}^3 f(i)$
3. $\sum_{i = 1}^4 \sum_{j = 3}^i i + j$
4. $\sum_{i = 1}^{50} 5i + 7 + \sqrt{i}$, pode usar gerenciador de planilha.

As respostas podem ser encontradas [aqui]({% link assets/answers/medidas-tendencia-central.md %}).

## Média Aritmética Simples

Considere que $x_1, x_2, x_3, \ldots, x_n$ são os valores de uma variável $x$.

Então, a média aritmética $\bar{x}$ é definida por:
$$\bar{x} = \frac{\sum x_i}{n}$$

Considere o desvio de um valor específico $x_i$ de $x$ em relação à média $\bar{x}$ dado por $d_i = x_i - \bar{x}$.

### Algumas Propriedades

- A soma dos desvios resulta em zero.
  $$\sum d_i = 0$$
- A média minimiza o quadrado dos desvios se comparada com qualquer outro número, por exemplo $w$.
  $$\sum d_i^2 \leq \sum (x_i - w)^2$$
- Se $n_1$ números tem média $\bar{x}_1$, $n_2$ números tem média $\bar{x}_2$, $\ldots$, $n_k$ números tem média $\bar{x}_k$, então a média $\bar{x}$ de todos esses números é dada por:
  $$\bar{x} = \frac{\sum n_i \bar{x}_i}{\sum n_i}$$
- Somar $w$ em cada número que compõe a média aumenta a média em $w$.
  Considere $y_i = x_i + w$:
  $$\bar{y} = \bar{x} + w$$
- Multiplicar por $w$ cada número que compõe a média multiplica a média em $w$.
  Considere $y_i = x_i \cdot w$:
  $$\bar{y} = \bar{x} \cdot w$$

## Média Aritmética Ponderada

Se $x_1, x_2, x_3, \ldots, x_k$ são os valores de uma variável $x$, $n_1, \ldots, n_k$ são os números absolutos de vezes que a variável assume cada um desses valores e $n = \sum n_i$.
Então, a média aritmética $\bar{x}$ é definida por:
$$\bar{x} = \frac{\sum n_i \cdot x_i}{n}$$

## Moda

É o valor de maior frequência.

- Quando existe apenas um, é unimodal.
- Quando existem dois, é bimodal.
- Quando existirem mais de dois, é multimodal.
- Quando todos os valores tem a mesma frequência, amodal.

## Mediana

Supondo que $x_1 \leq x_2 \leq x_3 \leq \cdots \leq x_n$ a mediana pode ser definida como $\mathrm{md}(x) = x_{(n+1)/2}$ se $n$ é ímpar, ou $\mathrm{md}(x) = (x_{n/2} + x_{n/2 + 1})/2$ se $n$ par.

## Quantis

O quantil $q(p)$, $0 \leq p \leq 1$, é o valor da variável tal que existem $p \cdot n$ valores são menores do que ela e $(1 - p) \cdot n$ valores maiores do que ela.

Se o quantil não existir, então usa-se a média aritmética dos valores mais próximos do quantil desejado, como por exemplo $q(0.5) = \mathrm{md}(x)$.

Os quantis mais famosos são os:

- $q(0.25)$: primeiro quartil.
- $q(0.5)$: segundo quartil ou *mediana*.
- $q(0.75)$: terceiro quartil.

## Midrange

É a média entre o maior e menor valores observados.

## Observações

- A média pode sofrer grandes alterações quando uma observação muito grande ou muito pequena é adicionada ao conjunto de observações.
- A mediana e a moda são mais robusta quanto a essas alterações.
- A moda pode ser usada também para variáveis qualitativas.
- Nem sempre faz sentido calcular medidas de tendência central só por uma variável ser numérica.
  De que nos serviria calcular a média dos CEPs de um conjunto de endereços, ou a mediana dos números de RG de uma população de um estado?

## Exercícios Resolvidos

### Exercício 1: Dados Brutos

Seja $x$ uma variável quantitativa discreta.
Com valores dados pela tabela abaixo:

| Identificação | $x$ |
| ------------- | --- |
| 1             | 0   |
| 2             | 0   |
| 3             | 2   |
| 4             | 2   |
| 5             | 3   |
| 6             | 5   |
| 7             | 7   |
| 8             | 9   |
| 9             | 10  |
| 10            | 20  |

1. Calcule a média aritmética de $x$.

   A média aritmética é definida por:
   $$\bar{x} = \frac{\sum x_i}{n}$$
   No caso, $n = 10$ e os valores são dados pela tabela.
   Resultado:
   $$\bar{x} = \frac{0 + 0 + 2 + 2 + 3 + 5 + 7 + 9 + 10 + 20}{10} = \frac{58}{10} = 5.8$$

2. Calcule a moda de $x$.

   A variável $x$ é bimodal com modas $0$ e $2$ ambas com duas observações cada.

3. Calcule a mediana de $x$.

   A mediana de $x$, como $n = 10$ é par é dada por
   $$\mathrm{md}(x) = \frac{x_{n/2} + x_{n/2 + 1}}{2} = \frac{x_5 + x_6}{2} = \frac{3 + 5}{2} = 4$$

### Exercício 2: Distribuição de Frequência

Agora, considerando a tabela de distribuição de frequência de $x$ responda as mesmas perguntas.

| Valor | $n_i$ |
| ----- | ----- |
| 0     | 2     |
| 2     | 2     |
| 3     | 1     |
| 5     | 1     |
| 7     | 1     |
| 9     | 1     |
| 10    | 1     |
| 20    | 1     |

1. Calcule a média aritmética de $x$.

   No caso, a média aritmética ponderada.

   $$\bar{x} = \frac{\sum n_i x_i}{n} = \frac{2 \cdot 0 + 2 \cdot 2 + 1 \cdot 3 + 1 \cdot 5 + 1 \cdot 7 + 1 \cdot 9 + 1 \cdot 10 + 1 \cdot 20}{10} = \frac{58}{10} = 5.8$$

2. Calcule a moda de $x$.

   Basta olhar o(s) maiores $n_i$ na tabela de distribuição de frequência.
   Os valores são $0$ e $2$ com duas observações.

3. Calcule a mediana de $x$.

   O problema está no fato de que a tabela de distribuição de frequência agrega os valores iguais, então para saber quais são os dois valores que estão *no meio* da fila de valores é necessário *desembrulhar* toda a fila.
   Dessa forma, o problema se resume à calcular a mediana da mesma maneira que na questão anterior.

### Exercício 3: Distribuição de Frequência com Dados Agrupados

Agora, considerando a tabela de distribuição de frequência de $x$ agrupado por classes responda as mesmas perguntas.

| Valor   | $n_i$ |
| ------- | ----- |
| 0 - 3   | 5     |
| 5 - 9   | 3     |
| 10 - 20 | 2     |

1. Calcule a média aritmética de $x$.

   Como a tabela está agrupada por classes, é necessário escolher um número para representar cada classe.
   Uma opção é escolher o *midrange* de cada classe.
   Ficariamos com $1.5$ para a primeira classe, $7$ para a segunda e $15$ para a terceira classe.
   A média aritmética seguindo essa convenção fica:

   $$\bar{x} = \frac{\sum n_i x_i}{n} = \frac{5  \cdot  1.5 + 3  \cdot  7 + 2  \cdot  15}{10} = \frac{58.5}{10} = 5.85$$

2. Calcule a moda de $x$.

   A moda terá que ser um membro da classe com maior quantidade de observações no caso $0 - 3$ que tem como *midrange* $1.5$.

3. Calcule a mediana de $x$.

   A mediana, como no exercício anterior, terá de ser calculada *desembrulhando* os valores das classes.
   Também teremos que utilizar algum valor para representar a classe.
   Ou seja, os valores considerados serão:

   $$1.5, 1.5, 1.5, 1.5, \textcolor{red}{1.5}, \textcolor{blue}{7}, 7, 7, 15, 15$$

   Que resulta em $\frac{1.5 + 7}{2} = 4.25$.

4. Qual é o menor e maior valor teórico para a média seguindo essa tabela de distribuição de frequência.

   Para saber o menor/maior valor teórico para a média aritmética, podemos usar os limites inferiores/superiores de cada classe em vez do *midrange* para representá-las.

   O menor valor seria:

   $$\bar{x} = \frac{5 \cdot 0 + 3 \cdot 5 + 2 \cdot 10}{10} = \frac{35}{10} = 3.5$$

   O maior valor seria:

   $$\bar{x} = \frac{5 \cdot 3 + 3 \cdot 9 + 2 \cdot 20}{10} = \frac{82}{10} = 8.2$$
