# Cheatsheet · Unit 8 · Topic 04 — Theory of Small Oscillations
> Questions: [../Questions/04-Small-Oscillations.md](../Questions/04-Small-Oscillations.md)

## 1. Set-up
- **Equilibrium:** $\partial V/\partial q_i = 0$ at $q = q^0$.
- **Stability (Lagrange–Dirichlet):** if $V$ has a strict local **minimum**, the equilibrium is stable. In one dimension, $V''(q_0) \gt  0$ means stable.
- Expand about equilibrium in $\eta = q - q^0$, for a scleronomic system:
```math
T = \tfrac12\sum T_{ij}\dot\eta_i\dot\eta_j,\qquad V = \tfrac12\sum V_{ij}\eta_i\eta_j,\qquad V_{ij} = \left.\frac{\partial^2V}{\partial q_i\partial q_j}\right|_0 .
```
  Here $T_{ij}$ is evaluated at equilibrium and is symmetric positive definite; $V_{ij}$ is symmetric.
- **Equations of motion:** $\mathbf T\ddot{\boldsymbol\eta} + \mathbf V\boldsymbol\eta = 0$.

## 2. Normal modes
- Try $\boldsymbol\eta = \mathbf a\thinspace e^{i\omega t}$. This gives $(\mathbf V - \omega^2\mathbf T)\mathbf a = 0$.
- **Secular (frequency) equation:**
$$\boxed{\det(\mathbf V - \omega^2\mathbf T) = 0}$$
  This is a degree-$`n`$ equation in $`\omega^2`$ with $`n`$ real roots (since $`\mathbf T \gt  0`$).
  - $\omega^2 \gt  0$: oscillation.
  - $\omega^2 = 0$: neutral or free motion, e.g. translation or rotation (a "zero mode").
  - $\omega^2 \lt  0$: instability (exponential growth).
- **Orthogonality:** $\mathbf a_k^{T}\mathbf T\mathbf a_l = \delta_{kl}$ (normalised) and $\mathbf a_k^{T}\mathbf V\mathbf a_l = \omega_k^2\delta_{kl}$. This holds even for degenerate roots, after a suitable choice of vectors.
- **Normal coordinates:** $\boldsymbol\eta = \mathbf A\mathbf Q$ with $\mathbf A = [\mathbf a_1\cdots\mathbf a_n]$. Then
$$L = \tfrac12\sum_k(\dot Q_k^2 - \omega_k^2Q_k^2),$$
  with **no cross terms**, so each $Q_k = C_k\cos(\omega_kt + \delta_k)$.
- In a single normal mode **all** coordinates oscillate with the same frequency, in phase or antiphase. A general motion is a superposition of the modes.
- The number of modes equals the number of degrees of freedom $`n`$. The modes can be degenerate (repeated $`\omega`$).
- **Rayleigh's principle:** $\omega_{\min}^2 \le \dfrac{\mathbf a^{T}\mathbf V\mathbf a}{\mathbf a^{T}\mathbf T\mathbf a} \le \omega_{\max}^2$. Adding a constraint raises the lowest frequency (or leaves it unchanged); adding stiffness raises the frequencies.

## 3. Standard systems
| System | Frequencies $\omega$ | Modes |
|---|---|---|
| 1-D potential $`V(x)`$, mass $`m`$ | $`\sqrt{V''(x_0)/m}`$ | — |
| Two masses with one spring (free) | $0,\ \sqrt{k/\mu}$ with $\mu = \dfrac{m_1m_2}{m_1+m_2}$ | translation, stretch |
| Two identical pendula with a coupling spring $k$ | $\sqrt{g/l},\ \sqrt{g/l + 2k/m}$ | in-phase $\theta_1 + \theta_2$, antiphase $\theta_1 - \theta_2$ |
| Two masses and three equal springs between walls | $\sqrt{k/m},\ \sqrt{3k/m}$ | $(1,1)$, $(1,-1)$ |
| Double pendulum (equal $`m`$, equal $`l`$) | $`\sqrt{(2\mp\sqrt2)\thinspace g/l}`$ | amplitude ratios $`\theta_2/\theta_1 = \pm\sqrt2`$ (lower frequency: $`+\sqrt2`$, in phase) |
| Linear triatomic molecule $`m`$–$`M`$–$`m`$ | $`0,\ \sqrt{k/m},\ \sqrt{\dfrac km\left(1 + \dfrac{2m}{M}\right)}`$ | translation, symmetric stretch (centre at rest), antisymmetric stretch |
| $`n`$ equal masses on a stretched string (tension $\tau$, spacing $a$, fixed ends) | $\omega_r = 2\sqrt{\dfrac{\tau}{ma}}\sin\dfrac{r\pi}{2(n+1)}$ | sine modes |
| Compound pendulum | $\sqrt{gh/(K^2 + h^2)}$ | equivalent length $(K^2 + h^2)/h$ |
| Rod of length $2a$ pivoted at one end | $\sqrt{3g/(4a)}$ | — |
| Bead on a hoop rotating at $\omega$ (about $\theta_0 \ne 0$) | $\omega\sin\theta_0$ | — |

### Quick algorithm for a $2\times2$ case with $\mathbf T = \mathbf 1$
For $`\mathbf V = \begin{pmatrix}a & b\cr  b & a\end{pmatrix}`$: $\omega^2 = a \pm b$, with normal coordinates $q_1 + q_2$ for $a + b$ and $q_1 - q_2$ for $a - b$.

## 4. Beats and energy transfer (weak coupling)
- With pendulum 1 displaced and pendulum 2 at rest:
  - $\theta_1 = \theta_0\cos\dfrac{\Delta\omega\thinspace t}{2}\cos\bar\omega t$
  - $\theta_2 = \theta_0\sin\dfrac{\Delta\omega\thinspace t}{2}\sin\bar\omega t$
- The energy has transferred completely to pendulum 2 at $t = \pi/\Delta\omega$. It returns to pendulum 1 after $2\pi/\Delta\omega$ (the beat period).

## 5. Forced and damped (for reference)
- Forced: $\ddot Q_k + \omega_k^2Q_k = F_k(t)$ in normal coordinates, with resonance at $\omega = \omega_k$.
- Damped: Rayleigh dissipation function $\mathcal F = \tfrac12\dot{\boldsymbol\eta}^{T}\mathbf F\dot{\boldsymbol\eta}$. A single equation decouples only if $\mathbf F$ is simultaneously diagonalisable with $\mathbf T$ and $\mathbf V$.

## Exam traps
- The equation is $\det(\mathbf V - \omega^2\mathbf T)$, **not** $\det(\mathbf T - \omega^2\mathbf V)$ (that gives $1/\omega^2$), and the power is $\omega^2$, not $\omega$.
- With a spring between the bobs, the antiphase stretch is $2x$, which gives $2k/m$, not $k/m$.
- Zero-frequency modes come from translation or rotation invariance. Count them in "number of modes".
- Normal frequencies can be degenerate.
- $`T_{ij}`$ must be evaluated **at equilibrium**: drop $q$-dependence in $T$ at quadratic order.
- Stability needs $V$ to be a minimum, not merely stationary; at a maximum $\omega^2 \lt  0$.
- The full energy-transfer time is $\pi/\Delta\omega$, not $2\pi/\Delta\omega$.
