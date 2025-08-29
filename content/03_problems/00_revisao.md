# Revisão de Eletromagnetismo

:::{exercise}
Um pêndulo de comprimento $l$ tem uma massa $m$ em sua ponta, carregada com carga $q$. A uma distânca $D$ do pêndulo, na altura mais baixa do pêndulo, em ambos os lados, são colocadas cargas $Q$. Considerando as três cargas pontuais, no regime de pequenas oscilações,

- Escreva a equação que governa o movimento do pêndulo.
- Assumindo que o pêndulo é largado do repouso em $x=x_0$, descreva o movimento subsequente e resolva a equação de movimento.
- Existe algum valor de $qQ$ em que o movimento não é limitado no tempo?
:::

:::{exercise}
Uma linha de carga com densidade de carga $\lambda$ ao longo do eixo $z$ se estende no intervalo de $-L \ge z\ge L$.

- Determine o campo elétrico de $z=0$.
- Considere agora uma faixa infinita $-\infty \ge y \infty \infty$ e calcule o campo elétrico na origem, usando o resultado anterior.
:::

:::{exercise}
Determine o campo elétrico no eixo de uma espira circular com densidade uniforme de carga.
:::

:::{exercise}
Considere um dipolo elétrico feito de duas linhas paralelas de cargas com polaridade oposta e densidade elétrica uniforme, a uma distância $d$.

- Determine o potencial elétrico $\phi(r, \phi, z)
- Determine o potencial e o campo elétrico para pontos muito distantes.
:::

:::{exercise}
Uma barra infinita carrega uma carga uniforme exceto por uma cavidade cilíndrica de raio $a$, centrada na barra, ao longo de seu comprimento.

- Determine o campo magnético em todo o espaço.
:::

:::{exercise}
Uma barra condutora desliza sem atrito sobre dois condutores, transveralmente, artavessados por uma corrente $I$ e ligados por uma resistência $R$. Assumindo que a posição da barra varia como $x-x_0 \propto \cos\omega t$, determine $B$.
:::

<!-- 
# Revisão de Eletromagnetismo — Soluções

## Exercício 1 — Pêndulo carregado com duas cargas laterais (pequenas oscilações)

:::{solution}
**Hipóteses.** Pêndulo de massa $$m$$ e carga $$q$$ preso por fio inextensível de comprimento $$l$$. Duas cargas fixas $$Q$$ colocadas simetricamente nas posições $$x=\pm D$$ ao nível da posição de equilíbrio (plano horizontal), com $$D>0$$. Ângulo do pêndulo medido por $$\theta$$ com a vertical. Pequenas oscilações: $$\theta\ll1$$. Força elétrica entre cargas puntiformes usa $$k=1/(4\pi\varepsilon_0)$$.

**(a) Equação do movimento (linearizada).**

Deslocamento horizontal do pêndulo $$x \simeq l\theta$$. Para pequenos $$\theta$$ a componente horizontal da força elétrica $$F_x$$ sobre $$q$$, pela soma das contribuições das duas cargas $$Q$$, lineariza-se como

$$
F_x(\theta) \approx \frac{2k q Q\, l}{D^3}\,\theta.
$$

Torque total (positivo para aumentar $$\theta$$):

$$
\tau = - m g l \theta + l\,F_x(\theta).
$$

Momento de inércia do pêndulo (massa concentrada na ponta): $$I=m l^2$$. Logo a equação angular:

$$
m l^2 \ddot\theta = - m g l \theta + l\left(\frac{2k q Q\, l}{D^3}\theta\right).
$$

Dividindo por $$m l^2$$:

$$
\boxed{\ddot\theta + \omega^2 \theta = 0,\qquad
\omega^2=\frac{g}{l} - \frac{2k\,qQ}{m D^3}.}
$$

**(b) Solução com condição inicial $$\theta(0)=\theta_0,\ \dot\theta(0)=0$$.**

- Se $$\omega^2>0$$ (estável):

$$
\theta(t)=\theta_0\cos(\omega t),\quad \omega=\sqrt{\dfrac{g}{l}-\dfrac{2kqQ}{mD^3}}.
$$

- Se $$\omega^2=0$$ (caso crítico): $$\theta(t)=\theta_0$$ (constante, com $$\dot\theta(0)=0$$).

