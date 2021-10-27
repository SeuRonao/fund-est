---
title: Medidas de Dispersão
---

São medidas que tentam resumir, em apenas um número, a variabilidade do conjunto de dados analisados.

Para simplificar a notação, todo somatório na forma $\sum_{i = 1}^n$ será escrito como $\sum$ quando o contexto dos itens a serem somados ficar claro.

## Amplitude

É o maior valor menos o menor valor observado.

## Desvio(s)

O desvio de uma observação $x_i$ da variável $x$ é dado por:

$$d_i = x_i - \bar{x}$$

Ele representa quanto essa observação se *desvia* da média dessa variável.

## Desvio médio/absoluto

O desvio médio ou absoluto de uma variável $x$ pode ser calculado pela seguinte fórmula:

$$\mathrm{dm}(x) = \frac{\sum \lvert x_i - \bar{x} \rvert}{n} = \frac{\sum \lvert d_i \rvert}{n}$$

É a média de todos os desvios observados.

## Variância

Existem duas fórmulas para a variância de uma variável.

Uma para amostras de uma população, outra para a própria população.

### Amostras

A variância para *amostras* de uma variável $x$, $s^2$ ou $\mathrm{var_s}(x)$, pode ser calculada por:

$$\mathrm{var_s}(x) = s^2 = \frac{\sum (x_i - \bar{x})^2}{n-1} = \frac{\sum d_i^2}{n-1}$$

### População

A variância para *populações* de uma variável $x$, $\sigma^2$ ou $\mathrm{var_p}(x)$, pode ser calculada por:

$$\mathrm{var_p}(x) = \sigma^2 = \frac{\sum (x_i - \bar{x})^2}{n} = \frac{\sum d_i^2}{n}$$


## Desvio padrão

O desvio padrão é a raiz quadrada da variancia.

Existem duas fórmulas para o desvio padrão de uma variável.

Uma para amostras de uma população, outra para a própria população.

### Amostras

O desvio padrão para amostras de uma variável $x$, $s$ ou $\mathrm{dp_s}(x)$, pode ser calculado por:

$$\mathrm{dp_s}(x) = s = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n-1}}$$

Ou de forma alternativa e mais rápida:

$$\mathrm{dp_s}(x) = s = \sqrt{\frac{n(\sum x_i^2) - (\sum x_i)^2}{n(n-1)}}$$

### População

O desvio padrão para a população de uma variável $x$, $\sigma$ ou $\mathrm{dp_p}(x)$, pode ser calculado por:

$$\mathrm{dp_p}(x) = \sigma = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n}}$$

Ou de forma alternativa e mais rápida:

$$\mathrm{dp_s}(x) = \sigma = \sqrt{\frac{n(\sum x_i^2) - (\sum x_i)^2 }{n^2}}$$

### Teorema de Chebyshev

Para qualquer conjunto de dados e qualquer valor $k > 1$, existe uma proporção de pelo menos $1 - \frac{1}{k^2}$ observações da variável $x$ no intervalo $\bar{x} - k \sigma$ e $\bar{x} + k \sigma$.

Ou seja:

- pelo menos $75\%$ dos valores observados estão entre $\bar{x} - 2\sigma$ e $\bar{x} + 2\sigma$
- pelo menos $89\%$ dos valores observados estão entre $\bar{x} - 3\sigma$ e $\bar{x} + 3\sigma$.
