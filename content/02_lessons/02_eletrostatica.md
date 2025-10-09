# Eletrostática

## Campos na Matéria

Podemos assumir que as equações que regem a dinâmica dos campos elétricos e magnéticos se aplicam aos mundos macroscópicos e microscópicos, pelo menos no regime de partículas não relativísticas. O campo elétrico macroscópico, que age sobre a matéria contínua, varia pouco na escala microscópica e é uma média espacial dos campos microscópicos, um procedimento chamado de média de Lorentz. Enquanto o procedimento de média aplicado for linear, teremos a validade das equações de Maxwell para as médias dos campos.

Embora o mundo microscópico seja populado por grandezas contínuas, um objeto macroscópico tem uma superfície definida de forma descontínua. Se temos uma distribuição microscópica de carga $\rho_0(\vec r)$, tal que

$$
\rho_0(z) = \bar \rho_0(z) + \sigma \lambda(z) \Rightarrow \bar \rho_0(z) + \sigma \delta(z)\\
\bar \rho_0(z) = \frac{1}{S}\int_A dxdy \;\rho_0(\vec r),
$$

ou seja, precisamos considerar cargas superficiais associadas as bordas de um objeto macroscópico.

Considerando uma fronteira em $z=0$, podemos escrever:

$$
\begin{align}
\vec E(\vec r) & = \vec E_R(\vec r) \Theta(z) + \vec E_L(\vec r) \Theta(-z)\\
\rho(\vec r) &= \rho_R(\vec r) \Theta(z) + \rho_L(\vec r) \Theta(-z) + \sigma \delta(z)\\
\nabla \cdot \vec E &= \nabla \cdot \vec E_R \Theta(z) + \nabla \cdot \vec E_L \Theta(-z) + \hat z \cdot (\vec E_R - \vec E_R)\delta(z) \Rightarrow \\
& \hat z\cdot (\vec E_R - \vec E_R) = \frac{\sigma}{\epsilon_0}
\end{align}
$$

Aplicando as equações de Maxwell obtemos condições gerais de contorno para os campos:

$$
\begin{align}
\hat n_2\cdot [\vec E_1 - \vec E_2] &= \frac{\sigma}{\epsilon_0}\\
\hat n_2\cdot [\vec B_1 - \vec B_2] &=0\\
\hat n_2\times [\vec E_1 - \vec E_2] &=0\\
\hat n_2\times [\vec B_1 - \vec B_2] &=\mu_0 \vec K
\end{align}
$$

## Energia Potencial Eletrostática

### Teorema da reciprocidade de Green

$$
\begin{align}
\delta V &= -\vec F\cdot \delta \vec s\\
\vec F &= -\nabla V\\
V_E &= q\phi(\vec r) \Rightarrow\\
V_E &= \int dV´ \rho(\vec r') \phi(\vec r') \Rightarrow \\
V_E &= \frac{1}{4\pi\epsilon_0} \int dV \int dV' \frac{\rho_2(\vec r) \rho_1(\vec r´)}{|\vec r - \vec r'|} \\
& \int dV´ \rho_1(\vec r') \phi_2(\vec r')
\end{align}
$$

### Energia Eletrostática total

Considere um sistema discreto de cargas $q_i$, para montar o sistema precisamos fornecer energia:

$$
\begin{align}
U &= \frac{1}{4\pi\epsilon_0} \sum_{j=1}^N\sum_{i>j}^N \frac{q_i\;q_j}{|\vec r_i - \vec r_j|}\\
&= \frac{1}{2} \frac{1}{4\pi\epsilon_0} \sum_{j=1}^N\sum_{i\ne j}^N \frac{q_i\;q_j}{|\vec r_i - \vec r_j|} \\
&= \frac{1}{2} \sum_{1=1}^N \frac{q_i\;\phi(\vec r_i)}{|\vec r_i - \vec r_j|}
\end{align}
$$

logo

$$
\begin{align}
U &= \frac{1}{2}\int dV \rho(\vec r)\phi(\vec r)\\
&= -\frac{1}{2}\epsilon_0\int dV \vec E \cdot \nabla \phi + \frac{1}{2}\epsilon_0 \int dS \nabla \cdot (\phi \vec E)\\
&= \frac{1}{2}\epsilon_0\int dV |\vec E^2|,
\end{align}
$$

assumindo que as cargas ocupam uma região finita do espaço.

Note que a energia esta nos campos, e a energia de uma partícula puntiforme é infinita. Na vida real os elétrons já foram construídos, e a energia de montar um sistema não deve levar em conta como construímos o elétron. Isto já teve muito pano para manga, e existe ma versão do eletromagnetismo qte tem autoenergia finita, o **eletromagnetismo de born-infeld**#️⃣

$$
\mathcal{L} = -b^2 \sqrt{-\det (\eta + \frac{F}{b})} + b^2
$$

## Problemas

### Teorema de Thomson