- Se $$\omega^2<0$$ (instabilidade): escrevendo $$\omega^2=-\gamma^2$$,

$$
\theta(t)=\theta_0\cosh(\gamma t),
$$
crescimento exponencial (movimento não limitado).

**(c) Condição para movimento não limitado.**  
O regime instável surge se $$\omega^2\le 0$$, i.e.
$$
\boxed{qQ \ge \frac{m g D^3}{2k l}.}
$$

Isto define um limiar entre estabilidade linear e instabilidade: para $$qQ$$ com sinal que reduz $$\omega^2$$ e magnitude superior ao valor acima, pequenas perturbações crescem sem limite (pelo modelo linearizado).
:::

---

## Exercício 2 — Linha de carga (segmento) e faixa infinita

:::{solution}
**Interpretação e hipóteses.** Linha de carga com densidade linear $$\lambda$$ situada ao longo do eixo $$z$$, mas limitada ao segmento $$z\in[-L,L]$$. Queremos (i) o campo elétrico no plano $$z=0$$ a uma distância radial $$\rho$$ do eixo (ponto $$P=(\rho,0,0)$$); e (ii) usar esse resultado para obter o campo de uma faixa construída estendendo essa linha em $$y$$ até $$-\infty<y<\infty$$ (strip infinito em $$y$$) e avaliar o campo no ponto de origem.

### (i) Campo devido ao segmento de linha $$[-L,L]$$ no ponto $$P=(\rho,0,0)$$

Elemento de carga: $$dq=\lambda\,dz'$$ localizado em $$(0,0,z')$$. A distância ao ponto $$P$$ é
$$
r=\sqrt{\rho^2+z'^2},
$$
e a contribuição radial (componente perpendicular ao eixo) ao campo é
$$
dE_\rho = k\frac{dq}{r^2}\cos\alpha
= k\frac{\lambda\,dz'}{\rho^2+z'^2}\cdot\frac{\rho}{\sqrt{\rho^2+z'^2}}
= k\lambda\,\frac{\rho\,dz'}{(\rho^2+z'^2)^{3/2}}.
$$

Integramos $$z'\in[-L,L]$$:

$$
\begin{aligned}
E_\rho(\rho)
&= k\lambda\,\rho\int_{-L}^{L}\frac{dz'}{(\rho^2+z'^2)^{3/2}}
= 2k\lambda\,\rho\int_{0}^{L}\frac{dz'}{(\rho^2+z'^2)^{3/2}}\$$6pt]
&=2k\lambda\left[\frac{z'}{\rho^2\sqrt{\rho^2+z'^2}}\right]_{0}^{L}
= \frac{2k\lambda L}{\rho\sqrt{\rho^2+L^2}}.
\end{aligned}
$$

Substituindo $$k=1/(4\pi\varepsilon_0)$$:

$$
\boxed{E_\rho(\rho)=\frac{\lambda}{2\pi\varepsilon_0}\,\frac{L}{\rho\sqrt{\rho^2+L^2}}.}
$$

**Limites de interesse.**

- $$L\to\infty$$ (linha infinita): $$E_\rho(\rho)\to \dfrac{\lambda}{2\pi\varepsilon_0\,\rho}$$ (campo clássico da linha infinita).
- $$\rho\to\infty$$: $$E_\rho\sim \dfrac{2k\lambda L}{\rho^2}$$ (decai como $$1/\rho^2$$ para distância grande comparada a $$L$$).

---

### (ii) Faixa infinita em $$y$$ — integral explícita e limite do plano

**Construção.** Formamos uma faixa infinita em $$y$$ tomando, para cada $$y\in(-\infty,\infty)$$, uma linha idêntica ao segmento $$[-L,L]$$ localizada em $$(x=\rho_0,y,z)$$. Para obter o campo no ponto de origem $$O$$ (aqui assumimos a faixa deslocada de modo que o ponto de observação fique a uma distância $$\rho_0$$ em $$x$$ do conjunto das linhas — se a faixa atravessa a origem a simetria muda; escolhi a configuração usual: a faixa está em $$x=\rho_0$$, cobrindo $$y\in\mathbb R$$ e $$z\in[-L,L]$$, e queremos $$E$$ no $$O=(0,0,0)$$). Cada linha em $$y$$ está a uma distância lateral $$\rho(y)=\sqrt{\rho_0^2+y^2}$$ do ponto $$O$$, e contribui com o resultado do item (i) substituindo $$\rho\to \rho(y)$$. Se a densidade superficial da faixa for $$\sigma$$ (carga por unidade área), relacionamos $$\sigma$$ com $$\lambda$$ por $$\lambda=\sigma\,dy$$ por elemento de largura $$dy$$.

