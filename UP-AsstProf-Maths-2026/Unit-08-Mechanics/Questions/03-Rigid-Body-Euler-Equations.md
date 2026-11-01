# Unit 8 · Topic 03 — Rigid Body Dynamics and Euler's Equations
> Syllabus coverage: Euler's dynamical equations of motion of a rigid body (moments and products of inertia, principal axes, Euler's equations, torque-free motion)
> Cheatsheet: [../Cheatsheets/03-Rigid-Body-Euler-Equations.md](../Cheatsheets/03-Rigid-Body-Euler-Equations.md)

**Q1.** `[Concept]` ★ With $A, B, C$ the principal moments of inertia at a fixed point (or at the centre of mass) and $N_1, N_2, N_3$ the torque components along the principal axes, the first of Euler's dynamical equations is

(A) $A\dot\omega_1 - (B - C)\,\omega_2\omega_3 = N_1$

(B) $A\dot\omega_1 + (B - C)\,\omega_2\omega_3 = N_1$

(C) $A\dot\omega_1 - (B + C)\,\omega_2\omega_3 = N_1$

(D) $A\dot\omega_1 - (C - A)\,\omega_3\omega_1 = N_1$

**Q2.** `[Concept]` ★ The products of inertia of a body at a point all vanish when the coordinate axes are

(A) parallel to the axes through the centre of mass

(B) axes of zero moment of inertia

(C) any set of mutually perpendicular axes

(D) principal axes at that point

**Q3.** `[Numerical]` ★ A rigid body rotates with $\vec\omega = (1, 2, -1)$ referred to principal axes with principal moments $A = 2,\ B = 3,\ C = 4$ (consistent units). Its rotational kinetic energy is

(A) 6

(B) 18

(C) 12

(D) 9

**Q4.** `[Numerical]` ★★ The moment of inertia of a uniform solid cube of mass $M$ and edge $a$ about one of its edges is

(A) $\dfrac{Ma^2}{6}$

(B) $\dfrac{Ma^2}{3}$

(C) $\dfrac{2Ma^2}{3}$

(D) $\dfrac{5Ma^2}{12}$

**Q5.** `[Numerical]` ★★ The inertia tensor of a body at a point is $I = \begin{pmatrix}2 & -1 & 0\\ -1 & 2 & 0\\ 0 & 0 & 3\end{pmatrix}$. Its principal moments of inertia are

(A) $1, 2, 3$

(B) $1, 3, 3$

(C) $2, 2, 3$

(D) $1, 1, 3$

**Q6.** `[Multi-Statement]` ★★ Consider the following statements about a rigid body.

I. At every point of a rigid body there exist three mutually perpendicular principal axes.

II. Any two principal moments of inertia at a point add up to at least the third.

III. Products of inertia are always non-negative.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** In torque-free motion of a body with $A = B$, the component $\omega_3$ along the symmetry axis stays constant.
**Reason (R):** For torque-free motion Euler's third equation reads $C\dot\omega_3 = (A - B)\,\omega_1\omega_2$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match each body (mass $M$) with its moment of inertia.

| List-I | List-II |
|---|---|
| a. Thin uniform rod of length $2a$, about a perpendicular axis through its centre | 1. $\tfrac25 Ma^2$ |
| b. Uniform solid sphere of radius $a$, about a diameter | 2. $\tfrac14 Ma^2$ |
| c. Thin uniform spherical shell of radius $a$, about a diameter | 3. $\tfrac13 Ma^2$ |
| d. Uniform circular disc of radius $a$, about a diameter | 4. $\tfrac23 Ma^2$ |

(A) a-3, b-4, c-1, d-2

(B) a-2, b-1, c-4, d-3

(C) a-3, b-1, c-4, d-2

(D) a-3, b-1, c-2, d-4

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true for a rigid body rotating about a fixed point?

(A) $T = \tfrac12\,\vec\omega\cdot\mathbf I\,\vec\omega$

(B) The angular momentum $\vec L$ is always parallel to $\vec\omega$.

(C) For a uniform sphere, every axis through the centre is a principal axis.

(D) $I = I_G + Md^2$, where $I_G$ is about the parallel axis through the centre of mass.

**Q10.** `[Application]` ★★ A rigid body has principal moments of inertia $1, 2, 3$ (distinct). In torque-free motion, steady rotation is stable about

(A) all three principal axes

(B) only the axis of moment 3

(C) the axes of moments 1 and 3, but not 2

(D) the axis of moment 2 only

**Q11.** `[Application]` ★★★ The moment of inertia of a uniform solid cube of mass $M$ and edge $a$ about a body diagonal is

(A) $\dfrac{Ma^2}{6}$

