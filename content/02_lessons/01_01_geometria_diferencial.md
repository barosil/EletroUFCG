# Preliminares Matemáticas

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

### Tensores Isotrópicos

Considere o espaço $\mathbb{R}^3$ com coordenadas cartesianas $(x^1, x^2, x^3)$, denotamos por $\{e_i\},\, i=1,2,3$ os **vetores ortonormais**. Vamos definir alguns objetos.

:::{definition} Delta de Kronecker

$$
\delta_{ij} =
\begin{cases}
1, & i=j \\
0, & i\neq j
\end{cases}
$$
:::

:::{definition} Símbolo de Levi-Civita

$$\epsilon_{ijk} =
\begin{cases}
+1 & \text{se $(i,j,k)$ é uma permutação par de (1,2,3)} \\
-1 & \text{se $(i,j,k)$ é uma permutação ímpar de (1,2,3)} \\
0 & \text{se quaisquer índices são repetidos}
\end{cases}
$$
:::

Assim, podemos escrever:
$$
\vec{a}\cdot\vec{b} = a_i b_i = \delta_{ij} a_i b_j \\
(\vec{a}\times\vec{b})_i = \epsilon_{ijk} a_j b_k
$$

Uma propriedade importate:
$$
\epsilon_{ijk} \epsilon_{lmn}
=

\begin{vmatrix}
\delta_{il} & \delta_{im} & \delta_{in} \\
\delta_{jl} & \delta_{jm} & \delta_{jn} \\
\delta_{kl} & \delta_{km} & \delta_{kn}
\end{vmatrix}
$$

Em particular
$$
\epsilon_{ijk} \epsilon_{imn} = \delta_{jm}\delta_{kn} - \delta_{jn}\delta_{km}
$$

### Operador $\nabla$

Considere um vetor:
$$
\vec{r} = x^i e_i
$$

temos que:
$$
d\vec{r} = dx^i e_i
$$

Vamos *sugerir* um operador:

$
\nabla = e_i \frac{\partial}{\partial x^i}
$

E definimos, exclusivamente para coordenadas cartesianas:
$$
\begin{aligned}
\nabla f & = \frac{\partial f}{\partial x^i} e_i & \quad \textbf{gradiente}\\

\nabla \cdot \vec{A} &= \partial_i A_i & \quad \textbf{divergente}\\

\nabla \cdot \vec{A} &= \partial_i A_i & \\

\nabla \times \vec{A} &= \vec B & \\
\nabla \times \vec{A} & = \epsilon_{ijk} \partial_j A_k e_i & \quad \textbf{rotacional}
\end{aligned}
$$

### Mudanças de Coordenadas

Considere agora um novo sistema de coordenadas locais não-cartesiano $(\xi^1, \xi^2, \xi^3)$ dado por funções

$$
\begin{aligned}
\vec{e}_i &=& \frac{\partial
\vec{r}}{\partial \xi^i}\\

\vec{e}_i &=& \frac{\partial x^j}{\partial \xi^i} e_j\\

J^j{}_i &=& \frac{\partial x^j}{\partial \xi^i}\\

\vec{e}_i &=& J^j{}_i e_j
\end{aligned}
$$

### Métrica e Elemento de linha

$$
ds^2 = dx^i dx^i = \frac{\partial x^i}{\partial \xi^j}\frac{\partial x^i}{\partial \xi^k} d\xi^j d\xi^k
$$

$$
g_{jk} = \vec{e}_j \cdot \vec{e}_k
$$
$$
ds^2 = g_{jk}\, d\xi^j d\xi^k
$$

### Elemento de Volume

$$

dV = \det(J) \, d\xi^1 d\xi^2 d\xi^3 \\
dV = \sqrt{g} \, d\xi^1 d\xi^2 d\xi^3
$$
