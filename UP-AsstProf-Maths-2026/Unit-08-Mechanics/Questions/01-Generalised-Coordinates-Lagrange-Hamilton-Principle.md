# Unit 8 · Topic 01 — Generalised Coordinates, Lagrange's Equations, Hamilton's Principle
> Syllabus coverage: Generalised coordinates, Lagrange's equations, Hamilton's variational principle (constraints, degrees of freedom, cyclic coordinates, conservation laws)
> Cheatsheet: [../Cheatsheets/01-Generalised-Coordinates-Lagrange-Hamilton-Principle.md](../Cheatsheets/01-Generalised-Coordinates-Lagrange-Hamilton-Principle.md)

**Q1.** `[Concept]` ★ The number of degrees of freedom of a rigid body moving freely in space is

(A) 3

(B) 5

(C) 6

(D) 9

**Q2.** `[Concept]` ★ A bead slides on a straight smooth wire that is made to rotate in a horizontal plane with constant angular velocity $\omega$ about a fixed vertical axis through one end. The constraint on the bead is

(A) holonomic and scleronomic

(B) holonomic and rheonomic

(C) non-holonomic and scleronomic

(D) non-holonomic and rheonomic

**Q3.** `[Concept]` ★ Two particles joined by a light rigid rod move in a plane. The number of degrees of freedom of the system is

(A) 2

(B) 5

(C) 4

(D) 3

**Q4.** `[Numerical]` ★ In a simple Atwood machine (light, frictionless pulley; inextensible string) the masses are $m_1 = 3$ kg and $m_2 = 1$ kg. Using the single generalised coordinate $x$ (the descent of $m_1$), Lagrange's equation gives the acceleration of $m_1$ as

(A) $g/4$

(B) $g/3$

(C) $3g/4$

(D) $g/2$

**Q5.** `[Numerical]` ★★ A particle moves in a plane under a force $\vec F = F_r\,\hat r + F_\theta\,\hat\theta$. The generalised force associated with the polar coordinate $\theta$ is

(A) $F_\theta$

(B) $r F_r$

(C) $F_\theta / r$

(D) $r F_\theta$

**Q6.** `[Multi-Statement]` ★★ Consider a system with Lagrangian $L(q,\dot q,t)$ and the Jacobi integral $h = \sum_j \dot q_j\,\dfrac{\partial L}{\partial \dot q_j} - L$.

I. If $\partial L/\partial t = 0$, then $h$ is a constant of motion.

II. $h$ always equals the total energy $T + V$.

III. Replacing $L$ by $L + \dfrac{dF(q,t)}{dt}$ leaves the equations of motion unchanged.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** For a charged particle in a magnetic field, the canonical momentum $\partial L/\partial \dot{\vec r}$ is not equal to $m\dot{\vec r}$.
**Reason (R):** The Lagrangian of a charged particle contains the velocity-dependent term $e\,\dot{\vec r}\cdot\vec A$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match List-I with List-II.

| List-I (Principle) | List-II (Statement) |
|---|---|
| a. Principle of virtual work | 1. $\delta\displaystyle\int_{t_1}^{t_2} L\,dt = 0$ with $\delta q(t_1)=\delta q(t_2)=0$ |
| b. D'Alembert's principle | 2. $\sum_i \vec F_i\cdot\delta\vec r_i = 0$ |
| c. Hamilton's principle | 3. $\dfrac{d}{dt}\dfrac{\partial L}{\partial \dot q_j} - \dfrac{\partial L}{\partial q_j} = 0$ |
| d. Lagrange's equations | 4. $\sum_i (\vec F_i - \dot{\vec p}_i)\cdot\delta\vec r_i = 0$ |

(A) a-2, b-4, c-1, d-3

(B) a-4, b-2, c-1, d-3

(C) a-2, b-4, c-3, d-1

(D) a-1, b-4, c-2, d-3

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following statements is NOT true?

(A) Lagrange's equations keep the same form under any point transformation $Q_j = Q_j(q,t)$.

(B) The Lagrangian of a system is uniquely determined by its equations of motion.

(C) The Lagrangians $L$ and $\lambda L$ ($\lambda$ a non-zero constant) give the same equations of motion.

(D) Generalised coordinates need not have the dimension of length.

**Q10.** `[Application]` ★★★ The Lagrangian $L = e^{\gamma t}\left(\tfrac12 m\dot q^2 - \tfrac12 k q^2\right)$, where $\gamma, m, k > 0$ are constants, describes

(A) a simple harmonic oscillator of frequency $\sqrt{k/m}$

(B) a damped oscillator $m\ddot q + \gamma m\dot q + kq = 0$

(C) a damped oscillator $m\ddot q + 2\gamma m\dot q + kq = 0$

(D) an oscillator with growing amplitude $m\ddot q - \gamma m\dot q + kq = 0$

**Q11.** `[Concept]` ★ Hamilton's principle applied to $\displaystyle\int_{x_1}^{x_2}\sqrt{1+y'^2}\,dx$ (the length of a plane curve) gives as extremals

(A) straight lines

(B) circles

(C) catenaries

(D) cycloids

**Q12.** `[Application]` ★★ Two particles of unit mass move on a line with Lagrangian $L = \tfrac12(\dot x^2 + \dot y^2) - V(x - y)$. Which quantity is necessarily conserved?

(A) $\dot x$

(B) $\dot x - \dot y$

