# Equações de Maxwell

:::{epigraph}
Algumas pessoas adquirem sua compreensão do mundo por meio de símbolos e matemática. Outras adquirem sua compreensão por meio da geometria pura e do espaço. Há outras que encontram uma aceleração no esforço muscular que lhes é imposto na compreensão, ao sentir a força dos objetos que se movem pelo mundo. O que elas desejam são palavras de poder que comovam suas almas como a lembrança da infância. Para o bem de pessoas desses diferentes tipos, quer queiram a palidez e a tenuidade do simbolismo matemático, quer queiram os aspectos robustos desse engajamento muscular, devemos apresentar todas essas maneiras. É a combinação delas que nos dá o melhor acesso à verdade.
*James Clerck Maxwell*

I saw that it was great, greater and greatest ... I was determined to master the book and set to work.
*Oliver Heaviside*

::::

:::{figure} ../00_images/02_lessons/00_maxwell.png
:name: fig-layout
:align: center
:width: 100%

Isaac Newton, James Clear Maxwell, Albert Einstein e os quatro *maxwellianos*: Heinrich Rudoph Hertz, George Francis FitzGerald, Oliver Lodge e Oliver Heaviside.

::::

## Um breve olhar historiográfico [^1]

[^1]: Baseado em [The Long Road to Maxwell’s Equations](https://spectrum.ieee.org/the-long-road-to-maxwells-equations)

- **1785** - **Charles-Augustin de Coulomb** reports that the force between two charges varies with the inverse square of the distance.

- **1800** - **Alessandro Volta** invents the first battery, which allowed experimenters to begin working with continuous direct current.

- **1820** - **Hans Christian Ørsted** shows that the needle of a compass can move when brought close to a current-carrying wire, the first evidence of a link between electricity and magnetism.

- **1820** - **André-Marie Ampère** shows that two parallel current-carrying wires can attract or repel each other, depending on the relative direction of their currents.

- **1831** - **Michael Faraday**, who conceived of electrical and magnetic fields, discovers electromagnetic induction.

- **1831** - **James Clerk Maxwell** is born in Edinburgh.

- **1855** - **Maxwell**’s first paper on Faraday’s observations and theories debuts.

- **1861 & 1862** - **Maxwell** publishes a four-part paper, “On Physical Lines of Force.” It introduces the core idea that a change in electric flux through a surface can create a magnetic field.

- **1864** - **Maxwell** presents new work before the Royal Society of London, published the next year. It suggests that electric and magnetic fields can move through space in waves and that light itself is such a wave.

- **1873** - **Maxwell** publishes his magnum opus, A Treatise on Electricity and Magnetism, which contains further mathematical and interpretive work.

- **1879** - **Heinrich Hertz**’s interest in Maxwell’s work is piqued by a Prussian Academy of Sciences competition to obtain experimental evidence for or against electro-magnetic waves.

- **1879** - Maxwell dies of stomach cancer at age 48.

- **1885** - **Oliver Heaviside** publishes a condensed version of Maxwell’s equations, reducing the equation count from 20 to four.

- **1888** - **Hertz**, several years after moving to a well-equipped laboratory in Karslruhe, reports confirmation of the existence of the electromagnetic waves predicted by Maxwell.

- **1940** - **Albert Einstein** gives the term “Maxwell’s equations” a boost with his monograph “Considerations Concerning the Fundaments of Theoretical Physics.”

## As equações e sua evolução

:::{admonition} As equações de Maxwell quaterniônicas
:class:dropdown

$$
\begin{aligned}
\mathfrak{B} &= V\cdot \nabla \mathfrak{A} &\\
S \cdot \nabla \mathfrak{A} &= 0 \quad &\textbf{indução magnética} \\
\mathfrak{E} &= V\cdot \mathfrak{GB} - \mathfrak{\dot A} - \nabla\Psi \quad &\textbf{Força eletromotriz} \\
\mathfrak{F} &= V\cdot \mathfrak{CB} + e \mathfrak{E} - m\nabla \Omega
&\textbf{Força Mecânica} \\
\mathfrak{B} &= \mathfrak{H} + 4\pi \mathfrak{J} &\textbf{magnetização} \\
4 \pi \mathfrak{C} &= V\cdot \nabla \mathfrak{H} &\textbf{Corrente Elétrica} \\
\mathfrak{K}&= C \mathfrak{E}&\textbf{Lei de Ohm} \\
\mathfrak{D}&= \frac{1}{4\pi} K \mathfrak{E}&\textbf{Deslocamento Elétrico} \\
\mathfrak{C}&= \mathfrak{K} + \mathfrak{\dot D}&\textbf{Corrente total} \\
\mathfrak{B}&= \mu \mathfrak{H}&\textbf{magnetização} \\
e &= S\cdot \nabla \mathfrak{D}&\textbf{densidade elétrica} \\
m &= S\cdot \nabla \mathfrak{J}&\textbf{densidade magnética} \\
\mathfrak{H}&= -\nabla \Omega &\textbf{magnetização} \\
\end{aligned}
$$
:::

:::{admonition} **Maxwell-Heaviside**
:class:dropdown

$$
\begin{aligned}
\nabla \cdot \mathfrak{E} &=& \frac{\rho}{\epsilon_0} \\
\nabla \cdot \mathfrak{B} &=& 0 \\
\nabla \times \mathfrak{E} &=& -\frac{\partial \mathfrak{B}}{\partial t} \\
\nabla \times \mathfrak{B} &=& \mu_0 \mathfrak{J} + \mu_0 \varepsilon_0 \frac{\partial \mathfrak{E}}{\partial t}
\end{aligned}
$$
:::

:::{admonition} **Formulação Covariante**
:class:dropdown

$$
\begin{aligned}
F_{\mu\nu} &=& \partial_{[\mu.}A_{\nu]} \\
\partial_\mu F^{\mu\nu} &=& J^\nu \\
\partial_\mu (\varepsilon^{\mu\nu\rho\sigma} F_{\rho\sigma}) &=& 0
\end{aligned}
$$
:::

:::{admonition} **Formas Diferenciais**
:class:dropdown

$$
\begin{aligned}
&dF = 0 \\
&d{*F} = J
\end{aligned}
$$
:::

:::{admonition} **Yang-Mills**
:class:dropdown

$$
\mathcal{L}_{\text{YM}} = -\frac{1}{4}  F_{\mu\nu}^a F^{\mu\nu}_a
$$
:::

:::{admonition} **Modelo Padrão das Partículas Elementares**
:class:dropdown

$$
\mathcal{L}_{\text{SM}} = \mathcal{L}_{\text{gauge}} + \mathcal{L}_{\text{fermions}} + \mathcal{L}_{\text{Higgs}} + \mathcal{L}_{\text{Yukawa}}
$$

$$
\begin{aligned}
\mathcal{L}_{\text{gauge}} &= -\frac{1}{4} G_{\mu\nu}^a G^{\mu\nu}*a - \frac{1}{4} W_{\mu\nu}^i W^{\mu\nu}*i - \frac{1}{4} B_{\mu\nu} B^{\mu\nu} \\
\mathcal{L}_{\text{fermions}} &= \sum_{\text{gerações}} \bar{\psi}_i i \gamma^\mu D_\mu \psi_i \\
\mathcal{L}_{\text{Higgs}} &= (D_\mu \phi)^\dagger (D^\mu \phi) - V(\phi) \\
\mathcal{L}_{\text{Yukawa}} &= - y_{ij} \bar{\psi}_i \phi \psi_j + \text{h.c.}
\end{aligned}
$$

:::
