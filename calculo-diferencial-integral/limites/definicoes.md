# Anotações de Cálculo — Limites

## Limites Trigonométricos Fundamentais

$$
\lim_{x \to 0} \frac{\sin(x)}{x} = 1
$$

## Outros casos

$$
\lim_{x \to \infty} \sin(x) \text{ não existe}
$$

(O seno oscila indefinidamente)

$$
\lim_{x \to \infty} \frac{\sin(x)}{x} = 0
$$

---

## Limite de Função em um Ponto

Considere:

$$
\lim_{x \to 1} \frac{x^2 - 1}{x - 1}
$$

Fatorando:

$$
x^2 - 1 = (x - 1)(x + 1)
$$

Logo:

$$
\lim_{x \to 1} \frac{(x - 1)(x + 1)}{x - 1}
$$

Cancelando:

$$
\lim_{x \to 1} (x + 1) = 2
$$

---

## Interpretação Gráfica

A função não está definida em $x = 1$, mas o valor se aproxima de:

$$
2
$$

Ou seja, há uma descontinuidade removível.

---

## Limite Lateral

Podemos aproximar pelos dois lados:

### Pela direita:

$$
\lim_{x \to a^+} f(x) = 3
$$

### Pela esquerda:

$$
\lim_{x \to a^-} f(x) = 1
$$

### No ponto:

$$
f(a) = 2
$$

---

## Definição de Limite

Dizemos que:

$$
\lim_{x \to a} f(x) = L
$$

se:

$$
\lim_{x \to a^+} f(x) = L
$$

e

$$
\lim_{x \to a^-} f(x) = L
$$

---

## Quando o limite não existe

Se:

$$
\lim_{x \to a^+} f(x) \neq \lim_{x \to a^-} f(x)
$$

então:

$$
\lim_{x \to a} f(x) \text{ não existe}
$$

---

## Exemplos Gráficos

### Caso 1

$$
\lim_{x \to a} f(x) = 2
$$

mas:

$$
f(a) = 4
$$

→ O limite existe, mas o valor da função é diferente.

---

### Caso 2

$$
\lim_{x \to a^+} f(x) = 4
$$

$$
\lim_{x \to a^-} f(x) = 2
$$

Logo:

$$
\lim_{x \to a} f(x) \text{ não existe}
$$

---

## Função por Partes

Considere:

$$
f(x) =
\begin{cases}
x^2 + 2, & x \geq 3 \\
x - 1, & x < 3
\end{cases}
$$

### Limite pela direita:

$$
\lim_{x \to 3^+} f(x) = 3^2 + 2 = 11
$$

### Limite pela esquerda:

$$
\lim_{x \to 3^-} f(x) = 3 - 1 = 2
$$

Como:

$$
11 \neq 2
$$

Então:

$$
\lim_{x \to 3} f(x) \text{ não existe}
$$

---

## Conclusão

- O limite descreve o comportamento da função **próximo** de um ponto  
- Não depende necessariamente do valor da função no ponto  
- Pode existir mesmo com descontinuidade  
- Só existe quando os limites laterais coincidem  
