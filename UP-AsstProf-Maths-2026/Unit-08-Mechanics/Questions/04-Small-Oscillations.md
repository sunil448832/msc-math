# Unit 8 · Topic 04 — Theory of Small Oscillations
> Syllabus coverage: Theory of small oscillations (normal modes, frequencies from $\det(V - \omega^2T) = 0$, coupled pendula, normal coordinates)
> Cheatsheet: [../Cheatsheets/04-Small-Oscillations.md](../Cheatsheets/04-Small-Oscillations.md)

**Q1.** `[Concept]` ★ Near a stable equilibrium, $T = \tfrac12\dot{\mathbf q}^{T}\mathbf T\dot{\mathbf q}$ and $V = \tfrac12\mathbf q^{T}\mathbf V\mathbf q$. The normal-mode frequencies $\omega$ are given by

(A) $\det(\mathbf T - \omega^2\mathbf V) = 0$

(B) $\det(\mathbf V - \omega\thinspace \mathbf T) = 0$

(C) $\det(\mathbf V - \omega^2\mathbf T) = 0$

(D) $\det(\mathbf V\mathbf T - \omega^2\mathbf 1) = 0$ with $\mathbf V\mathbf T$ in that order

**Q2.** `[Concept]` ★ Two masses $m_1, m_2$ joined by a spring of constant $k$ move freely along a line. The angular frequency of the vibrational mode is

(A) $\sqrt{k(m_1 + m_2)/(m_1m_2)}$

(B) $\sqrt{k/(m_1 + m_2)}$

(C) $\sqrt{2k/(m_1 + m_2)}$

(D) $\sqrt{k/m_1} + \sqrt{k/m_2}$

**Q3.** `[Numerical]` ★ A particle of unit mass moves in the potential $V(x) = x^4 - 2x^2$. The angular frequency of small oscillations about either stable equilibrium is

(A) $2$

(B) $4$

(C) $\sqrt8/2$

(D) $2\sqrt2$

**Q4.** `[Numerical]` ★★ Two identical simple pendula (mass $m$, length $l$) are coupled by a light spring of stiffness $k$ attached to the bobs. The normal-mode angular frequencies are

(A) $\sqrt{g/l}$ and $\sqrt{g/l + k/m}$

(B) $\sqrt{g/l}$ and $\sqrt{g/l + 2k/m}$

(C) $\sqrt{g/l - k/m}$ and $\sqrt{g/l + k/m}$

(D) $\sqrt{g/l + k/m}$ and $\sqrt{g/l + 2k/m}$

**Q5.** `[Numerical]` ★★ A system has $T = \tfrac12(\dot q_1^2 + \dot q_2^2)$ and $V = \tfrac12(5q_1^2 + 8q_1q_2 + 5q_2^2)$. The normal coordinate that oscillates with angular frequency $3$ is proportional to

(A) $q_1 - q_2$

(B) $q_1 + 2q_2$

(C) $q_1 + q_2$

(D) $2q_1 - q_2$

**Q6.** `[Multi-Statement]` ★★ For small oscillations with $\mathbf T$ positive definite and $\mathbf V$ real symmetric, consider:

I. There is a real linear change of coordinates that diagonalises $\mathbf T$ and $\mathbf V$ simultaneously.

II. All roots $\omega^2$ of the frequency equation are real.

III. The normal-mode frequencies are always distinct.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** A free linear symmetric triatomic molecule (e.g. CO$`_2`$ modelled by masses on springs along a line) has a normal mode of zero frequency.
**Reason (R):** Its potential energy is unchanged when the whole molecule is translated rigidly along the line.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match each system with its small-oscillation angular frequency.

| List-I | List-II |
|---|---|
| a. Simple pendulum of length $l$ | 1. $\sqrt{3g/(4a)}$ |
| b. Mass $m$ on a spring of stiffness $k$ | 2. $\sqrt{g/l}$ |
| c. Uniform rod of length $2a$ pivoted at one end | 3. $\sqrt{gh/(K^2 + h^2)}$ |
| d. Compound pendulum, centre of mass at distance $h$ from the pivot, radius of gyration $K$ about G | 4. $\sqrt{k/m}$ |

(A) a-2, b-4, c-3, d-1

(B) a-2, b-4, c-1, d-3

(C) a-4, b-2, c-1, d-3

(D) a-2, b-1, c-4, d-3

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Small oscillations about an unstable equilibrium lead to a negative $\omega^2$, i.e. exponentially growing solutions.

(B) In a normal mode all coordinates oscillate with the same frequency.

(C) A system with $n$ degrees of freedom has $n$ normal modes (counting zero-frequency modes).

(D) In terms of normal coordinates the Lagrangian contains cross terms $\dot Q_i\dot Q_j$ with $i \ne j$.

**Q10.** `[Numerical]` ★★★ For a double pendulum with two equal masses $m$ and two equal lengths $l$, the normal-mode angular frequencies are

(A) $\sqrt{(2 \pm \sqrt2)\thinspace g/l}$

(B) $\sqrt{(1 \pm 1/\sqrt2)\thinspace g/l}$

(C) $\sqrt{g/l}$ and $\sqrt{3g/l}$

(D) $\sqrt{(3 \pm \sqrt2)\thinspace g/l}$

**Q11.** `[Application]` ★★★ Two weakly coupled identical pendula have normal-mode frequencies $\omega_1 = 10$ rad/s and $\omega_2 = 10.5$ rad/s. Pendulum 1 is displaced and released while pendulum 2 is at rest at equilibrium. The energy has transferred completely to pendulum 2 for the first time after