**Enunciado:** Se várias superfícies são fixadas no espaço e uma carga total é colocada em cada superfície, então a energia eletrostática na região é um **mínimo absoluto** quando as cargas se distribuem de forma que cada superfície seja equipotencial (como ocorre com condutores).

---

#### Demonstração

Considere:

- N superfícies fixas S₁, S₂, ..., Sₙ
- Carga total Qᵢ em cada superfície Sᵢ (fixada)
- Distribuição de carga σᵢ(r) em cada superfície

##### Passo 1: Energia Eletrostática

A energia eletrostática pode ser escrita como:

$$U = \frac{\epsilon_0}{2} \int_{\text{todo espaço}} |\nabla \phi|^2 \, dV$$

onde φ é o potencial elétrico que satisfaz:

- ∇²φ = 0 no espaço entre as superfícies (equação de Laplace)
- Condições de contorno apropriadas nas superfícies

##### Passo 2: Comparação de Configurações

Sejam:

- **φ₀**: potencial na configuração de equilíbrio (superfícies equipotenciais)
- **σ₀**: distribuição de carga correspondente
- **φ**: qualquer outra distribuição de potencial com a mesma carga total em cada superfície
- **σ**: distribuição de carga correspondente

Defina a diferença:
$$\delta \phi = \phi - \phi_0$$

**Restrição:** A carga total em cada superfície deve ser preservada:
$$\int_{S_i} \sigma \, dA = \int_{S_i} \sigma_0 \, dA = Q_i$$

Portanto:
$$\int_{S_i} \delta\sigma \, dA = 0 \quad \text{para cada } i$$

onde δσ = σ - σ₀.

##### Passo 3: Expansão da Energia

A energia para a distribuição perturbada:

$$U[\phi] = \frac{\epsilon_0}{2} \int |\nabla(\phi_0 + \delta\phi)|^2 \, dV$$

$$U[\phi] = \frac{\epsilon_0}{2} \int \left[|\nabla\phi_0|^2 + 2\nabla\phi_0 \cdot \nabla(\delta\phi) + |\nabla(\delta\phi)|^2\right] dV$$

$$U[\phi] = U[\phi_0] + \epsilon_0 \int \nabla\phi_0 \cdot \nabla(\delta\phi) \, dV + \frac{\epsilon_0}{2} \int |\nabla(\delta\phi)|^2 \, dV$$

##### Passo 4: Termo Cruzado

Usando integração por partes e o teorema da divergência:

$$\int \nabla\phi_0 \cdot \nabla(\delta\phi) \, dV = \int \nabla \cdot [\phi_0 \nabla(\delta\phi)] \, dV - \int \phi_0 \nabla^2(\delta\phi) \, dV$$

Como ∇²(δφ) = 0 no volume (ambos satisfazem Laplace):

$$\int \nabla\phi_0 \cdot \nabla(\delta\phi) \, dV = \oint_{\text{superfícies}} \phi_0 \frac{\partial(\delta\phi)}{\partial n} \, dA$$

Nas superfícies condutoras, **φ₀ é constante** em cada superfície Sᵢ (equipotencial):

$$\oint_{\text{superfícies}} \phi_0 \frac{\partial(\delta\phi)}{\partial n} \, dA = \sum_i V_{0i} \oint_{S_i} \frac{\partial(\delta\phi)}{\partial n} \, dA$$

Mas pela condição de contorno eletrostática:
$$\frac{\partial \phi}{\partial n} = -\frac{\sigma}{\epsilon_0}$$

Portanto:
$$\oint_{S_i} \frac{\partial(\delta\phi)}{\partial n} \, dA = -\frac{1}{\epsilon_0} \int_{S_i} \delta\sigma \, dA = 0$$

**O termo cruzado é zero!**

### Passo 5: Conclusão

$$U[\phi] = U[\phi_0] + \frac{\epsilon_0}{2} \int |\nabla(\delta\phi)|^2 \, dV$$

Como o último termo é sempre **positivo** (é uma integral de um quadrado):

$$\boxed{U[\phi] \geq U[\phi_0]}$$

**A igualdade ocorre apenas quando** δφ = constante, ou seja, quando φ = φ₀.

---

## Interpretação Física

**O teorema prova que:**

1. Entre todas as distribuições de carga com cargas totais fixas, a configuração de **equilíbrio eletrostático** (superfícies equipotenciais) tem a **menor energia**.

2. Condutores naturalmente alcançam esta configuração porque as cargas se redistribuem até minimizar a energia.

3. Qualquer desvio da configuração equipotencial aumenta a energia do sistema.

**Significado:** Este é um **princípio variacional** - a natureza escolhe a configuração de mínima energia, que corresponde a superfícies equipotenciais.

### Capacitor de Placas Paralelas

---

:::{figure} ../00_images/02_lessons/capacitor.png

:::

