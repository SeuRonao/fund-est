---
title: Variáveis Aleatórias
---

É uma forma de resumir *a parte interessante* de um experimento aleatório.

## Exemplo

Seja o experimento aleatório em que uma pessoa é sorteada ao acaso.

Dependendo do estudo, pode-se ter interesse em saber a altura dessa pessoa, o peso, a quantidade de filhos, o grau de escolaridade, quantas calorias ela ingere por semana, se ela apoia ou não um projeto de lei.

Uma variável aleatória é uma função que associa um número ao resultado de um evento.
Por exemplo, associar o resultado de selecionar uma pessoa à altura dessa pessoa.

## Variáveis Aleatórias Discretas

É uma variável que associa um resultado em $\Omega$ à *um número inteiro*.

### Exemplos

- A quantidade de caras em um lançamento de $n$ moedas.
- A quantidade de filhos de uma pessoa selecionada aleatoriamente.
- A soma dos números em um lançamento de $n$ dados.

### Distribuição de Probabilidade

Dado um experimento aleatório com espaço amostral $\Omega$ e uma variável aleatória discreta $x$.

- Todo evento $A$ está associado à algum resultado de $x$.
- $P(x = k)$ é a probabilidade de ocorrer algum evento associado ao valor $k$.
  Ou seja, no caso de um lançamento de $n$ moedas e $x$ ser o número de caras, $P(x = 3)$ é a probabilidade de sairem exatamente $3$ caras nesse lançamento.
- $0 \leq P(x = k) \leq 1$ qualquer que seja $k$.
- $\sum_i P(x = i) = 1$.

### Parâmetros de uma v.a. $x$

- A média $\mu_x$:
  $$\mu_x = \sum_k k \cdot P(x = k)$$
- Variância $\sigma^2_x$:
  $$\sigma^2_x = \sum_k (k - \mu_x)^2 \cdot P(x = k)$$
  ou
  $$\sigma^2_x = \sum_k (k^2\cdot P(x = k)) - \mu^2_x$$
- Desvio padrão $\sigma_x$
  $$\sigma_x = \sqrt{\sum_k (k^2\cdot P(x = k)) - \mu^2_x}$$

O valor esperado $E(x)$ é dado por $\mu_x$.


## Distribuição Binomial

Considere um experimento aleatório que consiste em fazer vários testes com as seguintes caracteristicas:

- Número fixo de testes.
- Testes *independentes* entre si.
- Cada teste pode dar *sucesso* ou *falha*.
- Todos os testes tem a mesma chance de sucesso.

Dizemos que a v.a. que mede o número de sucessos desse tipo de experimento possui distribuição **binomial**.

Seja $p$ a chance de sucesso em *um* único teste, $q = 1 - p$ e $n$ o total de testes.

$$P(x = k) = \binom{n}{k} p^k q^{n - k}$$
ou
$$P(x = k) = \frac{n!}{(n - k)! k!} p^k q^{n - k}$$

### Parâmetros da distribuição de Probabilidade Binomial

- Média: $\mu = np$
- Variância: $\sigma^2 = npq$
- Desvio padrão: $\sigma = \sqrt{npq}$

#### Observação

É muito difícil que ao realizar o experimento você encontre algum valor de $x$ muito longe, i.e. $\mu \pm 2\sigma$ da média com esse tipo de distribuição.

## Variáveis Aleatórias Contínuas

É uma variável que associa um resultado em $\Omega$ à um número real.

### Exemplos

- A altura de uma pessoa.
- A taxa de glicose no sangue em jejum.
- A quantidade em gramas de chocolate que vem de fato em um pacote.

### Função de Densidade de Probabilidade

Dado um experimento aleatório com uma v.a. contínua $x$.

Suponha que $x$ seja a altura de uma pessoa, qual a chance de encontrarmos uma pessoa com *exatamente* $1.70$m.
Nem um átomo de altura à mais nem a menos do que isso.
Extrapolando esse conceito para qualquer outro valor $k$ de altura temos o mesmo problema.
Ou seja, $P(x = k) = 0$ qualquer que seja $k$ para uma variável contínua.

