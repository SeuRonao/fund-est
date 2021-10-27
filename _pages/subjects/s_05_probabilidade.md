---
title: Probabilidade
---

Retirado da [Wikipedia](https://pt.wikipedia.org/wiki/Probabilidade):

> A palavra probabilidade deriva do Latim *probare* (provar ou testar).
> Informalmente, provável é uma das muitas palavras utilizadas para eventos incertos ou desconhecidos, sendo também substituída por algumas palavras como *sorte*, *risco*, *azar*, *chance*, *incerteza*, *duvidoso*, dependendo do contexto inseridas á língua portuguesa e na linguagem matemática.

No contexto de estatística, a *probabilidade* será usada como uma ferramentas para se medir uma estimação ou testar uma hipótese.

## Conceitos Iniciais

- Um **experimento probabilístico** é um procedimento em que sabe-se que existem alguns, possivelmente infinitos, resultados possíveis e que pode ser repetido infinitamente.
  Alem disso, a frequência relativa dos resultados deve estabilizar com o aumento de realizações do experimento.
- Um **espaço amostral** é o conjunto de todos os possíveis resultados possíveis do experimento.
- Um **evento** é uma coleção de resultados possíveis.
- Um **evento simples** é um único resultado.

## Notação Matemática

- O espaço amostral é normalmente denotado por $\Omega$, leia-se ômega maiúsculo.
- Um evento é normalmente denotado por uma letra em maiúsculo do alfabeto: $A, B, C$.
- A probabilidade de um evento acontecer é normalmente definida como uma função que associa eventos do espaço amostral em um valor de zero até um.
  Zero significando que o evento é *impossível* e um que o evento em questão é *certeza*.
  Normalmente a função é denotada pela letra maiuscula $P$.

### Exemplo (Lançamento de Moedas)

Considere o experimento probabilístico em que uma moeda é lançada duas vezes e quando ela para no chão a face voltada para cima é visualizada em cada um dos lançamentos.

Podemos representar $\Omega$ como sendo o conjunto $\{(K, K), (K, C), (C, K), (C, C)\}$.
Assim, sair cara nos dois lançamentos seria representado pelo par $(K, K)$ e sair cara no primeiro lançamento e coroa no segundo pelo pelo par $(K, C)$.

Obviamente, existem outros tipos de resultado quando realizamos esse experimento na prática.
Por exemplo, alguém pode passar correndo e levar a moeda antes dela cair no chão, mas utilizaremos um modelo simplificado.

Seja $A$ o evento em que sai pelo menos uma cara, podemos representar $A$ como $\{(K, K), (K, C), (C, K)\}$.

A chance de $A$ acontecer ao realizar o experimento pode ser representada por $P(A)$.

## Como Calcular Probabilidades

Definir $P(A)$ qualquer que seja o evento $A$ em geral é um desafio que pode ser resolvido de algumas maneiras.

1. Experimentalmente: ao se realizar o experimento uma quantidade *significativa* de vezes, pode-se medir
   $$P(A) = \frac{\text{nº de vezes que } A \text{ aconteceu}}{\text{nº de testes}}$$
2. Abordagem Clássica: se $\Omega$ é tal que cada elemento tem chance $1/\lvert \Omega \rvert$ de acontecer, então 
   $$P(A) = \frac{\text{maneiras diferentes em que } A \text{ pode acontecer}}{\lvert \Omega \rvert}$$
3. Subjetividade: $P(A)$ é escolhida baseada na experiência e subjetividade.

### Exemplo (Lançamento de Moedas)

Se usarmos o método clássico para resolver esse problema podemos estimar $P(A)$ como $3/4 = 0.75 = 75\%$.

## Manipulando Probabilidades

Se $A$ é um evento, então o evento **complementar** de $A$ é tudo aquilo que não está em $A$ e é denotado por $A'$.

Sejam as seguintes abreviações $P(A \cap B) = P(A \text{ e } B)$ e $P(A \cup B) = P(A \text{ ou } B)$.

- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$.
- $P(A') = 1 - P(A)$.
- Se $A$ e $B$ são dois eventos **independentes** então $P(A \cap B) = P(A) P(B)$.

## Probabilidade Condicional/Independência

A probabilidade condicional de um evento é obtida quando temos informações adicionais a respeito da ocorrência de outro evento.

A notação $P(B \mid A)$ pode ser lida como: a probabilidade de $B$ acontecer sabendo que $A$ aconteceu.
Seu valor é
$$P(B \mid A) = \frac{P(A \cap B)}{P(A)}$$

Logo,
$$P(B \mid A) P(A) = P(A \cap B)$$

## Teorema de Bayes

Uma versão simplificada do teorema de Bayes é
$$P(A \mid B) = \frac{P(B \mid A) P(A)}{P(A) P(B \mid A) + P(A') P( B \mid A')}$$

### Intuição/Demonstração

1. Começando de $B = (B \cap A) \cup (B \cap A')$.
2. Temos que $P(B) = P((B \cap A) \cup (B \cap A'))$.
3. $P(B) = P(B \cap A) + P(B \cap A') - P((B \cap A) \cap (B \cap A')) = P(B \cap A) + P(B \cap A') - 0$.
4. Substituindo $P(B \cap A) = P(B \mid A) P(A)$ na a expressão acima:
5. $P(B) = P(B \cap A) + P(B \cap A') = P(B \mid A) P(A) + P(B \mid A') P(A')$.
6. $P(A \mid B) = \frac{P(A \cap B)}{P(B \mid A) P(A) + P(B \mid A') P(A')}$.
7. Como $P(A \cap B) = P(B \mid A) P(A)$ chegamos ao resultado.
