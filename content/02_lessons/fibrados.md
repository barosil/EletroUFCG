# Fibrados

:::{figure} ../00_images/02_lessons/toro.png
:name: equivariance
:align: center
:width: 100%

:::

Seja $M$ uma variedade e $T_xM$ o espaço tangente a $M$ no ponto $x$.  

Considere o objeto  

$$
TM := \bigcup_{x \in M} T_x M
$$

$TM$ tem estrutura de variedade.  

A projeção canônica é uma aplicação  

$$
\pi: TM \to M, \quad (x, v_x) \mapsto x
$$

Considere uma carta de $M$  

$$
\varphi: U \subset M \to \varphi(U) \subset \mathbb{R}^n
$$

Note que seu domínio  

$$
\hat{U} := \pi^{-1}(U) \subset TM
$$

As coordenadas canônicas são definidas tal que  

$$
(x \in U, v \in T_xM) \quad \Rightarrow \quad \psi(x, v) = (x^i, v^i)
$$

onde  

$$
v = v^i \frac{\partial}{\partial x^i}
$$

Sob uma mudança de coordenadas  

$$
x'^i = x'^i(x) \\
v'^i = \frac{\partial x'^i}{\partial x^j} v^j
$$

Podemos proceder de forma análoga com $T^*M$. Usualmente a projeção canônica é denotada por $\pi$:

$$
\pi: T^*M \to M, \quad (x, \omega_x) \mapsto x
$$

TM e T\*M são sempre orientáveis.  

As projeções satisfazem as relações:

$$
\pi: TM \to M, \quad \pi(x, v) = x
$$

$$
\pi_*: T(TM) \to TM
$$

$$
\pi_* \frac{\partial}{\partial x^i} = \frac{\partial}{\partial x^i}, \quad
\pi_* \frac{\partial}{\partial v^i} = 0
$$

$$
f(x) = x^i \frac{\partial}{\partial x^i}, \quad j = (x^i)
$$

---

## Definição: Fibrado $(E, \pi, M, F, G)$

- **Espaço total**: $E$  
- **Espaço base**: $M$  
- **Fibra**: $F$  
- **Projeção**: $\pi: E \to M$ sobrejetora e contínua  

$$
\pi^{-1}(p) \cong F \quad \text{a fibra em } p
$$

- Graças ao grupo $G$, transformam as coordenadas  
- Trivialização local  

$$
\phi: U \times F \to \pi^{-1}(U)
$$

---

# Fibração de Hopf: Um Exemplo Ilustrativo em Teoria de Fibrados

:::{figure} ../00_images/02_lessons/hopf.jpg
:name: hopf
:align: center
:width: 100%

:::

## 1. Introdução à Fibração de Hopf

A fibração de Hopf é uma das construções mais belas e importantes da topologia diferencial e geometria algébrica. Descoberta por Heinz Hopf em 1931, ela fornece um exemplo não trivial de uma **aplicação contínua** da esfera tridimensional na esfera bidimensional:

$$
\eta: S^3 \to S^2
$$

O que torna esta aplicação notável é que ela é um **fibrado principal** com fibra $S^1$, revelando uma estrutura profunda que conecta diferentes dimensões.

## 2. Construção Geométrica da Fibração de Hopf

### 2.1. Formulação via Números Complexos

Considere a esfera tridimensional como subconjunto de $\mathbb{C}^2$:

$$
S^3 = \{(z_1, z_2) \in \mathbb{C}^2 : |z_1|^2 + |z_2|^2 = 1\}
$$

A aplicação de Hopf é definida como:

$$
\eta(z_1, z_2) = (z_1, z_2) \mapsto z_1/z_2 \in \mathbb{C} \cup \{\infty\} \cong S^2
$$

onde identificamos a esfera $S^2$ com a reta projetiva complexa $\mathbb{C}P^1$.

### 2.2. Formulação Explícita em Coordenadas

Se escrevermos $z_1 = x_1 + i x_2$, $z_2 = x_3 + i x_4$ com $(x_1, x_2, x_3, x_4) \in \mathbb{R}^4$ e $x_1^2 + x_2^2 + x_3^2 + x_4^2 = 1$, então:

$$
\eta(x_1, x_2, x_3, x_4) = (2(x_1 x_3 + x_2 x_4), 2(x_2 x_3 - x_1 x_4), x_1^2 + x_2^2 - x_3^2 - x_4^2)
$$

Esta aplicação leva pontos de $S^3$ para pontos de $S^2$.

## 3. Estrutura de Fibrado Principal

### 3.1. Ação do Grupo $S^1$

O grupo $U(1) \cong S^1$ age em $S^3$ por:

$$
e^{i\theta} \cdot (z_1, z_2) = (e^{i\theta}z_1, e^{i\theta}z_2)
$$

Esta ação é livre (sem pontos fixos) e preserva as fibras da aplicação de Hopf.

### 3.2. Espaço Quociente e Projeção

O espaço de órbitas desta ação é exatamente $S^2$:

$$
S^3/S^1 \cong S^2
$$

A aplicação de Hopf $\eta: S^3 \to S^2$ é a projeção natural que associa a cada ponto sua órbita sob a ação de $S^1$.

### 3.3. Estrutura Local de Produto

Localmente, o fibrado de Hopf é trivial. Para qualquer ponto $p \in S^2$, existe uma vizinhança $U \subset S^2$ tal que:

$$
\eta^{-1}(U) \cong U \times S^1
$$

Esta é a propriedade fundamental de um **fibrado fibrado**.

## 4. Visualização Geométrica

### 4.1. Fibras como Círculos em $S^3$

Cada fibra $\eta^{-1}(p)$ para $p \in S^2$ é um grande círculo em $S^3$. Dois pontos distintos em $S^3$ estão na mesma fibra se e somente se:

