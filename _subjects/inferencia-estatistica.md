---
title: Inferência Estatística
order: 7
header:
  teaser: /assets/images/teasers/magnifying-glass-500x300.jpg
---
A **inferência estatística** é o nome que se dá ao conjunto de técnicas utilizadas para *estimar* o valor de uma característica de uma população baseado em algum valor de uma amostra dessa população.

## Definições

### População

Conjunto de todos os dados a ser estudado.

#### Parâmetro

Uma característica da população.

### Amostra

Parte do conjunto de dados a ser estudado.

#### Estatística

Uma característica da amostra.

### Estimador

É quando associamos uma *estatística* com um *parâmetro*.

Ou seja, usamos uma estatística para inferir o valor de um parâmetro.

### Vies

Considerando $n$ o tamanho de uma amostra de uma população.

Um estimador **não-viesado** é aquele que se aproxima do valor de seu parâmetro quando $n$ é grande o suficiente.

### Consistência

Considerando $n$ o tamanho de uma amostra de uma população.

Um estimador **consistente** é aquele que tem desvio padrão se aproximando de zero quando $n$ é grande o suficiente.


## Teorema do Limite Central

Seja $x$ uma variável aleatória qualquer com média $\mu$ e variância $\sigma^2$.

Seja $\\{X_1, X_2, X_3, \ldots, X_n\\}$ uma amostra aleatória simples com repetição de $x$, o *Teorema do Limite Central* diz que $X \sim N(\mu; \sigma/\sqrt{n})$.

Ou seja, independentemente do tipo de distribuição de $x$,
uma amostra aleatória simples de $x$ tem distribuição aproximadamente normal com média igual à media de $x$ e variância inversamente proporcional ao tamanho da amostra.

## Estimação Pontual de Proporções

Seja $p$ uma proporção de uma população.
A quantidade de pessoas que aprova um certo projeto de lei, por exemplo.

Seja $\hat{p}$ um proporção de uma amostra dessa população.

Queremos estimar o valor de $p$ baseado no valor de $\hat{p}$.

> Como $\hat{p}$ é uma característica de uma amostra, ele pode se aproximar ou se distanciar de $p$ a depender de qual amostra específica colhemos.
{: .notice--warning}

### Exemplo

Em uma enquete 1500 adultos foram entrevistados e 45% deles responderam que utilizam o Instagram.

Baseado nesse resultado encontre uma estimativa para a proporção de adultos, dentre todos os adultos, que utilizam o Instagram.

#### Resposta

A proporção $p$ de **todos** os adultos que utilizam o Instagram, pode ser estimada baseada na proporção $\hat{p}$ dos adultos entrevistados.

Como $\hat{p}$ é uma estatística e assumindo que a enquete parte de uma amostra aleatória simples.
Pelo [Teorema do Limite Central](#teorema-do-limite-central) temos que:

$$\hat{p} \sim N\left(p; \sqrt{\frac{p(1-p)}{n}}\right)$$

Ou seja:

- Como em média $\hat{p}$ é igual à $p$ temos que $\hat{p}$ é um estimador não-viesado.
- Como $\mathrm{dp}(\hat{p}) \approx 0$ quando $n \rightarrow \infty$ temos que $\hat{p}$ é um estimador consistente.

## Estimação Intervalar

### Intervalo de Confiança ou Margem de Erro

É um *intervalo* de valores usados para estimar o real valor do parâmetro em questão.

### Nível de Confiança

É a probabilidade $1 - \alpha$ do intervalo de confiança conter realmente o parâmetro estudado.

## Exemplo de Estimação Intervalar de Proporções

Considerando o estimador $\hat{p}$ para $p$ no exemplo anterior.

Antes mesmo de colhermos a amostra, supondo que $n = 1500$.

Pelo [TLC](#teorema-do-limite-central) sabemos que $\hat{p} \sim N\left(p; \sqrt{\frac{p(1-p)}{n}}\right)$.

Logo, podemos calcular a probabilidade de $\hat{p}$ diferir de $p$ em um valor $e$ por exemplo:

$$P(\lvert \hat{p} - p \rvert \leq e)$$

De forma mais específica, podemos inclusive escolher um valor $1 - \alpha$ para essa probabilidade...

$$P(\lvert \hat{p} - p \rvert \leq e) = 1 - \alpha$$

Fazendo algumas simplificações chegamos em:

$$P(\hat{p} - e \leq p \leq \hat{p} + e) = 1 - \alpha$$

Ou seja, a chance de $p$ estar entre $\hat{p} - e$ e $\hat{p} + e$ contenha realmente o parâmetro $p$ é de $1 - \alpha$$.

Como essa distribuição é normal, podemos escolher ou o tamanho da margem de erro $e$, ou o valor de $\alpha$ mas não ambos.

Caso façamos o *comum* e fixemos o valor de $\alpha$ em $0.05$:

$$P(\hat{p} - e \leq p \leq \hat{p} + e) = 1 - 0.05$$

$$P(\hat{p} - e \leq p \leq \hat{p} + e) = 0.95$$

Necessariamente, temos que $e = 1.96\sqrt{\frac{p(1-p)}{n}}$:

$$P\left(\hat{p} - 1.96\sqrt{\frac{p(1-p)}{n}} \leq p \leq \hat{p} + 1.96\sqrt{\frac{p(1-p)}{n}}\right) = 0.95$$

Finalmente, caso seja impossível saber o valor de $\sigma$ que é também um parâmetro da população podemos aproximar, nesse caso, por $\hat{p}(1 - \hat{p})$.
Assim terminamos com:

$$P\left(\hat{p} - 1.96\sqrt{\frac{\hat{p}(1-\hat{p})}{n}} \leq p \leq \hat{p} + 1.96\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right) = 0.95$$

Ou seja, fixando $\alpha$ em $0.05$:

- O intervalo de confiança é dado por:
  $$\left[\hat{p} - 1.96\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}, \hat{p} + 1.96\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}\right]$$
