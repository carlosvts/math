# Cálculo Diferencial — Método de Fermat (pré-derivada)

## Ideia central

Queremos encontrar pontos onde a função tem **máximo ou mínimo local**.

A estratégia usada é:

- Tomar dois pontos próximos: \( x_1 \) e \( x_2 \)
- Impor que:
  
  \[
  f(x_1) = f(x_2)
  \]

- E então fazer:

  \[
  x_2 \to x_1
  \]

Isso força o ponto a se tornar um extremo.

---

## Exemplo específico

Função:

\[
f(x) = -2x^3 + 45x^2
\]

### 1. Igualando valores

\[
f(x_1) = f(x_2)
\]

\[
-2x_1^3 + 45x_1^2 = -2x_2^3 + 45x_2^2 \quad (I)
\]

---

### 2. Reorganizando

\[
45(x_1^2 - x_2^2) = 2(x_1^3 - x_2^3)
\]

Fatorando:

\[
45(x_1 + x_2)(x_1 - x_2) = 2(x_1 - x_2)(x_1^2 + x_1x_2 + x_2^2)
\]

Cancelando \( (x_1 - x_2) \), com \( x_1 \ne x_2 \):

\[
45(x_1 + x_2) = 2(x_1^2 + x_1x_2 + x_2^2)
\]

---

### 3. Aproximação (ideia de Fermat)

Agora fazemos:

\[
x_2 \to x_1 \Rightarrow x_1 \approx x_2 \approx x_v
\]

Substituindo:

\[
45(2x_v) = 2(3x_v^2)
\]

\[
90x_v = 6x_v^2
\]

\[
15x_v = x_v^2
\]

\[
x_v = 0 \quad \text{ou} \quad x_v = 15
\]

---

### Visualização

```text
        ^
        |        *
        |      *   *
        |    *       *
        |  *           *
--------|------------------> x
       x1   xv    x2
```

# Método de Fermat (pré-derivada) — reconstrução das anotações

## Ideia geométrica (intuição)
Considere dois pontos no gráfico com a mesma altura:

f(x₁) = f(x₂)

Visualmente:

      •───•   ← mesma altura
     /     \
    /       \

x₁           x₂

À medida que:
x₂ → x₁

Os dois pontos “colapsam” em um ponto especial — o vértice:

x₁ ≈ x₂ ≈ xᵥ

---

## Generalização (polinômio cúbico)

Se:
f(x) = ax³ + bx² + cx + d

Igualando:
f(x₁) = f(x₂)

a(x₁³ − x₂³) + b(x₁² − x₂²) + c(x₁ − x₂) = 0

Fatorando:

a(x₁ − x₂)(x₁² + x₁x₂ + x₂²)
+ b(x₁ − x₂)(x₁ + x₂)
+ c(x₁ − x₂) = 0

Colocando em evidência:

(x₁ − x₂)[a(x₁² + x₁x₂ + x₂²) + b(x₁ + x₂) + c] = 0

Como:
x₁ ≠ x₂

Então:

a(x₁² + x₁x₂ + x₂²) + b(x₁ + x₂) + c = 0

---

## Aproximação (ideia-chave)

x₁ ≈ x₂ ≈ xᵥ

Substituindo:

x₁² + x₁x₂ + x₂² ≈ 3xᵥ²  
x₁ + x₂ ≈ 2xᵥ  

Logo:

a(3xᵥ²) + b(2xᵥ) + c = 0

---

## Interpretação

Esse método:

- Reduz o grau do polinômio em 1  
- Antecipia a ideia de derivada  
- Está essencialmente calculando onde a inclinação é zero  

---

## Caso quadrático

Se:
f(x) = ax² + bx + c

Igualando:
f(x₁) = f(x₂)

a(x₁² − x₂²) + b(x₁ − x₂) = 0

Fatorando:

a(x₁ − x₂)(x₁ + x₂) + b(x₁ − x₂) = 0

Colocando em evidência:

(x₁ − x₂)(a(x₁ + x₂) + b) = 0

Como:
x₁ ≠ x₂

Então:

a(x₁ + x₂) + b = 0

---

## Aproximação

x₁ ≈ x₂ ≈ xᵥ

a(2xᵥ) + b = 0

2axᵥ + b = 0

xᵥ = -b / (2a)

---