Claro — segue a solução em **Markdown** completa e organizada para o caso clássico do **capacitor de placas paralelas** com um **bloco dielétrico parcialmente inserido**. Vou assumir a configuração habitual (sem pedir confirmação): as placas têm área total (A) e separação (d); o bloco dielétrico de permissividade (\varepsilon=\varepsilon_0\varepsilon_r) tem comprimento de inserção (x) ao longo de um comprimento total (L) das placas (ou seja, a área coberta pelo dielétrico é (A_{\rm diel}=A,\frac{x}{L})). Se preferir outra geometria diga e eu adapto.

---

### Capacitor com dielétrico parcialmente inserido — energia e força

**Dados / definições**

- Placas paralelas, área total (A), separação (d).
- Comprimento "útil" das placas na direção de inserção: (L).
- Bloco dielétrico inserido até (x) $ (0\le x\le L) $.
- Permissividade do dielétrico: $\varepsilon=\varepsilon_0\varepsilon_r$.
- Área ocupada pelo dielétrico: $A_{\rm diel}=A\frac{x}{L}$.
- Área não ocupada (vácuo): $A_{\rm vac}=A-A_{\rm diel}=A\Big(1-\frac{x}{L}\Big)$)$.

## 1. Capacitância como função de (x)

As duas regiões (com e sem dielétrico) ficam lado a lado, portanto estão em **paralelo**: a capacitância total é a soma das capacitâncias das duas áreas:

$$
\begin{aligned}
C(x)
&= \frac{\varepsilon_0,A_{\rm vac}}{d} + \frac{\varepsilon,A_{\rm diel}}{d}\\
&= \frac{\varepsilon_0 A}{d}\Big(1-\frac{x}{L}\Big) + \frac{\varepsilon_0\varepsilon_r A}{d}\frac{x}{L} \\
&= \frac{\varepsilon_0 A}{d}\Big[1 + (\varepsilon_r-1)\frac{x}{L},\Big].
\end{aligned}
$$

É conveniente definir
$$
C_0 \equiv \frac{\varepsilon_0 A}{d},\qquad
\Delta C \equiv C_0(\varepsilon_r-1)\frac{x}{L},
$$
logo $C(x)=C_0+\Delta C$.

---

#### 2. Energia elétrica (U(x))

**Bateria ligada — tensão (V) fixa**

Se a bateria está conectada, a tensão entre as placas é constante (V). A energia eletrostática armazenada:

$$\boxed{ U_V(x) = \tfrac{1}{2}\; C(x)V^2 = \tfrac{1}{2} V^2 C_0 \Big(1+ (\varepsilon_r-1)\frac{x}{L}\Big).}
$$

**Bateria desligada — carga (Q) fixa**

Se o capacitor está isolado, a carga (Q) permanece constante. A energia:

$$
\boxed{ U_Q(x) \;=\; \frac{Q^2}{2\,C(x)}
\;=\; \frac{Q^2}{2\,C_0}\frac{1}{1+(\varepsilon_r-1)\dfrac{x}{L}}. \; }
$$

---

#### 3. Força sobre o dielétrico (na direção de aumentar (x))

A força (módulo) (F) que puxa o dielétrico para dentro pode ser obtida pela variação da energia com (x). A convenção: a força que tende a **aumentar** (x) é

$$F(x) = -\frac{dU_{\rm sistema}}{dx}$$

onde $(U_{\rm sistema})$ é a energia **mecano-eletrostática** apropriada ao caso.

**Bateria ligada ( (V=)const )**

Para V fixo a energia do campo aumenta com x (a bateria fornece/absorve energia). A força elétrica resultante é

$$
\boxed{ \; F_V(x) \;=\; \frac{1}{2}\,V^2\,\frac{dC}{dx}; }.
$$

Como
$$
\frac{dC}{dx} = C_0\frac{\varepsilon_r-1}{L},
$$

obtém-se

$$
\boxed{ \; F_V \;=\; \frac{1}{2}\,V^2,C_0\frac{\varepsilon_r-1}{L}
\;=\; \frac{1}{2}\,V^2\;\frac{\varepsilon_0 A}{d}\;\frac{\varepsilon_r-1}{L}. \; }
$$

O sinal positivo indica que a força **puxa o dielétrico para dentro** pois $(\varepsilon_r>1) ⇒ (dC/dx>0)$.

---

**Bateria desligada ( (Q=)const )**

Para carga fixada, a forma conveniente é

$$
\boxed{ \; F_Q(x) \;=\; -\frac{d}{dx}!\Big(\frac{Q^2}{2C(x)}\Big)
\;=\; \frac{Q^2}{2C(x)^2}\,\frac{dC}{dx}. \; }
$$

Usando $dC/dx$ acima:

$$
\boxed{ \; F_Q(x) \;=\; \frac{Q^2}{2\,C(x)^2};C_0\frac{\varepsilon_r-1}{L}
\;=\; \frac{1}{2},\frac{Q^2}{C(x)^2}\; \frac{\varepsilon_0 A}{d}\;\frac{\varepsilon_r-1}{L}. \; }
$$

### Capacitor quase paralelo

:::{figure} ../00_images/02_lessons/capacitor_2.png

