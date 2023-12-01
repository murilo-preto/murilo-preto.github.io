---
title: Mecanismos de transferência de calor
date: 2023-11-30 09:10 -300
categories: [UFABC, Fenômenos de transporte]
tags: [transferência,calor,condução]
math: true
image: https://ifsolutions.com/wp-content/uploads/2019/10/types-of-heat-exchangers-in-oil-and-gas-industry.jpg
---

# Módulo 3 -- Transferência de calor: Condução, Convecção e Radiação
A transferência de calor é um fenômeno que ocorre naturalmente sempre que há diferença de temperatura entre um ou mais meios. Por fim de classificação, a transferência de calor pode ocorrer através de três modos: condução, convecção e radiação.

## Modos de transferência de calor
Em uma visão geral, os modos de transferência de calor podem ser rudimentariamente descritos como:
1. Condução: Transferência de calor através do contato de partículas de dois meios estácionários.
2. Convecção: Transferência de calor através do contato de partículas em ao menos um meio em movimento.
3. Radiação: Transferência de calor através da emissão de ondas eletromagnéticas.

### Condução: mecanismo físico
A transferência ocorre através da colisão de partículas mais energéticas com partículas menos energéticas, transferindo momento no instante de contato.

![transferencia-calor-conducao](https://emerginginvestigators.org/rails/active_storage/representations/proxy/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBc2NKIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--aa8361f6d6eacb9a184b2f3e91dfc68dbd766403/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaDdCem9MWm05eWJXRjBTU0lJYW5CbkJqb0dSVlE2QzNKbGMybDZaVWtpRFRZd01IZzJNREErQmpzR1ZBPT0iLCJleHAiOm51bGwsInB1ciI6InZhcmlhdGlvbiJ9fQ==--a3b53ba1a0f83efef18f6e75a8d4ce784384bee2/Fig5_New.jpg)_Transferência de calor através de condução_

### Convecção: condução e advecção
A primeira etapa da convecção faz uso do mesmo mecanismo de transferência de calor da condução, isto é, a colisão entre partículas com maior energia a partículas com menor energia. Já a segunda etapa, dado que há movimento de partículas, as partículas aquecidas tendem a 'flutuar' através do aumento da força de empuxo pelo aquecimento, trocando de posição com partículas menos quentes. Esse ciclo de advecção implica em uma maior transferência de calor.

#### Convecção forçada e natural
Ademais, a convecção pode ser natural, ou seja, surgir em virtude da própria transferência de calor, como explicada pela advecção via aquecimento natural. Dito isso, a convecção pdoe ser estimulada forçadamente, por exemplo, ao introduzir um ventilador a um trocador de calor.

![conveccao-natural-forcada](https://www.ednasia.com/wp-content/uploads/sites/3/2021/05/fan-controls-figure-images-01-e1620421342148.jpg)_Transferência de calor através de convecção forçada e natural_

### Nomenclaturas
- $ q $ -- Calor \[J\]
- $ \dot{q} $ -- Taxa de transferência de calor \[$W$\]
- $ \dot{q}' $ -- Potência linear \[$\frac{W}{m}$\]
- $ \dot{q}'' $ -- Fluxo de calor \[$\frac{W}{m^2}$\]
- $ \dot{q}''' $ -- Densidade de potência \[$\frac{W}{m^3}$\]

### Lei de Fourier
- \$$ \large\dot{q}_{x} = -kA\frac{\partial{T}}{\partial{x}} $$
- \$$ \large\dot{q}_{x}''=\frac{\dot{q}_{x}}{A}=-k\frac{\partial{T}}{\partial{x}} $$

#### Equação de difusão de calor
$$ \large\frac{\partial{}}{\partial{x}}\left(k\frac{\partial{T}}{\partial{x}}\right) + \frac{\partial{}}{\partial{y}}\left(k\frac{\partial{T}}{\partial{y}}\right) + \frac{\partial{}}{\partial{z}}\left(k\frac{\partial{T}}{\partial{z}}\right) + q_{g}''' = \rho{}C_{p}\frac{\partial{T}}{\partial{t}} $$

## Condução em parede plana
No cenário onde a condução ocorre de maneira unidirecional, pode-se reduzir a equação de difusão de calor para: $$\frac{\partial{}}{\partial{x}}\left(k\frac{\partial{T}}{\partial{x}}\right)=0$$. Como $$\dot{q}_x''=-k\frac{\partial{T}}{\partial{x}}$$, logo $$\frac{\partial{q''}}{\partial{x}}=0$$. Então, $$\dot{q}_x''$$ ou $$-k\frac{\partial{T}}{\partial{x}}$$ é constante.

Integrando a equação obtida anteriormente em x, obtêm-se:
- \$$\int{-k\frac{\partial{T}}{\partial{x}}dx}=\int{Cdx}$$
- \$$T(x)=C_{1}x+C_{2}$$

Assim, nota-se que a temperatura varia de acordo com a distância percorrida dentro da parede unidimensional, em função de x (distância).    

![condução-parede-unidimensional](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-BAdQlBMwQo_M7nU7BTCohwtyG7A_v90D0Q&usqp=CAU)_Condução em parede unidimensional_

### Equação: temperatura total em função da distância
Tal que, de forma ingênua, pode-se deduzir uma equação simplificada para a transferência de calor via parede unidimensional:

$$ \large{}T(x)=(T_{2}-T_{1})\frac{x}{L}+T_{1} $$

Essa equação, todavia, prevê uso em condições específicas, como:
1. Condução unidimensional;
2. Regime estacionário;
3. Parede plana;
4. Sem geração de calor;
5. Condutividade térmica (k) constante.

Neste caso, espera-se que a transferência de calor deva comportar-se linearmente conforme x se aproxima de L. 

### Equação: transferência de temperatura por condução
Ignorando o coeficiente linear na equação para determinar a temperatura total, pode-se especificar a modelagem da equação de transporte:

$$ \large{}q_{x}=-kA\frac{dT}{dx}\approx{}kA\frac{T_{1}-T_{2}}{L} $$

No mesmo sentido, pode ser modelada a equação de fluxo de calor a partir da equação da taxa de transferência:

$$ \large{}q_{x}''=\frac{q_{x}}{A}\approx{}k\frac{T_{1}-T_{2}}{L} $$

### Analogia com circuitos elétricos
Assim como na lei de OHM, pode-se fazer uma relação similar entre a taxa de transferência de calor, a diferença de temperaturas e a resistência térmica. De tal forma, que muitos problemas podem ser simplificados ao montar um 'circuito térmico', que permite juntar resistências térmicas de diferentes materiais em uma conta unificada.

![analogia-circuitos](https://arquivos.respondeai.com.br/seo-mirror/theory/2023/238e3249-2554-4c6d-8b53-7540cbbb5608.webp){: .right }

Isolando na equação de transferência, pode-se obter as resistências:
- Resistência à condução: \$$R_{condução}=\frac{L}{kA}$$
- Resistência à convecção: \$$R_{convecção}=\frac{1}{hA}$$
- Resistência à radiação: \$$R_{radiação}=\frac{1}{h_{r}A}$$

## Sistemas radiais
O estudo de sistemas radiais é muito interessante, por exemplo, para a modelagem da transferência de calor em dutos e maquinários. A lei de fourier pode ser modificada para coordenadas cilíndricas com esse objetivo:

$$ \large\frac{1}{r}\frac{\partial{}}{\partial{r}}\left(kr\frac{\partial{T}}{\partial{r}}\right) + \frac{1}{r^2}\frac{\partial{}}{\partial{\phi}}\left(k\frac{\partial{T}}{\partial{\phi}}\right) + \frac{\partial{}}{\partial{z}}\left(k\frac{\partial{T}}{\partial{z}}\right) + q_{g}''' = \rho{}C_{p}\frac{\partial{T}}{\partial{t}} $$

Aplicando as mesmas simplificações, pode-se definir equação em função do raio, simplificando-a para problemas mais simples. Nesse caso, nota-se igualmente que um dos fatores deve ser constante para comportar as derivações.

$$ \large{}kr\frac{dT}{dr}=cte $$

Assim, obtêm se a família de soluções:

$$ \large{}T(r)=C_{1}\left(\ln{r}\right)+C_{2} $$

De tal forma que a resistência térmica pode ser definida como, para um **cilíndro oco**, por exemplo:

$$ \Large{}R_{t,condução}=\frac{\ln{}\left(\frac{r_2}{r_1}\right)}{2k\pi{}L} $$

![radial-composite](https://www.researchgate.net/publication/274075198/figure/fig1/AS:294743461384192@1447283725382/Oil-well-architecture-as-a-composite-cylindrical-wall.png)_Sistema radial com paredes compostas_

## Formulação concentrada
### Condução em regime transiente

