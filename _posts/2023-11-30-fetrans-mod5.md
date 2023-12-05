---
title: Escoamento interno e transferência de calor em dutos
date: 2023-11-30 10:07 -300
categories: [UFABC, Fenômenos de transporte]
tags: [transferência,calor,escoamento]
image: https://www.compadre.org/nexusph/course/images/Matter/HPSimpleModel.jpg
math: True
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

# Transferência de calor em dutos
Em tubulações, o calor é transferido ao fluido de forma a determinar um gradiente radial e axial para a variação da temperatura. Assim, é necessário ter um cuidado especial ao determinar a temperatura de referência.

## Exemplo
Água escoa através de um duto aquecido de 3 cm de diâmetro com velocidade média de 1 m/s. A temperatura de mistura da água na entrada da seção de aquecimento é igual a 18 °C. São transferidos 20 kW de potência para a água. Calcule a temperatura de mistura da água no ponto em que ela deixa o tubo.Despreze variações de energia cinética e potencial.

- \$$\overrightarrow{v}=1\frac{m}{s}$$
- \$$T_{m,e}=18°C$$
- \$$2r=3cm$$
- \$$\dot{q}=20kW$$
- \$$T_{m,s}=?$$

$$ T_{m,s}=\frac{\dot{q}''\cdot{}P\cdot{}x}{\dot{M}\cdot{}C_{p}}+T_{m,e} $$

$$ \dot{q}''=\frac{\dot{q}}{A_{s}}\to{}\dot{q}=q''\cdot{}A_{s} $$

$$ \dot{M}=\rho{}\cdot{}\overrightarrow{v}\cdot{}A_{t} $$

$$ T_{prop}=\frac{T_{m,a}+T_{m,s}}{2} $$

Estimando a temperatura final como sendo de 62°C, temos:

- \$$T_{prop}=\frac{18+62}{2}=40°C$$
- \$$\rho=992.3\frac{kg}{m^3}$$
- \$$C_p=4.179\frac{kJ}{kg\cdot{}°C}$$

$$ A_t=\frac{\pi{}D^2}{4}=7.07\cdot{}10^{-4}m^2 $$

$$ \dot{M}=992.3\cdot{}1\cdot{}7.07\cdot{}10^{-4}=0.7\frac{kg}{s} $$

$$ T_{m,s}=\frac{\dot{Q}}{\dot{M}\cdot{C_p}}+T_{m,e}=24.8°C $$

Como o valor obtido 24.8°C é diferente do valor estimado de 62°C, deve-se tentar novamente, tomando o valor obtido como novo valor estimado. Estimando agora o valor de 22°C:

- \$$ T_{prop}=\frac{18+22}{2}=20°C $$
- \$$ \rho=998.3\frac{kg}{m^3} $$
- \$$ C_{p}=4.182\frac{kJ}{kg\cdot{°C}} $$

$$ \dot{M}=0.705\frac{kg}{s} $$

$$ T_{m,s}=24.77°C $$

O novo valor indica também uma temperatura próxima de 24.8°C, fortalecendo a hipótese de que essa é a temperatura final. A baixa variabilidade entre as estimativas ocorre devido a pouca variação da densidade da água com variações em temperatura.