:::

## Dados do problema

- Placas retangulares com bordas de comprimento a e b
- Uma borda (comprimento a) separada por distância d₁
- Outra borda (comprimento a) separada por distância d₂
- Bordas de comprimento b mantêm a geometria
- Diferença de potencial: V

---

#### Potencial entre as placas

**Sistema de coordenadas:**

- Eixo x: ao longo da borda de comprimento b
- Eixo y: perpendicular às placas
- Eixo z: ao longo da borda de comprimento a

A separação varia linearmente com x:
$$d(x) = d_1 + \frac{(d_2 - d_1)x}{b}$$

**Assumindo campo aproximadamente unidimensional** (negligenciando efeitos de borda), o campo elétrico é perpendicular às placas e depende apenas de x.

Na posição x, se a placa inferior está em y = 0 e a superior em y = d(x), o potencial varia linearmente entre as placas:

$$\phi(x, y) = V_0 + \frac{V - V_0}{d(x)} \cdot y$$

Escolhendo a placa inferior como referência (V₀ = 0) e a superior com potencial V:

$$\boxed{\phi(x, y) = \frac{Vy}{d_1 + \frac{(d_2 - d_1)x}{b}}}$$

Ou, simplificando:

$$\boxed{\phi(x, y) = \frac{Vby}{d_1 b + (d_2 - d_1)x}}$$

---

#### Capacitância

**Método 1: Integração direta da carga**

O campo elétrico na posição x é:
$$E(x) = -\frac{\partial \phi}{\partial y} = \frac{V}{d(x)} = \frac{Vb}{d_1 b + (d_2 - d_1)x}$$

A densidade superficial de carga:
$$\sigma(x) = \epsilon_0 E(x) = \frac{\epsilon_0 Vb}{d_1 b + (d_2 - d_1)x}$$

**Carga total** em uma tira de largura dx:
$$dQ = \sigma(x) \cdot a \cdot dx = \frac{\epsilon_0 Vab \, dx}{d_1 b + (d_2 - d_1)x}$$

Integrando de x = 0 até x = b:
$$Q = \int_0^b \frac{\epsilon_0 Vab \, dx}{d_1 b + (d_2 - d_1)x}$$

Fazendo a substituição u = d₁b + (d₂ - d₁)x:

- du = (d₂ - d₁)dx
- Quando x = 0: u = d₁b
- Quando x = b: u = d₂b

$$Q = \frac{\epsilon_0 Vab}{d_2 - d_1} \int_{d_1 b}^{d_2 b} \frac{du}{u}$$

$$Q = \frac{\epsilon_0 Vab}{d_2 - d_1} \ln\left(\frac{d_2 b}{d_1 b}\right)$$

$$Q = \frac{\epsilon_0 Vab}{d_2 - d_1} \ln\left(\frac{d_2}{d_1}\right)$$

**Capacitância:**

$$\boxed{C = \frac{Q}{V} = \frac{\epsilon_0 ab}{d_2 - d_1} \ln\left(\frac{d_2}{d_1}\right)}$$

**Forma alternativa:**

$$\boxed{C = \frac{\epsilon_0 ab}{\ln(d_2/d_1)} \cdot \frac{\ln(d_2/d_1)}{d_2 - d_1} = \frac{\epsilon_0 ab}{d_2 - d_1} \ln\left(\frac{d_2}{d_1}\right)}$$

---

**Verificação (limite d₂ → d₁):**

Usando a expansão de Taylor: ln(1 + ε) ≈ ε para pequeno ε:

Se d₂ = d₁ + Δd com Δd << d₁:
$$\ln\left(\frac{d_2}{d_1}\right) = \ln\left(1 + \frac{\Delta d}{d_1}\right) \approx \frac{\Delta d}{d_1}$$

$$C \approx \frac{\epsilon_0 ab}{\Delta d} \cdot \frac{\Delta d}{d_1} = \frac{\epsilon_0 ab}{d_1}$$

---

### Campo e energia de interação de dipolos elétricos

# Cálculo Detalhado: Campo Elétrico e Potencial de Dipolos

## 1. Definições Fundamentais

Um **dipolo elétrico** consiste em duas cargas iguais e opostas (+q e -q) separadas por uma distância d.

**Momento de dipolo:**

$$
\vec p = q·\vec d

$$
onde $\vec d$ aponta da carga negativa para a positiva.

---

## 2. Potencial Elétrico de um Dipolo

### Dedução

Considere um dipolo com cargas +q em $r_+$ e -q em $-r_-$. O potencial em um ponto P a uma distância r é:

$$
V = [1/4πε₀](q/r_+ - q/r_-)

$$

Para $r >> d$ (aproximação de campo distante):

$$
r_+ ≈ r - (d/2)cos θ\\
r_- ≈ r + (d/2)cos θ
$$

onde $θ$ é o ângulo entre $\vec p$ e $\vec r$.

Expandindo em série de Taylor:

