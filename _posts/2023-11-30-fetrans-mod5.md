---
title: Escoamento interno e transferência de calor em dutos
date: 2023-11-30 10:07 -300
categories: [UFABC, Fenômenos de transporte]
tags: [transferência,calor,escoamento]
image: https://www.compadre.org/nexusph/course/images/Matter/HPSimpleModel.jpg
---

# Perda de carga

## Região de entrada fluidodinâmica
Em virtude dos efeitos viscosos, a velocidade do fluido varia ao percorrer um duto, como consequência do princípio do não-deslizamento. Conforme o fluido percorre o duto, os efeitos de viscosidade tendem a aumentar, até atingir a região de camada limite, onde a velocidade do fluido é estabilizada.

## Variação radial
Assim, pensando em como a variação radial afeta a área de escoamento, pode-se modelar a velocidade como variando de acordo com a aproximação do ponto central (da área) ao raio efetivo da tubulação.

## Forças viscosas
Ademais, as forças viscosas que agem no sentido contrário ao fluxo do fluido podem ser consideradas como atrito, e geralmente a perda de carga (head-loss) ocorre na transformação de energia cinética em calor. Assim, essa perda deve ser considerada no cálculo da potência necessária para o escoamento do fluido desejado.

Essa perda de carga pode ocorrer de forma distribuída, constante em relação ao comprimento do duto, ou localizada -- por exemplo, em uma curva aguda ou válvula. Ao final, essas perdas de carga devem ser somadas para que seja obtida a perda de carga total.

## Escoamento por diferença de pressão
Também é possível pensar na força de escoamento como a diferença de pressão no sentido favorável ao escoamento e no sentido contrário. De forma que só ocorrera o escoamento caso a pressão no sentido desejado supere a pressão contrária. Caso o balanço seja nulo, isso indicaria que o fluido está estacionário.

## Fator de atrito
Para calcular a relação entre o atrito e o escoamento do fluido, determina-se o valor adimensional **Fator de atrito**, que relaciona a *rugosidade relativa* (tabelada por material, lembrar de converter para metros) e o *número de Reynolds*. Pode-se utilizar o **Diagrama de Moody** para determinar o *fator de atrito*.

## Dutos de seção não circular
Caso o duto não seja perfeitamente radial, pode-se utilizar o diâmetro hidráulico como substituto para cálculos (aproximação).

## Perda de carga localizada
Deve ser cálculada utilizando valores tabelados para diferentes junções e equipamentos, de acordo com o diâmetro especificado.


