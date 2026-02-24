# Cálculo Diferencial e Integral

## De onde surgem as ideias?

-> Cálculo de áreas (Integral)  
-> Cálculo de retas tangentes (Diferencial)

Para uma reta:

$$
\tan(\theta) = \frac{\Delta y}{\Delta x}
$$

A ideia central é aproximar curvas por objetos mais simples (retas), capturando seu comportamento local.

---

## A ideia básica do cálculo

### Cálculo Integral (Área)

Queremos calcular áreas de figuras mais complexas.

Considere aproximações sucessivas:

$$
A_3 > A_2 > A_1
$$

Onde cada $A_n$ representa uma aproximação por um polígono com $n$ lados.

Exemplo: aproximação de um círculo por polígonos regulares.

À medida que aumentamos o valor de $n$, a aproximação melhora.

No limite:

$$
n \to \infty
$$

a aproximação tende exatamente à área da figura.

Esse processo é conhecido como método da exaustão.

Historicamente, Arquimedes utilizou esse método para estimar o valor de $\pi$:

$$
3.1408 < \pi < 3.1428
$$

---

## Problema

Mas como obter o valor exato da área de um círculo?

Vamos explorar isso.

---

## Área de um círculo

A ideia é decompor o círculo em vários triângulos.

Se o número de divisões for muito grande, podemos aproximar a área total pela soma das áreas desses triângulos.

Seja:

- $n$ = número de triângulos

Então:

$$
A \approx n \cdot A_T
$$

Cada triângulo possui área:

$$
A_T = \frac{1}{2} ab \sin(\theta)
$$

No caso do círculo:

$$
A \approx n \cdot \frac{1}{2} R^2 \sin(\theta)
$$

onde:

$$
\theta = \frac{2\pi}{n}
$$

Logo:

$$
A \approx \frac{1}{2} R^2 \cdot n \cdot \sin\left(\frac{2\pi}{n}\right)
$$

---

## Passagem ao limite

Para ângulos pequenos:

$$
\sin(\theta) \approx \tan(\theta) \approx \theta
$$

Quando:

$$
n \to \infty
$$

temos:

$$
\sin\left(\frac{2\pi}{n}\right) \approx \frac{2\pi}{n}
$$

Substituindo:

$$
A \approx \frac{1}{2} R^2 \cdot n \cdot \frac{2\pi}{n}
$$

Simplificando:

$$
A = \pi R^2
$$

---

## Conclusão

A área do círculo pode ser obtida como o limite de uma soma de áreas de triângulos:

$$
A = \lim_{n \to \infty} \frac{1}{2} R^2 \cdot n \cdot \sin\left(\frac{2\pi}{n}\right) = \pi R^2
$$

Esse é um dos exemplos fundamentais da ideia de limite que motiva o cálculo integral.


# Área de um Segmento de Parábola

## (I) Construção geométrica

Queremos calcular a área do segmento delimitado por uma parábola e uma corda.

### Visualização inicial

    A-------B
     \     /
      \   /
       \_/

A ideia é decompor a região em triângulos.

Dividimos a figura:

    A-------B
     \  M  /
      \   /
       \_/
        N

Separando em dois triângulos:

$$
A_{\triangle ABP} = A_{\triangle AMA} + A_{\triangle ANB}
$$

Seja $MN$ a base comum e $m$ a altura:

$$
A = \frac{MN \cdot m}{2} + \frac{MN \cdot m}{2}
$$

$$
A = MN \cdot m \quad (I)
$$

Pela propriedade de base média:

$$
MN + NS = \frac{AP + BP}{2}
$$

E como há simetria:

$$
MN = \frac{m}{2}
$$

Substituindo em (I):

$$
A_{\triangle ANB} = m^3
$$

---

## (II) Modelagem com função

Seja:

$$
f(x) = x^2
$$

Pontos no eixo:

- $P = (a,0)$  
- $S = (a+m,0)$  
- $Q = (a+2m,0)$  

Visualização:

    P----S----Q
    |    |    |
    |    |    |
    *    *    *
   f(a) f(a+m) f(a+2m)

Alturas:

$$
AP = f(a) = a^2
$$

$$
NS = f(a+m) = (a+m)^2
$$

$$
BQ = f(a+2m) = (a+2m)^2
$$

Substituindo na relação geométrica, obtemos:

$$
MN = m^2
$$

Logo:

$$
A_{\triangle ANB} = m^3
$$

---

## Lei observada

Cada novo triângulo gerado dentro do segmento tem área proporcional:

$$
A = m^3
$$

---

## Construção iterativa

Agora repetimos o processo dentro da parábola.

### Primeira aproximação

    A-------B
     \     /
      \   /
       \_/
        N

Área:

$$
A_P = A_T
$$

---

### Segunda etapa

Inserimos novos triângulos:

    A-------B
     \ /\  /
      X  X
       \_/
        N

Área:

$$
A_P = A_T + \frac{A_T}{4}
$$

---

### Terceira etapa

Subdivisão recursiva:

    A-------B
     \/\ /\ /
      X--X--X
     /\/ \/ \
        N

Área:

$$
A_P = A_T + \frac{A_T}{4} + \frac{A_T}{16}
$$

---

### Processo infinito

Continuando:

$$
A_P = A_T + \frac{A_T}{4} + \frac{A_T}{16} + \frac{A_T}{64} + \dots
$$

---

## Série geométrica

Fatorando:

$$
A_P = A_T \left(1 + \frac{1}{4} + \frac{1}{16} + \frac{1}{64} + \dots \right)
$$

Razão:

$$
r = \frac{1}{4}
$$

Soma infinita:

$$
\sum = \frac{1}{1 - r} = \frac{1}{1 - \frac{1}{4}} = \frac{4}{3}
$$

---

## Resultado final

$$
A_P = \frac{4}{3} A_T
$$

---

## Conclusão geométrica

A área do segmento de parábola é:

$$
\frac{4}{3}
$$

da área do triângulo inicial.

Esse resultado surge naturalmente ao repetir infinitamente o processo de subdivisão.