$$
1/r_+ ≈ [1/r](1 + (d cos θ)/(2r))\\
1/r_- ≈ [1/r](1 - (d cos θ)/(2r))
$$
Substituindo:

$$
V = [q/4πε_0r]((1 + (d cos θ)/(2r)) - (1 - (d cos θ)/(2r)))\\
V = (q/4πε_0r) · (d cos θ)/r
$$

$$
V(r, θ) = (1/4πε_0) · (p cos θ)/r²

$$
ou em forma vetorial:

$$
V(\vec r) = (1/4πε_0) · (\vec p · \hat r)/r²

$$
---

## 3. Campo Elétrico de um Dipolo

O campo elétrico é obtido por: $\vec E = -\nabla V$

Em coordenadas esféricas:

$$
\vec E = -[∂V/∂r r̂ + (1/r)(∂V/∂θ) θ̂]
$$

$$
E_r = -∂V/∂r = -∂/∂r[(p cos θ)/(4πε_0r^2)]\\
E_r = -(p cos θ)/(4πε_0) · ∂/∂r(r^{-2})\\
E_r = -(p cos θ)/(4πε_0) · (-2r^{-3})
$$

$$E_r = (1/4πε_0) · (2p cos θ)/r^3$$

$$
E_θ = -(1/r)(∂V/∂θ) = -(1/r) · ∂/∂θ[(p cos θ)/(4πε₀r²)]\\
E_θ = -(1/r) · (p)/(4πε₀r²) · (-sen θ)
$$

$$E_θ = (1/4πε₀) · (p sen θ)/r³$$

$$|\vec E| = (p/4πε₀r³)√(1 + 3cos²θ)$$

#### Campo e energia de interação de dipolos elétricos

Um dipolo pontual de momento dipolar **p**, localizado na origem, gera um **potencial elétrico** no ponto **r** dado por

$$
\Phi(\mathbf r) = \frac{1}{4\pi \varepsilon_0} , \frac{\mathbf p \cdot \mathbf r}{r^3},
$$
onde ( $r = |\mathbf r|$ ).

O campo é o **gradiente negativo** do potencial:

$$
\mathbf E(\mathbf r) = -\nabla \Phi(\mathbf r).
$$

Escrevendo o potencial em componentes:

$$
\Phi = \frac{1}{4\pi \varepsilon_0} p_j r_j r^{-3}.
$$

O gradiente (com notação de índices) é

$$
\partial_i (r_j r^{-3}) = \delta_{ij} r^{-3} - 3 r_i r_j r^{-5}.
$$

Assim,

$$
E_i = -\frac{1}{4\pi \varepsilon_0} p_j \big( \delta_{ij} r^{-3} - 3 r_i r_j r^{-5} \big)
= \frac{1}{4\pi \varepsilon_0} \left( 3\frac{(\mathbf p \cdot \mathbf r) r_i}{r^5} - \frac{p_i}{r^3} \right).
$$

Em forma vetorial:

$$
\boxed{
\mathbf E(\mathbf r)
= \frac{1}{4\pi \varepsilon_0}
\left(
\frac{3(\mathbf p \cdot \mathbf r), \mathbf r}{r^5}

- \frac{\mathbf p}{r^3}
  \right)
  = \frac{1}{4\pi \varepsilon_0} ,
  \frac{3(\mathbf p \cdot \mathbf r)\mathbf r - r^2 \mathbf p}{r^5}.
  }
  $$

---

## 3. Energia potencial entre dois dipolos

Considere dois dipolos elétricos **p₁** e **p₂**, separados por um vetor **r** (do dipolo 2 para o dipolo 1).

O **campo elétrico gerado por p₂** no ponto onde está **p₁** é

$$
\mathbf E_2(\mathbf r)
= \frac{1}{4\pi \varepsilon_0}
\frac{3(\mathbf p_2 \cdot \mathbf r)\mathbf r - r^2 \mathbf p_2}{r^5}.
$$

A **energia potencial** de interação é dada por

$$
W = - \mathbf p_1 \cdot \mathbf E_2(\mathbf r).
$$

Substituindo a expressão do campo:

$$
\begin{aligned}
W &= -\frac{1}{4\pi \varepsilon_0}
\frac{\mathbf p_1 \cdot \big[ 3(\mathbf p_2 \cdot \mathbf r)\mathbf r - r^2 \mathbf p_2 \big]}{r^5} \\
&= -\frac{1}{4\pi \varepsilon_0}
\frac{3(\mathbf p_2 \cdot \mathbf r)(\mathbf p_1 \cdot \mathbf r) - r^2(\mathbf p_1 \cdot \mathbf p_2)}{r^5}.
\end{aligned}
$$

Reorganizando os sinais:

$$
\boxed{
W =
\frac{1}{4\pi \varepsilon_0}
\frac{r^2 (\mathbf p_1 \cdot \mathbf p_2)

- 3(\mathbf p_1 \cdot \mathbf r)(\mathbf p_2 \cdot \mathbf r)}{r^5}.
  }
  $$