Campo total em $$O$$ (direção $$+\hat x$$ se as linhas estão em $$x>0$$):

$$
E_x
= \int_{-\infty}^{\infty} \frac{2k\lambda L}{\rho(y)\sqrt{\rho(y)^2+L^2}} \; \frac{\rho_0}{\rho(y)} \; dy,
$$
onde extraí a componente na direção do eixo $$x$$: para uma linha localizada em $$(x=\rho_0,y,*)$$ a direção radial ao ponto $$O$$ tem componente $$ \rho_0/\rho(y)$$ em $$x$$.

Substituindo $$\rho(y)=\sqrt{\rho_0^2+y^2}$$ e $$\lambda=\sigma\,dy$$ (elemento), rewrite integral contínua:

$$
E_x
= 2k L \sigma \int_{-\infty}^{\infty}
\frac{\rho_0}{\rho(y)^2\sqrt{\rho(y)^2+L^2}}\, dy
= 2k L \sigma \int_{-\infty}^{\infty}
\frac{\rho_0}{(\rho_0^2+y^2)\sqrt{\rho_0^2+y^2+L^2}}\, dy.
$$

Essa integral pode ser resolvida por substituição trigonométrica; deixando $$y=\rho_0 \tan t$$ (ou por substituição hiperbólica) obtemos uma forma fechada. Aqui vou apresentar a avaliação:

Defina $$y=\rho_0\tan t$$, $$dy=\rho_0\sec^2 t\,dt$$, e $$\rho(y)^2=\rho_0^2\sec^2 t$$. Então

$$
\begin{aligned}
E_x
&=2k L \sigma \int_{-\pi/2}^{\pi/2}
\frac{\rho_0}{\rho_0^2\sec^2 t\sqrt{\rho_0^2\sec^2 t + L^2}}
\cdot \rho_0\sec^2 t\, dt\\
&=2k L \sigma \int_{-\pi/2}^{\pi/2}
\frac{dt}{\sqrt{\rho_0^2\sec^2 t + L^2}}\\
&=2k L \sigma \int_{-\pi/2}^{\pi/2}
\frac{dt}{\sqrt{L^2+\rho_0^2\sec^2 t}}.
\end{aligned}
$$

Esta integral admite expressão em termos de funções elípticas para gerais $$L,\rho_0$$; contudo, nos limites físicos interessantes simplifica:

- **Faixa larga** $$L\to\infty$$: então $$\sqrt{L^2+\rho_0^2\sec^2 t}\sim L$$ e a integral tende a $$\pi/L$$, resultando em $$E_x\to 2kL\sigma\cdot(\pi/L)=2k\pi\sigma=\sigma/(2\varepsilon_0)$$. Ou seja, no limite de $$L\to\infty$$ (faixa infinitamente larga em $$z$$) e faixa infinita em $$y$$, recuperamos o campo do **plano infinito** carregado:

$$
\boxed{E=\frac{\sigma}{2\varepsilon_0},}
$$
apontando para longe do plano (se $$\sigma>0$$). Este é o resultado clássico: a superposição das linhas produz o campo constante do plano.

- Para $$L$$ e $$\rho_0$$ arbitrários, o integral anterior é a expressão correta e pode ser avaliado numericamente ou expresso por funções elípticas.  

**Resumo:** o campo do segmento é dado por uma integral elementar que resulta na fórmula fechada
$$
E_\rho(\rho)=\frac{2k\lambda L}{\rho\sqrt{\rho^2+L^2}}.
$$
Ao estender em $$y$$ e integrar, obtemos a integral explicita acima; no limite $$L\to\infty$$ e extensão em $$y\to\infty$$ recuperamos $$E=\sigma/(2\varepsilon_0)$$ (campo do plano infinito).
:::

---

## Exercício 3 — Campo elétrico no eixo de uma espira carregada

:::{solution}
**Dados.** Espira circular de raio $$a$$, carga total $$Q$$ distribuída uniformemente ao longo do fio (densidade linear $$\lambda = Q/(2\pi a)$$). Ponto $$P$$ no eixo perpendicular ao plano da espira, a distância $$z$$ do centro (origem).

