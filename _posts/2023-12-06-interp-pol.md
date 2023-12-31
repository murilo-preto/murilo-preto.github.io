---
title: Interpolação Polinomial
date: 2023-12-06 17:45 -300
categories: [UFABC, Cálculo Numérico]
tags: [calculo, numerico]
math: true
---

# Método da interpolação polinomial

A interpolação polinomial visa permitir interpolar dados próximos a valores tabelados, modelando um conjunto de pontos em uma função, cujo grau varia de acordo com a quantidade de pontos considerados para o método.

## Método de Lagrange

O método de Lagrange aparece como a soma de funções polinomiais calculadas para cada ponto experimental. Na forma de:

$$ P(x)=f(x)\_0\cdot{}L(x)\_0+f(x)\_1\cdot{}L(x)\_1+...+f(x)\_n\cdot{}L(x)\_n $$

$$ L\_{i}(x)=\frac{(x-x_0)(x-x_1)...(x-x_n)}{(x_i-x_0)(x_i-x_1)...(x_i-x_n)} $$

### Exemplo

Dado o conjunto de pontos:

|  x  | f(x) |
| :-: | :--: |
| -1  |  4   |
|  0  |  1   |
|  2  |  -1  |

Pode-se utilizar o método de interpolação polinomial de Lagrange para determinar uma função que os aproxime razoavelmente bem:

- \$$P(x)=f(x)_0\cdot{}L(x)_0+f(x)_1\cdot{}L(x)_1f(x)_n\cdot{}L(x)_n$$
- \$$L_{i}(x)=\frac{(x-x_0)(x-x_1)...(x-x_n)}{(x_i-x_0)(x_i-x_1)...(x_i-x_n)}$$

Para, respectivamente, os pontos: 1, 2 e 3; temos as funções L:

1. \$$L_0=\frac{(x-x_1)(x-x_2)}{(x_0-x_1)(x_0-x_2)}=\frac{(x-0)(x-2)}{(-1-0)(-1-2)}=\frac{x^2-2x}{3}$$
2. \$$L_1=\frac{(x-x_0)(x-x_2)}{(x_1-x_0)(x_1-x_2)}=\frac{(x+1)(x-2)}{(1)(-2)}=-\frac{x^2-x-2}{2}$$
3. \$$L_2=\frac{(x-x_0)(x-x_1)}{(x_2-x_0)(x_2-x_1)}=\frac{(x+1)(x)}{(2+1)(2)}=\frac{x^2+x}{6}$$

Plugando esses valores na função de P(x), temos:

$$ P(x)=4\frac{x^2-2x}{3}+1\frac{x^2-x-2}{-2}-1\frac{x^2+x}{6} $$

Que, simplificando, aparece na forma:

$$ P(x)=\frac{2}{3}x^2-\frac{7}{3}x+1 $$

## Método de Newton

A princípio, uma referência valiosa para o estudo desse método pode ser encontrada no vídeo incorporado a seguir:

<iframe width="560" height="315" src="https://www.youtube.com/embed/yuMjQPFiBe8?si=wqeBXG3rcmuBx5gg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Dito isso, o ponto principal desse método é permitir a interpolação através do cálculo de coeficientes através da variação entre os pontos experimentais.

Para isso, os pontos devem ser dispostos em um diagrama do tipo:

![diagrama-Newton](https://arquivos.respondeai.com.br/seo-mirror/theory/2023/7f2139d3-7635-42dc-a045-7d9506796640.webp)_Montagem do sistema para método de Newton_

De forma que a variação entre os pontos deve ser calculada pela diferença. Feito isso, basta montar a equação seguindo a fórmula:

$$ f(x)=a_0+a_1(x-x_0)+a_2(x-x_0)(x-x_1) $$

E obtêm-se o polinômio interpolador de Newton.

### Erro associado

Pode-se calcular o erro máximo de uma função, por exemplo, no segundo grau, a partir da expressão:

$$ Err(x)=\frac{(x-x_0)(x-x_1)(x-x_2)}{3!}\cdot{}\max{}f^{(3)}(\epsilon) $$

Tal que $$\max{}f^{(3)}$$ é o valor máximo da terceira derivada -- da função original -- no ponto $$x$$ onde deseja-se determinar o limite de erro máximo.
