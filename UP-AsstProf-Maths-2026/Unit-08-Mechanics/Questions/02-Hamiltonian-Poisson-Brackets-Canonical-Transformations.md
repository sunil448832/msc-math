# Unit 8 · Topic 02 — Hamiltonian, Poisson Brackets, Canonical Transformations
> Syllabus coverage: Hamilton's canonical equations, Poisson bracket, Canonical transformations (Legendre transform, PB properties / Jacobi identity, generating functions, conditions for canonicity)
> Cheatsheet: [../Cheatsheets/02-Hamiltonian-Poisson-Brackets-Canonical-Transformations.md](../Cheatsheets/02-Hamiltonian-Poisson-Brackets-Canonical-Transformations.md)

**Q1.** `[Concept]` ★ Hamilton's canonical equations of motion are

(A) $\dot q = -\dfrac{\partial H}{\partial p},\ \dot p = \dfrac{\partial H}{\partial q}$

(B) $\dot q = \dfrac{\partial H}{\partial p},\ \dot p = -\dfrac{\partial H}{\partial q}$

(C) $\dot q = \dfrac{\partial H}{\partial q},\ \dot p = -\dfrac{\partial H}{\partial p}$

(D) $\dot q = \dfrac{\partial L}{\partial p},\ \dot p = \dfrac{\partial L}{\partial q}$

**Q2.** `[Concept]` ★ If the Lagrangian depends explicitly on time, then $\partial H/\partial t$ equals

(A) $-\partial L/\partial t$

(B) $\partial L/\partial t$

(C) $0$

(D) $dL/dt$

**Q3.** `[Numerical]` ★ For a particle of mass $m$ in a plane with $L = \tfrac12 m(\dot r^2 + r^2\dot\theta^2) - V(r)$, the Hamiltonian is

(A) $\dfrac{p_r^2}{2m} + \dfrac{p_\theta^2}{2m} + V(r)$

(B) $\dfrac{p_r^2}{2m} + \dfrac{r^2 p_\theta^2}{2m} - V(r)$

(C) $\dfrac{p_r^2}{2m} + \dfrac{p_\theta^2}{2mr^2} + V(r)$

(D) $\dfrac{p_r^2}{2m} + \dfrac{p_\theta^2}{2mr^2} - V(r)$

**Q4.** `[Numerical]` ★★ For a particle of charge $e$ and mass $m$ with $L = \tfrac12 m\dot{\vec r}^{\thinspace 2} + e\thinspace \dot{\vec r}\cdot\vec A - e\phi$, the Hamiltonian is

(A) $\dfrac{p^2}{2m} + e\phi$

(B) $\dfrac{(\vec p + e\vec A)^2}{2m} + e\phi$

(C) $\dfrac{(\vec p - e\vec A)^2}{2m} + e\phi$

(D) $\dfrac{(\vec p - e\vec A)^2}{2m} - e\phi$

**Q5.** `[Numerical]` ★ With $L_x, L_y, L_z$ the components of $\vec L = \vec r\times\vec p$, the Poisson bracket $\lbrace L_x, L_y\rbrace$ is

(A) $0$

(B) $L^2$

(C) $-L_z$

(D) $L_z$

**Q6.** `[Numerical]` ★★ The transformation $Q = q^{\alpha}\cos(\beta p)$, $P = q^{\alpha}\sin(\beta p)$ is canonical for

(A) $\alpha = 2,\ \beta = 1/2$

(B) $\alpha = 1,\ \beta = 1$

(C) $\alpha = 1/2,\ \beta = 2$

(D) $\alpha = 1/2,\ \beta = 1/2$

**Q7.** `[Multi-Statement]` ★★ Consider the following statements.

I. $\lbrace q_i, p_j\rbrace  = \delta_{ij}$ and $\lbrace q_i, q_j\rbrace  = \lbrace p_i, p_j\rbrace  = 0$.

II. If $f$ and $g$ are constants of motion (with no explicit $t$-dependence), so is $\lbrace f, g\rbrace$.

III. The Hamiltonian is always a constant of motion.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** The transformation $Q = p$, $P = q$ is canonical.
**Reason (R):** The transformation simply interchanges the roles of coordinate and momentum.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match each type of generating function with its transformation equations.

| List-I | List-II |
|---|---|
| a. $F_1(q,Q,t)$ | 1. $p = \dfrac{\partial F}{\partial q},\ Q = \dfrac{\partial F}{\partial P}$ |
| b. $F_2(q,P,t)$ | 2. $q = -\dfrac{\partial F}{\partial p},\ Q = \dfrac{\partial F}{\partial P}$ |
| c. $F_3(p,Q,t)$ | 3. $p = \dfrac{\partial F}{\partial q},\ P = -\dfrac{\partial F}{\partial Q}$ |
| d. $F_4(p,P,t)$ | 4. $q = -\dfrac{\partial F}{\partial p},\ P = -\dfrac{\partial F}{\partial Q}$ |

(A) a-1, b-3, c-4, d-2

(B) a-3, b-1, c-4, d-2

(C) a-3, b-1, c-2, d-4

(D) a-4, b-1, c-3, d-2

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) $F_2 = \sum_i q_iP_i$ generates the identity transformation.

(B) $F_1 = \sum_i q_iQ_i$ generates $Q_i = p_i,\ P_i = -q_i$.

(C) The Hamiltonian always equals the total energy $T + V$.

(D) Canonical transformations preserve phase-space volume.

**Q11.** `[Application]` ★★ For the oscillator $H = \dfrac{p^2}{2m} + \dfrac12 m\omega^2q^2$, use the canonical transformation $q = \sqrt{\dfrac{2P}{m\omega}}\sin Q$, $p = \sqrt{2Pm\omega}\cos Q$. The new Hamiltonian $K(Q,P)$ and the motion of $Q$ are