### Cálculo da polarização dentro de uma esfera dielétrica

Considere uma esfera homogênea de raio (R) e constante dielétrica (\varepsilon_p), imersa em um meio de constante (\varepsilon_m). Sobre ela atua um campo elétrico externo uniforme (\mathbf{E}_0) (por exemplo (\mathbf{E}_0 = E_0\hat z)). Usamos a solução eletrostática já conhecida para o potencial.

#### Campo interno da esfera

Ao resolver a equação de Laplace com simetria esférica (ver derivação padrão), o potencial interno tem a forma
$$
\Phi_{\text{in}}(r,\theta) = -B E_0 r\cos\theta,
$$

com

$$
B = \frac{3\varepsilon_m}{\varepsilon_p + 2\varepsilon_m}.
$$

Portanto o **campo elétrico no interior** da esfera é uniforme e dado por

$$
\mathbf{E}*{\text{in}} = -\nabla \Phi*{\text{in}} = B,\mathbf{E}_0
= \frac{3\varepsilon_m}{\varepsilon_p + 2\varepsilon_m},\mathbf{E}_0.
$$

No caso que nos interessa (esferas no vácuo) $\varepsilon_m=1$, assim

$$
\boxed{\displaystyle
\mathbf{E}_{\text{in}} = \frac{3}{\varepsilon_p + 2},\mathbf{E}_0.
}
$$

---

#### Polarização dentro da esfera

Para um dielétrico linear, a relação entre deslocamento e campo dentro da matéria é

$$
\mathbf{D}*{\text{in}} = \varepsilon_0 \varepsilon_p \mathbf{E}*{\text{in}}.
$$

A polarização (densidade dipolar) é $\mathbf{P} = \mathbf{D} - \varepsilon_0 \mathbf{E}$, portanto, dentro da esfera:

$$
\mathbf{P}*{\text{in}} = \varepsilon_0(\varepsilon_p - 1)\mathbf{E}*{\text{in}}.
$$

Substituindo $\mathbf{E}_{\text{in}}$:

$$
\boxed{\displaystyle
\mathbf{P}_{\text{in}}
= \varepsilon_0(\varepsilon_p - 1),\frac{3\varepsilon_m}{\varepsilon_p + 2\varepsilon_m},\mathbf{E}_0.
}
$$

No vácuo $\varepsilon_m=1$:

$$
\boxed{\displaystyle
\mathbf{P}_{\text{in}} = 3\varepsilon_0,
\frac{\varepsilon_p - 1}{\varepsilon_p + 2},\mathbf{E}_0.
}
$$

---

## 3. Relação com o momento dipolar total da esfera

O momento dipolar induzido total da esfera é o volume vezes a polarização média (a polarização interna é uniforme, logo média = valor interno):

$$
\mathbf{p} = \mathbf{P}_{\text{in}} , v
= \left(3\varepsilon_0\frac{\varepsilon_p - 1}{\varepsilon_p + 2}\mathbf{E}_0\right)\left(\frac{4}{3}\pi R^3\right)
= 4\pi\varepsilon_0 R^3 \frac{\varepsilon_p - 1}{\varepsilon_p + 2},\mathbf{E}_0,
$$
isto é,
$$
\boxed{\displaystyle
\mathbf{p} = \alpha,\mathbf{E}_0,
\qquad
\alpha = 4\pi\varepsilon_0 R^3\frac{\varepsilon_p - 1}{\varepsilon_p + 2}.
}
$$

Note que ( $\mathbf{P}_{\text{in}} = \mathbf{p}/v$ ), conforme esperado.

### Pó de Esferas Dielétricas (Stony Brook)

Um pó composto por pequenas partículas esféricas (raio ( R = 100,\mathrm{nm} )) está disperso no vácuo, com uma concentração ( n ) de partículas por unidade de volume.

Quer-se determinar a **constante dielétrica efetiva** ( $\varepsilon_{\text{eff}}$ ) do meio.

Explique também por que a resposta aparente
$$
\varepsilon_{\text{eff}} = 1 + n v (\varepsilon_p - 1)
$$
(onde ( v ) é o volume de uma partícula) está **errada**.

---

## 1. Polarizabilidade de uma esfera

Considere uma esfera homogênea de constante dielétrica $\varepsilon_p $ imersa em um meio com constante ($ \varepsilon_m $) (no vácuo, ($ \varepsilon_m = 1 $)).

Quando submetida a um campo elétrico uniforme ( $\mathbf{E}_0 $), a esfera se comporta como um **dipolo induzido** com momento:

$$
\mathbf{p} = \alpha, \mathbf{E}_0.
$$

A polarizabilidade ( $\alpha$ ) é obtida resolvendo a equação de Laplace para o potencial com simetria esférica e condições de contorno contínuas em ( $\Phi$ ) e ($ \varepsilon \partial_r \Phi$ ):

