---
title: Lista de Exercícios 2 - Respostas
toc: false
---

Respostas dos Exercícios.

## Tabela 1: Acidentes de Trânsito

Para os exercícios a seguir utilize a seguinte tabela a respeito do uso de cinto de segurança em acidentes.

| Cinto/Acidente | Letais | Não Letais |
| -------------- | ------ | ---------- |
| Com            | 3655   | 7005       |
| Sem            | 4402   | 3040       |

### Eventos

-   $C$: usa cinto de segurança.
-   $L$: sofreu acidente letal.

Selecionar aleatoriamente um motorista resulta em:

-   $P(C) = \frac{\lvert C \rvert}{\lvert\Omega \rvert} \approx 0.59$
-   $P(L) = \frac{\lvert L \rvert}{\lvert \Omega \rvert} = 0.24$
-   $P(C') = 1 - P(C) = 0.41$
-   $P(L') = 1 - P(L) = 0.76$

## Questão 1

Se um motorista é selecionado ao acaso, qual a probabilidade dele estar usando o cinto de segurança?

### Resposta

-   Qual o espaço amostral?
    O espaço amostral é cada um dos motoristas.
    Ou seja, cada um dos motoristas pode ser selecionado.
    Como não tem nenhuma menção de um motorista ter a chance maior do que outro ao ser selecionado.
    A chance de um motorista qualquer ser selecionado é de $1/\lvert\Omega\rvert = 1/18102$
-   Qual o evento desejado?
    $A$ é o evento em que um motorista que usa cinto de seguranca.
    $\lvert A \rvert = 3655 + 7005 = 10660$
-   Qual a probabilidade desse evento?
    Como o espaço é equiprovavel, podemos usar o método clássico:
    $$ \frac{\lvert A \rvert}{\lvert \Omega \rvert} = \frac{10660}{18102} = 0.5888852060545796 \approx 0.59 = 59\% $$

## Questão 2

Selecionando aleatoriamente, qual a probabilidade de escolher um motorista que não sofreu um acidente letal sabendo que ele usava cinto de segurança?

### Resposta

$$P(L' \mid C) = \frac{P(L' \cap C)}{P(C)} = \frac{\lvert L' \cap C \rvert / \lvert \Omega \rvert}{P(C)} = \frac{7005/18102}{0.59} \approx 0.66$$

## Questão 3

Qual a probabilidade de escolher um motorista que sofreu um acidente letal sabendo que ele não usava cinto de segurança?

### Resposta

$$P(L \mid C') = \frac{P(L \cap C')}{P(C')} = \frac{\lvert L \cap C' \rvert / \lvert \Omega \rvert}{P(C')} = \frac{4402/18102}{0.41} \approx 0.59$$

## Questão 4

Qual a probabilidade de selecionar aleatoriamente um motorista que usa cinto ou não sofreu acidente letal?

### Resposta

-   Qual o espaço amostral?
    O espaço amostral é cada um dos motoristas.
    Ou seja, cada um dos motoristas pode ser selecionado.
    Como não tem nenhuma menção de um motorista ter a chance maior do que outro ao ser selecionado.
    A chance de um motorista qualquer ser selecionado é de $1/\lvert\Omega\rvert = 1/18102$
-   Qual o evento desejado?
    Na realidade são dois eventos:
    -   $A$ motorista que usa cinto.
    -   $B$ motorista que não sofreu acidente.
-   Qual a probabilidade desse(s) evento(s)?
    $$P(A) = \frac{\lvert A \rvert}{\lvert \Omega \rvert} = \frac{10660}{18102}$$
    $$P(B) = \frac{\lvert B \rvert}{\lvert \Omega \rvert} = \frac{10045}{18102}$$
-   A pergunta é qual o valor de $P(A \cup B) = P( A \text{ ou } B)$?
    $$ P(A \cup B) = P(A) + P(B) - P(A \cap B) = \frac{10660}{18102} + \frac{10045}{18102} - \frac{7005}{18102} = 0.76 $$

## Questão 5

Qual a probabilidade de selecionar aleatoriamente um motorista que não usava cinto ou não sofreu acidente letal?

## Questão 6

Se dois motoristas são selecionados aleatoriamente sem reposição, qual a chance de ambos usarem cinto de segurança?

## Questão 7

Se dois motoristas são selecionados aleatoriamente com reposição, qual a chance dos dois terem sofrido um acidente letal?

## Questão 8

Se $A$ é o evento em que um motorista selecionado aleatoriamente estava usando cinto de segurança.
Qual o significado de $A'$?
Qual o valor de $P(A')$?

## Questão 9

Se $A$ é o evento em que um motorista selecionado aleatoriamente não sofreu acidente letal.
Qual o significado de $A'$?
Qual o valor de $P(A')$?

## Questão 10

Se 3 motoristas são selecionados aleatoriamente sem reposição, qual a probabilidade de nenhum ter sofrido um acidente letal?

## Questão 11

Qual a probabilidade de ganhar o maior prêmio da mega-sena com um jogo só de 6 números?

## Questão 12

Considerando um jogo de Pôquer Texas Hold'em.

1. Qual a probabilidade de ter em suas mãos duas cartas do mesmo naipe?
2. Qual a probabilidade de ter em suas mãos um par de ases?
3. Qual a probabilidade de ter em suas mãos um par qualquer?
4. Qual a probabilidade de ter em suas mãos um par de ases, sabendo que uma das cartas é um ás?
5. Qual a probabilidade de ter duas cartas do mesmo naipe em sequência?
6. Qual a probabilidade de ter duas cartas em sequência?
7. Qual a probabilidade de completar um trio qualquer, sabendo que na sua mão já tem um par de cartas?

## Questão 13

Sendo $x$ uma v.a. discreta que conta a soma dos lados do lançamento de dois dados de seis lados.

Qual o valor médio de $x$?

### Resposta

Seja $x$ a variável aleatória que conta a soma dos lados do lancamento de dois dados de seis lados.

| $D_1/ D_2$ | 1   | 2   | 3   | 4   | 5   | 6   |
| ---------- | --- | --- | --- | --- | --- | --- |
| 1          | 2   | 3   | 4   | 5   | 6   | 7   |
| 2          | 3   | 4   | 5   | 6   | 7   | 8   |
| 3          | 4   | 5   | 6   | 7   | 8   | 9   |
| 4          | 5   | 6   | 7   | 8   | 9   | 10  |
| 5          | 6   | 7   | 8   | 9   | 10  | 11  |
| 6          | 7   | 8   | 9   | 10  | 11  | 12  |

$$ \Omega = \\{ (1,1), (1,2), (1,3), \ldots, (1,6), (2,1),\ldots, (6,6) \\}$$

$$ x((1,1)) = 2 $$
$$ x((4,5)) = 9 $$
$$ x((6,6)) = 12 $$

$$ P(x = 1) = 0$$
$$ P(x = 2) = P(\\{(1,1)\\}) = 1/36 $$
$$ P(x = 3) = P(\\{(1,2), (2,1)\\}) = 2/36 $$
$$ P(x = 4) = P(\\{(1,3), (2,2), (3,1)\\}) = 3/36 $$
$$ P(x = 5) = 4/36$$
$$ P(x = 6) = 5/36$$
$$ P(x = 7) = 6/36$$
$$ P(x = 8) = 5/36$$
$$ P(x = 9) = 4/36$$
$$ P(x = 10) = 3/36$$
$$ P(x = 11) = 2/36$$
$$ P(x = 12) = 1/36$$

Calculando a média, ou valor esperado, ou esperança:

$$\mu = 2 \cdot \frac{1}{36} + 3 \cdot \frac{2}{36} + 4 \cdot \frac{3}{36} + \cdots + 12 \cdot \frac{1}{36} = 7.$$

## Resposta versão 2

Seja $y_1$ a variável aleatória que mede o número que sai no primeiro dado lançado.

Seja $y_2$ a variável aleatória que mede o número que sai no segundo dado lançado.

Observe que $x = y_1 + y_2$.

Como os dois dados são iguais e independentes.

$$ P(y_1 = k) = P(y_2 = k)$$

Como os dados são equilibrados:

$$P(y_1 = 1) = P(y_1 = 2) = \cdots = P(y_1 = 6) = 1/6$$
$$P(y_2 = 1) = P(y_2 = 2) = \cdots = P(y_2 = 6) = 1/6$$

$$\mu_{y_1} = 1 \cdot \frac{1}{6} + 2 \cdot \frac{1}{6} + \cdots + 6 \cdot \frac{1}{6} = 3.5$$
$$\mu_{y_2} = 1 \cdot \frac{1}{6} + 2 \cdot \frac{1}{6} + \cdots + 6 \cdot \frac{1}{6} = 3.5$$
Como **a média de uma variável aleatória composta da soma de outras variáveis aleatórias é linear**:

$$x = y_1 + y_2$$
$$\mu_x = \mu_{y_1} + \mu_{y_2} = 3.5 + 3.5 = 7$$

## Questão 14

Sendo $x$ uma v.a. discreta que conta a soma dos lados do lançamento de $n$ dados de seis lados.

Qual o valor médio de $x$?

### Resposta

E se $x$ for a soma dos lançamentos de $n$ dados.

Como $x = n \cdot y$ aonde $y$ é o resultado do lançamento de um dado.

Como **a média de uma variável aleatória composta da soma de outras variáveis aleatórias é linear**:

Então $\mu_x = n \mu_y = n \cdot 3.5$

## Questão 15

Em um jogo de RPG, um personagem tem a opção de utilizar um martelo que causa dois dados de seis lados de dano em um inimigo ou utilizar um machado de guerra que causa um dado de 12 lados de dano no inimigo.
Assumindo que seria melhor escolher a arma que causa mais dano, qual seria essa escolha?

## Questão 16

Suponha que você consegue acertar uma cesta de basquete de 3 pontos com probabilidade 1%, em média quantas tentativas tem que ser feitas até que você acerte a primeira cesta?

## Questão 17

Considere o jogo do [São Petersburgo](https://en.wikipedia.org/wiki/St._Petersburg_paradox).
Nele uma moeda é jogada até que saia cara.

Para jogar o jogo um valor de R\\$100.00 deve ser pago e o prêmio recebido é de $2^n$ aonde $n$ é o número de vezes que a moeda é jogada.

Em média, qual o valor do prêmio nesse jogo?

Em média, qual o lucro que se obtem ao jogar esse jogo?

## Questão 18

As empresas $A$ e $B$ produzem um tipo de lubrificante para motores.
Segundo a empresa $A$ o tempo de vida útil em horas de funcionamento do seu lubrificante segue distribuição normal com média 1000 e desvio padrão 200.
Já o da empresa $B$ segue distribuição normal com média 800 e desvio padrão 400.
Em um depósito de lubrificantes existem 500 lubrificantes da empresa $A$ e 300 da empresa $B$.

1. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1000 horas, sabendo que ele veio da empresa $A$?
2. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1000 horas, sabendo que ele veio da empresa $B$?
3. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1200 horas, sabendo que ele veio da empresa $A$?
4. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1200 horas, sabendo que ele veio da empresa $B$?
5. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1000 horas?
6. Qual a chance de um lubrificante selecionado ao acaso funcionar corretamente pelo menos 1200 horas?

## Questão 19

Uma moeda é jogada ao acaso 100 vezes, qual a probabilidade dela cair cara em pelo menos 70% dessas vezes?

## Questão 20

Um oráculo disse que 35% das pessoas apoiam um projeto de lei.
Assumindo que a afirmação anterior é verdadeira, responda.

1. Selecionando aleatoriamente 200 pessoas, qual a chance de pelo menos 70 aprovarem o projeto de lei?
2. Selecionando aleatoriamente 200 pessoas, qual a chance de no máximo 70 aprovarem o projeto de lei?
