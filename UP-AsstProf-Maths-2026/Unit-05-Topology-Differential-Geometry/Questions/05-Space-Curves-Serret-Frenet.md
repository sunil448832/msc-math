# Unit 5 · Topic 05 — Space Curves: Curvature, Torsion, Serret–Frenet Formulae
> Syllabus coverage: Space curves - their curvature and torsion, Serret-Frenet formulae
> Cheatsheet: [../Cheatsheets/05-Space-Curves-Serret-Frenet.md](../Cheatsheets/05-Space-Curves-Serret-Frenet.md)

*Convention: $`s`$ = arc length, $`(T,N,B)`$ = Frenet frame, $`B'=-\tau N`$.*

**Q1.** `[Numerical]` ★ For the circular helix $\mathbf r(t)=(a\cos t,\ a\sin t,\ bt)$ with $a\gt 0$, the curvature $\kappa$ and torsion $\tau$ are

(A) $\kappa=\dfrac1a,\ \tau=\dfrac1b$

(B) $\kappa=\dfrac{b}{a^2+b^2},\ \tau=\dfrac{a}{a^2+b^2}$

(C) $\kappa=\dfrac{a}{a^2+b^2},\ \tau=\dfrac{b}{a^2+b^2}$

(D) $\kappa=\dfrac{a}{\sqrt{a^2+b^2}},\ \tau=\dfrac{b}{\sqrt{a^2+b^2}}$

**Q2.** `[Numerical]` ★★ For the twisted cubic $\mathbf r(t)=(t,t^2,t^3)$, the curvature and torsion at $t=0$ are

(A) $\kappa=2,\ \tau=3$

(B) $\kappa=2,\ \tau=6$

(C) $\kappa=1,\ \tau=3$

(D) $\kappa=2,\ \tau=-3$

**Q3.** `[Concept]` ★ A regular space curve with nowhere-vanishing curvature is a plane curve if and only if

(A) its curvature is constant

(B) its torsion is identically zero

(C) $\kappa/\tau$ is constant

(D) its binormal is perpendicular to a fixed direction

**Q4.** `[Multi-Statement]` ★★ For a unit-speed curve with Frenet frame $`(T,N,B)`$, consider:

I. $T'=\kappa N$

II. $N'=-\kappa T+\tau B$

III. $B'=\tau N$

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★

**Assertion (A):** A space curve with constant curvature $\kappa\gt 0$ and torsion $\tau\equiv0$ is (part of) a circle of radius $1/\kappa$.

**Reason (R):** The curvature and torsion functions (with $\kappa\gt 0$) determine a curve uniquely up to a rigid motion.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match List-I with List-II.

| List-I | List-II |
|---|---|
| A. Osculating plane | 1. spanned by $T$ and $B$ |
| B. Normal plane | 2. spanned by $N$ and $B$ |
| C. Rectifying plane | 3. spanned by $T$ and $N$ |
| D. $dB/ds$ | 4. $-\tau N$ |

(A) A-3, B-1, C-2, D-4

(B) A-2, B-3, C-1, D-4

(C) A-3, B-2, C-1, D-4

(D) A-1, B-2, C-3, D-4

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following statements is NOT true?

(A) For a circular helix, $\kappa$ and $\tau$ are both constant.

(B) The tangent of a circular helix makes a constant angle with the axis.

(C) A curve (with $\kappa\ne0$) is a generalized helix if and only if $\kappa/\tau$ is constant.

(D) Every curve with $\kappa/\tau$ constant is a circular helix.

**Q8.** `[Numerical]` ★ The arc length of the helix $\mathbf r(t)=(\cos t,\sin t,t)$ from $t=0$ to $t=2\pi$ is

(A) $2\pi$

(B) $2\sqrt2\thinspace \pi$

(C) $4\pi$

(D) $\sqrt2\thinspace \pi$

**Q9.** `[Application]` ★★★ A unit-speed curve has constant curvature $\kappa=1$ and constant torsion $\tau=1$. Then it is a circular helix lying on a cylinder of radius

(A) $1$

(B) $\tfrac1{\sqrt2}$

(C) $\tfrac12$

(D) $2$

**Q10.** `[Numerical]` ★★★ For $\mathbf r(t)=(\cosh t,\ \sinh t,\ t)$, the curvature and torsion at $t=0$ are

(A) $\kappa=\tfrac1{\sqrt2},\ \tau=\tfrac1{\sqrt2}$

(B) $\kappa=\tfrac12,\ \tau=-\tfrac12$

(C) $\kappa=1,\ \tau=1$

(D) $\kappa=\tfrac12,\ \tau=\tfrac12$

**Q11.** `[Concept]` ★ The Serret–Frenet formulae can be written as $X'=\boldsymbol\omega\times X$ for $X\in\lbrace T,N,B\rbrace$. The Darboux vector is $\boldsymbol\omega=$

(A) $\kappa T+\tau B$

(B) $\kappa T-\tau B$

(C) $\tau N$

(D) $\tau T+\kappa B$