**Solução.** Simetria implica que só a componente $$E_z$$ é não nula; componente radial cancela. Tomando elemento $$dq=\lambda a d\phi$$ em ângulo $$\phi$$, a distância ao ponto $$P$$ é $$r=\sqrt{a^2+z^2}$$ e a componente axial do campo é

$$
dE_z = \frac{1}{4\pi\varepsilon_0}\frac{dq}{r^2}\cos\alpha
= \frac{1}{4\pi\varepsilon_0}\frac{\lambda a\,d\phi}{a^2+z^2}\cdot\frac{z}{\sqrt{a^2+z^2}}.
$$

Integrando $$\phi\in[0,2\pi)$$:

$$
E_z(z)=\frac{1}{4\pi\varepsilon_0}\frac{\lambda a \, (2\pi) \, z}{(a^2+z^2)^{3/2}}
= \frac{1}{4\pi\varepsilon_0}\frac{Q z}{(a^2+z^2)^{3/2}}.
$$

Portanto

$$
\boxed{ \mathbf E(z) = \frac{Q z}{4\pi\varepsilon_0 (a^2+z^2)^{3/2}}\ \hat z. }
$$
:::

---

## Exercício 4 — Dipolo feito de duas linhas paralelas de cargas opostas (densidade $$\pm\lambda$$, separação $$d$$)

:::{solution}
**Configuração.** Linhas infinitas, paralelas ao eixo $$z$$, localizadas em $$x=\pm d/2$$, $$y=0$$. Densidades $$\lambda$$ (em $$x=+d/2$$) e $$-\lambda$$ (em $$x=-d/2$$). Problema efetivamente 2D (independência em $$z$$).

**(a) Potencial $$\phi(x,y)$$.** Potencial de uma linha infinita com densidade $$\lambda$$ em posição $$\mathbf r_0$$ é (escolhendo constante apropriada)

$$
\phi(\mathbf r)=\frac{\lambda}{2\pi\varepsilon_0}\ln\frac{1}{|\mathbf r-\mathbf r_0|}.
$$

Superpondo duas linhas com densidades opostas:

$$
\boxed{
\phi(x,y) = \frac{\lambda}{4\pi\varepsilon_0}\ln\!\frac{(x+d/2)^2+y^2}{(x-d/2)^2+y^2}.
}
$$

**(b) Potencial e campo para $$r\gg d$$.** Em coordenadas polares $$(r,\varphi)$$ centradas no meio das linhas, para $$r\gg d$$ expandimos:

$$
\phi(r,\varphi)\approx \frac{\lambda d}{2\pi\varepsilon_0}\,\frac{\cos\varphi}{r} + O\!\Big(\frac{d^3}{r^3}\Big).
$$

Então o potencial decai como $$1/r$$ (comportamento dipolar em 2D); o campo elétrico $$\mathbf E = -\nabla\phi$$ tem magnitude $$\sim (\lambda d)/(2\pi\varepsilon_0 r^2)$$ dirigida como um dipolo com orientação ao longo do eixo $$x$$.
:::

---

## Exercício 5 — Barra infinita com corrente uniforme exceto por cavidade cilíndrica *deslocada* (não coaxial)

:::{solution}
**Interpretação (hipótese).** Temos um cilindro infinito (eixo $$z$$) de condutor que transporta corrente total $$I$$ distribuída uniformemente em sua seção transversal, exceto por uma cavidade cilíndrica de raio $$a$$ cujo eixo é paralelo ao eixo do cilindro mas deslocado (vetor deslocamento $$\mathbf d$$ no plano transversal). Desejamos o campo magnético $$\mathbf B(\mathbf r)$$ em todo o espaço (regiões dentro da cavidade, no corpo do condutor e fora do condutor).

**Estratégia (método da superposição).** Considere:

- Um cilindro sólido cheio (centro original) com densidade de corrente volumétrica $$\mathbf J$$ (constante, ao longo de $$+\hat z$$). Esse sólido teria corrente total $$I$$ e produz campo conhecido.
- Subtrair um cilindro (o que corresponde à cavidade) com densidade de corrente volumétrica $$\mathbf J$$ (mesma magnitude, mas assumimos que na cavidade não existe corrente, então subtrai-se a contribuição do cilindro com densidade igual e sinal oposto — equivalentemente somamos um cilindro com densidade $$-\mathbf J$$ centrado na posição da cavidade).