(A) $\pi/10$ s

(B) $\pi$ s

(C) $2\pi$ s

(D) $4\pi$ s

**Q12.** `[Application]` ★★★ A linear symmetric triatomic molecule has masses $m, M, m$ joined by springs of stiffness $k$. Its two non-zero normal-mode angular frequencies are

(A) $\sqrt{k/m}$ and $\sqrt{k/M}$

(B) $\sqrt{k/M}$ and $\sqrt{\dfrac{k}{M}\left(1 + \dfrac{2M}{m}\right)}$

(C) $\sqrt{2k/m}$ and $\sqrt{\dfrac{k}{m}\left(1 + \dfrac{m}{M}\right)}$

(D) $\sqrt{k/m}$ and $\sqrt{\dfrac{k}{m}\left(1 + \dfrac{2m}{M}\right)}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | A | Concept |
| 3 | D | Numerical |
| 4 | B | Numerical |
| 5 | C | Numerical |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | B | Match |
| 9 | D | NOT-true / Counterexample |
| 10 | A | Numerical |
| 11 | C | Application |
| 12 | D | Application |

## Solutions
**Q1 — (C).** Substituting $\mathbf q = \mathbf a\cos(\omega t - \delta)$ into $\mathbf T\ddot{\mathbf q} + \mathbf V\mathbf q = 0$ gives $(\mathbf V - \omega^2\mathbf T)\mathbf a = 0$. Option (A) gives $1/\omega^2$ instead, and (B) has the wrong power of $\omega$. (D) would be right only with $\mathbf T^{-1}\mathbf V$.

**Q2 — (A).** The relative coordinate obeys $\mu\ddot x = -kx$ with $\mu = m_1m_2/(m_1 + m_2)$, so $\omega = \sqrt{k/\mu}$. The other mode is the zero-frequency translation of the centre of mass.

**Q3 — (D).** $V' = 4x^3 - 4x = 0$ gives $x = 0, \pm1$. Then $V''(\pm1) = 12 - 4 = 8 \gt  0$, so these are stable, and $\omega = \sqrt{V''/m} = \sqrt8 = 2\sqrt2$. The origin is unstable ($V''(0) = -4$).

**Q4 — (B).** The in-phase mode leaves the spring unstretched, so $\omega_1 = \sqrt{g/l}$. In the antiphase mode each bob feels an extra force $2kx$, so $\omega_2^2 = g/l + 2k/m$. The spring stretches by $2x$, which is why (A) is wrong.

**Q5 — (C).** $`\mathbf V = \begin{pmatrix}5&4\cr 4&5\end{pmatrix}`$ has eigenvalue $9$ with eigenvector $(1,1)$ and eigenvalue $1$ with eigenvector $(1,-1)$. So $\omega = 3$ belongs to $Q \propto q_1 + q_2$, and $\omega = 1$ belongs to $q_1 - q_2$ (checked with sympy).

**Q6 — (B).** Simultaneous diagonalisation with $\mathbf T$ as the metric gives I and II. III is false: degeneracies occur, for example the isotropic 2-D oscillator, or the two bending modes of CO$`_2`$.

**Q7 — (A).** Translation invariance gives a neutral direction $\mathbf V\mathbf a = 0$ with $\mathbf a = (1,1,1)$. This is a root $\omega = 0$, the uniform translation. R is exactly the cause.

**Q8 — (B).** For the rod, $I = \tfrac13 M(2a)^2 = \tfrac43 Ma^2$ and $h = a$, so $\omega^2 = Mga/I = 3g/(4a)$. For the compound pendulum, $\omega^2 = Mgh/(M(K^2 + h^2))$.

**Q9 — (D).** Normal coordinates diagonalise both forms: $L = \tfrac12\sum(\dot Q_i^2 - \omega_i^2Q_i^2)$, with no cross terms. (A), (B) and (C) are true.

**Q10 — (A).** With $`\mathbf T = ml^2\begin{pmatrix}2&1\cr 1&1\end{pmatrix}`$ and $`\mathbf V = mgl\begin{pmatrix}2&0\cr 0&1\end{pmatrix}`$, the equation $\det(\mathbf V - \omega^2\mathbf T) = 0$ gives $\omega^2 = (2 \pm \sqrt2)\thinspace g/l$ (verified with sympy). Option (B) comes from forgetting the cross term in $\mathbf T$ or mis-scaling.

**Q11 — (C).** $x_1 = a\cos\dfrac{(\omega_2-\omega_1)t}{2}\cos\dfrac{(\omega_1+\omega_2)t}{2}$, so the amplitude of pendulum 1 first vanishes when $\dfrac{(\omega_2 - \omega_1)t}{2} = \dfrac{\pi}{2}$. That gives $t = \pi/\Delta\omega = \pi/0.5 = 2\pi$ s. The answer $4\pi$ s ($= 2\pi/\Delta\omega$) is the time for the energy to come back to pendulum 1.

**Q12 — (D).** The symmetric stretch (centre atom at rest) gives $\omega^2 = k/m$. The antisymmetric stretch gives $\omega^2 = \dfrac{k}{m}\left(1 + \dfrac{2m}{M}\right)$. Together with $\omega = 0$ (translation), these are the roots of $\det(\mathbf V - \omega^2\mathbf T) = 0$ (verified with sympy).
