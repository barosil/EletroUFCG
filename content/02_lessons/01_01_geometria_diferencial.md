# Preliminares Matemáticas

:::{figure} ../00_images/01_preliminares/geomdiff.webp
:name: geomdiff_foundingfathers
:align: center
:width: 100%

**Carl Friedrich Gauss** (1777-1855), **Bernhard Riemann** (1826-1866), **Élie Cartan** (1869-1951), **Henri Poincaré** (1854-1912)
:::

:::{admonition} Conteúdo
:class: dropdown

1. Unidade: Preliminares Matemáticos
   1. Geometria Diferencial
      1. Vetores e Tensores
      2. Tensores isotrópicos
      3. Coordenadas Ortogonais
      4. Interlúdio: formas diferenciais
      5. Operadores Diferenciais
      6. Operadores Diferenciais em 3 dimensões
      7. Teorema de stokes para formas diferenciais
   2. Análise Matemática
      1. Distribuições
      2. Teorema de Helmholtz
      3. Função de Green, Problema de Sturm Liouville e Transformadas Integrais.
      4. Laplaciano em Coordenadas Esféricas
:::

## Geometria Diferencial

:::{admonition} **Convenções Gerais**
:class: attention
:name: convencoes

- Métrica de Minkowsky:
$$\eta_{\mu\nu} = \mathrm{diag}(+1, -1, -1, -1)$$
- Sistema de Unidades: **SI**
- Ocasionalmente usaremos o sistema de unidades natural:
$$c=1,\; G=1,\; \hbar=1\;$$
:::

:::{admonition} **Convenções Sobre Vetores**
:class: attention
:name: convencao_vetores

Vamos procurar ser consistentes com os índices vetoriais. Para vetores cartesianos isto não é relevante, mas para qualquer outra situação existe uma diferença importante.