(A) $K = \omega P$; $Q = \omega t + \text{const}$

(B) $K = P^2/2m$; $Q = Pt/m + \text{const}$

(C) $K = \omega P$; $Q = \text{const}$

(D) $K = m\omega^2 P$; $Q = \omega t + \text{const}$

**Q12.** `[Application]` ★★★ For a particle (Hamiltonian with no explicit time dependence) it is known that $L_x$ and $L_y$ are constants of motion. Then

(A) $L_z$ need not be conserved

(B) $L_x^2 + L_y^2$ is conserved but $L_z$ need not be

(C) $L_z$ is conserved only if the force is central

(D) $L_z$ is also conserved

**Q13.** `[Numerical]` ★★★ For $\vec L = \vec r\times\vec p$, the Poisson bracket $\lbrace x, L_z\rbrace$ equals

(A) $-y$

(B) $y$

(C) $p_y$

(D) $0$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | A | Concept |
| 3 | C | Numerical |
| 4 | C | Numerical |
| 5 | D | Numerical |
| 6 | C | Numerical |
| 7 | B | Multi-Statement |
| 8 | D | Assertion-Reason |
| 9 | B | Match |
| 10 | C | NOT-true / Counterexample |
| 11 | A | Application |
| 12 | D | Application |
| 13 | A | Numerical |

## Solutions
**Q1 — (B).** $H = \sum p\dot q - L$. Compare $dH = \sum(\dot q\thinspace dp - \dot p\thinspace dq) - \dfrac{\partial L}{\partial t}dt$ with Lagrange's equation $\dot p = \partial L/\partial q$.

**Q2 — (A).** The same Legendre-transform differential gives $\partial H/\partial t = -\partial L/\partial t$. Also $dH/dt = \partial H/\partial t$ along the motion.

**Q3 — (C).** $p_r = m\dot r$ and $p_\theta = mr^2\dot\theta$. Since $T$ is quadratic and the system is scleronomic, $H = T + V$. Writing it in terms of momenta gives $p_\theta^2/(2mr^2)$. In (A) the $r^2$ is missing; in (D) the sign of $V$ is wrong.

**Q4 — (C).** $\vec p = m\dot{\vec r} + e\vec A$, so $m\dot{\vec r} = \vec p - e\vec A$. Then $H = \vec p\cdot\dot{\vec r} - L = \tfrac12 m\dot r^2 + e\phi = (\vec p - e\vec A)^2/2m + e\phi$. The sign inside the bracket is the usual trap.

**Q5 — (D).** $\lbrace L_x, L_y\rbrace  = L_z$ (cyclic), which is the classical analogue of $[L_x, L_y] = i\hbar L_z$. Checked symbolically: $\lbrace L_x,L_y\rbrace  = xp_y - yp_x$.

**Q6 — (C).** $\lbrace Q,P\rbrace _{q,p} = \alpha\beta\thinspace q^{2\alpha-1}(\cos^2\beta p + \sin^2\beta p) = \alpha\beta\thinspace q^{2\alpha-1}$. This equals 1 identically iff $2\alpha - 1 = 0$ and $\alpha\beta = 1$, so $\alpha = 1/2$, $\beta = 2$. Option (D) gives $\lbrace Q,P\rbrace  = 1/4$.

**Q7 — (B).** I gives the fundamental brackets. II is Poisson's theorem, which follows from the Jacobi identity. III is false: $dH/dt = \partial H/\partial t$, so $H$ is not conserved when it depends explicitly on $t$ (for example a driven oscillator).

**Q8 — (D).** $\lbrace Q,P\rbrace  = \lbrace p,q\rbrace  = -1 \ne 1$, so A is false. R is a true description of the map. The correct exchange transformation is $Q = p,\ P = -q$ (or $Q = -p,\ P = q$).

**Q9 — (B).** The four standard types:
- $F_1$: $p = \partial_q F_1,\ P = -\partial_Q F_1$
- $F_2$: $p = \partial_q F_2,\ Q = \partial_P F_2$
- $F_3$: $q = -\partial_p F_3,\ P = -\partial_Q F_3$
- $F_4$: $q = -\partial_p F_4,\ Q = \partial_P F_4$

**Q10 — (C).** (A): $p = \partial F_2/\partial q = P$ and $Q = \partial F_2/\partial P = q$, so it is the identity. (B): $p = Q$ and $P = -q$, so it is true. (D) is Liouville's theorem (the Jacobian of a canonical map is 1). (C) is false: $H = T + V$ needs scleronomic constraints and a velocity-independent $V$. For example, for a charged particle $H$ is not given by $p^2/2m + V$, and in a rotating frame $H \ne E$.

**Q11 — (A).** Substituting gives $K = P\omega(\cos^2Q + \sin^2Q) = \omega P$, and one checks $\lbrace q,p\rbrace _{Q,P} = 1$. Then $\dot Q = \partial K/\partial P = \omega$ and $\dot P = 0$. This is the action–angle form. Option (C) confuses $Q$ with the conserved $P$.

**Q12 — (D).** By Poisson's theorem, $\lbrace L_x, L_y\rbrace  = L_z$ is a constant of motion because $L_x$ and $L_y$ are. If two components of $\vec L$ are conserved, so is the third. (C) adds an unnecessary hypothesis.

**Q13 — (A).** $L_z = xp_y - yp_x$. Then $\lbrace x, L_z\rbrace  = \dfrac{\partial x}{\partial x}\dfrac{\partial L_z}{\partial p_x} = -y$. The answer $+y$ is $\lbrace L_z, x\rbrace$, the bracket with the order reversed (antisymmetry).