$$
(z_1, z_2) = e^{i\theta}(w_1, w_2)
$$

para algum $\theta \in \mathbb{R}$.

### 4.2. Link de Hopf

A imagem inversa de dois pontos distintos em $S^2$ são dois círculos em $S^3$ que estão **enlaçados** - este é o famoso "link de Hopf". O número de enlace destes dois círculos é 1.

## 5. A Fibração de Hopf como Fibrado Principal

### 5.1. Definição Formal

O fibrado de Hopf é um **fibrado principal** com:

- Espaço total: $S^3$
- Espaço base: $S^2$
- Grupo de estrutura: $S^1$
- Projeção: $\eta: S^3 \to S^2$

### 5.2. Invariantes Topológicos

O fibrado de Hopf possui propriedades notáveis:

- **Não é trivial**: $S^3$ não é homeomorfo a $S^2 \times S^1$
- **Classe de Chern**: A primeira classe de Chern do fibrado associado é não nula
- **Invariante de Hopf**: O número de Hopf é um invariante que classifica as aplicações $S^3 \to S^2$

## 6. Generalizações e Importância

### 6.1. Fibrações de Hopf Generalizadas

Existem generalizações para dimensões superiores:

- $\eta: S^7 \to S^4$ (fibração de Hopf quaterniónica)
- $\eta: S^{15} \to S^8$ (fibração de Hopf octoniónica)

Estas estão relacionadas com os números complexos, quatérnios e octônios, respectivamente.

### 6.2. Significado em Física

A fibração de Hopf aparece em:

- **Mecânica Quântica**: Estados quânticos com fases
- **Teoria de Gauge**: Fibrados com grupo de gauge $U(1)$
- **Cosmologia**: Modelos do universo com topologia não trivial

## 7. Conclusão

A fibração de Hopf é um exemplo paradigmático que ilustra:

1. A riqueza da teoria de fibrados
2. A conexão entre álgebra, geometria e topologia
3. A importância de simetrias contínuas em matemática e física

Sua elegância e profundidade continuam a inspirar pesquisas em diversas áreas da matemática e física teórica.

## Mapas de Fibrados

Considere 2 variedades $M$ e $N$:  

$$
f: M \to N
$$

$$
\pi_M: TM \to M, \quad \pi_N: TN \to N
$$

Induzindo um mapa entre vetores.  

Considerando a ação nos fibrados:  

$$
Tf: TM \to TN, \quad (Tf)(v) \in T_{f(x)}N
$$

Se $f$ é uma aplicação de corpos:  

$$
TM \xrightarrow{Tf} TN \\
\pi_M \downarrow \quad \quad \downarrow \pi_N \\
M \xrightarrow{f} N
$$

Se $g_i: F \to F$ é homomorfismo:  

$$
g_{ij}(p) = g_j(p) \cdot g_i(p)^{-1}, \quad T\pi \circ g_j(p)
$$

---

### Seção local

Uma seção local $s: M \to E$ é uma aplicação suave tal que  

$$
\pi \circ s = id_M
$$

---

### Fibrado principal

Um fibrado principal tem um grupo como fibra e a ação do grupo preserva a estrutura.  

Dada uma trivialização local:  

$$
g: \pi^{-1}(U) \to U \times G
$$

---

Seja $(P, M, G)$ fibrado principal e $G_p$ a fibra em $p$:  

$$
\rho: T_p P \to V_p, \quad V_p \subset T_p P
$$

### Mapa Exponencial

Seja $\mathfrak{g}$ a álgebra de $G$, $\mathfrak{g} \cong T_e G$.  
Sejam $X(G)$ os vetores invariantes à direita de $\mathfrak{g}$:

$$
L_{gh} = g h, \quad (L_g)_* X_h = X_{gh}
$$

Seja $\xi \in X(\mathfrak{g})$, $X_\xi$ o vetor único que corresponde:  

$$
X_\xi(e) = \xi
$$

<!-- ## Espaço Vertical

O espaço vertical $V_p$ é o subespaço de $T_p P$ que é tangente à fibra em $U$.

---

### Considerar o campo de gauge

$$
X \in \mathfrak{X}(P), \quad X \sim A_\mu dx^\mu
$$

$$
\pi(A_\mu(x)dx^\mu) = p, \quad \text{potenciais e conexões em $G$}
$$

---

### Ação no fibrado

$$
A^f(x) = d(f(x)) f(x)^{-1}
$$

Seja  

$$
f: P \to P \quad \text{arbitrário}
$$

$$
X^* \in \mathfrak{X}^V \quad \text{campo vertical fundamental}
$$ -->

<!-- 
Seja
$$
\#: \mathfrak{g} \to V_pP
$$
um isomorfismo. -->

### Espaço Horizontal

O espaço horizontal é o complemento de $V$.  

### Conexão

:::{figure} ../00_images/02_lessons/Equivariance_of_Principal_bundle_connection.png
:name: equivariance
:align: center
:width: 100%

:::

:::{figure} ../00_images/02_lessons/Ehresmann_connection.png
:name: ehresman
:align: center
:width: 100%

:::

Uma **conexão** é uma separação única:  

$$
T_pP = H_pP \oplus V_pP
$$

$$
H_{gp} = R_g \, H_pP
$$

---

A conexão 1-forma $\omega \in \mathfrak{g} \otimes T^*P$ é o **projetor** de $T_pP$ na componente vertical $V_pP \cong \mathfrak{g}$:

