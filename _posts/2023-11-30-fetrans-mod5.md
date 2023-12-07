---
title: Escoamento interno e transferência de calor em dutos
date: 2023-11-30 10:07 -300
categories: [UFABC, Fenômenos de transporte]
tags: [transferência,calor,escoamento]
image: https://www.compadre.org/nexusph/course/images/Matter/HPSimpleModel.jpg
math: True
---

# Escoamento interno e transferência de calor em dutos

## Perda de carga

### Região de entrada fluidodinâmica
Em virtude dos efeitos viscosos, a velocidade do fluido varia ao percorrer um duto, como consequência do princípio do não-deslizamento. Conforme o fluido percorre o duto, os efeitos de viscosidade tendem a aumentar, até atingir a região de camada limite, onde a velocidade do fluido é estabilizada.

### Variação radial
Assim, pensando em como a variação radial afeta a área de escoamento, pode-se modelar a velocidade como variando de acordo com a aproximação do ponto central (da área) ao raio efetivo da tubulação.

### Forças viscosas
Ademais, as forças viscosas que agem no sentido contrário ao fluxo do fluido podem ser consideradas como atrito, e geralmente a perda de carga (head-loss) ocorre na transformação de energia cinética em calor. Assim, essa perda deve ser considerada no cálculo da potência necessária para o escoamento do fluido desejado.

Essa perda de carga pode ocorrer de forma distribuída, constante em relação ao comprimento do duto, ou localizada -- por exemplo, em uma curva aguda ou válvula. Ao final, essas perdas de carga devem ser somadas para que seja obtida a perda de carga total.

### Escoamento por diferença de pressão
Também é possível pensar na força de escoamento como a diferença de pressão no sentido favorável ao escoamento e no sentido contrário. De forma que só ocorrera o escoamento caso a pressão no sentido desejado supere a pressão contrária. Caso o balanço seja nulo, isso indicaria que o fluido está estacionário.

### Fator de atrito
Para calcular a relação entre o atrito e o escoamento do fluido, determina-se o valor adimensional **Fator de atrito**, que relaciona a *rugosidade relativa* (tabelada por material, lembrar de converter para metros) e o *número de Reynolds*. Pode-se utilizar o **Diagrama de Moody** para determinar o *fator de atrito*.

### Dutos de seção não circular
Caso o duto não seja perfeitamente radial, pode-se utilizar o diâmetro hidráulico como substituto para cálculos (aproximação).

### Perda de carga localizada
Deve ser cálculada utilizando valores tabelados para diferentes junções e equipamentos, de acordo com o diâmetro especificado.

## Transferência de calor em dutos
Em tubulações, o calor é transferido ao fluido de forma a determinar um gradiente radial e axial para a variação da temperatura. Assim, é necessário ter um cuidado especial ao determinar a temperatura de referência.

### Exemplo
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

## Cálculo do coeficiente convectivo

### Escoamento laminar

### Escoamento turbilento

### Exemplo 1
Ar seco escoando com vazão mássica de $$0.987\frac{kg}{h}$$ será aquecido passando através de uma tubulação aquecida eletricamente. O diâmetro interno do tubo é de $$1cm$$ e a seção de aquecimento possui $$0.5m$$ de comprimento. A seção de aquecimento é precedida por uma seção de tubulação sem aquecimento, de tal maneira que o escoamento entra na seção de aquecimento com perfil de velocidades completamente desenvolvido. Sabendo que a temperatura da parede da tubulação não pode exceder $$200°C$$ e que a temperatura da entrada corresponde a $$20°C$$, qual será a temperatura máxima do ar que deixa a seção de
aquecimento?

Informações
- \$\dot{M}=0.987\frac{kg}{h}$$$
- \$$d_{int}=1cm$$
- \$$L=0.5m$$
- Perfil de velocidade completamente desenvolvido
- \$$T_{parede}\le{}200°C$$
- \$$T_{entrada}=20°C$$
- \$$T_{saida-max}=?$$

Considerações
1. Duto circular
2. \$$T_{prop}=\frac{T_e+T_s}{2}$$

Estimando $$T_s=100°C$$ na primeira iteração, temos $$T{prop}=60°C$$.
- \$$C_p=1.008\frac{kJ}{kg\cdot{}°C}$$
- \$$\rho=1.0596\frac{kg}{m^3}$$
- \$$v=18.9\cdot{}10^{-6}$$
- \$$k=28.52\cdot{}10^{-3}$$
- \$$Pr=0.708$$

3. $$Re_d=\frac{v\cdot{}D}{v}$$

$$ \dot{M}=\rho{}\cdot{}v\cdot{}A\cdot{}t $$

$$ A_t=\frac{\pi\cdot{}(0.01)^2}{4}=7.8\cdot{}10^{-5}m^2 $$

$$ \frac{0.987}{3600}=1.0596\cdot{}v\cdot{}7.8\cdot{}10^{-5} $$

$$ v=3.3\frac{m}{s} $$

$$ Re_d=\frac{3.3\cdot{}0.01}{18.9\cdot{}10^{-6}}=1746\to{}\text{Laminar} $$

4. Problema de Q constante
5. $$Nu_x$$ (ponto de saída)
6. Caso 2

$$ Pe\frac{d}{L}=Re\cdot{}P\cdot{}\frac{d}{L} $$

$$ 1746\cdot{}0.708\cdot{}\frac{0.01}{0.5}=27.24\to{}27.24\lt{}1000 $$

7. \$$Nu_x=4.36$$
8. \$$h_x=\frac{Nu_x\cdot{}K_f}{D}$$

$$ h_x=\frac{4.36\cdot{}28.52\cdot{}10^{-3}}{0.01}=11.56\cdot{}\frac{W}{m^2\cdot{}°C} $$

9. \$$T_{m,s}=\frac{\dot{q}''\cdot{}A_s}{\dot{M}\cdot{}C_p}+T_{m,e}$$

$$ \dot{q}''=h_x\cdot{}(T_p-T_{m,s}) $$

$$ T_{m,s}=\frac{h_x\cdot{}(T_p-T_s)\cdot{}A_s}{\dot{M}\cdot{}C_p}+T_e $$

$$ A_s=\pi{}\cdot{}D\cdot{}L=\pi{}\cdot{}0.01\cdot{}0.5=0.02m^2 $$

$$ T_{m,s}=\frac{11.56\cdot{}(200-T_{m,s})\cdot{}0.02}{\frac{0.987}{3600}\cdot{}1.008\cdot{}10^3}+20 $$

$$ \large{}T_{m,s}=91.3°C $$