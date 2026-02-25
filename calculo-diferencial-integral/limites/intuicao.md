# Limites: Intuição e Problemas

## Problema 01: Velocidade Instantânea

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

## Solução 03: Abordagem por Diferença de Quadrados

Nesta abordagem, em vez de substituir $t_2$ por $1 + \delta$, mantemos as variáveis $t_1$ e $t_2$ e utilizamos a fatoração algébrica para simplificar a expressão da velocidade média antes de aplicar o limite.

### Definição Formal
A inclinação da reta tangente ($m$), que representa a velocidade instantânea, é dada por:
$$m = \tan \theta = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$
> **Nota:** Também podemos utilizar a notação $f'(x)$ para representar essa derivada.

---

### Desenvolvimento para $s(t) = t^2$

Considerando dois instantes de tempo distintos $t_1$ e $t_2$:

1. **Velocidade Média ($V_m$):**
   $$V_m = \frac{\Delta s}{\Delta t} = \frac{s_2 - s_1}{t_2 - t_1} = \frac{t_2^2 - t_1^2}{t_2 - t_1}$$

2. **Fatoração (Diferença de Quadrados):**
   Sabemos que $a^2 - b^2 = (a - b)(a + b)$. Aplicando ao numerador:
   $$V_m = \frac{(t_2 - t_1)(t_2 + t_1)}{t_2 - t_1}$$

3. **Simplificação:**
   Como estamos interessados no limite onde $t_2 \to t_1$, mas $t_2 \neq t_1$, podemos cancelar o termo $(t_2 - t_1)$:
   $$V_m = t_2 + t_1$$

4. **Aplicação do Limite:**
   Para encontrar a velocidade instantânea em $t_1$, fazemos $t_2$ tender a $t_1$:
   $$\lim_{t_2 \to t_1} V_m = \lim_{t_2 \to t_1} (t_2 + t_1) = t_1 + t_1 = 2t_1$$

### Conclusão Formal
$$\lim_{t_2 \to t_1} V_m = 2t_1$$
Para o caso específico de $t = 1s$:
$$V_{inst} = 2(1) = 2 \, m/s$$


## A Regra do Tombo (Power Rule)

Existe uma propriedade geral para derivadas de funções potências que simplifica o processo de limite. Basicamente, o expoente "cai" para a esquerda multiplicando a base, e o novo expoente é subtraído em uma unidade.

### Regra Geral
Para uma função do tipo $f(x) = x^n$, a sua derivada $f'(x)$ será:
$$f'(x) = n \cdot x^{n-1}$$

### Exemplos Práticos
* **Caso $x^3$:** O $3$ desce multiplicando e o expoente vira $3-1=2$.
    $$x^3 \implies 3x^2$$
* **Caso $x^2$ (O problema anterior):** O $2$ desce e o expoente vira $2-1=1$.
    $$x^2 \implies 2x^1 = 2x$$
* **Caso $x^{100}$:** $$x^{100} \implies 100x^{99}$$

> **Conexão com os problemas anteriores:** > Na nossa análise de $s(t) = t^2$, chegamos ao resultado $2t$ através do limite. A Regra do Tombo confirma esse resultado de forma instantânea: ao "tombar" o expoente $2$, obtemos diretamente $2t^1$, validando toda a nossa construção algébrica.