# Alguns Exercícios sobre Equações Diferenciais Parciais

## Delta de Dirac

### Definição em 1D

A função delta de Dirac é uma **distribuição generalizada** que satisfaz:
$$
\int_{-\infty}^{\infty} \delta(x) f(x)\, dx = f(0).
$$

Propriedades fundamentais:

- **Localização:** $\delta(x) = 0$ para $x \neq 0$.
- **Normalização:** $\int_{-\infty}^{\infty} \delta(x)\, dx = 1$.
- **Translação:** $\delta(x-a)$ seleciona o valor da função em $a$.

---

### Generalização para D dimensões

No espaço $\mathbb{R}^D$:
$$
\int_{\mathbb{R}^D} \delta^{(D)}(\vec{r}) f(\vec{r})\, d^D r = f(\vec{0}).
$$

Em coordenadas esféricas/hiperesféricas:
$$
d^D r = r^{D-1} dr\, d\Omega_{D-1}, \quad
\delta^{(D)}(\vec{r}) = \frac{\delta(r)}{r^{D-1} S_{D-1}},
$$
onde
$$
S_{D-1} = \frac{2\pi^{D/2}}{\Gamma(D/2)}
$$
é a área da esfera unitária em $\mathbb{R}^D$.

---

### Propriedades adicionais importantes

- **Escalonamento do argumento:**

$$
\delta(ax) = \frac{1}{|a|}\delta(x), \quad a \in \mathbb{R}\setminus\{0\}.
$$

- **Derivada da delta:**

$$
\int_{-\infty}^{\infty} \delta'(x) f(x)\, dx = - f'(0).
$$
Mais geralmente:
$$
\int \delta^{(n)}(x) f(x)\, dx = (-1)^n f^{(n)}(0).
$$

---

### Exercícios

```{exercise} **Sequência delta gaussiana**  
   Mostre que
   $$
   \delta_\epsilon(x) = \frac{1}{\sqrt{\pi}\epsilon} e^{-x^2/\epsilon^2}
   $$
   converge para $\delta(x)$ quando $\epsilon \to 0$.
```

```{exercise} **Transformação para coordenadas esféricas**  
   Partindo de
   $\delta^{(3)}(\vec{r}) = \delta(x)\delta(y)\delta(z)$,
   derive a forma em coordenadas esféricas.
```

```{exercise} **Integral de teste em 3D**  
   Verifique que:
   $$
   \int_{\mathbb{R}^3} \delta^{(3)}(\vec{r}) e^{-r^2}\, d^3r = 1.
   $$
```

```{exercise} **Generalização para $D$ dimensões**  

   Prove que:
   $$
   \int_0^\infty \delta(r) g(r) r^{D-1}\, dr = g(0).
   $$
```

```{exercise} **Escalonamento**  
   Calcule:
   $$
   \int_{-\infty}^\infty \delta(3x) f(x)\, dx.
   $$
   Compare o resultado com $\int \delta(x) f(x)\, dx$.

```

```{exercise} **Delta em argumento geral**  
   Mostre que:
   $$
   \delta(g(x)) = \sum_i \frac{\delta(x-x_i)}{|g'(x_i)|},
   $$
   onde $x_i$ são as raízes simples de $g(x)$.  
   Aplique para $g(x) = x^2 - a^2$.
```

```{exercise} **Derivada da delta**  
   Verifique que:
   $$
   \int_{-\infty}^\infty \delta'(x) \, e^{ikx}\, dx = -ik.
   $$
```

```{exercise} **Generalização**  
   Mostre que:
   $$
   \int \delta^{(n)}(x) f(x)\, dx = (-1)^n f^{(n)}(0).
   $$
```

---

### Aplicação em eletromagnetismo

Mostre que a equação de Poisson para uma carga pontual:
$$
\nabla^2 \left(\frac{1}{r}\right) = -4\pi \delta^{(3)}(\vec{r}),
$$
é consistente com a definição da delta em coordenadas esféricas.

## Funções de Green e solução da equação de Poisson

A equação fundamental:
$$
\nabla^2 G(\vec{r},\vec{r}') = -\delta^{(D)}(\vec{r}-\vec{r}')
$$

### Casos particulares

- **Em 3D:**

$$
G(\vec{r},\vec{r}') = -\frac{1}{4\pi |\vec{r}-\vec{r}'|}
$$

- **Em 2D:**

