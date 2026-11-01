# Unit 8 · Topic 05 — Fluid Kinematics: Continuity, Velocity Potential, Stream Lines, Vorticity
> Syllabus coverage: Equation of continuity in fluid motion, Velocity potential, Stream lines, Vorticity (Lagrangian/Eulerian descriptions, irrotational flow, pathlines, stream function)
> Cheatsheet: [../Cheatsheets/05-Fluid-Kinematics-Continuity-Potential-Vorticity.md](../Cheatsheets/05-Fluid-Kinematics-Continuity-Potential-Vorticity.md)

**Q1.** `[Concept]` ★ The equation of continuity $\dfrac{\partial\rho}{\partial t} + \nabla\cdot(\rho\vec q) = 0$ expresses conservation of

(A) mass

(B) momentum

(C) energy

(D) vorticity

**Q2.** `[Numerical]` ★ Which of the following velocity fields $(u, v)$ represents a possible two-dimensional motion of an incompressible fluid?

(A) $(x^2,\ y^2)$

(B) $(xy,\ xy)$

(C) $(x,\ 2y)$

(D) $(x + y,\ x - y)$

**Q3.** `[Numerical]` ★ The vorticity of the two-dimensional flow $u = -\Omega y,\ v = \Omega x$ (rigid rotation) is

(A) $\Omega$

(B) $0$

(C) $2\Omega$

(D) $\Omega/2$

**Q4.** `[Numerical]` ★★ The streamlines of the steady flow $u = x,\ v = -y$ are

(A) straight lines through the origin

(B) circles $x^2 + y^2 = c$

(C) rectangular hyperbolas $xy = c$

(D) rectangular hyperbolas $x^2 - y^2 = c$

**Q5.** `[Numerical]` ★★ For the steady flow $\vec q = (x, -y, 0)$, the magnitude of the fluid acceleration at the point $(1, 1, 0)$ is

(A) $0$

(B) $1$

(C) $2$

(D) $\sqrt2$

**Q6.** `[Multi-Statement]` ★★ Consider the following statements.

I. In steady flow, streamlines and pathlines coincide.

II. Two streamlines can cross at a point where the velocity is non-zero.

III. If a flow is irrotational in a simply connected region, a single-valued velocity potential exists there.

Which of the above is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** The flow $u = -\dfrac{y}{x^2 + y^2},\ v = \dfrac{x}{x^2 + y^2}$ is irrotational everywhere except at the origin.
**Reason (R):** The circulation of this flow round the unit circle $x^2 + y^2 = 1$ equals $2\pi$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match each situation with the appropriate form of the equation of continuity ($\vec q$ is the velocity).

| List-I | List-II |
|---|---|
| a. Lagrangian form | 1. $\dfrac{\partial\rho}{\partial t} + \dfrac{1}{r^2}\dfrac{\partial}{\partial r}(r^2\rho q_r) = 0$ |
| b. Spherically symmetric radial flow | 2. $\dfrac{\partial\rho}{\partial t} + \dfrac1r\dfrac{\partial}{\partial r}(r\rho q_r) = 0$ |
| c. Cylindrically symmetric (axial-independent) radial flow | 3. $\rho\,J = \rho_0$, $J = \dfrac{\partial(x,y,z)}{\partial(a,b,c)}$ |
| d. Incompressible fluid | 4. $\nabla\cdot\vec q = 0$ |

(A) a-3, b-2, c-1, d-4

(B) a-4, b-1, c-2, d-3

(C) a-3, b-1, c-2, d-4

(D) a-1, b-3, c-2, d-4

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Every irrotational flow is incompressible.

(B) The material derivative is $\dfrac{D}{Dt} = \dfrac{\partial}{\partial t} + \vec q\cdot\nabla$.

(C) The Lagrangian method follows the history of individual fluid particles.

(D) For an incompressible fluid with velocity potential $\phi$, $\nabla^2\phi = 0$.

**Q10.** `[Application]` ★★★ Consider the velocity field
$$u = -\frac{2xyz}{(x^2+y^2)^2},\qquad v = \frac{(x^2 - y^2)z}{(x^2+y^2)^2},\qquad w = \frac{y}{x^2+y^2}.$$
Then

(A) it is a possible motion of an incompressible fluid and the motion is irrotational

(B) it is a possible motion of an incompressible fluid but the motion is rotational

(C) it is not a possible motion of an incompressible fluid

(D) it is irrotational but violates the equation of continuity

**Q11.** `[Numerical]` ★★ A two-dimensional incompressible flow has stream function $\psi = x^2 - y^2$. The speed of the fluid at the point $(1, 2)$ is

(A) $\sqrt5$

(B) $2\sqrt5$

(C) $3$

(D) $5$

**Q12.** `[Application]` ★★ An incompressible fluid flows radially and steadily in three dimensions with velocity $q_r = f(r)$ (spherical symmetry, away from the origin). Then $f(r)$ is proportional to