$$
\omega(A^\#) = A, \quad A \in \mathfrak{g}
$$

$$
R_g^* \omega = \mathrm{Ad}_{g^{-1}} \, \omega
$$

$$
R_g^*\omega_x(X) = \omega_{g x}(R_{g*} X) = g^{-1} \, \omega_x(X) \, g
$$

$$
H_pP = \{ X \in T_pP \mid \omega(X) = 0 \}
$$

---

Seja $g_\xi(t)$ uma curva integral de $X_\xi$ que passa em $e \in G$, para $t=0$:  

$$
e^\xi = g_\xi(1), \quad e^{t\xi} = g_\xi(t)
$$

---

Seja $\{U_i\}$ abertos de $M$, $\sigma_i$ seções locais:  

$$
A_i = \sigma_i^* \omega \in \mathfrak{g} \otimes \Omega^1(U_i)
$$

$A_i$ é definido unicamente se:  

$$
A_j = g_{ij}^{-1} A_i g_{ij} + g_{ij}^{-1} d g_{ij}
$$

---

A conexão é responsável pelo **transporte paralelo** de vetores de $M$ levantados para o fibrado.  
O objeto que codifica se o espaço horizontal é integrável é a **curvatura**:  

$$
D = \text{integrável} \iff \{ U, V \in D^H \Rightarrow d\omega(U,V) = 0 \}
$$

$$
\Omega = d\omega + \tfrac{1}{2} [\omega \wedge \omega]
$$

onde  

$$
D\omega = 0, \quad \Omega = \text{hor}(d\omega)
$$

---

## Formas Diferenciais com valores em $\mathfrak{g}$

$$
\alpha = \alpha^i E_i, \quad \beta = \beta^j E_j
$$

$$
\alpha \wedge \beta = \alpha^i \wedge \beta^j [E_i, E_j]
$$

Agora:  

$$
\alpha \wedge \beta = -(-1)^{pq} \beta \wedge \alpha
$$

$$
(\alpha \wedge \beta)(U,V) = [\alpha(U), \beta(V)] + [\alpha(V), \beta(U)]
$$

---

Finalmente:  

$$
\Omega = d\omega + \tfrac{1}{2} (\omega \wedge \omega)
$$

Um vetor pode ser escrito como:  

$$
U_p = U_p^h + \xi_X(p)
$$

---

## Derivada Covariante

$$
D = d + A, \quad F = dA + A \wedge A
$$

onde $A$ é a 1-forma de conexão e $F$ é a curvatura (campo de força).

## Eletromagnetismo, Conexões de Fibrados e Ações de Campos

### **Potencial Eletromagnético como 1-forma de Conexão**

- No eletromagnetismo abeliano ($U(1)$):
  - O espaço-tempo é a variedade base $M$.
  - O fibrado principal: $P(M, U(1))$.
  - O potencial eletromagnético é uma 1-forma de conexão $\alpha$ no fibrado principal.
- A **conexão** $\alpha$ é a 1-forma que "conecta" as fibras e nos permite comparar vetores em fibras vizinhas.
- A **curvatura** (também conhecida como forma de curvatura) é a 2-forma $F = d\alpha$.

### **O Campo Eletromagnético como 2-forma de Curvatura**

- O tensor de campo eletromagnético $F_{\mu\nu}$ é a curvatura $F$ da conexão $\alpha$.
  - Em termos de componentes: $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$.
  - As **Equações de Maxwell homogêneas** são a condição de Bianchi para a curvatura: $dF = 0$, que em componentes é $\partial_{[\alpha} F_{\mu\nu]} = 0$.
  - Isso implica a existência de um potencial $\alpha$ tal que $F = d\alpha$ em qualquer região simplesmente conexa.

### **A Ação de Maxwell (sem fontes)**

- A **ação de Yang-Mills** para o grupo de gauge abeliano $U(1)$ é a ação de Maxwell.
- A ação é a integral da **densidade de Lagrangeana** $\mathcal{L}$ sobre o espaço-tempo $M$.
  - $\mathcal{L} = -\frac{1}{4} F_{\mu\nu} F^{\mu\nu}$.
  - A ação total é $S = \int \mathcal{L} \sqrt{|g|} d^4x$.
- Variando a ação em relação ao potencial $A_\mu$, obtemos as equações de movimento.

## 4. **Inclusão de Fontes e Equações de Maxwell Completas**

- A corrente de 4 vetores $J^\mu$ é uma 1-forma $J = J_\mu dx^\mu$.
- A ação com fontes é $S = \int (\mathcal{L}_{Maxwell} + \mathcal{L}_{int}) \sqrt{|g|} d^4x$.
  - $\mathcal{L}_{int} = -J^\mu A_\mu$.
- A equação de movimento (E-L) resultante é a equação de Maxwell com fontes: $\nabla_\mu F^{\mu\nu} = J^\nu$.
  - Em termos de diferenciais, isso é $d*F = *J$.
- A **conservação de carga** segue da identidade de Bianchi para o Hodge dual de $F$: $d(d*F)=0$. Isso implica $\nabla_\nu J^\nu = 0$, que é a equação de continuidade.

## 5. **Tensor de Energia-Momento Eletromagnético**

- O tensor de energia-momento $T_{\mu\nu}$ é a resposta da ação de Maxwell a um "difeomorfismo" (uma deformação da métrica do espaço-tempo).
- Para o eletromagnetismo, ele é dado por $T_{\mu\nu} = F_{\mu\rho} F^\rho{}_\nu + \frac{1}{4} \eta_{\mu\nu} F_{\rho\sigma}F^{\rho\sigma}$.
- Em 3D, isso dá a energia armazenada nos campos, o vetor de Poynting e as tensões eletromagnéticas.

### Análise do Termo de Chern-Pontryagin

Lembre que:

$$F = \frac{1}{2} F_{\mu\nu} dx^\mu \wedge dx^\nu.$$

Com convenções usuais:

$$F_{0i} = E_i, \quad F_{ij} = - \epsilon_{ijk} B_k.$$

Assim:

$$F = E_i \, dt \wedge dx^i - \frac{1}{2}\epsilon_{ijk} B_k \, dx^i \wedge dx^j.$$

$$F \wedge F = \left( E_i \, dt \wedge dx^i - \frac{1}{2}\epsilon_{ijk} B_k \, dx^i \wedge dx^j \right) \wedge \left( E_m \, dt \wedge dx^m - \frac{1}{2}\epsilon_{mnp} B_p \, dx^m \wedge dx^n \right).$$

O termo $(dt \wedge dx^i) \wedge (dt \wedge dx^m)$ desaparece, pois $dt \wedge dt = 0$.

O termo puramente magnético $(dx^i \wedge dx^j) \wedge (dx^m \wedge dx^n)$ em 4D também se anula (seria uma 4-forma só espacial, mas em dimensão 4 isso requer 5 índices diferentes).

O termo cruzado sobrevive:

$$F \wedge F = - E_i \epsilon_{mnp} B_p \, dt \wedge dx^i \wedge dx^m \wedge dx^n.$$

A base de 4-formas é $dt \wedge dx^1 \wedge dx^2 \wedge dx^3 \equiv d^4x$.

Precisamos reorganizar $dt \wedge dx^i \wedge dx^m \wedge dx^n$ nessa base.
De fato:

$$dt \wedge dx^i \wedge dx^m \wedge dx^n = \epsilon_{imn} \, d^4x.$$

Portanto:

$$F \wedge F = - E_i B_p \, \epsilon_{mnp} \epsilon_{imn} \, d^4x.$$

A identidade:

$$\epsilon_{mnp} \epsilon_{imn} = 2 \delta_{ip}.$$

Assim:

$$F \wedge F = - 2 E_i B_i \, d^4x = - 2 \, \vec{E} \cdot \vec{B} \, d^4x.$$

$$F \wedge F = - 2 \, \vec{E} \cdot \vec{B} \, d^4x.$$

Portanto:

O termo de **Chern–Pontryagin** em $U(1)$ é proporcional a $\vec{E} \cdot \vec{B}$.

É também uma derivada total:

$$F \wedge F = d(A \wedge F).$$

## Ação da Partícula

### Ação da Partícula: Formalismo Geométrico Avançado

A ação que descreve uma partícula de massa $m$ e carga $q$ em um espaço-tempo curvo com métrica $g_{\mu\nu}$ acoplada a um campo eletromagnético $A_\mu$ é dada por:

$$
S[x(\tau)] = -m \int ds + q \int A_\mu \dot{x}^\mu d\tau
$$

onde $\tau$ é um parâmetro afim ao longo da trajetória.

#### Interpretação Geométrica do Elemento de Linha

O elemento de linha $ds$ é definido pela métrica $g_{\mu\nu}$:

$$
ds = \sqrt{g_{\mu\nu} dx^\mu dx^\nu} = \sqrt{g_{\mu\nu} \dot{x}^\mu \dot{x}^\nu} d\tau
$$

Geometricamente, $ds$ representa o comprimento de arco ao longo da trajetória da partícula na variedade riemanniana do espaço-tempo.

#### Formulação em Termos de Formas Diferenciais

Na linguagem de formas diferenciais, podemos expressar a ação como:

$$
S = -m \int \sqrt{-g(\dot{\gamma},\dot{\gamma})} d\tau + q \int_\gamma A
$$

onde $A = A_\mu dx^\mu$ é a 1-forma do potencial eletromagnético e $\gamma$ é a curva que representa a trajetória da partícula.

### Derivação das Equações de Movimento

#### Variação da Ação

Aplicando o princípio de mínima ação ($\delta S = 0$), obtemos:

$$
\delta S = -m \int \delta(ds) + q \int \delta(A_\mu \dot{x}^\mu d\tau) = 0
$$

#### Equação de Movimento Resultante

A variação completa resulta na equação:

$$
m \frac{D}{d\tau}\left(\frac{\dot{x}^\mu}{ds/d\tau}\right) + m \Gamma^\mu_{\rho\sigma} \frac{\dot{x}^\rho \dot{x}^\sigma}{ds/d\tau} = q F^\mu_{\ \nu} \dot{x}^\nu
$$

onde $F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu$ é o tensor campo eletromagnético.

#### Formulação Covariante

Usando o tempo próprio $\tau$ como parâmetro (onde $ds = cd\tau$), a equação simplifica para:

$$
m \frac{D u^\mu}{d\tau} = m \left(\frac{du^\mu}{d\tau} + \Gamma^\mu_{\rho\sigma} u^\rho u^\sigma\right) = q F^\mu_{\ \nu} u^\nu
$$

onde $u^\mu = \frac{dx^\mu}{d\tau}$ é a quadrivelocidade.

### Simetrias e Conservação via Teorema de Noether

#### Simetria de Gauge e Conservação de Carga

A invariância de gauge da ação sob $A_\mu \to A_\mu + \partial_\mu \Lambda$ implica na conservação da corrente:

$$
\nabla_\mu J^\mu = 0
$$

onde $J^\mu$ é a corrente elétrica.

### 3.2. Formulação em Linguagem de Fibrados

No formalismo de fibrados, o campo eletromagnético é descrito por uma conexão $A$ em um fibrado principal $P(M, U(1))$ sobre a variedade espaço-tempo $M$. A partícula carregada é uma seção de um fibrado associado.

## O Monopolo Magnético na Linguagem de Formas Diferenciais

## 1. O Campo do Monopolo Magnético

### 1.1. Formulação em Coordenadas Cartesianas

O campo de um monopolo magnético de carga $g$ localizado na origem é dado por:

$$
\vec{B} = \frac{g}{4\pi} \frac{\vec{r}}{r^3}
$$

Na linguagem de formas diferenciais, o campo eletromagnético é representado pela 2-forma $F$:

$$
F = \frac{1}{2} F_{\mu\nu} dx^\mu \wedge dx^\nu
$$

Para o monopolo magnético, temos:

$$
F = B_x dy \wedge dz + B_y dz \wedge dx + B_z dx \wedge dy
$$

Substituindo as componentes do campo:

$$
F = \frac{g}{4\pi r^3} (x dy \wedge dz + y dz \wedge dx + z dx \wedge dy)
$$

### 1.2. Transformação para Coordenadas Esféricas

Para expressar $F$ em coordenadas esféricas $(r, \theta, \phi)$, usamos as relações:

$$
x = r \sin\theta \cos\phi, \quad y = r \sin\theta \sin\phi, \quad z = r \cos\theta
$$

O diferencial exterior $d$ em coordenadas esféricas:

$$
dx = \sin\theta \cos\phi dr + r \cos\theta \cos\phi d\theta - r \sin\theta \sin\phi d\phi
$$
$$
dy = \sin\theta \sin\phi dr + r \cos\theta \sin\phi d\theta + r \sin\theta \cos\phi d\phi
$$
$$
dz = \cos\theta dr - r \sin\theta d\theta
$$

Calculando os produtos wedge:

$$
dy \wedge dz = r \sin\theta \cos\phi (dr \wedge d\theta) + r^2 \sin^2\theta \cos\phi (d\theta \wedge d\phi) + \cdots
$$
$$
dz \wedge dx = r \sin\theta \sin\phi (dr \wedge d\theta) + r^2 \sin^2\theta \sin\phi (d\theta \wedge d\phi) + \cdots
$$
$$
dx \wedge dy = r \cos\theta (dr \wedge d\theta) + r^2 \sin\theta \cos\theta (d\theta \wedge d\phi) + \cdots
$$

Substituindo na expressão de $F$ e simplificando:

$$
F = \frac{g}{4\pi r^3} \left[ r^3 \sin\theta d\theta \wedge d\phi + \text{termos em } dr \wedge d\theta \text{ e } dr \wedge d\phi \right]
$$

Os termos envolvendo $dr$ se cancelam, resultando em:

$$
F = \frac{g}{4\pi} \sin\theta d\theta \wedge d\phi
$$

Esta é a expressão elegante do campo do monopolo magnético em coordenadas esféricas.

## 2. Potenciais Vetores e a Conexão com a Topologia

### 2.1. Os Potenciais "Norte" e "Sul"

### Obtenção do Potencial Vetor A a partir do Campo F

Dada a 2-forma do campo eletromagnético $F$ que satisfaz $dF = 0$ (equações homogêneas de Maxwell), queremos encontrar uma 1-forma $A$ tal que:

$$
F = dA
$$

Este é um problema de encontrar uma **primitiva** ou **potencial** para a forma fechada $F$.

Para o monopolo magnético, temos:

$$
F = \frac{g}{4\pi} \sin\theta  d\theta \wedge d\phi
$$

Queremos encontrar $A$ tal que $dA = F$.

Observando que:
$$
d(\cos\theta  d\phi) = -\sin\theta  d\theta \wedge d\phi
$$

Portanto:
$$
d(-\cos\theta  d\phi) = \sin\theta  d\theta \wedge d\phi
$$

Assim, uma solução seria:
$$
A = -\frac{g}{4\pi} \cos\theta  d\phi
$$

Esta potencial tem uma singularidade ao longo do eixo $z$ (onde $\theta = 0$ ou $\theta = \pi$), pois $d\phi$ não é bem definida nos pólos.

Para verificar, calculemos a integral de linha ao longo de um pequeno círculo around do eixo $z$:

$$
\oint A = -\frac{g}{4\pi} \cos\theta \oint d\phi = -\frac{g}{4\pi} \cos\theta \cdot 2\pi = -\frac{g}{2} \cos\theta
$$

Quando $\theta \to 0$ ou $\theta \to \pi$, esta integral não se anula, indicando uma singularidade real (não apenas coordenada).

Para a região $U_N = \{\theta < \pi/2 + \epsilon\}$ (hemisfério norte estendido):

$$
A^N = \frac{g}{4\pi} (1 - \cos\theta) d\phi
$$

Verificação:
$$
dA^N = \frac{g}{4\pi} d(1 - \cos\theta) \wedge d\phi = \frac{g}{4\pi} \sin\theta  d\theta \wedge d\phi = F
$$

Este potencial é regular em $\theta = \pi$ mas singular em $\theta = 0$.

Para a região $U_S = \{\theta > \pi/2 - \epsilon\}$ (hemisfério sul estendido):

$$
A^S = -\frac{g}{4\pi} (1 + \cos\theta) d\phi
$$

Verificação:
$$
dA^S = -\frac{g}{4\pi} d(1 + \cos\theta) \wedge d\phi = -\frac{g}{4\pi} (-\sin\theta d\theta) \wedge d\phi = \frac{g}{4\pi} \sin\theta  d\theta \wedge d\phi = F
$$

Este potencial é regular em $\theta = 0$ mas singular em $\theta = \pi$.

Na região de sobreposição $U_N \cap U_S$ (em torno do equador):

$$
A^N - A^S = \frac{g}{4\pi} [(1 - \cos\theta) - (-1 - \cos\theta)] d\phi = \frac{g}{4\pi} (2) d\phi = \frac{g}{2\pi} d\phi
$$

Como $d\phi$ é fechada mas não exata em $S^2 - \{\text{pontos}\}$, a diferença é uma forma exata apenas localmente.

Para formas fechadas, podemos usar uma construção integral explícita.

Se $F$ é fechada ($dF = 0$), então localmente:

$$
A(x) = \int_0^1 t \cdot \iota_R F(tx) dt
$$

onde $R = x^\mu \partial_\mu$ é o vetor radial e $\iota_R$ é a contração.

Para $F = \frac{g}{4\pi} \sin\theta  d\theta \wedge d\phi$, em coordenadas cartesianas:

$$
F = \frac{g}{4\pi r^3} (x dy \wedge dz + y dz \wedge dx + z dx \wedge dy)
$$

Contração com $R = x\partial_x + y\partial_y + z\partial_z$:

$$
\iota_R F = \frac{g}{4\pi r^3} [x \cdot (x \cdot 0 + y \cdot dz - z \cdot dy) + \cdots]
$$

Calculando termo a termo:

$$
\iota_R(x dy \wedge dz) = x \cdot (y dz - z dy) = xy dz - xz dy
$$
$$
\iota_R(y dz \wedge dx) = y \cdot (z dx - x dz) = yz dx - xy dz
$$
$$
\iota_R(z dx \wedge dy) = z \cdot (x dy - y dx) = zx dy - zy dx
$$

Somando:

$$
\iota_R F = \frac{g}{4\pi r^3} [(yz - zy) dx + (zx - xz) dy + (xy - yx) dz] = 0
$$

Este resultado nulo indica que a fórmula integral precisa ser adaptada para formas que não se anulam na origem.

Para formas com singularidades, usamos uma versão projetiva:

$$
A(x) = \int_0^1 t \cdot \varphi_t^* (\iota_R F) dt
$$

onde $\varphi_t(x) = tx$ é o fluxo do vetor radial.

Para o monopolo, este método reproduz os potenciais $A^N$ e $A^S$ dependendo da escolha de gauge.

Verificamos que $dA^N = dA^S = F$:

$$
dA^N = \frac{g}{4\pi} \sin\theta d\theta \wedge d\phi = F
$$
$$
dA^S = -\frac{g}{4\pi} (-\sin\theta d\theta \wedge d\phi) = \frac{g}{4\pi} \sin\theta d\theta \wedge d\phi = F
$$

### 2.2. Transformação de Gauge na Região de Sobreposição

Na região de interseção (em torno do equador $\theta = \pi/2$), os dois potenciais estão relacionados por uma transformação de gauge:

$$
A^N - A^S = \frac{g}{4\pi} [(1 - \cos\theta) - (-1 - \cos\theta)] d\phi = \frac{g}{2\pi} d\phi
$$

Esta diferença é uma forma exata ($d\phi$), portanto:

$$
A^N = A^S + \frac{g}{2\pi} d\phi
$$

A transformação de gauge correspondente é:

$$
\psi_{NS} = \frac{g}{2\pi} \phi
$$

tal que $A^N = A^S + d\psi_{NS}$.

## 3. Holonomia e Quantização da Carga

### 3.1. Holonomia ao Longo de um Laço

Considere um laço fechado $C$ no equador ($\theta = \pi/2$). A holonomia da conexão $A$ ao longo de $C$ é:

$$
\text{Hol}_C(A) = \exp\left( iq \oint_C A \right)
$$

Usando o potencial $A^N$:

$$
\oint_C A^N = \frac{g}{4\pi} (1 - \cos\theta) \oint_C d\phi = \frac{g}{4\pi} (1 - 0) \cdot 2\pi = \frac{g}{2}
$$

A holonomia é então:

$$
\text{Hol}_C(A^N) = \exp\left( iq \frac{g}{2} \right)
$$

### 3.2. Condição de Quantização

Para que a função de onda da partícula seja bem definida, a holonomia deve ser a mesma calculada com $A^N$ ou $A^S$. Isto impõe:

$$
\exp\left( iq \oint_C A^N \right) = \exp\left( iq \oint_C A^S \right)
$$

Mas:

$$
\exp\left( iq \oint_C A^N \right) = \exp\left( iq \oint_C (A^S + d\psi_{NS}) \right) = \exp\left( iq \oint_C A^S \right) \cdot \exp\left( iq \oint_C d\psi_{NS} \right)
$$

Portanto:

$$
\exp\left( iq \oint_C d\psi_{NS} \right) = 1
$$

Calculando:

$$
\oint_C d\psi_{NS} = \psi_{NS}(2\pi) - \psi_{NS}(0) = \frac{g}{2\pi} (2\pi - 0) = g
$$

A condição torna-se:

$$
\exp(iq g) = 1 \quad \Rightarrow \quad q g = 2\pi n \hbar \quad (n \in \mathbb{Z})
$$

Esta é a **condição de quantização de Dirac**:

$$
q g = 2\pi n \hbar \quad \text{ou} \quad \frac{q g}{\hbar} = 2\pi n
$$

## 4. Interpretação em Termos de Fibrados

### 4.1. A Estrutura do Fibrado

O monopolo magnético é descrito por um **fibrado principal $U(1)$** sobre $\mathbb{R}^3 - \{0\}$ (espaço menos a origem). Este fibrado é não-trivial devido à singularidade na origem.

A base do fibrado é $M = \mathbb{R}^3 - \{0\} \simeq S^2 \times \mathbb{R}^+$. A não-trivialidade do fibrado é capturada pelo fato de que não podemos definir um potencial vetor $A$ globalmente não-singular.

### 4.2. Descrição em Termos de Cartas

Cobrimos a base com duas cartas:

- **Carta Norte**: $U_N = \{\theta < \pi/2 + \epsilon\}$ (hemisfério norte estendido)
- **Carta Sul**: $U_S = \{\theta > \pi/2 - \epsilon\}$ (hemisfério sul estendido)

Na interseção $U_N \cap U_S$ (uma faixa em torno do equador), os potenciais $A^N$ e $A^S$ estão relacionados pela função de transição:

$$
g_{NS} = \exp(i e \psi_{NS}/\hbar) = \exp(i e g \phi/2\pi\hbar)
$$

A não-trivialidade do fibrado é medida pela classe de Chern:

$$
c_1 = \frac{1}{2\pi} \int_{S^2} F = \frac{1}{2\pi} \int_{S^2} \frac{g}{4\pi} \sin\theta d\theta \wedge d\phi = \frac{g}{2\pi}
$$

### 4.3. Interpretação Física

A condição de quantização de Dirac $q g = 2\pi n \hbar$ garante que:

1. A função de transição $g_{NS}$ é bem definida (periódica em $\phi$)
2. A função de onda da partícula carregada é uma seção bem definida do fibrado vetorial associado
3. O fibrado é classificado por um número inteiro $n$ (o primeiro número de Chern)

Esta é uma realização física profunda do relacionamento entre:

- Topologia diferencial (fibrados e classes características)
- Teoria de gauge (conexões e curvatura)
- Física quântica (quantização e fases geométricas)

O monopolo magnético de Dirac ilustra beautifulmente como requisitos de consistência matemática na descrição geométrica de sistemas físicos levam a condições de quantização profundas.

## 5. Interpretação em Termos de Cohomologia

### 5.1. Obstução Topológica

A não-existência de um potencial global $A$ é medida pela classe de cohomologia de de Rham:

$$
[F] \in H^2(S^2, \mathbb{R})
$$

A integral sobre $S^2$:

$$
\int_{S^2} F = \int_0^{2\pi} \int_0^\pi \frac{g}{4\pi} \sin\theta  d\theta d\phi = g
$$

Se $F = dA$ globalmente, então pelo teorema de Stokes:

$$
\int_{S^2} F = \int_{S^2} dA = \int_{\partial S^2} A = 0
$$

Como $g \neq 0$, temos uma contradição, mostrando que $F$ não é exata globalmente.

### 5.2. Solução com Múltiplas Cartas

A solução é usar um cobrimento com duas cartas:

- $U_N = \{\theta < 2\pi/3\}$ (cone norte)
- $U_S = \{\theta > \pi/3\}$ (cone sul)

Com potenciais:

- $A^N$ regular em $U_N$
- $A^S$ regular em $U_S$

Na interseção $U_N \cap U_S$ (zona equatorial), temos:

$$
A^N = A^S + d\psi, \quad \psi = \frac{g}{2\pi} \phi
$$

## 6. Conclusão

A obtenção de $A$ a partir de $F$ envolve:

1. **Análise local**: Resolver $dA = F$ em cada carta coordenada
2. **Análise global**: Estudar a compatibilidade nas intersecções
3. **Topologia**: A obstrução à existência de solução global é medida pela classe de cohomologia $[F]$

Para o monopolo magnético:

- $F$ é fechada mas não exata em $\mathbb{R}^3 - \{0\}$
- Podemos definir potenciais locais $A^N$ e $A^S$
- A diferença $A^N - A^S = d\psi$ define uma classe de cohomologia
- A quantização $qg = 2\pi n\hbar$ garante que a função de transição é bem definida

Esta construção é um exemplo belo da interação entre geometria diferencial, topologia e física.

# O Efeito Aharonov-Bohm: Simetria de Gauge e Conexões em Mecânica Quântica

## 1. A Equação de Schrödinger e sua Simetria de Fase Global

### 1.1. Equação de Schrödinger Livre

A equação de Schrödinger para uma partícula livre:

$$
i\hbar\frac{\partial\psi}{\partial t} = -\frac{\hbar^2}{2m}\nabla^2\psi
$$

### 1.2. Simetria de Fase Global

Esta equação é invariante sob uma **transformação de fase global**:

$$
\psi(\vec{r}, t) \rightarrow \psi'(\vec{r}, t) = e^{i\alpha}\psi(\vec{r}, t)
$$

onde $\alpha$ é uma constante real. Verificamos:

$$
i\hbar\frac{\partial\psi'}{\partial t} = i\hbar e^{i\alpha}\frac{\partial\psi}{\partial t} = e^{i\alpha}\left(-\frac{\hbar^2}{2m}\nabla^2\psi\right) = -\frac{\hbar^2}{2m}\nabla^2\psi'
$$

A invariância é manifesta.

## 2. Tornando a Simetria Local: O Princípio de Gauge

### 2.1. Transformação de Fase Local

Agora exigimos que a teoria seja invariante sob uma **transformação de fase local**:

$$
\psi(\vec{r}, t) \rightarrow \psi'(\vec{r}, t) = e^{i\alpha(\vec{r}, t)}\psi(\vec{r}, t)
$$

onde $\alpha(\vec{r}, t)$ é uma função suave do espaço-tempo.

### 2.2. O Problema com a Derivada Ordinária

Sob esta transformação, a derivada temporal transforma-se como:

$$
\frac{\partial\psi'}{\partial t} = e^{i\alpha}\frac{\partial\psi}{\partial t} + i\frac{\partial\alpha}{\partial t}e^{i\alpha}\psi
$$

Similarmente, para o gradiente:

$$
\nabla\psi' = e^{i\alpha}\nabla\psi + i(\nabla\alpha)e^{i\alpha}\psi
$$

O termo extra rompe a invariância da equação de Schrödinger:

$$
i\hbar\frac{\partial\psi'}{\partial t} + \frac{\hbar^2}{2m}\nabla^2\psi' \neq e^{i\alpha}\left(i\hbar\frac{\partial\psi}{\partial t} + \frac{\hbar^2}{2m}\nabla^2\psi\right)
$$

## 3. Introduzindo a Conexão: A Derivada Covariante

### 3.1. Definição da Derivada Covariante

Para restaurar a invariância, introduzimos uma **derivada covariante** $D_\mu$:

$$
D_\mu = \partial_\mu - i\frac{q}{\hbar}A_\mu
$$

onde $A_\mu$ é um campo de gauge que se transforma de maneira específica.

### 3.2. Transformação do Campo de Gauge

Exigimos que a derivada covariante transforme-se covarianteamente:

$$
D_\mu\psi \rightarrow (D_\mu\psi)' = e^{i\alpha}D_\mu\psi
$$

Isto impõe uma condição sobre a transformação de $A_\mu$:

$$
(\partial_\mu - i\frac{q}{\hbar}A_\mu')(e^{i\alpha}\psi) = e^{i\alpha}(\partial_\mu - i\frac{q}{\hbar}A_\mu)\psi
$$

Expandindo:

$$
\partial_\mu(e^{i\alpha}\psi) - i\frac{q}{\hbar}A_\mu'e^{i\alpha}\psi = e^{i\alpha}\partial_\mu\psi + i(\partial_\mu\alpha)e^{i\alpha}\psi - i\frac{q}{\hbar}A_\mu'e^{i\alpha}\psi
$$

E o lado direito:

$$
e^{i\alpha}\partial_\mu\psi - i\frac{q}{\hbar}e^{i\alpha}A_\mu\psi
$$

Igualando, obtemos:

$$
i(\partial_\mu\alpha)e^{i\alpha}\psi - i\frac{q}{\hbar}A_\mu'e^{i\alpha}\psi = - i\frac{q}{\hbar}e^{i\alpha}A_\mu\psi
$$

Simplificando:

$$
A_\mu' = A_\mu + \frac{\hbar}{q}\partial_\mu\alpha
$$

### 3.3. Equação de Schrödinger com Campo Eletromagnético

A equação de Schrödinger invariante de gauge é:

$$
i\hbar\frac{\partial\psi}{\partial t} = \frac{1}{2m}\left(-i\hbar\nabla - q\vec{A}\right)^2\psi + q\phi\psi
$$

Ou, em notação covariante:

$$
i\hbar D_t\psi = -\frac{\hbar^2}{2m}D_iD^i\psi
$$

## 4. O Efeito Aharonov-Bohm

### 4.1. O Experimento Mental

Consideremos um solenoide longo e fino com fluxo magnético $\Phi$ confinado em seu interior. Fora do solenoide, $\vec{B} = 0$, mas $\vec{A} \neq 0$.

### 4.2. Cálculo do Efeito de Fase

A função de onda de um elétron se propagando na região onde $\vec{B} = 0$ mas $\vec{A} \neq 0$ adquire uma fase:

$$
\psi = \psi_0 \exp\left(\frac{iq}{\hbar}\int_{\vec{r}_0}^{\vec{r}} \vec{A} \cdot d\vec{l}\right)
$$

onde $\psi_0$ é a solução sem campo.

### 4.3. Interferência entre dois caminhos

Para dois caminhos $\gamma_1$ e $\gamma_2$ contornando o solenoide:

$$
\psi_1 = \psi_0^{(1)} \exp\left(\frac{iq}{\hbar}\int_{\gamma_1} \vec{A} \cdot d\vec{l}\right)
$$
$$
\psi_2 = \psi_0^{(2)} \exp\left(\frac{iq}{\hbar}\int_{\gamma_2} \vec{A} \cdot d\vec{l}\right)
$$

A diferença de fase é:

$$
\Delta\varphi = \frac{q}{\hbar}\left(\int_{\gamma_1} \vec{A} \cdot d\vec{l} - \int_{\gamma_2} \vec{A} \cdot d\vec{l}\right) = \frac{q}{\hbar}\oint_C \vec{A} \cdot d\vec{l}
$$

Pelo teorema de Stokes:

$$
\Delta\varphi = \frac{q}{\hbar}\int_S \vec{B} \cdot d\vec{S} = \frac{q}{\hbar}\Phi
$$

### 4.4. Observabilidade do Efeito

O padrão de interferência é deslocado por:

$$
I \propto 1 + \cos\left(\varphi_0 + \frac{q}{\hbar}\Phi\right)
$$

onde $\varphi_0$ é a diferença de fase na ausência de fluxo.

## 5. Interpretação Geométrica

### 5.1. Fibrado e Conexão

A função de onda é uma **seção** de um fibrado complexo sobre o espaço. O potencial $A_\mu$ é a **conexão** neste fibrado.

### 5.2. Holonomia

A fase de Aharonov-Bohm é a **holonomia** da conexão:

$$
\text{Hol}_C(A) = \exp\left(\frac{iq}{\hbar}\oint_C A\right)
$$

### 5.3. Invariância de Gauge

Sob uma transformação de gauge $A \rightarrow A + d\lambda$, a holonomia transforma-se como:

$$
\text{Hol}_C(A + d\lambda) = \exp\left(\frac{iq}{\hbar}\oint_C A\right) \cdot \exp\left(\frac{iq}{\hbar}[\lambda(\text{fim}) - \lambda(\text{início})]\right)
$$

Para um loop fechado, $\lambda(\text{fim}) = \lambda(\text{início})$, então:

$$
\text{Hol}_C(A + d\lambda) = \text{Hol}_C(A)
$$

A holonomia é **invariante de gauge**, confirmando que o efeito Aharonov-Bohm é físico e observável.

## 6. Significado Fundamental

O efeito Aharonov-Bohm demonstra que:

1. O potencial eletromagnético $A_\mu$ é mais fundamental que o campo $F_{\mu\nu}$ em mecânica quântica
2. A fase da função de onda tem significado físico observável
3. A teoria de gauge não é meramente uma redundância matemática, mas reflete estrutura física profunda
4. A geometria dos fibrados é essencial para descrever consistentemente sistemas quânticos com simetrias de gauge

Esta realização foi um marco no desenvolvimento da física teórica moderna, influenciando profundamente nossa compreensão das teorias de gauge e sua role na descrição das interações fundamentais.
