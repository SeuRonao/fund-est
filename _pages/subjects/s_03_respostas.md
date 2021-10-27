---
title: Respostas dos Exercícios
toc: false
---

1. $\sum_{i = 1}^6 3$

   Esse somatório está dizendo que $f(i) = 3$.

   $$\sum_{i = 1}^6 3 = f(1) + f(2) + f(3) + f(4) + f(5) + f(6)$$

   $$\sum_{i = 1}^6 3 = 3 + 3 + 3 + 3 + 3 + 3 = 6 \cdot 3 = 18$$
2. $\sum_{i = 4}^3 f(i)$

   Quando o somatório tem o *começo* maior que o *fim* vamos ter que aplicar $f(i)$ em um conjunto vazio de elementos.
   Assim por convenção o resultado de uma soma vazia de parcelas é *zero*.

   $$\sum_{i = 4}^3 f(i) = 0$$

3. $\sum_{i = 1}^4 \sum_{j = 3}^i i + j$

   O que temos aqui é um somatório aninhado em outro.
   No caso $\sum_{i=1}^4 f(i)$, com $f(i) = \sum_{j = 3}^i i + j$.

   $$\sum_{i = 1}^4 \left(\sum_{j = 3}^i i + j\right)$$

   $$\sum_{i = 1}^4 f(i) = f(1) + f(2) + f(3) + f(4)$$

   $$\sum_{i = 1}^4 f(i) = \left(\sum_{j = 3}^1 1 + j\right) + \left(\sum_{j = 3}^2 2 + j\right) + \left(\sum_{j = 3}^3 3 + j\right) + \left(\sum_{j = 3}^4 4 + j\right)$$

   - $\sum_{j = 3}^1 1 + j = 0$
   - $\sum_{j = 3}^2 2 + j = 0$
   - $\sum_{j = 3}^3 3 + j = 3 + 3 = 6$
   - $\sum_{j = 3}^4 4 + j = (4 + 3) + (4 + 4) = 15$

   $$\sum_{i = 1}^4 f(i) = 0 + 0 + 6 + 15 = 21$$

4. $\sum_{i = 1}^{50} 5i + 7 + \sqrt{i}$, pode usar gerenciador de planilha.

   Usando um gerenciador de planilha pode se encontrar o valor de aproximadamente 6964.04