- Todos os **vetores** serão escritos com componentes com índice em cima.
- O índice que rotula o elemento da base é embaixo.
- Os coordenadas são vetores, tem índice em cima.
- Derivadas tem uma coisa com índice em cima (a coordenada) na parte de baixo de uma fração e portanto tem índices embaixo.
- Podemos subir ou abaixar os índices contraindo com a métrica.
- No caso cartesiano a métrica é a identidade e portanto podemos subir e descer os índices livremente.
- Vamos utilizar a [**convenção da soma de Einstein**](#soma)
:::

:::{prf:definition}**Convenção da Soma de Einstein**
:label: soma

- Em uma expressão usando componentes de objetos multilineares (vetores, tensores...), sempre que um índice aperecer duas vezes subentende-seuma soma neste índice sobre o número de dimensões do objeto.
- Embora existam expressões corretas com um índice repetido mais do que 2 vezes, este é um caso ultra-excepcional. Se você pensar em fazer isto, provavelmente tem um erro no seu cálculo.
- Índices de soma são chamados de **índices mudos** e a letra que se usa para designá-los pode ser alterada livremente.
- Igualdades devem ter os mesmos conjuntos de índices livres, independentemente dos índices mudos.
:::

### Tensores Isotrópicos (em 3D)

:::{prf:definition}**Delta de Kroenecker**
:label: kroenecker
$$\delta_{ij} = \left[
   \begin{array}{ll}
   0 & i\ne j \\
   1 & i=j  \\
   \end{array}
\right.
$$
:::

:::{prf:definition}**Símbolo de Levi-Civita**
:label: civita
$$\epsilon_{i_1 \cdots i_d} =
\begin{cases}
+1 & \text{se $\{i_i\}$ é uma permutação par de $(1, 2, 3\cdots d)$} \\
-1 & \text{se $\{i_i\}$ é uma permutação ímpar de $(1, 2, 3\cdots d)$} \\
0 & \text{se quaisquer índices são repetidos}
\end{cases}
$$
:::

Um tensor é dito isotrópico se a sua representação em coordenadas é a mesma para todos os sistemas de coordenadas que podm ser obtidos por rotações.

É trivial observar que os escalares são isotrópicos e o único vetor isotrópico é o vetor nulo.

Para objetos tensoriais de posto 2 começamos a encontrar objetos não triviais. Considere uma matriz $A$, se esta é isotrópica temos:

$$
A = RAR^T,
$$

onde $R$ são matrizes de rotação arbitrárias. Atacar este problema com as matrizes de rotação pode ser assustador, contudo, podemos escrevê-las em termos dos geradores do grupo de rotação, usando o fato de que o grupo de rotações é ortogonal e usando a fórmula de hadamard obter uma resposta simples para o problema:

$$
\begin{align}
R &= e^{\mathbb{\omega} \cdot \mathbb{L}} \\
R^T &= R^{-1} = e^{-\mathbb{\omega} \cdot \mathbb{L}} \\
e^{B} C e^{-B} &= \sum\frac{1}{n!}[\ldots[[[C, B], B],B]\ldots] \Rightarrow \\
[\mathbb{\omega} \cdot \mathbb{L}, A] &= 0 \\
\mathbb{\omega} \cdot \mathbb{L} &=
\begin{pmatrix}
0 & -z & y \\
z & 0 & -x \\
-y & x & 0
\end{pmatrix}
\end{align}
$$

Portanto a única matriz isotrópica (tensor de posto 2) é proporcional a $\delta_{ij}$.

Para construir um invariante com posto três é necessário usar a álgebra dos geradores, vamoas omitir os detalhes e apenas enunciar de $\epsilon_{ijk}$ é o tensor isotrópico de ordem 3.

:::{exercise}

Mostre que a condição

$$A_{ijk} = R^l_i R^m_j R^n_k A_{lmn}$$

implica em $A$ proporcional ao símbolo de Levi-Civita.

:::

:::{admonition} Propriedades
:class: important
:name: eps_delta_props

$$
\begin{align}
\hat e_i \cdot \hat e_j &= \delta_{ij} \\
\delta_{ii} &= d \\
\delta_{ij} &= \epsilon^{ijk} = 0 \\
[A \times B]^i &= \epsilon^{ijk} A_j B_j \\
\epsilon^{ijk}\epsilon_{ijk} &= 6 \\
\mathrm{det} A &= \epsilon_{ijk}C_{i1}C_{j2}C_{k3} \\
\epsilon_{lmn}\mathrm{det} A &= \epsilon_{ijk}C_{il}C_{jm}C_{kn} \\
\epsilon_{ijk} \epsilon_{lmn} &= \begin{vmatrix}
\delta_{il} & \delta_{im} & \delta_{in} \\
\delta_{jl} & \delta_{jm} & \delta_{jn} \\
\delta_{kl} & \delta_{km} & \delta_{kn}
\end{vmatrix}\\
\epsilon_{ijk} \epsilon_{imn} &= \delta_{jm}\delta_{kn} - \delta_{jn}\delta_{km}
\end{align}
$$
:::

:::{exercise}

Demonstre as propriedades [acima](#eps_delta_props).

:::

## Operador Diferenciais em Coordenadas Cartesianas

:::{admonition} Gradiente
:class: important

O **gradiente** de uma função escalar $f:\mathbb{R}^3 \to \mathbb{R}$ é o vetor cujas componentes são as derivadas parciais de $f$:

$$\nabla f(x,y,z) \;=\;
\left(
\frac{\partial f}{\partial x}, \;
\frac{\partial f}{\partial y}, \;
\frac{\partial f}{\partial z}
\right).
$$

**Definição como limite**:  
O gradiente é o vetor que aponta na direção de maior crescimento de $f$, definido pelo limite

$$
\nabla f(\mathbf{r}) \;=\;
\lim_{V \to 0} \frac{1}{V} \int_{\partial V} f(\mathbf{r}) \, \hat{n} \, dS,
$$

onde $V$ é um volume contendo o ponto $\mathbf{r}=(x,y,z)$, $\partial V$ sua superfície e $\hat{n}$ o vetor normal unitário.
:::

:::{admonition} Divergente
:class: important

O **divergente** de um campo vetorial $\mathbf{F}:\mathbb{R}^3 \to \mathbb{R}^3$ é dado por:

$$
\nabla \cdot \mathbf{F} \;=\;
\frac{\partial F_x}{\partial x} +
\frac{\partial F_y}{\partial y} +
\frac{\partial F_z}{\partial z}.
$$

**Definição como limite**:  
É a medida da taxa de variação de fluxo que sai de um ponto, definida por

$$
\nabla \cdot \mathbf{F}(\mathbf{r}) \;=\;
\lim_{V \to 0} \frac{1}{V}
\int_{\partial V} \mathbf{F} \cdot \hat{n} \, dS.
$$
:::

:::{admonition} Rotacional
:class: important

O **rotacional** de um campo vetorial $\mathbf{F}:\mathbb{R}^3 \to \mathbb{R}^3$ é dado por:

$$
\nabla \times \mathbf{F} \;=\;
\left(
\frac{\partial F_z}{\partial y} - \frac{\partial F_y}{\partial z}, \;
\frac{\partial F_x}{\partial z} - \frac{\partial F_z}{\partial x}, \;
\frac{\partial F_y}{\partial x} - \frac{\partial F_x}{\partial y}
\right).
$$

**Definição como limite**:  
É a medida da tendência de rotação local do campo, definida por

$$
\nabla \times \mathbf{F}(\mathbf{r}) \;=\;
\lim_{A \to 0} \frac{1}{A}
\int_{\partial A} \mathbf{F} \cdot d\mathbf{r},
$$

onde $A$ é uma superfície orientada contendo $\mathbf{r}$ e $\partial A$ sua curva de contorno.
:::

De um ponto de vista mnemônico, podemos construir o operador **nabla**:

$
\nabla = e_i \frac{\partial}{\partial x^i},
$

com o qual escrevemos, exclusivamente para coordenadas cartesianas:

$$
\begin{aligned}
\nabla f & = \frac{\partial f}{\partial x^i} e_i & \quad \textbf{gradiente}\\
\nabla \cdot \vec{A} &= \partial_i A^i & \quad \textbf{divergente}\\
[\nabla \times \vec{A}]_i & = \epsilon_{ijk} \partial^j A^k & \quad \textbf{rotacional}
\end{aligned}
$$

::::{admonition} Identidades Vetoriais em Coordenadas Cartesianas
:class: important

Aqui estão algumas identidades vetoriais fundamentais, em $\mathbb{R}^3$, escritas na notação indicial.

---

### 1. Produto vetorial duplo

$$
\vec A \times (\vec B \times \vec C) =
\vec B \, (\vec A \cdot \vec C) - \vec C \, (\vec A \cdot \vec B)
$$

:::{dropdown} Demonstração
Usando $\epsilon^{ijk}$ para o símbolo de Levi-Civita:

$$
\bigl[ \vec A \times (\vec B \times \vec C) \bigr]^i
= \epsilon^{ijk} A^j \, (\epsilon^{klm} B^l C^m).
$$

Expandindo com a identidade de contração:

$$
\epsilon^{ijk}\epsilon^{klm}
= \delta^{il}\delta^{jm} - \delta^{im}\delta^{jl},
$$

temos

$$
= (\delta^{il}\delta^{jm} - \delta^{im}\delta^{jl}) A^j B^l C^m
= B^i (A^j C^j) - C^i (A^j B^j).
$$
:::

### 2. Divergente de um rotacional

$$
\nabla \cdot (\nabla \times \vec A) = 0
$$

:::{dropdown} Demonstração

$$
\nabla \cdot (\nabla \times \vec A)
= \partial_i \bigl( \epsilon^{ijk} \partial_j A^k \bigr).
$$

Como $\epsilon^{ijk}$ é constante:

$$
= \epsilon^{ijk} \partial_i \partial_j A^k.
$$

As derivadas comutam, de modo que o termo é simétrico em $(i,j)$, mas $\epsilon^{ijk}$ é antissimétrico.  
Portanto, o resultado é **zero**.
:::

### 3. Rotacional no Produto Vetorial

$$
\nabla \cdot (\vec A \times \vec B) = \vec A\nabla\cdot \vec B - (\vec A \cdot \nabla) \vec B + (\vec B \cdot \nabla) \vec A - (\vec B \nabla \cdot \vec A
$$

:::{dropdown}Demonstração
Começamos com

$$
\bigl[\nabla \times (\vec A \times \vec B)\bigr]^i
= \epsilon^{ijk} \partial_j (\epsilon^{klm} A^l B^m).
$$

Usando a contração de Levi-Civita:

$$
= (\delta^{il}\delta^{jm} - \delta^{im}\delta^{jl}) \, \partial_j (A^l B^m).
$$

Expansão:

$$
= \partial_j (A^i B^j) - \partial_j (A^j B^i).
$$

Distribuindo as derivadas:

$$
= B^j \partial_j A^i + A^i \partial_j B^j
- \bigl(A^j \partial_j B^i + B^i \partial_j A^j\bigr).
$$

Ou seja,

$$
(\vec B \cdot \nabla)A^i - (\vec A \cdot \nabla)B^i
- A^i (\nabla \cdot \vec B) - B^i (\nabla \cdot \vec A).
$$
:::

### Rotacional Duplo

$$
\nabla \times \nabla \times \vec A = \nabla(\nabla\cdot \vec A) - \nabla^2 \vec A
$$

:::{dropdown}Demonstração

$$
\bigl[\nabla \times (\nabla \times \vec B)\bigr]^i
= \epsilon^{ijk} \partial_j \bigl( \epsilon^{klm} \partial_l B^m \bigr).
$$

Contraindo Levi-Civita:

$$
= (\delta^{il}\delta^{jm} - \delta^{im}\delta^{jl}) \partial_j \partial_l B^m.
$$

Primeiro termo:

$$
\delta^{il}\delta^{jm} \partial_j \partial_l B^m
= \partial_j \partial_i B^j
= \partial_i (\partial_j B^j).
$$

Segundo termo:

$$
- \delta^{im}\delta^{jl} \partial_j \partial_l B^m
= - \partial_j \partial_j B^i
= - \nabla^2 B^i.
$$

Logo,

$$
\nabla \times (\nabla \times \vec B)
= \nabla (\nabla \cdot \vec B) - \nabla^2 \vec B.
$$
:::

::::

## Mudanças de Coordenadas

Considere agora um novo sistema de coordenadas locais não-cartesiano $(\xi^1, \xi^2, \xi^3)$ dado por funções

$$
\begin{aligned}
e_i'&= \frac{\partial
\vec{r}}{\partial \xi^i}\\
e_i' &= \frac{\partial x^j}{\partial \xi^i} e_j = J^j{}_i e_j
\end{aligned}
$$

Um vetor é um objeto geométrico invariante por mudanças de coordenadas, logo

$$
\begin{aligned}
X &= X^i e_i = {X^j}' e_j' \Rightarrow \\
{X^j}' &= \frac{\partial \xi^j}{\partial x^i} X^i = {J^{-1}}_i^jX^i
\end{aligned}
$$

## Coordenadas Curvilíneas Ortogonais

:::{admonition} Coordenadas polares (2D)
:class: important

**Relação com Cartesianas**  
$$
x = r\cos\theta,\qquad y = r\sin\theta,\qquad r\ge 0,\ \theta\in[0,2\pi).
$$

**Base ortonormal**  
$$
\hat{\mathbf e}_r=(\cos\theta,\sin\theta),\quad
\hat{\mathbf e}_\theta=(-\sin\theta,\cos\theta).
$$

Fatores de escala (Lamé): $h_r=1,\ h_\theta=r$.

**Matriz jacobiana** $J=\frac{\partial(x,y)}{\partial(r,\theta)}$

$$
J=
\begin{pmatrix}
\cos\theta & -r\sin\theta\\
\sin\theta & \ \ r\cos\theta
\end{pmatrix},
\qquad |J|=r.
$$

**Elemento de linha e área**  
$$
ds^2 = dr^2 + r^2\,d\theta^2,\qquad dA = r\,dr\,d\theta.
$$
:::

:::{admonition} Coordenadas parabólicas (2D)
:class: important

**Relação com Cartesianas** (parabólicas planas)  

$$
x=\tfrac{1}{2}\bigl(\xi^2-\eta^2\bigr),\qquad y=\xi\,\eta,
\qquad \xi\in[0,\infty),\ \eta\in(-\infty,\infty).
$$

**Base ortonormal**  

$$
\frac{\partial \mathbf r}{\partial \xi}=(\xi,\eta),\quad
\frac{\partial \mathbf r}{\partial \eta}=(-\eta,\xi).
$$

**Fatores de escala**

$$
h_\xi=\Bigl\lVert \tfrac{\partial \mathbf r}{\partial \xi}\Bigr\rVert
=h_\eta=\Bigl\lVert \tfrac{\partial \mathbf r}{\partial \eta}\Bigr\rVert
=\sqrt{\xi^2+\eta^2}.
$$
$$
\hat{\mathbf e}_\xi=\frac{1}{\sqrt{\xi^2+\eta^2}}(\xi,\eta),\quad
\hat{\mathbf e}_\eta=\frac{1}{\sqrt{\xi^2+\eta^2}}(-\eta,\xi).
$$

**Matriz jacobiana**

$$
J=
\begin{pmatrix}
\xi & -\eta\\
\eta & \ \ \xi
\end{pmatrix},
\qquad |J|=\xi^2+\eta^2.
$$

**Elemento de linha e área**  
$$
ds^2=(\xi^2+\eta^2)\,(d\xi^2+d\eta^2),\qquad
dA=(\xi^2+\eta^2)\,d\xi\,d\eta.
$$
:::

:::{admonition} Coordenadas cilíndricas (3D)
:class: important

**Relação com Cartesianas**  
$$
x=\rho\cos\varphi,\quad y=\rho\sin\varphi,\quad z=z,
\qquad \rho\ge 0,\ \varphi\in[0,2\pi).
$$

**Base ortonormal**  
$$
\hat{\mathbf e}_\rho=(\cos\varphi,\sin\varphi,0),\quad
\hat{\mathbf e}_\varphi=(-\sin\varphi,\cos\varphi,0),\quad
\hat{\mathbf e}_z=(0,0,1).
$$

**Fatores de escala**: $h_\rho=1,\ h_\varphi=\rho,\ h_z=1.$

**Matriz jacobiana**

$$
J=
\begin{pmatrix}
\cos\varphi & -\rho\sin\varphi & 0\\
\sin\varphi & \ \ \rho\cos\varphi & 0\\
0&0&1
\end{pmatrix},
\qquad |J|=\rho.
$$

**Elemento de linha e volume**  
$$
ds^2=d\rho^2+\rho^2\,d\varphi^2+dz^2,\qquad
dV=\rho\,d\rho\,d\varphi\,dz.$$
:::

:::{admonition} Coordenadas esféricas (3D)
:class: important

**Relação com Cartesianas** (convenção: $\theta$ polar, $\varphi$ azimutal)  

$$
x=r\sin\theta\cos\varphi,\quad
y=r\sin\theta\sin\varphi,\quad
z=r\cos\theta,
$$
$$
r\ge 0,\ \theta\in[0,\pi],\ \varphi\in[0,2\pi).
$$

**Base ortonormal**  
$$
\hat{\mathbf e}_r=(\sin\theta\cos\varphi,\sin\theta\sin\varphi,\cos\theta),\quad
\hat{\mathbf e}_\theta=(\cos\theta\cos\varphi,\cos\theta\sin\varphi,-\sin\theta),\quad
\hat{\mathbf e}_\varphi=(-\sin\varphi,\cos\varphi,0).
$$

**Fatores de escala**: $h_r=1,\ h_\theta=r,\ h_\varphi=r\sin\theta.$

**Matriz jacobiana**

$$
J=
\begin{pmatrix}
\sin\theta\cos\varphi & r\cos\theta\cos\varphi & -r\sin\theta\sin\varphi\\
\sin\theta\sin\varphi & r\cos\theta\sin\varphi & \ \ r\sin\theta\cos\varphi\\
\cos\theta            & -r\sin\theta           & 0
\end{pmatrix},
\qquad |J|=r^2\sin\theta.
$$

**Elemento de linha e volume**  
$$
ds^2=dr^2+r^2\,d\theta^2+r^2\sin^2\theta\,d\varphi^2,\qquad
dV=r^2\sin\theta\,dr\,d\theta\,d\varphi.$$
:::

:::{admonition} Coordenadas hiperesféricas (d dimensões)
:class: important

**Relação com Cartesianas**  
Coordenadas $(r,\phi_1,\ldots,\phi_{d-1})$ com
$$
\begin{aligned}
x_1 &= r\cos\phi_1,\\
x_2 &= r\sin\phi_1\cos\phi_2,\\
x_3 &= r\sin\phi_1\sin\phi_2\cos\phi_3,\\
&\ \ \vdots\\
x_{d-1} &= r\sin\phi_1\cdots\sin\phi_{d-2}\cos\phi_{d-1},\\
x_d &= r\sin\phi_1\cdots\sin\phi_{d-2}\sin\phi_{d-1},
\end{aligned}
$$
com domínios $r\ge 0$, $\phi_1,\ldots,\phi_{d-2}\in[0,\pi]$, $\phi_{d-1}\in[0,2\pi)$.

**Base ortonormal e fatores de escala**  
Sistema **ortogonal** com
$$
h_r=1,\qquad
h_{\phi_k}=r\prod_{j=1}^{k-1}\sin\phi_j\quad (k=1,\ldots,d-1),
$$
(produto vazio $=1$, logo $h_{\phi_1}=r$, $h_{\phi_2}=r\sin\phi_1$, …).  
Versores: $\hat{\mathbf e}_q=\frac{1}{h_q}\,\partial \mathbf r/\partial q$.

**Determinante jacobiano**  
Para sistemas ortogonais, $|J|=\prod h_i$. Assim,
$$
|J|=r^{\,d-1}\,\prod_{k=1}^{d-2}\bigl(\sin\phi_k\bigr)^{\,d-1-k}.
$$

**Elemento de linha e volume**  
$$
ds^2=dr^2+\sum_{k=1}^{d-1} h_{\phi_k}^2\,d\phi_k^{\,2}
=dr^2+r^2\!\left[d\phi_1^2+\sin^2\!\phi_1\,d\phi_2^2+\cdots
+\Bigl(\!\prod_{j=1}^{d-2}\sin^2\!\phi_j\Bigr)d\phi_{d-1}^2\right],
$$
$$
dV=|J|\,dr\,d\phi_1\cdots d\phi_{d-1}
= r^{\,d-1}\!\left(\prod_{k=1}^{d-2}\sin^{\,d-1-k}\!\phi_k\right)\!dr\,d\phi_1\cdots d\phi_{d-1}.$$
:::

## Variedades Diferenciais, vetores e formas diferenciais

Uma **variedade diferencial** $M$ de dimensão $n$ é um espaço topológico que localmente se parece com $\mathbb{R}^n$ e admite um atlas de cartas coordenadas sobre as quais podemos definir funções suaves e derivadas.

:::{figure} ../00_images/02_lessons/manifolds.png
:name: manifolds_fig

Uma Variedade diferencial e algumas aplicações lineares discutidas no texto abaixo.
:::

:::{admonition} **Variedade Diferencial**
Uma variedade diferencial $n$-dimensional $\mathcal{M}$ é um espaço topologicamente Hausdorff, com base contável, localmente homeomorfo a $\mathbb{R^d}$. Sejam $\{U_i\}$ uma coleção de abertos de $\mathcal{M}$ e $\{V_i\}$ abertos de $\mathbb{R^d}$ tais que $\phi: U_i \mapsto V_i$ são os homeomofismos.

- $\phi: U_i \mapsto V_i$: definem as cartas e o sistema de coordenadas.
- $U_i$é a vizinhança coordenada.
- $\phi(p)$ são as coordenadas locais do ponto $p$.
- $\bigcup U_i = \mathcal{M}$: as cartas fazem um cobrimento da variedade.
- O conjunto de cartas é um atlas.
:::

:::{exercise}
:label: s2_etereo

Considere $S^2$ como uma variedade diferencial. Considere duas cartas com a projeção estereográfica, cobrindo toda a variedade.
:::

Para definir vetores em uma variedade é necessário compreender que os vetores são objetos locais e não globais, formando um espaço vetorial de mesma dimensão, para cada ponto da variedade.

:::{figure} ../00_images/02_lessons/tangent_01.webp
:name: tangent_fig_01
Visualizando os espaços tangentes da esfera $S^2$.
:::

Para realizar esta construção e revelar as suas propriedades, vamos considerar um ponto $p \in \mathcal{M}$ e um conjunto de curvas suaves $\gamma: (-\epsilon, \epsilon) \in \mathbb{R} \mapsto \mathcal{M}$ tais que $\gamma(0) = p$. Este conjunto de curvas na variedade tem coordenadas em $\mathbb{R}^d$ e podemos escrever o vetor tangente a curva no ponto $p$ sem ambiguidade. O que ainda deve ser levado em conta é que muitas curvas passando por $p$ possuem o mesmo vetor tangente, mas esta propriedade é uma relação de equivalência e podemos definir:

:::{admonition} **Espaço Tangente**
:class: important

$$
T_pM = \left\{ [\gamma]_p \vert \gamma: (-\epsilon, \epsilon) \in \mathbb{R} \mapsto \mathcal{M} \land \gamma(0) = p \right\}
$$

:::

:::{figure} ../00_images/02_lessons/tangent_02.webp
:name: tangent_fig_02

Visualizando os espaços tangentes como a derivada direcional.
:::

Esta definição é equivalente a dizer que os vetores são operadores lineares que implementam uma diferenciação no espaço das funções suaves sobre $\mathcal{M}$, $\Chi(\mathcal{M})$. A ação dos vetores é dada pela derivada direcional:

$$
\begin{aligned}
v_p[f] &= D_{[\gamma]_p} f \\
&= \left. \frac{\partial (f\circ \gamma)}{\partial t} \right \rvert_{t=0}\\
&= \left. \frac{\partial (f(x^i(t)))}{\partial t} \right \rvert_{t=0} \\
&= \left. \frac{\partial f}{\partial x^i}\right \rvert_{\gamma(0)} \left. \frac{\partial x^i}{\partial t} \right \rvert_{t=0} \\
&= \left. \frac{\partial f}{\partial x^i}\right \rvert_{p} v^i
\end{aligned}
$$

O **espaço tangente** $T_pM$ em um ponto $p\in M$ é o espaço vetorial formado pelos vetores tangentes às curvas em $M$ que passam por $p$.  

Em coordenadas locais $(x^1,\dots,x^n)$, uma base de $T_pM$ é
$$
\left\{ \frac{\partial}{\partial x^1}\Big|_p, \dots, \frac{\partial}{\partial x^n}\Big|_p \right\}.
$$

O **espaço cotangente** $T_p^*M$ é o dual de $T_pM$, isto é, o espaço das formas lineares que agem sobre vetores tangentes.  

A base dual é dada por $\{dx^1|_p, \dots, dx^n|_p\}$, com $dx^i\!\left(\tfrac{\partial}{\partial x^j}\right)=\delta^i_j$.

:::{admonition} **Tensor**
:class: important

Seja $L$ um espaço linear n-dimensional e $L^\star$ seu espaço dual. Um tensor de tipo $(p, q)$ é uma aplicação multilinear:

$$
t: \underbrace{L \times L \cdots \times L \times L^\star}_{q} \underbrace{\times L^\star \cdots \times L^\star}_{p} \mapsto \mathbb{R} \\
(v_{i_1}, \ldots v_{i_q}; \omega_{j_1}, \ldots \omega_{j_p}) \mapsto t(v_{i_1}, \ldots v_{i_q}; \omega_{j_1}, \ldots \omega_{j_p}) \in \mathbb{R}\\
t(\ldots v_{i_q} + \lambda w \ldots) = t(\ldots v_{i_q} \ldots) + + \lambda t(\ldots w \ldots)
$$

para todas as posições. O espaço vetorial obtido com a coleção destes objetos é o espaço $T_q^p(L)$, e $T_0^0(L) \equiv \mathbb{R}$
:::

:::{admonition} **p-formas**
:class: important

Dado o espaço dos tensores $T_p^0(L)$, um tensor $\omega$ é uma p forma se é completamente antisimétrico. A coleção das p-formas forma o espaço vetorial $\Omega^p$.

- $\Omega^0 \equiv \mathbb{R}$
- $\Omega^1 \equiv T_1^0(\mathbb{M}) \equiv T_p^\star(M)$

Podemos definir uma operação de projeção:

$$
\pi^A: T_p^0 \mapsto \Omega^p \\
(\pi^A t)(v_{i_1},\ldots,v_{i_p}) = \frac{1}{p!}\sum_\sigma t(\sigma(v_{i_1},\ldots,v_{i_p}))
$$

E agora podemos definir uma estrutura algébrica utilizando o produto exterior:

$$
\wedge : \Omega^p \times \Omega^q \mapsto \Omega^{p+q} \\
(\alpha, \wedge) \mapsto \alpha \wedge \beta \\
\alpha \wedge \beta \equiv \frac{(p+q)!}{p!q!}\pi^A(\alpha \otimes \beta)
$$

e pode-se mostrar sem dificuldade que este produto é **bilinear**, **associativo** e $mathbb{Z}$-graduado.

$$
\alpha \wedge \beta = (-1)^{pq} \beta \alpha.
$$
:::

Em coordenadas, uma 1-forma é
$$
\alpha = \alpha_i(x)\,dx^i,
$$
e uma 2-forma é
$$
\beta = \tfrac{1}{2}\beta_{ij}(x)\,dx^i\wedge dx^j,\quad \beta_{ij}=-\beta_{ji}.
$$

Em uma variedade $n$-dimensional, o espaço de $p$-formas $\Omega^p(M)$ tem dimensão
$$
\dim \Omega^p(M)=\binom{n}{p}.
$$

A **derivada exterior** $d:\Omega^k(M)\to\Omega^{k+1}(M)$ é definida por:

- $d(f)=df=\partial_i f\, dx^i$ para funções,
- satisfaz linearidade, regra de Leibniz e $d^2=0$.

Exemplo em $\mathbb{R}^3$:  
Se $\alpha = f\,dx+g\,dy+h\,dz$, então
$$
d\alpha = (\partial_x g - \partial_y f)\,dx\wedge dy + (\partial_y h - \partial_z g)\,dy\wedge dz + (\partial_z f - \partial_x h)\,dz\wedge dx.
$$

-----------
#### Aplicações de tensores e campos

Dadas duas variedades $\mathcal{M}, \mathcal{N}$, e funções suaves $\chi, \psi, f$ como no diagrama:

$$
\mathbb{R} \xleftarrow{\chi} \mathcal{M} \xrightarrow{f} \mathcal{N} \xrightarrow{\psi} \mathbb{R},
$$

Vemos que a aplicação $\psi$ induz uma função sobre $\mathcal{N}:

$$
\mathcal{M} \xrightarrow{f} \mathcal{N} \xrightarrow{\psi} \mathbb{R} \\
\psi \circ f: \mathcal{M} \rightarrow \mathbb{R},
$$

contudo a operação semelhante com a função $\chi$ necessitaria da inversa de $f$ que não assumimos que exista. Nesta situação, vemos que funções são transportadas "seta acima", ou seja, elas são **pulled back**.

Funções são campos tensoriais de tipo $(0,0)$.

:::{admonition} **pullback** de uma função
:class: important

Seja $f: \mathcal{M} \rightarrow \mathcal{N}$ uma aplicação suave e $\psi : \mathcal{N} \rightarrow \mathbb{R}$ uma função de $\mathcal{N}$.

- $f^\star \psi := \psi \circ f$ induz uma função $f^\star: \mathcal{M} \rightarrow \mathbb{R}$
- Em coordenadas locais:
$$
f: x^i \mapsto y^i \Rightarrow (f^\star \psi)(x) = \psi(y(x))
$$
- Para uma composição $\mathcal{M} \xrightarrow{f} \mathcal{N} \xrightarrow{g} \mathcal{S}  $:
$$
(g\circ f)^\star = f^\star\circ g^\star
$$

A aplicação tangente, ou o diferencial, ou ainda o **pushforward** é

$$
T_x f \equiv f_\star: T_x\mathcal{M} \rightarrow T_{f(x)} \mathcal{N}\\
f_\star[\gamma] \equiv [f\circ \gamma]\\
f_\star(V_i\partial_i) = (\frac{\partial y^a}{\partial x^i} V^i) \partial_a
$$

- Em coordenadas locais:
$$
f: x^i \mapsto y^i \Rightarrow (f^\star \psi)(x) = \psi(y(x))
$$
- Para uma composição $\mathcal{M} \xrightarrow{f} \mathcal{N} \xrightarrow{g} \mathcal{S}  $:
$$
(g\circ f)^\star = f^\star\circ g^\star
$$

Aplicando isto para o espaço dos covetores:

$$
f: \mathcal{N} \mapsto \mathcal{N}\\
f^\star: T^\star_{f(x)}\mathcal{N} \rightarrow T^\star_{f(x)}\mathcal{M}
\langle f\star \alpha, V\rangle \equiv \langle \alpha, f_\star V\rangle \\
f^\star dy^a = \frac{\partial y^a}{\partial x^i} dx^i = J^a_i dx^i
$$

covetores e campos covariantes podem ser propagados usando o **pullback**, definindo campos em variedades derivadas. O procedimento não se generaliza para campos vetoriais. Apenas de $f$ é um **difeomorfismo** podemos propagar os campos vetoriais via **puhforward**.
:::

#### Métrica

Em uma variedade $\mathcal{M}$ em que consideramos tensores arbitrários $(p, q)$, existe um tensor canônico do tipo $(1, 1) que se constitui no pareamento canônico:

$$
\hat{\mathbb{1}} \langle V, \alpha \rangle
\langle \alpha, V \rangle \Rightarrow \hat{\mathbb{1}} \langle V, \cdot \rangle = V, \hat{\mathbb{1}} \langle \cdot, \alpha \rangle = \alpha \\
\hat{\mathbb{1}} = dx^i\otimes \partial_j \Rightarrow \hat{\mathbb{1}}^1_j = \delta^i_ j
$$

Um tensor $(0,2)$ positivo definido define uma métrica riemanniana na variedade, com a qual é possível construir:
- Produto interno de vetores
- Elemento de Linha
- Isomorfismos musicais
- Abaixamento e levantamento de índices (via isomorfismos musicais)
- Forma de volume (acrescida de uma orientação)

:::{admonition} **Métrica e Propriedades**
:class: important

$$
\begin{aligned}
g \in \mathcal{T}^0_2 &\Rightarrow g: T_p\mathcal{M} \times T_p\mathcal{M} \mapsto \mathbb{R}\\
g(U, V) = g(V, U) \;&\land g(U, U) \ge 0 \; \land g(U, U)=0 \Leftrightarrow U \equiv 0 \\
g(U, V) &= (g_{ij} dx^i\otimes dx^j )(U^k\partial_k, V^l\partial_l) \\
&= g_{ij} U^k V^l (dx^i \otimes \partial_k) (dx^i \otimes \partial_k) \\
&= g_{ij} U^k V^l \delta^i_k \delta^j_l = g_{ij} U^i V^j\\
\flat_g: T_p\mathcal{M} &\mapsto T^\star_p\mathcal{M}\\
\flat_g (V^i\partial_i) &= g_{ij} V^j dx^i = V_i dx^i \\
\sharp_g: T^\star_p\mathcal{M} &\mapsto T_p\mathcal{M}\\
\sharp_g (\omega_i dx^i) &= g^{ij} \omega_i \partial_i = \omega^i \partial_i \\
g_{ij}(x) &= \langle \partial_i, \partial_j \rangle \\
&= \langle \frac{\partial x'^r}{\partial x^i} \partial'_r, \frac{\partial x'^s}{\partial x^j}\partial'_s\rangle \Rightarrow\\
g_{ij} &= \frac{\partial x'^r}{\partial x^i}\frac{\partial x'^r}{\partial x^i} g'_{rs} \\
ds^2 &= g_{ij} dx^i dx^j
\end{aligned}
$$
:::

:::{figure} ../00_images/02_lessons/maps.webp
:name: maps_fig_01

Visualizando os espaços tangentes, cotangente, pullback, pushforward e isomorfismos musicais.
:::

Em uma variedade orientada com métrica $g$, a **forma de volume** é
$$
\mathrm{vol} = \sqrt{|g|}\, dx^1\wedge\cdots\wedge dx^n,
$$
onde $|g|=\det(g_{ij})$.

:::{admonition} **Operador de Hodge**
:class: important
Seja um espaço linear n-dimensional $L$ dotado de uma métrica $g$ e uma orientação $o$. Seja $\omega \equiv \omega_{g,o}$ a correspondente forma de volume. O Operador de Hodge é:
$$
\alpha \mapsto \star\alpha, \quad \alpha \in \Omega^pL, \quad \star \alpha \in \Omega^{n-p}L \\
\star \alpha_{i_1\ldots i_p} := \frac{1}{p!}\alpha^{i_{p+1}\ldots i_{n}}\omega_{i_1\ldots i_p\;i_{p+1}\ldots i_{n}}\\
\star_g \mathbb{1} = \omega_g \\
\star \omega_g = \mathrm{sign}\;g \\
\star_g \star_g = \mathrm{sign}\;g (-1)^{p(n-p)}\\
\alpha \wedge \star_g \beta = \langle \alpha, \beta \rangle_g\; \omega_g
$$
:::

A **coderivada** $\delta:\Omega^k(M)\to\Omega^{k-1}(M)$ é definida via o Hodge:
$$
\delta = (-1)^{n(k+1)+1} d.
$$

Ela é o adjunto formal da derivada exterior em relação ao produto interno definido pela métrica.

O **Laplaciano de Hodge** é
$$
\Delta = d\delta+\delta d.
$$

Em funções escalares ($0$-formas), em $\mathbb{R}^n$ euclidiano, reduz-se ao Laplaciano usual
$$
\Delta f = \sum_{i=1}^n \partial_i^2 f.
$$

Os operadores diferenciais usuais em 3 dimensões podem ser definidos de forma simples com este formalismo:

:::{figure} ../00_images/02_lessons/3dops.png
:name: 3dops_fig_01
:::

- **Gradiente**:
$$
\begin{aligned}
   f \in \Chi(\mathcal{M}) \cong \Omega^0 &\xrightarrow{\,d\,} df \in \Omega^1 \xrightarrow{\,\#\,} \nabla f \in T_p\mathcal{M}. \\
   \nabla: \Chi(\mathcal{M}) &\mapsto T_p\mathcal{M} \\
   \nabla f &= (df)^\sharp \\
   &=\sum_i \frac{1}{h_i}\frac{\partial f}{\partial u^i}\, \hat e_i.
\end{aligned}
$$

- **Divergente**:

 $$
 \mathbf{A}\;(\text{vetor}) \xrightarrow{\,b\,} \mathbf{A}^b\;(\text{1-forma})
 \xrightarrow{\,\star\,} (\text{2-forma})
 \xrightarrow{\,d\,} (\text{3-forma})
 \xrightarrow{\,\star\,} (\text{0-forma})
 $$

$$
\nabla \cdot X = * d (X^\flat) = \frac{1}{h_1 h_2 h_3}
\sum_i \frac{\partial}{\partial u^i}\Bigg(
\frac{h_1 h_2 h_3}{h_i} X^i
\Bigg). = \frac{1}{\sqrt{|g|}} \partial_i\!\bigl(\sqrt{|g|}\, A^i\bigr),
$$

- **Rotacional**:
$$
   \mathbf{A}\;(\text{vetor}) \xrightarrow{\,b\,} \mathbf{A}^b\;(\text{1-forma})
   \xrightarrow{\,d\,} (\text{2-forma})
   \xrightarrow{\,*\,} (\text{1-forma})
   \xrightarrow{\,\#\,} (\text{vetor}) = \nabla\times\mathbf{A}.
   $$
$$
\nabla \times X = (* d X^\flat)^\sharp = \frac{1}{h_j h_k}
\left[
\frac{\partial}{\partial u^j}(h_k X^k) -
\frac{\partial}{\partial u^k}(h_j X^j)
\right] = \frac{1}{\sqrt{|g|}} \varepsilon^{ijk} \partial_j (g_{k\ell} A^\ell),
$$

- **Laplaciano**:

$$
\Delta f = \delta d f = - d df = \frac{1}{h_1 h_2 h_3}
\sum_i \frac{\partial}{\partial u^i}
\Bigg( \frac{h_1 h_2 h_3}{h_i^2} \frac{\partial f}{\partial u^i} \Bigg) = \frac{1}{\sqrt{|g|}} \partial_i\!\Bigl(\sqrt{|g|}\, g^{ij}\partial_j f\Bigr).
$$

Vamos utilizar este poderoso formalismo para revelar a estrutura íntima das equações de Maxwell.