(C) $\tfrac12\dot x^2 + V(x-y)$

(D) $\dot x + \dot y$

**Q13.** `[Application]` ★★★ A bead slides on a smooth circular hoop of radius $a$ which rotates with constant angular velocity $\omega$ about its vertical diameter. With $\theta$ measured from the downward vertical, $L = \tfrac12 m a^2(\dot\theta^2 + \omega^2\sin^2\theta) + mga\cos\theta$. If $\omega^2 = 2g/a$, the angular frequency of small oscillations about the stable equilibrium $\theta_0 \neq 0$ is

(A) $\sqrt{g/a}$

(B) $\sqrt{2g/a}$

(C) $\sqrt{3g/(2a)}$

(D) $\sqrt{g/(2a)}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Concept |
| 3 | D | Concept |
| 4 | D | Numerical |
| 5 | D | Numerical |
| 6 | C | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | A | Match |
| 9 | B | NOT-true / Counterexample |
| 10 | B | Application |
| 11 | A | Concept |
| 12 | D | Application |
| 13 | C | Application |

## Solutions
**Q1 — (C).** Three coordinates fix the position of the centre of mass and three angles (for example the Euler angles) fix the orientation. The distractor 9 comes from counting the nine direction cosines, which are tied together by 6 orthogonality relations.

**Q2 — (B).** The constraint can be written as an equation $y\cos\omega t - x\sin\omega t = 0$ between the coordinates, so it is holonomic. That equation contains $t$ explicitly, so it is rheonomic. "Scleronomic" would need a fixed wire.

**Q3 — (D).** Two particles in a plane have $2\times 2 = 4$ coordinates, and the rod gives one holonomic constraint $|\vec r_1 - \vec r_2| = \ell$. So there are $4 - 1 = 3$ degrees of freedom (the centre $x, y$ and an angle). The answer 5 is the count for the same system in 3-D ($6-1$).

**Q4 — (D).** $T = \tfrac12(m_1+m_2)\dot x^2$ and $V = -m_1 g x + m_2 g x$. Lagrange's equation gives $(m_1+m_2)\ddot x = (m_1-m_2)g$, so $\ddot x = \tfrac{2}{4}g = g/2$.

**Q5 — (D).** $Q_\theta = \vec F\cdot\partial\vec r/\partial\theta$ and $\partial\vec r/\partial\theta = r\hat\theta$, so $Q_\theta = rF_\theta$, which is the torque. A generalised force need not have the dimension of force, so (A) is wrong.

**Q6 — (C).** I: $dh/dt = -\partial L/\partial t$, so I is true. II is false: $h = T+V$ only when $T$ is a homogeneous quadratic in $\dot q$ (scleronomic constraints) and $V$ does not depend on velocity. For the rotating hoop of Q13, $h = T_2 - T_0 + V \ne T + V$. III is the gauge invariance of $L$, which is true.

**Q7 — (A).** $L = \tfrac12 m\dot{\vec r}^2 - e\phi + e\dot{\vec r}\cdot\vec A$, so $\vec p = m\dot{\vec r} + e\vec A$. The velocity-dependent term is exactly what makes $\vec p$ differ from $m\dot{\vec r}$, so R explains A.

**Q8 — (A).** Virtual work (statics) is $\sum \vec F\cdot\delta\vec r = 0$. D'Alembert adds the inertial "force" $-\dot{\vec p}$. Hamilton's principle is the stationary action $\delta\int L\,dt = 0$. The Euler–Lagrange form is Lagrange's equations.

**Q9 — (B).** The Lagrangian is not unique. $L$ and $L + dF/dt$, and also $L$ and $\lambda L$, give the same equations. (A), (C) and (D) are standard true facts.

**Q10 — (B).** $\dfrac{d}{dt}\left(e^{\gamma t} m\dot q\right) = -e^{\gamma t} k q$. Expanding gives $e^{\gamma t}(m\ddot q + \gamma m\dot q + kq) = 0$. This is the Caldirola–Kanai Lagrangian. The factor 2 in (C) is a common slip; it appears only if one writes $e^{2\gamma t}$.

**Q11 — (A).** $F = \sqrt{1+y'^2}$ does not contain $y$, so $\partial F/\partial y' = y'/\sqrt{1+y'^2} = $ const. Hence $y' = $ const and the extremals are straight lines. Cycloids answer the brachistochrone problem and catenaries answer the minimum surface of revolution.

**Q12 — (D).** Change to $u = x - y$ and $s = x + y$. Then $L = \tfrac14(\dot u^2 + \dot s^2) - V(u)$ and $s$ is cyclic. Equivalently, $\dot p_x + \dot p_y = -V' + V' = 0$, so the total momentum $\dot x + \dot y$ is conserved (translation invariance). Option (C) leaves out the kinetic energy of $y$; the conserved energy is $\tfrac12(\dot x^2+\dot y^2)+V$.

**Q13 — (C).** The equation of motion is $\ddot\theta = \sin\theta\,(\omega^2\cos\theta - g/a)$, so equilibrium needs $\cos\theta_0 = g/(a\omega^2) = 1/2$. Linearising about $\theta_0$ gives $\ddot\eta = -\omega^2\sin^2\theta_0\,\eta$. So $\Omega^2 = \omega^2\sin^2\theta_0 = (2g/a)(3/4) = 3g/(2a)$. (A non-trivial equilibrium exists only if $\omega^2 > g/a$.)