Claramente temos que $P(0 \leq x \leq 2)$ não é zero pois é relativamente fácil encontrar alguem com menos de dois metros de altura.

Ou seja, teremos que mudar um pouco os conceitos para que a probabilidade de uma v.a. contínua faça sentido.

Seja $f(x)$ a **função de densidade de probabilidade** de $x$ isso significa que:
$$P(a \leq x \leq b) = \int^b_a f(x)$$
Em outras palavras, $P(a \leq x \leq b)$ é a área abaixo da curva comecando em $a$ e terminando em $b$ quando fazemos o desenho de $f(x)$ no plano cartesiano.

Uma função de densidade de probabilidade é tal que a área total da curva tem que ser **exatamente** um.

#### Exemplos

{% include figure image_path="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Uniform_Distribution_PDF_SVG.svg/250px-Uniform_Distribution_PDF_SVG.svg.png" alt="Exemplo de Função de Densidade de Probabilidade" caption="Exemplo de Função de Densidade de Probabilidade 1"%}

{% include figure image_path="https://upload.wikimedia.org/wikipedia/commons/thumb/6/63/Uniform_cdf.svg/250px-Uniform_cdf.svg.png" alt="Exemplo de Função de Densidade de Probabilidade" caption="Exemplo de Função de Densidade de Probabilidade 2" %}

Várias curvas normais:

{% include figure image_path="https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Normal_Distribution_PDF.svg/1200px-Normal_Distribution_PDF.svg.png" alt="Exemplos de Curvas Normais" caption="Exemplos de Curvas Normais" %}

### Distribuição Normal

A distribuição normal é uma v.a. que tem função de densidade de probabilidade:
$$f(x) = \frac{1}{\sigma \sqrt{2\pi}}e^{\frac{1}{2}\left(\frac{x - \mu}{\sigma}\right)^2}$$

Aonde $\sigma$ e $\mu$ são valores escolhidos.
Por definição uma v.a. que tenha uma função de densidade de probabilidade acima é tal que ela tem média $\mu$ e desvio padrão $\sigma$.

Vamos denotar uma v.a. normal com média $\mu$ e desvio padrão $\sigma$ como $x \sim N(\mu; \sigma)$.

#### Distribuição Normal Padrão

A v.a. $Z \sim N(0; 1)$ é comumente chamada de distribuição normal padrão.
Obviamente, ela tem média $0$ e desvio padrão $1$.

## Aproximação da Binomial à Normal

- Seja $x$ uma v.a. binomial com $10.000$ testes e $p = 0.5$.
- $\mu_x = np = 5000$, $\sigma_x = \sqrt{npq} = \sqrt{2500} = 50$.
- Tente calcular $P(4900 \leq x)$.
  No mínimo você tera que calcular:
  $$\binom{5000}{4900} = \frac{5000!}{100!4900!}$$
  Boa sorte.
- Por outro lado, uma curva binomial parece muito com uma curva normal quando a quantidade de testes é grande:
  {% include figure image_path="https://wiki.analytica.com/images/1/14/BinomialDistribution.png" alt="Curva Binomial" caption="Curva Binomial com 100 testes e 0.3 chance de sucesso" %}
- Assim, podemos usar a curva normal no lugar da binomial para fazer as contas.

### Exemplo

- Vamos fazer o cálculo acima usando uma curva normal em vez da binomial.
- Como $x$ tem média $\mu_x = 5.000$ e $\sigma = 50$, temos que utilizar a curva normal $N(5.000; 50)$.
- Se no lugar usarmos $x \sim N(5.000; 50)$ podemos calcular $P(4900 \leq x)$ de forma [direta](https://homepage.divms.uiowa.edu/~mbognar/applets/normal.html) que resulta em $0.97725$.