**Q12.** `[Application]` ★★★ For a unit-speed curve with curvature $\kappa\gt 0$ and torsion $\tau$, the curvature of its **tangent indicatrix** (the curve $s\mapsto T(s)$ on the unit sphere) is

(A) $\dfrac{\sqrt{\kappa^2+\tau^2}}{\kappa}$

(B) $\dfrac{\sqrt{\kappa^2+\tau^2}}{\tau}$

(C) $\dfrac{\kappa}{\tau}$

(D) $\sqrt{\kappa^2+\tau^2}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Numerical |
| 2 | A | Numerical |
| 3 | B | Concept |
| 4 | B | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | C | Match |
| 7 | D | NOT-true |
| 8 | B | Numerical |
| 9 | C | Application |
| 10 | D | Numerical |
| 11 | D | Concept |
| 12 | A | Application |

## Solutions
**Q1 — (C).** $|\mathbf r'|=\sqrt{a^2+b^2}=:c$ and $|\mathbf r'\times\mathbf r''|=ac$, so $\kappa=ac/c^3=a/c^2$. Also $(\mathbf r'\times\mathbf r'')\cdot\mathbf r'''=a^2b$, so $\tau=a^2b/(a^2c^2)=b/c^2$. Option (A) wrongly treats the helix as a circle of radius $a$ (that is only right when $b=0$).

**Q2 — (A).** At $0$: $\mathbf r'=(1,0,0)$, $\mathbf r''=(0,2,0)$, $\mathbf r'''=(0,0,6)$, and $\mathbf r'\times\mathbf r''=(0,0,2)$. So $\kappa=2/1=2$ and $\tau=\dfrac{(0,0,2)\cdot(0,0,6)}{|(0,0,2)|^2}=\dfrac{12}{4}=3$. Option (B) forgets to divide by $|\mathbf r'\times\mathbf r''|^2$.

**Q3 — (B).** $\tau=0\iff B'=0\iff B$ is constant, and then $(\mathbf r-\mathbf r_0)\cdot B$ is constant, so the curve lies in a plane. Option (D) is wrong because a planar curve has $B$ *constant*, i.e. *parallel* to a fixed direction. (C) characterises generalized helices.

**Q4 — (B).** The correct third formula is $`B'=-\tau N`$. You can derive it by differentiating $`B\cdot B=1`$ and $`B\cdot T=0`$.

**Q5 — (A).** A circle of radius $1/\kappa$ has curvature $\kappa$ and torsion $0$. By the fundamental theorem of curves (R), any curve with the same $\kappa,\tau$ is congruent to it, so R explains A.

**Q6 — (C).** Osculating plane $`=\langle T,N\rangle`$, normal plane $`=\langle N,B\rangle`$, rectifying plane $`=\langle T,B\rangle`$, and $`B'=-\tau N`$.

**Q7 — (D).** Lancret's theorem: $\kappa/\tau$ is constant $\iff$ generalized helix (the tangent makes a constant angle with a fixed direction). A generalized helix need not lie on a circular cylinder. Only when $\kappa$ and $\tau$ are **both** constant is it a circular helix.

**Q8 — (B).** $|\mathbf r'|=\sqrt{\sin^2t+\cos^2t+1}=\sqrt2$, so the length is $\sqrt2\cdot2\pi$.

**Q9 — (C).** For the helix in Q1, $a=\kappa/(\kappa^2+\tau^2)$ and $b=\tau/(\kappa^2+\tau^2)$. With $\kappa=\tau=1$ this gives radius $a=\tfrac12$. The value $1/\kappa=1$ is the circle radius, which is the trap.

**Q10 — (D).** $\mathbf r'=(\sinh t,\cosh t,1)$, $\mathbf r''=(\cosh t,\sinh t,0)$, $\mathbf r'''=(\sinh t,\cosh t,0)$, and $\mathbf r'\times\mathbf r''=(-\sinh t,\cosh t,-1)$. This gives $\kappa=\tau=\dfrac1{2\cosh^2t}$ for all $t$ (checked with sympy). At $t=0$ both equal $\tfrac12$. Since $\kappa/\tau\equiv1$, the curve is a generalized helix.

**Q11 — (D).** Check: $\boldsymbol\omega\times T=\kappa B\times T=\kappa N$ and $\boldsymbol\omega\times B=\tau T\times B=-\tau N$, which match $T'=\kappa N$ and $`B'=-\tau N`$. Also $|\boldsymbol\omega|=\sqrt{\kappa^2+\tau^2}$ (the total curvature).

**Q12 — (A).** Let $\sigma$ be the arc length of $T(s)$. Then $d\sigma/ds=\kappa$, and $dT/d\sigma=N$, so $d^2T/d\sigma^2=N'/\kappa=(-\kappa T+\tau B)/\kappa$. Its length is $\sqrt{\kappa^2+\tau^2}/\kappa$. Check with the helix: $T$ traces a circle of radius $a/c$ on $S^2$, whose curvature is $c/a=\sqrt{\kappa^2+\tau^2}/\kappa$.
