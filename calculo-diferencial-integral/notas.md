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