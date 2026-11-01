# Unit 8 · Topic 06 — Fluid Dynamics: Euler's Equation, Two-dimensional Flows, Motion of a Sphere
> Syllabus coverage: Euler's equation of motion for perfect fluid, Two-dimensional fluid motion, complex potential, source and sink, doublets, motion of sphere in perfect fluid (Bernoulli, vortex, image systems, Milne-Thomson circle theorem, Blasius)
> Cheatsheet: [../Cheatsheets/06-Fluid-Dynamics-Euler-Equation-2D-Flows-Sphere.md](../Cheatsheets/06-Fluid-Dynamics-Euler-Equation-2D-Flows-Sphere.md)

**Q1.** `[Concept]` ★ Euler's equation of motion for a perfect (inviscid) fluid with body force $\vec F$ per unit mass is

(A) $\dfrac{D\vec q}{Dt} = \vec F - \dfrac1\rho\nabla p$

(B) $\dfrac{\partial\vec q}{\partial t} = \vec F - \rho\nabla p$

(C) $\dfrac{D\vec q}{Dt} = \vec F + \dfrac1\rho\nabla p + \nu\nabla^2\vec q$

(D) $\dfrac{D\rho}{Dt} + \rho\nabla\cdot\vec q = 0$

**Q2.** `[Concept]` ★ Kelvin's circulation theorem says that, for an inviscid barotropic fluid under conservative body forces, the circulation round a closed curve moving with the fluid

(A) increases linearly with time

(B) remains constant in time

(C) is always zero

(D) is proportional to the kinetic energy

**Q3.** `[Numerical]` ★ Water flows out of a small orifice $5$ m below the free surface of a large open tank. Taking $g = 9.8$ m/s², the speed of efflux is approximately

(A) $7.0$ m/s

(B) $9.9$ m/s

(C) $49$ m/s

(D) $98$ m/s

**Q4.** `[Numerical]` ★★ For the two-dimensional flow with complex potential $w = z^2$, the speed of the fluid at $z = 1 + i$ is

(A) $2$

(B) $\sqrt2$

(C) $2\sqrt2$

(D) $4$

**Q5.** `[Concept]` ★★ The streamlines of the flow with complex potential $w = \mu/z$ ($\mu$ real, $\mu \ne 0$) are

(A) circles through the origin, with centres on the $y$-axis (touching the $x$-axis at $O$)

(B) circles through the origin, with centres on the $x$-axis (touching the $y$-axis at $O$)

(C) concentric circles about the origin

(D) straight lines through the origin

**Q6.** `[Numerical]` ★★ A uniform stream of speed $U$ along the $x$-axis flows past a two-dimensional source at the origin which emits volume $Q$ per unit time per unit length. The stagnation point is at

(A) $x = Q/(2\pi U)$

(B) $x = -U/(2\pi Q)$

(C) $x = -Q/(4\pi U)$

(D) $x = -Q/(2\pi U)$

**Q7.** `[Multi-Statement]` ★★ Consider the following statements about image systems in two-dimensional irrotational flow.

I. If the motion is steady and irrotational under conservative forces, Bernoulli's constant is the same throughout the fluid.

II. The image of a line source in a rigid plane wall is an equal source at the mirror-image point.

III. The image of a line source outside the circular cylinder $|z| = a$ is just an equal source at the inverse point $a^2/\bar z_0$.

Which of the above is/are correct?

(A) I and II only

(B) II only

(C) II and III only

(D) I, II and III

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** The complex potential $w = ik\log z$ ($k$ real) represents a line vortex at the origin.
**Reason (R):** For a line vortex the streamlines are radial lines through the vortex.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match each complex potential (constants $U, m, \mu, k$ real) with the flow it represents.

| List-I | List-II |
|---|---|
| a. $w = Uz$ | 1. Line vortex |
| b. $w = m\log z$ | 2. Doublet (dipole) |
| c. $w = \mu/z$ | 3. Uniform stream |
| d. $w = ik\log z$ | 4. Line source or sink |

(A) a-3, b-4, c-2, d-1

(B) a-3, b-2, c-4, d-1

(C) a-4, b-3, c-2, d-1

(D) a-3, b-4, c-1, d-2

**Q10.** `[NOT-true / Counterexample]` ★★ For a solid sphere of radius $a$ moving with constant velocity $U$ through an infinite perfect fluid of density $\rho$ that is at rest at infinity, which statement is NOT true?

(A) The velocity potential is $\phi = \dfrac{Ua^3}{2r^2}\cos\theta$ (with $\vec q = -\nabla\phi$, $\theta$ measured from the direction of motion).

(B) The kinetic energy of the fluid is $\tfrac13\pi\rho a^3U^2$.

(C) The virtual (added) mass is half the mass of the fluid displaced.

(D) The sphere experiences a drag force proportional to $U^2$.

**Q11.** `[Application]` ★★★ A small spherical air bubble (density negligible compared with the liquid) is released from rest in a perfect liquid. Ignoring viscosity and change of size, its initial upward acceleration is

(A) $g$

(B) $2g$

(C) $g/2$

(D) $3g$

**Q12.** `[Application]` ★★★ In uniform flow $U$ past a fixed circular cylinder $|z| = a$ (no circulation), $w = U\left(z + \dfrac{a^2}{z}\right)$. The surface pressure equals the pressure $p_\infty$ at infinity at the points where the polar angle $\theta$ (from the upstream direction or the downstream direction) is

