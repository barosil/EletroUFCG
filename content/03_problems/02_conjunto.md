# Variedades Diferenciais

## Definições

:::{admonition} **Definition**: Produto wegde
:class: important

Uma base para as $k$-formas em uma variedade $d$ dimensional é dada por:
$$
dx^{i_1}\wedge dx^{i_2}\wedge\cdots\wedge dx^{i_k} = \mathrm{sgn}(i) dx^{1}\wedge\cdots\wedge dx^{k}
$$
:::

:::{admonition} **Definition**: Derivada Exterior
:class: important

Seja $\omega$ uma  $k$-formas em uma variedade $d$ dimensional é dada por:
$$
d\omega = \partial_\mu \omega_{i_1\cdots i_k} dx^{\mu}\wedge dx^{i_1}\wedge dx^{i_2}\wedge\cdots\wedge dx^{i_k}
$$
:::

:::{admonition} **Definition**: Dual de Hodge
:class: important

Seja $\omega$ uma  $k$-formas em uma variedade $d$ dimensional é dada por:
$$
\star\omega = \frac{\sqrt{g}}{(d-k)!} g^{i_1 j_1} \cdots g^{i_k j_k} \epsilon_{j_1 j_2 \cdots j_d }  \omega_{i_1\cdots i_k} dx^{i_{k+1}}\wedge\cdots\wedge dx^{j_n}
$$
:::

:::{admonition} **Definition**: Coderivada
:class: important

$$
d^\dagger = (-1)^{n(k+1)+1}\star d \star
$$
:::

## Problemas

:::{admonition} Problema: **Dual de Hodge**

- Mostre que:
  $$\star \star \omega = (-1)^{(k(n-k))} \omega, \quad \forall \omega \in \Omega_k$$
- Mostre que:

$$
d^\dagger = (-1)^{k}\star^{-1} d \star
$$
:::

:::{admonition} Problema: **levi civita**

- Sejam $x^\mu$ e $x'^\nu$ dois sistemas de coordenadas. Mostre que:

$$
\epsilon_{j_1 j_2 \cdots j_d }` = J \epsilon_{j_1 j_2 \cdots j_d }, \quad \mathrm{onde} \\
J = \det \frac{\partial x^\nu}{\partial x'^\nu}
  $$

- Mostre que:

$$
g' = J^2 g
$$

- Mostre que $\sqrt|{g} \epsilon_{j_1 j_2 \cdots j_d }$ é invariante.

- Mostre que:

$$\epsilon^{j_1 j_2 \cdots j_d } = \frac{1}{\sqrt{g}} \epsilon^{j_1 j_2 \cdots j_d }$$
:::

:::{admonition} Problema: **Divergência**

- Calcule $\star d \star omega$ em componentes, para uma $1$-forma em 3 dimensões.
- A partir do resultado acima, escreva asequencia de operações necessárias para escrever o divergente de um vetor em três dimensões.
- Considerando um sistema de coordenadas ortogonais, escreva a expressão para o divergente de um vetor na base ortonormal.
- Considerando coordenadas cilíndricas, escreva a expressão para o divergente.
- Considerando coordenadas esféricas, escreva a expressão para o divergente.
:::

:::{admonition} Problema: **Pull Back**

Sejam $M$ e $N$ variedades diferenciais de dimensões $m$ e $n$ respectivamente. Suponha $g: M\mapsto N$ uma aplicação suave. A aplicação $g^\star: \Omega(N) \mapsto \Omega(M)$ que mapeia as formas de $N$ nas formas de $M$ é chamada de **pullback** de $g$ e satisfaz:

1.Se $f: N \mapsto \mathrm{R}$ é função sobre $N$:

$$
g^\star f = f \circ g
$$

2.Se $\eta, \omega \in \Omega_p(N)$:

$$
g^\star (\eta \wedge \omega) = (g^\star \eta) (g^\star \omega)
$$

3.Se $\omega \in \Omega_p(N)$:

$$
g^\star (d\omega) = d(g^\star \omega)
$$

- Procure se convencer de que a primeira propriedade define o pullback das $0$-formas.

- Considerando coordenadas $y^i$ em $N$ e $x^i$ em $M$, se convença de que:

$$
g^\star (dy^i) (x) = d(y^i\circ g)(x) \Rightarrow \\
g^\star \omega(x) = \omega(g(x))_{i_1\cdots i_k} dg^{i_1}\wedge \cdots dg^{i_k}
$$

1. Agora, demonstre que esta definição satisfaz a propriedade 2.
2. Demonstre que esta definição satisfaz a propriedade 3.
3. COnsidere o caso em que $M$ e $N$ são idênticos e considere o pullback atuando na forma de volume. Qual é o resultado?
4. Seja $U = (0, \infty) \times (0, 2\pi)$, $V=\mathbb{R}^2-{\textrm{eixo x não negativo}}$. Use coordenadas $(r, \theta)$ para $U$ e $(x, y)$ para $V$. Considere a aplicação $g(r, \theta) = (r\cos\theta, r\sin\theta)$. Considere $h=g^{-1}$. Finalmente, sobre $V$ considere a forma $\omega = e^{x^2 + y^2} dx \wedge dy$:
   1. Calcule $g^\star(x), g^\star(y), g^\star(dx), g^\star(dy), g^\star(dx \wedge dy), g^\star \omega$.
   2. Calcule $h^\star(r), h^\star(\theta), h^\star(dr), h^\star(d\theta)$.

:::