(A) $r$

(B) $1/r$

(C) $1/r^3$

(D) $1/r^2$

**Q13.** `[Application]` ★★★ For the unsteady two-dimensional flow $u = \dfrac{x}{1+t},\ v = 1$, the pathline of the particle that is at $(1, 0)$ at time $t = 0$ is

(A) $x = e^{y}$

(B) $x = 1 + y$

(C) $x = 1 + y^2$

(D) $y = \ln x$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | D | Numerical |
| 3 | C | Numerical |
| 4 | C | Numerical |
| 5 | D | Numerical |
| 6 | B | Multi-Statement |
| 7 | B | Assertion-Reason |
| 8 | C | Match |
| 9 | A | NOT-true / Counterexample |
| 10 | A | Application |
| 11 | B | Numerical |
| 12 | D | Application |
| 13 | B | Application |

## Solutions
**Q1 — (A).** It is the differential form of $\dfrac{d}{dt}\displaystyle\int_V\rho\,dV = -\oint\rho\,\vec q\cdot d\vec S$, i.e. conservation of mass.

**Q2 — (D).** Incompressibility needs $\partial u/\partial x + \partial v/\partial y = 0$. For (D), $1 - 1 = 0$. The others give $2x + 2y$, $y + x$ and $3$.

**Q3 — (C).** $\zeta = \partial v/\partial x - \partial u/\partial y = \Omega + \Omega = 2\Omega$. The vorticity is twice the local angular velocity, so the answer $\Omega$ is the trap.

**Q4 — (C).** $\dfrac{dx}{x} = \dfrac{dy}{-y}$ gives $\ln x = -\ln y + c$, so $xy = c$. The hyperbolas $x^2 - y^2 = c$ are the equipotentials (with $\phi \propto x^2 - y^2$), which are orthogonal to the streamlines.

**Q5 — (D).** $\vec a = (\vec q\cdot\nabla)\vec q = (u\,u_x,\ v\,v_y) = (x,\ y)$. At $(1,1)$, $|\vec a| = \sqrt2$. The flow is steady, but the acceleration is not zero (A), because the convective part survives.

**Q6 — (B).** I is true: in steady flow a particle stays on its streamline. II is false: at a crossing point the velocity would have two directions, so crossings occur only at stagnation points or singularities. III is true: $\nabla\times\vec q = 0$ on a simply connected domain gives $\vec q = -\nabla\phi$ with $\phi$ single-valued.

**Q7 — (B).** $\partial v/\partial x - \partial u/\partial y = \dfrac{y^2 - x^2}{r^4} + \dfrac{x^2 - y^2}{r^4} = 0$ for $r \ne 0$, so A is true. The circulation is $\displaystyle\int_0^{2\pi}(\sin^2\theta + \cos^2\theta)\,d\theta = 2\pi$, so R is true. But a non-zero circulation round the origin does not explain irrotationality away from it. It only shows that the potential $\phi = -\theta$ is many-valued (the region is not simply connected).

**Q8 — (C).** The Lagrangian form is $\rho J = \rho_0$. The spherical divergence carries $r^2$ and the cylindrical one carries $r$. Incompressible flow means $\nabla\cdot\vec q = 0$.

**Q9 — (A).** The potential flow $\vec q = (x, y)$ (with $\phi = -\tfrac12(x^2 + y^2)$) is irrotational, but $\nabla\cdot\vec q = 2 \ne 0$. (D) is true because $\nabla\cdot\vec q = -\nabla^2\phi = 0$ (with either sign convention).

**Q10 — (A).** A direct calculation gives $\nabla\cdot\vec q = 0$ and $\nabla\times\vec q = \vec 0$ (verified with sympy). So the motion is possible and irrotational. This is a textbook classic; the field is $-\nabla\phi$ with $\phi = \dfrac{yz}{x^2+y^2}$ up to sign.

**Q11 — (B).** In either sign convention, speed $= |\nabla\psi| = \sqrt{(2x)^2 + (2y)^2} = 2\sqrt{x^2 + y^2} = 2\sqrt5$. The answer $\sqrt5$ forgets the factor 2.

**Q12 — (D).** The continuity equation $\dfrac{1}{r^2}\dfrac{d}{dr}(r^2f) = 0$ gives $r^2f = $ const. Equivalently, the flux through every sphere $4\pi r^2f$ is the same. The answer $1/r$ is the 2-D (cylindrical) result.

**Q13 — (B).** The pathline equations are $\dfrac{dx}{dt} = \dfrac{x}{1+t}$, giving $x = 1 + t$, and $\dfrac{dy}{dt} = 1$, giving $y = t$. Eliminating $t$ gives $x = 1 + y$. The trap (A)/(D): $x = e^{y}$ is the **streamline** through $(1,0)$ at $t = 0$, from $\dfrac{dx}{x} = \dfrac{dy}{1+t}$ with $t$ frozen at 0. In unsteady flow pathlines and streamlines differ.