(A) $\theta = 45^\circ$

(B) $\theta = 60^\circ$

(C) $\theta = 30^\circ$

(D) $\theta = 90^\circ$

**Q13.** `[Application]` ★★ A long circular cylinder with circulation $\Gamma = 3$ m²/s about it is held fixed in a uniform stream of water ($\rho = 1000$ kg/m³) with speed $U = 2$ m/s. By the Blasius theorem (Kutta–Joukowski), the force on the cylinder per unit length is

(A) zero, by d'Alembert's paradox

(B) $3000$ N/m, along the stream

(C) $12000$ N/m, perpendicular to the stream

(D) $6000$ N/m, perpendicular to the stream

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | B | Concept |
| 3 | B | Numerical |
| 4 | C | Numerical |
| 5 | A | Concept |
| 6 | D | Numerical |
| 7 | A | Multi-Statement |
| 8 | C | Assertion-Reason |
| 9 | A | Match |
| 10 | D | NOT-true / Counterexample |
| 11 | B | Application |
| 12 | C | Application |
| 13 | D | Application |

## Solutions
**Q1 — (A).** This is Newton's second law for a fluid element with only the pressure force $-\nabla p$ per unit volume and the body force. (C) is Navier–Stokes with a sign error, and (D) is the continuity equation.

**Q2 — (B).** $\dfrac{D\Gamma}{Dt} = \oint\dfrac{D\vec q}{Dt}\cdot d\vec r + \oint\vec q\cdot d\vec q = 0$ under these hypotheses. A corollary is Lagrange's theorem: once irrotational, always irrotational.

**Q3 — (B).** By Torricelli, $v = \sqrt{2gh} = \sqrt{98} \approx 9.9$ m/s. Option (D) is $2gh$ without the square root.

**Q4 — (C).** $q = |dw/dz| = |2z| = 2|1+i| = 2\sqrt2$. The complex velocity is $u - iv = dw/dz$ (up to the sign convention), and its modulus is the speed.

**Q5 — (A).** $w = \mu\dfrac{x - iy}{x^2+y^2}$, so $\psi = -\dfrac{\mu y}{x^2+y^2}$. Setting $\psi =$ const gives $x^2 + y^2 + \lambda y = 0$: circles through $O$ with centres on the $y$-axis, tangent to the $x$-axis (the doublet axis). Option (B) describes the equipotentials ($\phi =$ const).

**Q6 — (D).** On the axis $u = U + \dfrac{Q}{2\pi x}$. Setting $u = 0$ gives $x = -Q/(2\pi U)$, which is upstream. Option (A) is on the wrong side: downstream both velocities point the same way. This is the Rankine half-body.

**Q7 — (A).** I: for irrotational flow, Bernoulli holds between **any** two points. II is true by symmetry, because the wall is a streamline. III is false: by the Milne-Thomson circle theorem the image is a source at the inverse point **plus an equal sink at the centre**, so that no net flux leaves the cylinder.

**Q8 — (C).** $w = ik\log z = ik(\ln r + i\theta)$ gives $\phi = -k\theta$ and $\psi = k\ln r$. The streamlines $\psi =$ const are **circles**, and the circulation is $\mp2\pi k$, so this is a vortex and A is true. R is false: radial streamlines belong to a source.

**Q9 — (A).** These are the standard elementary complex potentials. The signs depend on convention, but the types are fixed.

**Q10 — (D).** By d'Alembert's paradox, uniform motion through a perfect fluid gives **no** drag. The kinetic energy is $\tfrac12 M'U^2$ with $M' = \tfrac12\cdot\tfrac43\pi a^3\rho$, which gives (B) and (C). (A) is the standard potential, which satisfies $-\partial\phi/\partial r = U\cos\theta$ at $r = a$.

**Q11 — (B).** For a sphere of density $\sigma$, $\left(\sigma + \tfrac12\rho\right)V\dot U = (\rho - \sigma)Vg$, so the upward acceleration is $\dfrac{\rho - \sigma}{\sigma + \rho/2}\thinspace g$. With $\sigma \to 0$ this is $2g$. Answering $g$ or "infinite" ignores the added mass.

**Q12 — (C).** On $r = a$ the speed is $q = 2U|\sin\theta|$. Bernoulli gives $p = p_\infty + \tfrac12\rho U^2(1 - 4\sin^2\theta)$, which equals $p_\infty$ when $\sin^2\theta = \tfrac14$, i.e. at $\theta = 30^\circ$ (and $150^\circ$, $210^\circ$, $330^\circ$). At $90^\circ$ the pressure is minimum, $p_\infty - \tfrac32\rho U^2$.

**Q13 — (D).** Blasius' theorem $X - iY = \dfrac{i\rho}{2}\displaystyle\oint\left(\dfrac{dw}{dz}\right)^2dz$ applied to $w = U\left(z + \dfrac{a^2}{z}\right) + \dfrac{i\Gamma}{2\pi}\log z$ gives no drag and a lift $\rho U\Gamma = 1000\times2\times3 = 6000$ N/m, perpendicular to the stream (the Magnus effect). d'Alembert's paradox (A) kills only the drag; with circulation there is a lift.