A superposição produz o campo do corpo com cavidade: $$\mathbf B = \mathbf B_{\text{full}} + \mathbf B_{\text{missing}}$$, onde $$\mathbf B_{\text{missing}}$$ é o campo do cilindro de raio $$a$$ com densidade $$-\mathbf J$$ e centro deslocado por $$\mathbf d$$.

**Campo do cilindro sólido uniforme (fórmula conhecida).** Para um cilindro infinito com densidade constante $$\mathbf J=J\hat z$$:

- No interior do cilindro (distância radial $$r$$ ao centro original, $$r<R$$):
  $$
  \mathbf B_{\text{full}}(\mathbf r)=\frac{\mu_0 J}{2}\,(\hat z\times \mathbf r),
  $$
  ou em componentes polares $$B_\varphi=\dfrac{\mu_0 J r}{2}$$.
- No exterior ($$r\ge R$$):
  $$
  \mathbf B_{\text{full}}(\mathbf r)=\frac{\mu_0 I}{2\pi r}\,\hat\varphi
  =\frac{\mu_0 J \pi R^2}{2\pi r}\,\hat\varphi
  =\frac{\mu_0 J R^2}{2 r}\,\hat\varphi,
  $$
  que em forma vetorial pode ser escrita como $$\dfrac{\mu_0 J R^2}{2 r^2}\,(\hat z\times\mathbf r)$$.

**Campo do cilindro 'missing' (com centro $$\mathbf r_0=\mathbf d$$ e densidade $$-J$$).**

- Para um ponto $$\mathbf r$$ tal que $$|\mathbf r-\mathbf r_0| < a$$ (dentro do cilindro faltante), usamos a fórmula de campo interior (com densidade $$-J$$):
  $$
  \mathbf B_{\text{missing}}(\mathbf r)
  = -\frac{\mu_0 J}{2}\, \hat z \times (\mathbf r - \mathbf r_0).
  $$
- Para $$|\mathbf r-\mathbf r_0| \ge a$$ (fora do cilindro faltante), o campo do cilindro faltante equivale ao campo de uma linha de corrente total $$I_{\text{missing}} = J\pi a^2$$ localizada em $$\mathbf r_0$$:
  $$
  \mathbf B_{\text{missing}}(\mathbf r)
  = -\frac{\mu_0 J a^2}{2|\mathbf r-\mathbf r_0|^2}\,\hat z\times(\mathbf r-\mathbf r_0).
  $$
  (isto porque para o cilindro preenchido de raio $$a$$ e densidade $$J$$, o campo fora é $$\mu_0 J a^2/(2s)\,\hat\varphi_s$$, e escrevemos isso em forma vetorial.)

**Superposição: campo total $$\mathbf B(\mathbf r)$$.** Para qualquer ponto $$\mathbf r$$ no plano transversal:

$$
\boxed{
\mathbf B(\mathbf r) = \frac{\mu_0 J}{2}\,\hat z\times\mathbf r
\;+\;
\mathbf B_{\text{missing}}(\mathbf r),
}
$$
com $$\mathbf B_{\text{missing}}$$ dada por uma das fórmulas acima, dependendo se $$|\mathbf r-\mathbf r_0|$$ é $$<a$$ ou $$\ge a$$.

**Conclusões importantes e casos especiais**

- **Dentro da cavidade** ($$|\mathbf r-\mathbf r_0|<a$$): as duas contribuições lineares em $$\mathbf r$$ de fato se simplificam e o campo resultante é **uniforme**:

  $$
  \begin{aligned}
  \mathbf B(\mathbf r)
  &= \frac{\mu_0 J}{2}\,\hat z\times\mathbf r
     \;-\;\frac{\mu_0 J}{2}\,\hat z\times(\mathbf r-\mathbf r_0)\$$4pt]
  &= \frac{\mu_0 J}{2}\,\hat z\times\mathbf r_0,
  \end{aligned}
  $$

  isto é, uma **campo magnético uniforme** dentro da cavidade, com intensidade proporcional ao deslocamento $$\mathbf r_0$$ da cavidade em relação ao centro do cilindro cheio. (Resultado clássico: cavidade deslocada dentro de condutor com corrente produz campo uniforme na cavidade.)

