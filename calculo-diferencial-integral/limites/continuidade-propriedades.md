# Anotações de Cálculo: Continuidade e Limites

---

## Definição: Continuidade

Define-se uma função $f(x)$ como contínua em $x = a$, se:

1. $f(a)$ existir
2. $\lim_{x \to a} f(x)$ existir
3. $\lim_{x \to a} f(x) = f(a)$

**Ou seja:**
* Existe $f(a)$
* Existe limite tal que seus laterais sejam idênticos: $\lim_{x \to a^-} f(x) = \lim_{x \to a^2} f(x)$

---

## Limites no Infinito

### Caso 1: $\lim_{x \to a} = \pm \infty$ (Não existe)

**Exemplo:**
$f(x) = \frac{(x-3)(x-5)\sin(x)\ln(x)}{(x-2)^2}$

Possui uma **assíntota vertical** em $x = 2$, pois ocorre uma divisão por zero.
$\therefore \lim_{x \to 2} f(x) = +\infty$

### Caso 2: $\lim_{x \to \pm \infty} f(x) = L$


Quando o limite tende a um valor constante $L$ conforme $x$ cresce ou decresce infinitamente, temos uma **Assíntota Horizontal** de $f(x)$.

**Exemplo:**
$f(x) = \frac{\sin(x)}{(x-1)^2} + 3$
$\lim_{x \to \infty} f(x) = 3 \therefore y = 3$ é uma assíntota horizontal.

---

## Teorema de Bolzano

**Exemplo Prático:**
$\cos(x) = x \implies f(x) = x - \cos(x)$

* $f(0) = 0 - \cos(0) = -1 < 0$  **(-)**
* $f(1) = 1 - \cos(1) > 0$  **(+)**

Como existe um $f(x)$ positivo e outro $f(x) < 0$ e a função é contínua, **EXISTE** pelo menos um valor onde $f(x) = 0$.

### Enunciado:
Seja $f: [a, b] \to \mathbb{R}$ contínua em $[a, b]$.
Se $f(a) \cdot f(b) < 0$, então existe $c \in [a, b]$ tal que $f(c) = 0$.

**Exemplo 3.12:**
$f(x) = e^x - 3x$
Raiz: $f(x) = 0 \implies e^x - 3x = 0 \implies e^x = 3x$

Pelo Teorema de Bolzano:
1. $f(0) = e^0 - 3(0) = 1$
2. $f(1) = e^1 - 3(1) = \text{número} < 0$
Provamos que existe uma raiz no intervalo.

---

## Teorema do Valor Intermediário (TVI)


Seja $f: [a, b]$ contínua em $[a, b]$.
Seja $k$ um valor entre $f(a)$ e $f(b)$.
Então, existe $c$ tal que $f(c) = k$.

### Demonstração:
Seja $f: [a, b] \to \mathbb{R}$ contínua; seja $k$ um valor entre $f(a)$ e $f(b)$.

1. **Caso 01:** $k = f(a)$ ou $f(b)$ (Trivial)
2. **Caso 02:** $f(a) < k < f(b)$

Seja $g(x) = f(x) - k$ (também contínua).
* $g(a) = f(a) - k \implies (-)$
* $g(b) = f(b) - k \implies (+)$
$\implies g(a) \cdot g(b) < 0$

Pelo Teorema de Bolzano, existe $c \in [a, b]$ tal que $g(c) = 0$.
$f(c) - k = 0 \implies f(c) = k$

---

## Propriedades dos Limites

1. $\lim_{x \to a} [k \cdot f(x)] = k \cdot \lim_{x \to a} f(x)$, onde $k$ é uma constante.
2. $\lim_{x \to a} [f(x) \pm g(x)] = \lim_{x \to a} f(x) \pm \lim_{x \to a} g(x)$
   * *Ex:* $\lim_{x \to 0} (x^2 + x + 1) \implies \lim_{x \to 0} x^2 + \lim_{x \to 0} x + \lim_{x \to 0} 1 = 1$
3. $\lim_{x \to a} [f(x) \cdot g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)$
4. $\lim_{x \to a} \left[ \frac{f(x)}{g(x)} \right] = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}$, se $\lim_{x \to a} g(x) \neq 0$.