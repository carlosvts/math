# Limites: Intuição e Problemas

## Problema 01: O Barco e a Corda

```text
       Pescador
          O
         /|        Corda
        / |_________________  V (Velocidade da corda)
          |                /
          |      \theta   /  Barco
   _______|__________.---/____ > (Velocidade do barco?)
          |~~~~~~~~~/~~~~~~~|
          |~~~~~~~~~~~~~~~~~|
```

## Problema 02: Velocidade Instantânea

Um carro se move pela função de posição $s(t) = t^2$. Qual sua velocidade em $t = 1s$?

### Solução 01: Abordagem Numérica (Tabela de Aproximação)

Para achar a velocidade instantânea, calculamos com um $\Delta t \to 0$.

A fórmula utilizada é: $v_m = \frac{\Delta s}{\Delta t} = \frac{s_2 - s_1}{t_2 - t_1}$

| $t_2$ | $\Delta t$ | $s_2$ | $\Delta s$ | $v_m$ |
| :--- | :--- | :--- | :--- | :--- |
| 2 | 1 | 4 | 3 | 3 |
| 1,1 | 0,1 | 1,21 | 0,21 | 2,1 |
| 1,01 | 0,01 | 1,0201 | 0,0201 | 2,01 |
| 1,001 | 0,001 | 1,002001 | 0,002001 | 2,001 |
| $\Delta t \to 0$ | | | | **2** |

### Solução 02: Abordagem Algébrica (Formalização)

Seja $v_m = \frac{\Delta s}{\Delta t}$. Definimos $t_1 = 1s$ e $t_2 = t_1 + \delta = 1 + \delta$, onde $\delta \neq 0$.

**Cálculo de $\Delta t$:**
$$\Delta t = t_2 - t_1 \implies (1 + \delta) - 1 = \delta$$

**Cálculo de $v_m$:**
$$v_m = \frac{s_2 - s_1}{\delta} \implies \frac{t_2^2 - t_1^2}{\delta} \implies \frac{(1 + \delta)^2 - 1^2}{\delta}$$

**Desenvolvimento do Polinômio:**
$$v_m = \frac{1 + 2\delta + \delta^2 - 1}{\delta} \implies \frac{2\delta + \delta^2}{\delta} \implies 2 + \delta$$

**Conclusão:** Ao aplicarmos o limite onde o intervalo de tempo tende a zero ($\delta \to 0$):
$$v_m = 2 + \delta \xrightarrow{\delta \to 0} 2$$