# Lista de Exercícios Eletrostática

:::{admonition} **Instruções**
:class: alert

- Respondam as questões de forma clara e organizada, usando a notação matemática adequada.
- Explicite leis, princípios e teoremas utilizados, com seus enunciados.
- Faça diagramas ou esboços para auxiliar na interpretação.
- Se você tem uma letra linda, escreva a mão, caso contrário, colabore com a presbiobia do professor e escreva em LateX ou markdown
:::

:::{exercise}
:label: 03-01

Em uma região do espaço livre de cargas, as componentes cartesianas do campo elétrico são:

$$
E_k = C_k + D_{jk} r_k,
$$

onde $C_k$ e $D_{jk}$ são contantes. Mostre que $D_{jk}$ é símétrico e de traço nulo.

:::

:::{exercise}
:label: 03-02

Considere um modelo do átomo de hidrogênio com distribuição de carga

$$
\rho(\vec r) = -\frac{e}{\pi a^2 r}\; e^{-2r/a},
$$

Mostre que a energia de ionização (necessária para remover a carga eletrônica até o infinito) é

$$
E_0 = \frac{3}{8}\frac{e^2}{\pi \epsilon_0 a}.
$$
:::

:::{exercise}
:label: 03-03

- Considere duas cargas puntiformes, de sinais opostos. Seja $\vec n$ o vetor unitário paralelo a linha que une as cargas.  Escreva o potencial elétrico $\phi(\vec r)$ e o campo elétrico $\vec E(\vec r)$ para $r \gg d$, onde $f$ é a separação entre cargas.
- Sabendo que podemos escrever o potencial de uma distribuição como:

$$
\phi(\vec r) = \frac{1}{4\pi\epsilon_0} \iiint \frac{dq}{|\vec r - \vec r´|} = \frac{1}{4\pi\epsilon_0} \iiint \frac{\rho(\vec r') d^3r'}{|\vec r - \vec r´|},
$$

considere $r \gg r'$ e expanda o integrando em série de taylor até a segunda ordem.

- Explicite os termos de monopolo, dipolo e quadropolo elétrico.
- Considere um dipolo elétrico pontual puro, calcule o campo elétrico.
- Determine a força entre dois dipolos.
- Determine a Energia potencial de uma configuração com dois dipolos em posições $r_1$ e $r_2$

:::

:::{exercise}
:label: 03-04

Mostre que
$$
\int_{-1}^1 dx P_l(x) P_m(x) = \frac{2}{2l+1}\delta_{ll´}
$$

:::

:::{exercise}
:label: 03-05

Um modelo inicial do núcleo atômico é o chamado modelo da gota líquida, em que o núcleo é modelado por uma esfera de distribuição uniforme de carga que pode sofrer deformações.

- Mostre que, até termos de quadrupolo, a mais geral distorção azimutalmente simétrica de uma esfera de carga $q$ e raio $R_0$, a qual preserva volume e a posição do centro, é

$$
R(\theta) = R_0\left\{1 - \frac{\alpha^2}{5} + \alpha P_2(\cos\theta \right\}, \alpha \gg 1.
$$

- Seja $U_0$ a autoenergia do núcleo não perturbado, mostre que a perturbação acima corresponde a:

$$
\Delta U_E = -\frac{1}{5}U_0 \alpha^2
$$
:::