$$
G(\vec{r},\vec{r}') = \frac{1}{2\pi} \ln |\vec{r}-\vec{r}'|
$$

- **Em D dimensões (D ≥ 3):**

$$
G(\vec{r},\vec{r}') = \frac{1}{(2-D)\, S_{D-1}} \, \frac{1}{|\vec{r}-\vec{r}'|^{D-2}}
$$
onde $S_{D-1} = \frac{2\pi^{D/2}}{\Gamma(D/2)}$.

---

### 2. Solução da equação de Poisson

A equação de Poisson:
$$
\nabla^2 \phi(\vec{r}) = -\rho(\vec{r})
$$

possui solução formal via convolução:
$$
\phi(\vec{r}) = \int G(\vec{r},\vec{r}') \, \rho(\vec{r}') \, d^D r'
$$

---

### 3. Problema separável como Sturm–Liouville

O operador de Laplace em coordenadas esféricas permite separação de variáveis:
$$
\nabla^2 \phi(r,\theta,\varphi) =
\frac{1}{r^2}\frac{\partial}{\partial r}\!\left(r^2 \frac{\partial \phi}{\partial r}\right)
- \frac{1}{r^2 \sin\theta}\frac{\partial}{\partial \theta}\!\left(\sin\theta \frac{\partial \phi}{\partial \theta}\right)
- \frac{1}{r^2 \sin^2\theta} \frac{\partial^2 \phi}{\partial \varphi^2}
$$

A parte angular obedece a uma equação de Sturm–Liouville:
$$
\frac{1}{\sin\theta} \frac{d}{d\theta}\left(\sin\theta \frac{d\Theta}{d\theta}\right)
- \left[\ell(\ell+1) - \frac{m^2}{\sin^2\theta}\right]\Theta = 0
$$

---

### 4. Ortogonalidade dos autovetores

Os autovalores $\ell(\ell+1)$ geram autovetores que são os **harmônicos esféricos**:
$$
Y_\ell^m(\theta,\varphi) = N \, P_\ell^m(\cos\theta) \, e^{im\varphi}
$$

Ortogonalidade:
$$
\int_{S^2} Y_\ell^m(\theta,\varphi)\, Y_{\ell'}^{m'*}(\theta,\varphi)\, d\Omega = \delta_{\ell\ell'}\delta_{mm'}
$$

---

### 5. Polinômios de Legendre

#### Função geratriz

$$
\frac{1}{\sqrt{1 - 2xt + t^2}} = \sum_{\ell=0}^\infty P_\ell(x)\, t^\ell
$$

#### Fórmula de Rodrigues

$$
P_\ell(x) = \frac{1}{2^\ell \ell!} \frac{d^\ell}{dx^\ell} \left[ (x^2-1)^\ell \right]
$$

#### Ortogonalidade

$$
\int_{-1}^1 P_\ell(x) P_m(x)\, dx = \frac{2}{2\ell+1} \delta_{\ell m}
$$

---

#### Exercícios

```{exercise} **Green em 3D**  
   Verifique que $G(\vec{r},\vec{r}') = -1/(4\pi|\vec{r}-\vec{r}'|)$ satisfaz a equação fundamental do Laplaciano.
```

```{exercise} **Comparação entre 2D e 3D**  
   Mostre que em 2D o logaritmo surge como limite do caso $D \to 2$ da expressão geral.
```

```{exercise} **Expansão multipolar**  
   Expanda
   $$
   \frac{1}{|\vec{r}-\vec{r}'|}
   $$
   em série de Legendre, assumindo $r>r'$.
```

```{exercise} **Sturm–Liouville**  
   Mostre explicitamente que a equação diferencial para $\Theta(\theta)$ é de Sturm–Liouville e deduza a condição de ortogonalidade.
```

```{exercise} **Rodrigues**  
   Use a fórmula de Rodrigues para calcular $P_0(x), P_1(x), P_2(x), P_3(x)$.
```

```{exercise} **Função geratriz**  
   A partir da função geratriz, derive uma relação de recorrência entre $P_\ell(x)$.
```

```{exercise} **Ortogonalidade**  
   Verifique numericamente a ortogonalidade de $P_2(x)$ e $P_3(x)$.
```

## Equação de onda não homogênea e potenciais retardado/avançado

Consideremos a equação de onda escalar em $d=3$ dimensões:

$$
\left(\frac{1}{c^2}\frac{\partial^2}{\partial t^2} - \nabla^2 \right) \psi(\mathbf{r},t) = S(\mathbf{r},t),
$$

onde $S(\mathbf{r},t)$ é a fonte.

### Função de Green

Definimos a função de Green $G(\mathbf{r},t)$ como solução da equação

$$
\left(\frac{1}{c^2}\frac{\partial^2}{\partial t^2} - \nabla^2 \right) G(\mathbf{r},t) = \delta(\mathbf{r}) \, \delta(t).
$$

No espaço-tempo 3+1, duas soluções relevantes aparecem:

- **Função de Green retardada:**

$$
G_{\text{ret}}(\mathbf{r},t) = \frac{\delta\!\left(t - \tfrac{|\mathbf{r}|}{c}\right)}{4\pi |\mathbf{r}|} \, \Theta(t),
$$

- **Função de Green avançada:**

$$
G_{\text{adv}}(\mathbf{r},t) = \frac{\delta\!\left(t + \tfrac{|\mathbf{r}|}{c}\right)}{4\pi |\mathbf{r}|} \, \Theta(-t).
$$

Aqui, $\Theta$ é a função de Heaviside.

### Solução geral

A solução da equação de onda é então escrita como a convolução:

$$
\psi(\mathbf{r},t) = \int d^3 r' \, dt' \, G(\mathbf{r}-\mathbf{r}', t-t') \, S(\mathbf{r}',t').
$$

Escolhendo $G = G_{\text{ret}}$, obtemos a solução física **retardada**:

$$
\psi(\mathbf{r},t) = \frac{1}{4\pi} \int d^3 r' \, \frac{S\!\left(\mathbf{r}', \, t - \tfrac{|\mathbf{r}-\mathbf{r}'|}{c}\right)}{|\mathbf{r}-\mathbf{r}'|}.
$$

De forma análoga, usando $G_{\text{adv}}$, obtemos a solução **avançada**, dependente de valores futuros da fonte.

---

### Exercícios

```{exercise} **Verificação direta:**

 Mostre que $G_{\text{ret}}$ satisfaz a equação da função de Green.
```

```{exercise} **Interpretação física:**
Explique por que $G_{\text{adv}}$ não é usado na eletrodinâmica clássica, mas pode aparecer em formulações de absorção (Wheeler–Feynman).
```

```{exercise} **Redução a 1D:**

Encontre a função de Green retardada da equação de onda em 1+1 dimensões.

```

```{exercise} **Aplicação**
Resolva a equação de onda com uma fonte pontual oscilante
   $$
   S(\mathbf{r},t) = \delta(\mathbf{r}) \cos(\omega t).
   $$
```

---