(B) $\dfrac{Ma^2}{3}$

(C) $\dfrac{2Ma^2}{3}$

(D) $\dfrac{Ma^2}{2}$

**Q12.** `[Numerical]` ★★★ A torque-free body has principal moments $A = B = 1$, $C = 2$. Initially $\omega_1 = 1$, $\omega_2 = 0$, $\omega_3 = 1$. Then $\omega_2(t)$ equals

(A) $\cos t$

(B) $\sin t$

(C) $\sin 2t$

(D) $-\sin t$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | D | Concept |
| 3 | D | Numerical |
| 4 | C | Numerical |
| 5 | B | Numerical |
| 6 | D | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | C | Match |
| 9 | B | NOT-true / Counterexample |
| 10 | C | Application |
| 11 | A | Application |
| 12 | B | Numerical |

## Solutions
**Q1 — (A).** From $\dot{\vec L} + \vec\omega\times\vec L = \vec N$ in body axes, with $\vec L = (A\omega_1, B\omega_2, C\omega_3)$, the first component is $A\dot\omega_1 + (C - B)\omega_2\omega_3 = N_1$. This is the same as (A). Option (B) has the wrong sign of the cross term.

**Q2 — (D).** By definition, principal axes diagonalise the inertia tensor, so all products of inertia vanish. Central axes (A) need not be principal unless the body has suitable symmetry.

**Q3 — (D).** $T = \tfrac12(A\omega_1^2 + B\omega_2^2 + C\omega_3^2) = \tfrac12(2 + 12 + 4) = 9$. The answer 18 forgets the $\tfrac12$.

**Q4 — (C).** About a central axis parallel to an edge the moment is $\tfrac16 Ma^2$. The edge is at distance $a/\sqrt2$ from that axis, so the parallel-axis theorem gives $\tfrac16 Ma^2 + \tfrac12 Ma^2 = \tfrac23 Ma^2$.

**Q5 — (B).** The $2\times2$ block $\begin{pmatrix}2&-1\\-1&2\end{pmatrix}$ has eigenvalues $1$ and $3$, and the third moment is $3$. So the principal moments are $1, 3, 3$ (checked numerically). The trace is $7$, which rules out (A), (C) and (D).

**Q6 — (D).** I: the inertia tensor is real symmetric, so it has an orthonormal eigenbasis. II: $A + B - C = 2\int z^2\,dm \ge 0$ (equality for a lamina, which gives the perpendicular-axis theorem). III is false: $\int xy\,dm$ can have either sign.

**Q7 — (A).** Euler's third equation is $C\dot\omega_3 - (A - B)\omega_1\omega_2 = 0$. With $A = B$ the right side vanishes, so $\omega_3$ is constant. R gives exactly the reason.

**Q8 — (C).**
- Rod of length $2a$: $\tfrac{M(2a)^2}{12} = \tfrac13 Ma^2$.
- Solid sphere: $\tfrac25 Ma^2$.
- Spherical shell: $\tfrac23 Ma^2$.
- Disc about a diameter: $\tfrac14 Ma^2$ (it is $\tfrac12 Ma^2$ about the axis).

**Q9 — (B).** $\vec L = \mathbf I\vec\omega$ is parallel to $\vec\omega$ only when $\vec\omega$ lies along a principal axis (or the body is isotropic). A dumbbell rotating about an oblique axis is the standard counterexample. In (D) the axis must pass through **G**, and it does.

**Q10 — (C).** Linearising Euler's equations about rotation $\omega_0$ about axis 1 gives $\ddot\omega_2 = \dfrac{(C - A)(A - B)}{BC}\omega_0^2\,\omega_2$. This oscillates when $A$ is the largest or the smallest moment and grows when $A$ is intermediate. So the axes of maximum and minimum moment are stable and the intermediate axis is unstable (the tennis-racket theorem).

**Q11 — (A).** At the centre of a cube $A = B = C = \tfrac16 Ma^2$ with no products of inertia, so the momental ellipsoid is a sphere. Every line through the centre, including a body diagonal, therefore has moment $\tfrac16 Ma^2$. The answer $\tfrac23 Ma^2$ (about an edge) is the trap.

**Q12 — (B).** The equations are $\dot\omega_1 = (B - C)\omega_2\omega_3/A = -\omega_2$ and $\dot\omega_2 = (C - A)\omega_3\omega_1/B = \omega_1$, with $\omega_3 = 1$ constant. So $\omega_1 = \cos t$ and $\omega_2 = \sin t$, a precession at rate $\Omega = (C - A)\omega_3/A = 1$. Option (D) has the wrong sense of precession; that would be the answer for an oblate/prolate swap ($C < A$).