$$
\boxed{
\alpha = 4\pi \varepsilon_0 \varepsilon_m R^3
\frac{\varepsilon_p - \varepsilon_m}{\varepsilon_p + 2\varepsilon_m}.
}
$$

No vácuo (( $\varepsilon_m = 1 $)):

$$
\boxed{
\alpha = 4\pi \varepsilon_0 R^3
\frac{\varepsilon_p - 1}{\varepsilon_p + 2}
= 3\varepsilon_0 v \frac{\varepsilon_p - 1}{\varepsilon_p + 2},
}
$$
onde ($ v = \tfrac{4}{3}\pi R^3 $) é o volume da partícula.

---

#### Polarização macroscópica e campo local

Para uma densidade de partículas ( n ), a **polarização média** do meio é

$$
\mathbf{P} = n \mathbf{p} = n \alpha \mathbf{E}_{\text{loc}},
$$
onde o **campo local** é dado pela aproximação de Lorentz:

$$
\mathbf{E}_{\text{loc}} = \mathbf{E} + \frac{\mathbf{P}}{3\varepsilon_0}.
$$

Substituindo:

$$
\mathbf{P} = n\alpha\left(\mathbf{E} + \frac{\mathbf{P}}{3\varepsilon_0}\right)
\quad\Rightarrow\quad
\mathbf{P}\left(1 - \frac{n\alpha}{3\varepsilon_0}\right) = n\alpha,\mathbf{E}.
$$

Assim,

$$
\mathbf{P} = \frac{n\alpha}{1 - \dfrac{n\alpha}{3\varepsilon_0}},\mathbf{E}.
$$

---

#### Constante dielétrica efetiva

A relação entre ( $\mathbf{D}$ ) e ( $\mathbf{E}$ ) é

$$
\mathbf{D} = \varepsilon_0 \mathbf{E} + \mathbf{P}
= \varepsilon_0 \varepsilon_{\text{eff}} \mathbf{E}.
$$

Logo,

$$
\varepsilon_{\text{eff}} = 1 + \frac{P}{\varepsilon_0 E}
= 1 + \frac{n\alpha/\varepsilon_0}{1 - \dfrac{n\alpha}{3\varepsilon_0}}.
$$

Definindo

$$
\beta = \frac{n\alpha}{3\varepsilon_0},
$$

temos

$$
\boxed{
\frac{\varepsilon_{\text{eff}} - 1}{\varepsilon_{\text{eff}} + 2} = \beta
= n v \frac{\varepsilon_p - 1}{\varepsilon_p + 2}.
}
$$

Esta é a **fórmula de Clausius–Mossotti**.

---

#### 4. Expansão para baixas concentrações

Para frações volumétricas pequenas ( $f = n v \ll 1$ ):

$$
\varepsilon_{\text{eff}} \approx 1 + 3f,\frac{\varepsilon_p - 1}{\varepsilon_p + 2} + O(f^2).
$$

---

#### Por que a expressão aparente está errada

A expressão
$$
\varepsilon_{\text{eff}} = 1 + n v (\varepsilon_p - 1)
$$
é uma **média linear ingênua**, que ignora o campo local e os efeitos de **despolarização** das esferas.

O campo dentro de cada esfera **não é igual** ao campo aplicado, pois as cargas induzidas na superfície alteram o campo interno e externo.

O fator de correção
$$
\frac{3}{\varepsilon_p + 2}
$$
vem justamente da solução da equação de Laplace para uma esfera no campo uniforme.

Portanto, a média linear só seria válida se as partículas tivessem a mesma constante dielétrica do meio — o que não é o caso geral.

---

#### Fórmula final

$$
\boxed{
\frac{\varepsilon_{\text{eff}} - 1}{\varepsilon_{\text{eff}} + 2}
= n v \frac{\varepsilon_p - 1}{\varepsilon_p + 2}
\qquad \text{(Clausius–Mossotti relation)}.
}
$$

- Válido para partículas pequenas e diluídas (sem interação direta entre dipolos).
- Para metais (( $|\varepsilon_p| \gg 1 $)), o termo no denominador pode divergir, indicando ressonância ou percolação.
- O modelo é isotrópico e assume partículas esféricas idênticas.

### Configuração do Problema

- **Hemisfério superior** (θ < π/2): potencial φ = +V
- **Hemisfério inferior** (θ > π/2): potencial φ = -V
- **Plano equatorial** (θ = π/2): separação com dielétrico fino
- Raio da esfera: R

---

**Coordenadas Esféricas**

Usamos coordenadas esféricas (r, θ, φ) onde θ é o ângulo polar medido do eixo z.

**Equação de Laplace**

No espaço fora da esfera (r > R) e dentro (r < R), o potencial satisfaz:

$$\nabla^2 \Phi = 0$$

Por simetria azimutal (independente de φ):

$$\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2 \frac{\partial \Phi}{\partial r}\right) + \frac{1}{r^2 \sin\theta}\frac{\partial}{\partial \theta}\left(\sin\theta \frac{\partial \Phi}{\partial \theta}\right) = 0$$