- **Dentro do condutor, fora da cavidade** ($$|\mathbf r|<R$$ e $$|\mathbf r-\mathbf r_0|\ge a$$): aplica-se a superposição usando interior para o cilindro cheio e exterior para o cilindro faltante, obtendo uma expressão em termos de $$\hat z\times\mathbf r$$ e $$\hat z\times(\mathbf r-\mathbf r_0)$$ com coeficientes apropriados (ver fórmulas acima).

- **Fora do condutor** ($$|\mathbf r|>R$$): a corrente total encerrada é $$I$$, portanto longe do conjunto obtemos o campo de uma linha de corrente total $$I$$ centrada no centro do cilindro: $$\mathbf B=\dfrac{\mu_0 I}{2\pi r}\hat\varphi$$. A presença da cavidade deslocada altera o campo localmente, mas a corrente total não muda, então a expressão assintótica permanece a mesma.

**Observação prática.** As fórmulas acima são compactas e práticas: para cálculo numérico, avalie $$\mathbf B_{\text{missing}}$$ usando a expressão interna (linear) quando $$|\mathbf r-\mathbf r_0|<a$$ e a expressão externa (decai $$ \propto 1/|\mathbf r-\mathbf r_0|$$) caso contrário.
:::

---

## Exercício 6 — Barra condutora deslizando (motional EMF) — EMF e corrente fixa

:::{solution}
**Interpretações e hipóteses.** Barra condutora de comprimento $$L$$ desliza sem atrito sobre trilhos formando um circuito, em campo magnético uniforme $$\mathbf B=\!B\hat z$$ perpendicular ao plano do circuito (ou orientado de forma que a força sobre a barra seja tangencial ao deslocamento). Resistência total do circuito $$R$$. Supomos que a barra descreve um movimento prescrito $$x(t)=x_0\cos(\omega t)$$. Adotamos o regime **motional EMF** — a fem induzida é $$\mathcal E = -\dot\Phi$$. A corrente resultante é $$I(t)=\mathcal E(t)/R$$. O enunciado pede para determinar $$B$$ assumindo **corrente fixa conhecida** (ou relacionar $$B$$ a $$I$$).

**Fórmulas básicas.** Área varrida pelo circuito dependente de $$x(t)$$ é $$A(t)=L\,x(t)$$ (se $$L$$ é comprimento da barra e $$x$$ distância entre a barra e a referência). Fluxo magnético $$\Phi=B\,A(t)=B L x(t)$$.

Fem induzida:

$$
\mathcal E = -\dot\Phi = -B L \dot x(t).
$$

Corrente induzida (lei de Ohm):

$$
I(t)=\frac{\mathcal E}{R} = -\frac{B L}{R}\,\dot x(t).
$$

**Se a corrente imposta for $$I(t)=I_0\sin(\omega t)$$** (por exemplo), e o movimento $$x(t)=x_0\cos(\omega t)$$, então $$\dot x(t)=-x_0\omega\sin(\omega t)$$ e as dependências temporais coincidem (sinal apropriado). Igualando amplitudes:

$$
I_0 = \frac{B L}{R}\, x_0\omega
\quad\Longrightarrow\quad
\boxed{B = \frac{R I_0}{L x_0 \omega}.}
$$

Isto fornece o campo $$B$$ necessário para que o movimento $$x(t)=x_0\cos\omega t$$ gere a corrente $$I_0\sin\omega t$$ via motional EMF.

**Força magnética sobre a barra (amortecimento).** A corrente induzida gera força magnética sobre a barra de módulo

$$
F_B = I L B = -\frac{B^2 L^2}{R}\,\dot x(t),
$$

que é proporcional a $$\dot x$$ (força dissipativa amortecedora). Incluindo massa $$M$$ e (se houver) força restauradora $$ -K(x-x_{\rm eq})$$, a equação do movimento é

$$
M\ddot x + \frac{B^2 L^2}{R}\dot x + K(x-x_{\rm eq})=0.
$$

Sem força externa periódica essa equação descreve um oscilador amortecido (amplitude decrescente). Se desejamos uma oscilação permanente $$x(t)=x_0\cos\omega t$$ com corrente fixa, então é necessário que haja uma fonte que mantenha a corrente (ou uma fonte externa que compense a perda).
::: -->