- O nível de confiança é de $1 - \alpha = 0.95$.

Substituindo em valores:

- **Proporção encontrada**: $\hat{p} = 0.45$, do exemplo anterior.
- **Intervalo de Confiança**: $\left[0.45 - 1.96 \cdot 0.012, 0.45 + 1.96 \cdot 0.012 \right] = \left[0.424, 0.475\right]$.
- **Nível de Confiança**: $0.95$.

### Procedimento para Estimação Intervalar de Proporções

1. Defina o valor de $\alpha$.
2. Calcule, baseado em $Z = N(0; 1)$ qual valor $e$ que satisfaz:
   $$P(-e \leq Z \leq e) = 1 - \alpha$$
3. Colha a amostra $\hat{p}$ de tamanho $n$.
4. Calcule $E = e\sqrt{\frac{\hat{p} (1 - \hat{p})}{n}}$
5. O intervalo de confiança: $\left[\hat{p} - E, \hat{p} + E\right]$.
6. O nível de confiança: $1 - \alpha$.

> Caso se deseje uma margem de erro fixa $E$, em vez de escolher o tamanho de $n$ é possível substituir $e\sqrt{\frac{\hat{p} (1 - \hat{p})}{n}}$ por $e\sqrt{\frac{0.25}{n}}$
{: .notice}

## Estimação Pontual de Médias

Seja $\mu$ uma média de uma variável aleatória baseada em uma população.
Por exemplo, a altura das pessoas em uma certa idade.

Seja $x = \\{x_1, x_2, \ldots, x_n\\}$ uma amostra aleatória simples dessa população.

Queremos estimar o valor de $\mu$ baseado no valor de $\bar{x}$.

> Como $\bar{x}$ é uma característica de uma amostra, ele pode se aproximar ou se distanciar de $\mu$ a depender de qual amostra específica colhemos.
{: .notice--warning}

### Procedimento para Estimação Intervalar de Proporções

Seja $x$ uma v.a. qualquer de uma população, por exemplo, a altura.
Suponha que $\mu$ é desconhecida e que $\sigma$ é conhecida para facilitar a análise.

Seja $X = \\{X_1, X_2, \ldots, X_n\\}$ uma amostra aleatória simples de $x$.

Pelo [TLC](#teorema-do-limite-central): $\bar{X} \sim N\left(\mu; \frac{\sigma}{\sqrt{n}}\right)$.

Ou seja, dada uma margem de erro $e$ e um nível de confiança $1 - \alpha$ podemos calcular:

$$ P\left(\bar{X} - e \leq \mu \leq \bar{X} + e\right) = 1 - \alpha $$

Do mesmo modo que no exemplo anterior, se usarmos $\alpha = 0.05$:

$$ P\left(\bar{X} - 1.96 \frac{\sigma}{\sqrt{n}} \leq \mu \leq \bar{X} + 1.96 \frac{\sigma}{\sqrt{n}} \right) = 1 - \alpha $$

**Resumo**:

1. Defina o valor de $\alpha$.
2. Calcule, baseado em $Z = N(0; 1)$ qual valor $e$ que satisfaz:
   $$P(-e \leq Z \leq e) = 1 - \alpha$$
3. Colha a amostra $\bar{X}$ de tamanho $n$.
4. Fazendo $E = 1.96 \sigma/\sqrt{n}$
5. O intervalo de confiança: $\left[\bar{X} - E, \bar{X} + E\right]$.
6. O nível de confiança: $1 - \alpha$.