**Expansão em Harmônicos Esféricos**

A solução geral é:

$$\Phi(r, \theta) = \sum_{l=0}^{\infty} \left(A_l r^l + \frac{B_l}{r^{l+1}}\right) P_l(\cos\theta)$$

**Região interna (r < R):**
Como o potencial deve ser finito em r = 0, B_l = 0:

$$\Phi_{\text{in}}(r, \theta) = \sum_{l=0}^{\infty} A_l r^l P_l(\cos\theta)$$

**Região externa (r > R):**
Como o potencial deve ir a zero quando r → ∞, A_l = 0:

$$\Phi_{\text{out}}(r, \theta) = \sum_{l=0}^{\infty} \frac{C_l}{r^{l+1}} P_l(\cos\theta)$$

**Condições de Contorno na Superfície (r = R)**

Na superfície da esfera:

$$\Phi(R, \theta) = \begin{cases} +V & \text{se } 0 \leq \theta < \pi/2 \\ -V & \text{se } \pi/2 < \theta \leq \pi \end{cases}$$

Esta é uma **função degrau** em cos θ.

**Expansão em Polinômios de Legendre**

Precisamos expandir a função degrau:

$$f(\cos\theta) = \begin{cases} +V & \text{se } \cos\theta > 0 \\ -V & \text{se } \cos\theta < 0 \end{cases}$$

Os coeficientes são:

$$A_l R^l = \int_{-1}^{1} f(x) P_l(x) \, dx \cdot \frac{2l+1}{2}$$

$$A_l R^l = \frac{2l+1}{2}\left$$\int_0^1 V P_l(x) \, dx + \int_{-1}^0 (-V) P_l(x) \, dx\right$$$$

$$A_l R^l = \frac{(2l+1)V}{2}\left$$\int_0^1 P_l(x) \, dx - \int_{-1}^0 P_l(x) \, dx\right$$$$

**Propriedade dos Polinômios de Legendre:**

- Para l par: P_l(-x) = P_l(x) → os termos se cancelam → A_l = 0
- Para l ímpar: P_l(-x) = -P_l(x) → os termos se somam

Para **l ímpar:**

$$A_l R^l = (2l+1)V \int_0^1 P_l(x) \, dx$$

**Cálculo das Integrais**

Usando a fórmula de recorrência e propriedades:

$$\int_0^1 P_l(x) \, dx = \frac{P_{l-1}(0) - P_{l+1}(0)}{2l+1}$$

Para l ímpar, os valores de P_l(0) podem ser calculados:

- P₁(0) = 0
- P₃(0) = 0
- P₅(0) = 0
- Em geral, P_l(0) = 0 para l ímpar

Mas P_l(0) para l par:

- P₀(0) = 1
- P₂(0) = -1/2
- P₄(0) = 3/8

Usando a relação:
$$\int_0^1 P_{2n+1}(x) \, dx = \frac{(-1)^n}{2^{2n+1}} \binom{2n}{n} \frac{1}{n+1}$$

Ou mais simplesmente:
$$\int_0^1 P_1(x) \, dx = \frac{1}{2}$$
$$\int_0^1 P_3(x) \, dx = -\frac{1}{8}$$
$$\int_0^1 P_5(x) \, dx = \frac{1}{16}$$

- Solução Final - Região Interna (r ≤ R)

$$\boxed{\Phi(r, \theta) = V\sum_{l=1,3,5,...}^{\infty} (2l+1)\left(\frac{r}{R}\right)^l P_l(\cos\theta) \int_0^1 P_l(x) \, dx}$$

**Primeiros termos:**

$$\Phi(r, \theta) = \frac{3V}{2}\frac{r}{R}\cos\theta - \frac{7V}{8}\frac{r^3}{R^3}P_3(\cos\theta) + \frac{11V}{16}\frac{r^5}{R^5}P_5(\cos\theta) + ...$$

Onde:

- P₁(cos θ) = cos θ
- P₃(cos θ) = (5cos³θ - 3cos θ)/2
- P₅(cos θ) = (63cos⁵θ - 70cos³θ + 15cos θ)/8

- Solução Aproximada (Dipolo)

Para grandes distâncias (r >> R), o **termo dominante é l = 1**:

$$\boxed{\Phi(r, \theta) \approx \frac{3V}{2}\frac{r}{R}\cos\theta \quad (r < R)}$$

$$\boxed{\Phi(r, \theta) \approx \frac{3VR^2}{2r^2}\cos\theta \quad (r > R)}$$

Isto é o **potencial de um dipolo elétrico** com momento:

$$\boxed{p = 3\pi\epsilon_0 R^2 V}$$

---

## Interpretação Física

1. A configuração cria um **dipolo elétrico** alinhado com o eixo z
2. O termo l = 1 domina em distâncias grandes
3. Termos de ordem superior (l = 3, 5, ...) são correções multipolares
4. A descontinuidade no equador cria uma densidade de carga superficial
