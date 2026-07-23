# Cálculo — guia aplicado para provas

> Material de revisão sobre funções, limites, derivadas, integrais e suas principais aplicações. O objetivo não é apenas memorizar fórmulas, mas reconhecer **qual ferramenta usar**, organizar a resolução e interpretar o resultado.

---

## Sumário

1. [Visão geral](#1-visão-geral)
2. [Funções e gráficos](#2-funções-e-gráficos)
3. [Limites e continuidade](#3-limites-e-continuidade)
4. [Derivadas](#4-derivadas)
5. [Análise de funções](#5-análise-de-funções)
6. [Aplicações das derivadas](#6-aplicações-das-derivadas)
7. [Integrais](#7-integrais)
8. [Aplicações das integrais](#8-aplicações-das-integrais)
9. [Questões analisadas e resolvidas](#9-questões-analisadas-e-resolvidas)
10. [Estratégia para provas](#10-estratégia-para-provas)
11. [Erros frequentes](#11-erros-frequentes)
12. [Resumo de fórmulas](#12-resumo-de-fórmulas)
13. [Exercícios para treino](#13-exercícios-para-treino)

---

## 1. Visão geral

O Cálculo estuda principalmente duas ideias:

- **variação:** como uma grandeza muda em relação a outra;
- **acumulação:** quanto foi somado ao longo de um intervalo.

Essas ideias são representadas por três ferramentas centrais:

| Ferramenta | Pergunta respondida | Interpretação |
|---|---|---|
| **Limite** | Para qual valor a função se aproxima? | Comportamento próximo de um ponto |
| **Derivada** | Quão rápido a função muda? | Taxa de variação ou inclinação |
| **Integral** | Quanto foi acumulado? | Soma contínua ou área com sinal |

### Relação entre os assuntos

1. Uma **função** descreve a relação entre grandezas.
2. O **limite** analisa o comportamento da função perto de um ponto.
3. A **derivada** usa um limite para medir uma variação instantânea.
4. A **integral** acumula pequenas quantidades.
5. O **Teorema Fundamental do Cálculo** conecta derivadas e integrais.

---

## 2. Funções e gráficos

Uma função associa cada valor permitido de entrada a um único valor de saída:

$$
y=f(x)
$$

- $x$: variável independente;
- $f(x)$ ou $y$: variável dependente;
- **domínio:** valores de $x$ aceitos pela função;
- **imagem:** valores que a função pode produzir.

### 2.1 Domínio

Antes de calcular limites, derivadas ou integrais, observe onde a função existe.

#### Restrições comuns

1. **Denominador diferente de zero**

$$
f(x)=\frac{1}{x-3}
$$

Como $x-3\neq 0$, temos $x\neq 3$.

2. **Raiz de índice par com radicando não negativo**

$$
f(x)=\sqrt{x-2}
$$

É necessário $x-2\geq 0$, portanto $x\geq 2$.

3. **Logaritmo com argumento positivo**

$$
f(x)=\ln(x+1)
$$

É necessário $x+1>0$, portanto $x>-1$.

### 2.2 Elementos importantes de um gráfico

Em questões de análise gráfica, procure:

- interseções com os eixos;
- intervalos de crescimento e decrescimento;
- máximos e mínimos;
- concavidade;
- pontos de inflexão;
- assíntotas;
- descontinuidades;
- comportamento quando $x\to\pm\infty$.

### 2.3 Funções mais frequentes

| Tipo | Forma básica | Característica |
|---|---|---|
| Linear | $f(x)=ax+b$ | Taxa de variação constante |
| Quadrática | $f(x)=ax^2+bx+c$ | Gráfico em forma de parábola |
| Polinomial | $f(x)=a_nx^n+\cdots+a_0$ | Contínua em todo número real |
| Racional | $f(x)=p(x)/q(x)$ | Pode apresentar assíntotas |
| Exponencial | $f(x)=a^x$ | Crescimento ou decaimento proporcional |
| Logarítmica | $f(x)=\ln x$ | Inversa da exponencial |
| Trigonométrica | $\sin x$, $\cos x$, $\tan x$ | Comportamento periódico |

---

## 3. Limites e continuidade

### 3.1 Ideia de limite

A expressão

$$
\lim_{x\to a}f(x)=L
$$

indica que $f(x)$ se aproxima de $L$ quando $x$ se aproxima de $a$.

O limite analisa valores **próximos** de $a$. Por isso, $f(a)$ pode:

- ser igual ao limite;
- ser diferente do limite;
- nem sequer existir.

### 3.2 Limites laterais

- pela esquerda: $\lim_{x\to a^-}f(x)$;
- pela direita: $\lim_{x\to a^+}f(x)$.

O limite bilateral só existe quando os dois limites laterais existem e são iguais:

$$
\lim_{x\to a^-}f(x)=\lim_{x\to a^+}f(x)
$$

### 3.3 Como resolver limites

#### Caso 1 — substituição direta

Se a função for contínua no ponto, substitua $x=a$.

**Exemplo:**

$$
\lim_{x\to 2}(x^2+3x)=2^2+3(2)=10
$$

#### Caso 2 — indeterminação $0/0$

Encontrar $0/0$ não encerra a questão. Esse resultado indica que a expressão precisa ser transformada.

Técnicas frequentes:

- fatoração;
- racionalização;
- denominador comum;
- identidades trigonométricas;
- limites notáveis;
- regra de L'Hôpital, quando autorizada.

#### Exemplo com fatoração

$$
\lim_{x\to 2}\frac{x^2-4}{x-2}
$$

A substituição direta gera $0/0$. Fatorando:

$$
x^2-4=(x-2)(x+2)
$$

Logo,

$$
\frac{(x-2)(x+2)}{x-2}=x+2,\qquad x\neq 2
$$

Portanto:

$$
\boxed{\lim_{x\to 2}\frac{x^2-4}{x-2}=4}
$$

#### Exemplo com racionalização

$$
\lim_{x\to 0}\frac{\sqrt{x+1}-1}{x}
$$

Multiplicando pelo conjugado:

$$
\frac{\sqrt{x+1}-1}{x}\cdot
\frac{\sqrt{x+1}+1}{\sqrt{x+1}+1}
=
\frac{x}{x(\sqrt{x+1}+1)}
$$

Cancelando $x$:

$$
\lim_{x\to 0}\frac{1}{\sqrt{x+1}+1}=\boxed{\frac12}
$$

### 3.4 Limites notáveis

$$
\lim_{x\to 0}\frac{\sin x}{x}=1
$$

$$
\lim_{x\to 0}\frac{1-\cos x}{x}=0
$$

$$
\lim_{x\to 0}\frac{e^x-1}{x}=1
$$

> Nos limites trigonométricos, o ângulo deve estar em **radianos**.

### 3.5 Limites no infinito

Em funções racionais, compare os graus do numerador e do denominador.

Para

$$
\lim_{x\to\infty}\frac{a_nx^n+\cdots}{b_mx^m+\cdots}:
$$

- se $n<m$, o limite é $0$;
- se $n=m$, o limite é $a_n/b_m$;
- se $n>m$, normalmente há crescimento ilimitado ou assíntota não horizontal.

**Exemplo:**

$$
\lim_{x\to\infty}\frac{3x^2+1}{2x^2-5}=\boxed{\frac32}
$$

### 3.6 Continuidade

Uma função é contínua em $x=a$ quando:

1. $f(a)$ existe;
2. $\lim_{x\to a}f(x)$ existe;
3. $\lim_{x\to a}f(x)=f(a)$.

Em uma função definida por partes, essas três condições são frequentemente usadas para descobrir um parâmetro desconhecido.

---

## 4. Derivadas

### 4.1 Interpretação

A derivada de $f$ em $x=a$ é

$$
f'(a)=\lim_{h\to 0}\frac{f(a+h)-f(a)}{h}
$$

Ela pode representar:

- inclinação da reta tangente;
- velocidade instantânea;
- taxa de crescimento;
- custo marginal;
- sensibilidade de uma variável;
- taxa de variação de uma quantidade em relação a outra.

### 4.2 Derivadas básicas

| Função | Derivada |
|---|---|
| $c$ | $0$ |
| $x^n$ | $nx^{n-1}$ |
| $e^x$ | $e^x$ |
| $a^x$ | $a^x\ln a$ |
| $\ln x$ | $1/x$ |
| $\sin x$ | $\cos x$ |
| $\cos x$ | $-\sin x$ |
| $\tan x$ | $\sec^2x$ |

### 4.3 Regras de derivação

#### Soma e diferença

$$
(f\pm g)'=f'\pm g'
$$

#### Produto

$$
(fg)'=f'g+fg'
$$

#### Quociente

$$
\left(\frac{f}{g}\right)'=\frac{f'g-fg'}{g^2}
$$

#### Regra da cadeia

Se $y=f(g(x))$, então:

$$
y'=f'(g(x))\cdot g'(x)
$$

A regra da cadeia é usada em funções compostas.

**Exemplo:**

$$
f(x)=(3x^2+1)^5
$$

- função externa: $u^5$;
- função interna: $u=3x^2+1$.

Assim:

$$
f'(x)=5(3x^2+1)^4\cdot 6x
$$

$$
\boxed{f'(x)=30x(3x^2+1)^4}
$$

### 4.4 Reta tangente

A reta tangente ao gráfico de $f$ no ponto $x=a$ é:

$$
y-f(a)=f'(a)(x-a)
$$

#### Exemplo

Determine a reta tangente a $f(x)=x^2+1$ em $x=2$.

1. Ponto:

$$
f(2)=5
$$

2. Inclinação:

$$
f'(x)=2x\Rightarrow f'(2)=4
$$

3. Equação:

$$
y-5=4(x-2)
$$

$$
\boxed{y=4x-3}
$$

### 4.5 Derivação implícita

Quando $y$ não está isolado, derive os dois lados em relação a $x$.

**Exemplo:**

$$
x^2+y^2=25
$$

Derivando:

$$
2x+2y\frac{dy}{dx}=0
$$

Logo:

$$
\boxed{\frac{dy}{dx}=-\frac{x}{y}}
$$

---

## 5. Análise de funções

As derivadas permitem reconstruir o comportamento de um gráfico.

### 5.1 Crescimento e decrescimento

- se $f'(x)>0$, a função é crescente;
- se $f'(x)<0$, a função é decrescente;
- se $f'(x)=0$ ou não existe, pode haver um ponto crítico.

### 5.2 Máximos e mínimos

Um ponto crítico $x=c$ pode ser classificado pelo sinal de $f'$:

- $f'$ muda de positivo para negativo: máximo local;
- $f'$ muda de negativo para positivo: mínimo local;
- não há troca de sinal: não é extremo local.

Também pode ser usado o teste da segunda derivada:

- $f''(c)>0$: mínimo local;
- $f''(c)<0$: máximo local;
- $f''(c)=0$: teste inconclusivo.

### 5.3 Concavidade e inflexão

- $f''(x)>0$: concavidade para cima;
- $f''(x)<0$: concavidade para baixo.

Um ponto de inflexão exige **mudança de concavidade**. Resolver apenas $f''(x)=0$ fornece candidatos, não uma conclusão automática.

### 5.4 Exemplo de análise completa

Considere:

$$
f(x)=x^3-3x
$$

#### 1. Pontos críticos

$$
f'(x)=3x^2-3=3(x-1)(x+1)
$$

Logo:

$$
x=-1\quad\text{e}\quad x=1
$$

#### 2. Crescimento

Analisando o sinal de $f'$:

- crescente em $(-\infty,-1)$;
- decrescente em $(-1,1)$;
- crescente em $(1,\infty)$.

Portanto:

- $x=-1$ é máximo local;
- $x=1$ é mínimo local.

#### 3. Concavidade

$$
f''(x)=6x
$$

- para $x<0$, $f''(x)<0$: concavidade para baixo;
- para $x>0$, $f''(x)>0$: concavidade para cima.

Assim, $x=0$ é ponto de inflexão.

#### Resultado da análise

| Elemento | Resultado |
|---|---|
| Máximo local | $(-1,2)$ |
| Mínimo local | $(1,-2)$ |
| Ponto de inflexão | $(0,0)$ |
| Crescente | $(-\infty,-1)\cup(1,\infty)$ |
| Decrescente | $(-1,1)$ |

---

## 6. Aplicações das derivadas

### 6.1 Movimento

Se $s(t)$ representa a posição:

$$
v(t)=s'(t)
$$

$$
a(t)=v'(t)=s''(t)
$$

- o móvel está parado quando $v(t)=0$;
- move-se no sentido positivo quando $v(t)>0$;
- move-se no sentido negativo quando $v(t)<0$;
- sua rapidez aumenta quando velocidade e aceleração têm o mesmo sinal.

### 6.2 Economia

Se $C(q)$ é o custo de produzir $q$ unidades:

$$
C'(q)=\text{custo marginal}
$$

Se $R(q)$ é a receita:

$$
L(q)=R(q)-C(q)
$$

Para maximizar o lucro, procure pontos em que:

$$
L'(q)=0
$$

Depois, confirme se o ponto realmente representa um máximo.

### 6.3 Otimização

Roteiro para problemas de máximo ou mínimo:

1. identifique a quantidade a otimizar;
2. escreva a função objetivo;
3. use a restrição para deixar a função com uma variável;
4. determine o domínio físico do problema;
5. calcule os pontos críticos;
6. compare os candidatos e extremos do intervalo;
7. responda com unidade e interpretação.

#### Exemplo

Um retângulo tem perímetro de $40$ m. Quais dimensões produzem a maior área?

Restrição:

$$
2x+2y=40\Rightarrow y=20-x
$$

Área:

$$
A(x)=xy=x(20-x)=20x-x^2
$$

Derivada:

$$
A'(x)=20-2x
$$

Ponto crítico:

$$
20-2x=0\Rightarrow x=10
$$

Então $y=10$. Como $A''(x)=-2<0$, o ponto é máximo.

$$
\boxed{10\text{ m}\times 10\text{ m}}
$$

### 6.4 Taxas relacionadas

Quando duas ou mais grandezas variam com o tempo:

1. escreva uma equação que relacione as grandezas;
2. derive implicitamente em relação ao tempo;
3. substitua os valores do instante analisado;
4. resolva a taxa desconhecida.

> Não substitua valores constantes antes de derivar se as grandezas variam com o tempo.

---

## 7. Integrais

### 7.1 Integral indefinida

A integral indefinida procura uma família de primitivas:

$$
\int f(x)\,dx=F(x)+C
$$

em que $F'(x)=f(x)$ e $C$ é uma constante.

### 7.2 Primitivas básicas

| Integral | Resultado |
|---|---|
| $\int x^n\,dx$, $n\neq-1$ | $\dfrac{x^{n+1}}{n+1}+C$ |
| $\int \dfrac1x\,dx$ | $\ln|x|+C$ |
| $\int e^x\,dx$ | $e^x+C$ |
| $\int \cos x\,dx$ | $\sin x+C$ |
| $\int \sin x\,dx$ | $-\cos x+C$ |
| $\int \sec^2x\,dx$ | $\tan x+C$ |

### 7.3 Integral definida

A integral definida representa acumulação líquida:

$$
\int_a^b f(x)\,dx
$$

Pelo Teorema Fundamental do Cálculo, se $F'(x)=f(x)$:

$$
\int_a^b f(x)\,dx=F(b)-F(a)
$$

#### Exemplo

$$
\int_0^2(3x^2+1)\,dx
$$

Uma primitiva é:

$$
F(x)=x^3+x
$$

Logo:

$$
F(2)-F(0)=(8+2)-0=\boxed{10}
$$

### 7.4 Substituição

A substituição desfaz a regra da cadeia.

**Exemplo:**

$$
\int 2x\cos(x^2)\,dx
$$

Escolha:

$$
u=x^2\Rightarrow du=2x\,dx
$$

Então:

$$
\int\cos u\,du=\sin u+C
$$

Voltando para $x$:

$$
\boxed{\sin(x^2)+C}
$$

### 7.5 Integração por partes

A fórmula é:

$$
\int u\,dv=uv-\int v\,du
$$

É útil principalmente em produtos envolvendo:

- polinômios e exponenciais;
- polinômios e funções trigonométricas;
- logaritmos;
- funções trigonométricas inversas.

**Exemplo:**

$$
\int xe^x\,dx
$$

Escolhendo $u=x$ e $dv=e^x dx$:

$$
du=dx,\qquad v=e^x
$$

Portanto:

$$
\boxed{\int xe^x\,dx=xe^x-e^x+C}
$$

---

## 8. Aplicações das integrais

### 8.1 Área entre uma curva e o eixo $x$

A integral calcula **área com sinal**:

- acima do eixo $x$: contribuição positiva;
- abaixo do eixo $x$: contribuição negativa.

Para obter área geométrica total, separe os intervalos e use valores absolutos.

### 8.2 Área entre duas curvas

Se $f(x)\geq g(x)$ no intervalo $[a,b]$:

$$
A=\int_a^b[f(x)-g(x)]\,dx
$$

Procedimento:

1. encontre as interseções resolvendo $f(x)=g(x)$;
2. determine qual função fica acima;
3. integre “função superior menos função inferior”.

### 8.3 Deslocamento e distância

Se $v(t)$ é a velocidade:

$$
\text{deslocamento}=\int_a^b v(t)\,dt
$$

$$
\text{distância total}=\int_a^b|v(t)|\,dt
$$

Deslocamento e distância não são necessariamente iguais. Se a velocidade muda de sinal, separe os intervalos para calcular a distância.

### 8.4 Acumulação a partir de uma taxa

Se $r(t)$ é uma taxa e $Q(a)$ é a quantidade inicial:

$$
Q(t)=Q(a)+\int_a^t r(s)\,ds
$$

Exemplos:

- integrar vazão fornece volume;
- integrar densidade linear fornece massa;
- integrar velocidade fornece deslocamento;
- integrar custo marginal fornece variação do custo.

### 8.5 Valor médio de uma função

O valor médio de $f$ em $[a,b]$ é:

$$
f_{\text{médio}}=\frac{1}{b-a}\int_a^b f(x)\,dx
$$

---

## 9. Questões analisadas e resolvidas

### Questão 1 — limite e indeterminação

Calcule:

$$
\lim_{x\to 3}\frac{x^2-9}{x-3}
$$

**Análise:** a substituição direta gera $0/0$. Como há uma diferença de quadrados, a técnica adequada é fatoração.

**Resolução:**

$$
x^2-9=(x-3)(x+3)
$$

$$
\lim_{x\to 3}\frac{(x-3)(x+3)}{x-3}
=
\lim_{x\to 3}(x+3)
=\boxed{6}
$$

---

### Questão 2 — continuidade de uma função por partes

Considere:

$$
f(x)=
\begin{cases}
2x+k, & x<2\\
x^2, & x\geq2
\end{cases}
$$

Determine $k$ para que $f$ seja contínua em $x=2$.

**Análise:** os limites laterais devem ser iguais ao valor $f(2)$.

Pela direita e pelo valor da função:

$$
f(2)=2^2=4
$$

Pela esquerda:

$$
\lim_{x\to2^-}f(x)=4+k
$$

Igualando:

$$
4+k=4\Rightarrow\boxed{k=0}
$$

---

### Questão 3 — reta tangente

Encontre a reta tangente a $f(x)=x^3-2x$ em $x=1$.

**Análise:** precisamos do ponto $(1,f(1))$ e da inclinação $f'(1)$.

$$
f(1)=1-2=-1
$$

$$
f'(x)=3x^2-2\Rightarrow f'(1)=1
$$

Aplicando a equação da reta tangente:

$$
y+1=1(x-1)
$$

$$
\boxed{y=x-2}
$$

---

### Questão 4 — movimento

A posição de uma partícula é

$$
s(t)=t^3-6t^2+9t
$$

Determine os instantes em que ela está parada.

**Análise:** a partícula está parada quando sua velocidade é zero.

$$
v(t)=s'(t)=3t^2-12t+9
$$

$$
3(t^2-4t+3)=0
$$

$$
3(t-1)(t-3)=0
$$

Logo:

$$
\boxed{t=1\quad\text{ou}\quad t=3}
$$

---

### Questão 5 — máximo e mínimo absolutos

Determine o máximo e o mínimo de

$$
f(x)=x^3-3x
$$

no intervalo $[-2,2]$.

**Análise:** em um intervalo fechado, compare os valores da função nos pontos críticos e nas extremidades.

Pontos críticos:

$$
f'(x)=3x^2-3=0\Rightarrow x=\pm1
$$

Tabela de valores:

| $x$ | $f(x)$ |
|---:|---:|
| $-2$ | $-2$ |
| $-1$ | $2$ |
| $1$ | $-2$ |
| $2$ | $2$ |

Portanto:

- máximo absoluto: $\boxed{2}$, atingido em $x=-1$ e $x=2$;
- mínimo absoluto: $\boxed{-2}$, atingido em $x=-2$ e $x=1$.

---

### Questão 6 — integral definida

Calcule:

$$
\int_1^3(2x+1)\,dx
$$

Uma primitiva é:

$$
F(x)=x^2+x
$$

Logo:

$$
F(3)-F(1)=(9+3)-(1+1)=\boxed{10}
$$

---

### Questão 7 — área entre curvas

Calcule a área entre $y=x$ e $y=x^2$ no intervalo $[0,1]$.

**Análise:** nesse intervalo, $x\geq x^2$. Portanto, a função superior é $x$.

$$
A=\int_0^1(x-x^2)\,dx
$$

$$
A=\left[\frac{x^2}{2}-\frac{x^3}{3}\right]_0^1
$$

$$
A=\frac12-\frac13=\boxed{\frac16}
$$

---

### Questão 8 — taxa de acumulação

Água entra em um tanque à taxa

$$
r(t)=4t+2
$$

litros por minuto. Quanto entra entre $t=0$ e $t=5$ minutos?

**Análise:** integrar uma taxa fornece a quantidade acumulada.

$$
\int_0^5(4t+2)\,dt
=
[2t^2+2t]_0^5
$$

$$
=50+10=\boxed{60\text{ litros}}
$$

---

## 10. Estratégia para provas

### 10.1 Como identificar a ferramenta

| Se o enunciado pedir... | Pense em... |
|---|---|
| Valor para o qual algo se aproxima | Limite |
| Continuidade em um ponto | Limites laterais e valor da função |
| Inclinação ou taxa instantânea | Derivada |
| Reta tangente | Ponto e derivada |
| Crescimento ou decrescimento | Sinal de $f'$ |
| Máximo ou mínimo | Pontos críticos e extremos do domínio |
| Concavidade ou inflexão | Segunda derivada |
| Quantidade total a partir de uma taxa | Integral |
| Área entre curvas | Integral da função superior menos a inferior |
| Deslocamento | Integral da velocidade |
| Distância total | Integral do módulo da velocidade |

### 10.2 Roteiro de resolução

1. **Leia o comando:** destaque exatamente o que deve ser encontrado.
2. **Liste os dados:** identifique valores, funções, intervalo e unidades.
3. **Verifique o domínio:** descarte resultados matematicamente ou fisicamente inválidos.
4. **Escolha a ferramenta:** limite, derivada ou integral.
5. **Mostre os passos essenciais:** uma resposta sem justificativa pode perder pontos.
6. **Teste o resultado:** confira sinal, unidade e ordem de grandeza.
7. **Interprete:** responda em uma frase relacionada ao contexto.

### 10.3 Checklist antes de entregar

- [ ] Respondi o que foi pedido?
- [ ] Verifiquei o domínio?
- [ ] Usei parênteses corretamente?
- [ ] Incluí a constante $C$ na integral indefinida?
- [ ] Analisei todos os pontos críticos?
- [ ] Comparei os extremos do intervalo fechado?
- [ ] Separei áreas ou distâncias quando houve mudança de sinal?
- [ ] Coloquei a unidade?
- [ ] Interpretei o resultado no contexto?

---

## 11. Erros frequentes

### Limites

- tratar $0/0$ como resposta;
- verificar apenas um limite lateral;
- cancelar termos em vez de fatores;
- usar limites trigonométricos com ângulos em graus.

### Derivadas

- esquecer a regra da cadeia;
- usar $(fg)'=f'g'$;
- errar o sinal da derivada de $\cos x$;
- concluir que todo ponto com $f'(x)=0$ é máximo ou mínimo;
- não testar extremos de um intervalo fechado.

### Integrais

- esquecer a constante $C$ em integrais indefinidas;
- somar $1$ ao expoente sem dividir pelo novo expoente;
- considerar integral definida sempre positiva;
- confundir deslocamento com distância total;
- não alterar os limites após uma substituição, quando a resolução permanece na nova variável.

---

## 12. Resumo de fórmulas

### Limites

$$
\lim_{x\to0}\frac{\sin x}{x}=1
$$

$$
\lim_{x\to0}\frac{e^x-1}{x}=1
$$

### Derivadas

$$
(x^n)'=nx^{n-1}
$$

$$
(fg)'=f'g+fg'
$$

$$
\left(\frac fg\right)'=\frac{f'g-fg'}{g^2}
$$

$$
(f\circ g)'(x)=f'(g(x))g'(x)
$$

$$
y-f(a)=f'(a)(x-a)
$$

### Integrais

$$
\int x^n\,dx=\frac{x^{n+1}}{n+1}+C,\qquad n\neq-1
$$

$$
\int_a^b f(x)\,dx=F(b)-F(a)
$$

$$
\int u\,dv=uv-\int v\,du
$$

### Aplicações

$$
v(t)=s'(t),\qquad a(t)=s''(t)
$$

$$
\text{deslocamento}=\int_a^b v(t)\,dt
$$

$$
\text{distância}=\int_a^b|v(t)|\,dt
$$

$$
A=\int_a^b(\text{superior}-\text{inferior})\,dx
$$

$$
f_{\text{médio}}=\frac1{b-a}\int_a^b f(x)\,dx
$$

---

## 13. Exercícios para treino

Tente resolver antes de consultar o gabarito.

### Limites

1. Calcule $\lim_{x\to4}\dfrac{x^2-16}{x-4}$.
2. Calcule $\lim_{x\to0}\dfrac{\sin(5x)}{x}$.
3. Determine $\lim_{x\to\infty}\dfrac{2x^2-1}{5x^2+3x}$.

### Derivadas

4. Derive $f(x)=4x^3-2x^2+7$.
5. Derive $g(x)=\sin(x^2)$.
6. Encontre a reta tangente a $f(x)=\sqrt{x}$ em $x=4$.
7. Determine os pontos críticos de $f(x)=x^3-12x$.

### Integrais

8. Calcule $\int(3x^2-4x+1)\,dx$.
9. Calcule $\int_0^2(x+3)\,dx$.
10. Calcule $\int 2xe^{x^2}\,dx$.

### Aplicações

11. A posição é $s(t)=t^2-4t+1$. Em que instante a partícula está parada?
12. Um retângulo possui área de $100\text{ m}^2$. Quais dimensões minimizam seu perímetro?
13. A velocidade é $v(t)=3t^2$. Qual o deslocamento entre $t=0$ e $t=2$?

### Gabarito

1. $8$.
2. $5$.
3. $2/5$.
4. $f'(x)=12x^2-4x$.
5. $g'(x)=2x\cos(x^2)$.
6. $y-2=\dfrac14(x-4)$, ou $y=\dfrac{x}{4}+1$.
7. $x=-2$ e $x=2$.
8. $x^3-2x^2+x+C$.
9. $8$.
10. $e^{x^2}+C$.
11. $t=2$.
12. $10\text{ m}\times10\text{ m}$.
13. $8$ unidades de comprimento.

---

## Conclusão

Para estudar Cálculo de forma eficiente, associe cada operação a uma interpretação:

- **limite:** aproximação;
- **derivada:** variação;
- **integral:** acumulação.

Em uma prova, a maior dificuldade costuma ser reconhecer a estrutura do problema. Antes de começar a conta, pergunte:

1. O que varia?
2. O que deve ser encontrado?
3. Preciso analisar aproximação, taxa ou acúmulo?
4. O resultado faz sentido no contexto?

Essa leitura transforma fórmulas isoladas em ferramentas de resolução.
