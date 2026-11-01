# Unit 4 · Topic 05 — Conformal Mappings and Möbius Transformations
> Syllabus coverage: Conformal mappings, Mobius transformations (incl. fixed points, cross ratio, mappings of half-plane and disc, classification, standard elementary maps)
> Cheatsheet: [../Cheatsheets/05-Conformal-Mappings-Mobius-Transformations.md](../Cheatsheets/05-Conformal-Mappings-Mobius-Transformations.md)

**Q1.** `[Concept]` ★ A Möbius transformation is uniquely determined by the images of

(A) one point and the derivative there

(B) two distinct points

(C) four distinct points

(D) three distinct points

**Q2.** `[Numerical]` ★ The fixed points of $w = \dfrac{z-1}{z+1}$ are

(A) $\pm 1$

(B) $\pm i$

(C) $0$ and $\infty$

(D) $1$ only

**Q3.** `[Concept]` ★ The map $w = \bar z$

(A) is conformal everywhere

(B) preserves the magnitudes of angles but reverses their orientation, so it is not conformal

(C) preserves neither the magnitude nor the orientation of angles

(D) is conformal everywhere except at $z = 0$

**Q4.** `[Numerical]` ★★ The Möbius transformation that maps $1,\ i,\ -1$ to $0,\ 1,\ \infty$ respectively is

(A) $w = i\thinspace \dfrac{1-z}{1+z}$

(B) $w = \dfrac{z-1}{z+1}$

(C) $w = i\thinspace \dfrac{z-1}{z+1}$

(D) $w = -i\thinspace \dfrac{1+z}{1-z}$

**Q5.** `[Numerical]` ★★ The image of the circle $|z| = 1$ under $w = \dfrac{z+1}{z-1}$ is

(A) the circle $|w| = 1$

(B) the real axis

(C) the imaginary axis

(D) the line $\operatorname{Re} w = 1$

**Q6.** `[Numerical]` ★★ With the cross ratio defined as $(z_1,z_2,z_3,z_4) = \dfrac{(z_1-z_3)(z_2-z_4)}{(z_1-z_4)(z_2-z_3)}$, the value of $(0,\thinspace 1,\thinspace -1,\thinspace i)$ is

(A) $\dfrac{1+i}{2}$

(B) $\dfrac{1-i}{2}$

(C) $-1$

(D) $2$

**Q7.** `[Multi-Statement]` ★★ Consider the statements:

I. The composition of two Möbius transformations is a Möbius transformation.

II. A Möbius transformation maps the family of circles and straight lines onto itself.

III. A non-identity Möbius transformation can have three distinct fixed points in $\hat{\mathbb{C}}$.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q8.** `[Assertion-Reason]` ★★ 
**Assertion (A):** $w = e^{z}$ is conformal at every point of $\mathbb{C}$.
**Reason (R):** $w = e^{z}$ is one-to-one on $\mathbb{C}$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match each map, restricted to the given domain, with its image:

| List-I | List-II |
|---|---|
| (a) $w = e^{z}$ on $\lbrace 0 \lt  \operatorname{Im} z \lt  \pi/2\rbrace$ | 1. unit disc $\lvert w\rvert \lt  1$ |
| (b) $w = \operatorname{Log} z$ on $\lbrace \operatorname{Im} z \gt  0\rbrace$ | 2. right half-plane $\operatorname{Re} w \gt  0$ |
| (c) $w = \dfrac{z-i}{z+i}$ on $\lbrace \operatorname{Im} z \gt  0\rbrace$ | 3. first quadrant |
| (d) $w = \dfrac{1+z}{1-z}$ on $\lbrace \lvert z\rvert \lt  1\rbrace$ | 4. strip $0 \lt  \operatorname{Im} w \lt  \pi$ |

(A) a-3, b-4, c-2, d-1

(B) a-4, b-3, c-1, d-2

(C) a-3, b-4, c-1, d-2

(D) a-3, b-1, c-4, d-2

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Every Möbius transformation is a bijection of the extended plane $\hat{\mathbb{C}}$ onto itself.

(B) The cross ratio of four distinct points is invariant under Möbius transformations.

(C) Every conformal bijection of the unit disc onto itself has the form $e^{i\theta}\dfrac{z-a}{1-\bar a z}$ with $|a| \lt  1$.

(D) A Möbius transformation maps every circle onto a circle.

**Q11.** `[Application]` ★★★ The Möbius transformation $T(z) = \dfrac{3z-4}{z-1}$ is

(A) elliptic

(B) hyperbolic

(C) parabolic, with the single fixed point $z = 2$

(D) loxodromic

**Q12.** `[Application]` ★★★ Let $f$ be a conformal bijection of the unit disc onto itself with $f(1/2) = 0$. Then $|f'(1/2)|$ equals

(A) $\dfrac34$

(B) $1$

(C) $2$

(D) $\dfrac43$

**Q13.** `[Application]` ★★★ $T$ is the Möbius map of the upper half-plane onto the unit disc with $T(2i) = 0$ and $T(\infty) = 1$. Then $|T'(2i)|$ equals

(A) $\dfrac14$

(B) $\dfrac12$

(C) $1$

(D) $4$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | B | Concept |
| 4 | A | Numerical |
| 5 | C | Numerical |
| 6 | A | Numerical |
| 7 | B | Multi-Statement |
| 8 | C | Assertion-Reason |
| 9 | C | Match |
| 10 | D | NOT-true / Counterexample |
| 11 | C | Application |
| 12 | D | Application |
| 13 | A | Application |

## Solutions
**Q1 — (D).** A Möbius map has 3 complex degrees of freedom. Given distinct $z_1, z_2, z_3$ and distinct $w_1, w_2, w_3$, exactly one $T$ satisfies $T(z_k) = w_k$, because cross ratios are preserved.

**Q2 — (B).** Setting $z(z+1) = z - 1$ gives $z^2 = -1$, so $z = \pm i$. Option (C) applies only to maps of the form $w = kz$.

**Q3 — (B).** $\bar z$ is a reflection: it is isogonal but sense-reversing, and it is not analytic. Conformal means preserving both the angle and its sense.

**Q4 — (A).** Sending $1 \mapsto 0$ and $-1 \mapsto \infty$ gives $w = k\frac{z-1}{z+1}$. The condition $w(i) = 1$ gives $k = \frac{i+1}{i-1} = -i$, so $w = -i\frac{z-1}{z+1} = i\frac{1-z}{1+z}$. Check: $w(i) = i\cdot\frac{1-i}{1+i} = i\cdot(-i) = 1$. Option (D) is the inverse-type map.

**Q5 — (C).** $z = 1$ goes to $\infty$, so the image is a line. For $z = e^{i\theta}$, $\frac{e^{i\theta}+1}{e^{i\theta}-1} = -i\cot\frac\theta2$, which is purely imaginary. As $\theta$ varies the image is the whole imaginary axis.

**Q6 — (A).** $\frac{(0+1)(1-i)}{(0-i)(1+1)} = \frac{1-i}{-2i} = \frac{(1-i)\thinspace i}{2} = \frac{1+i}{2}$. The value is non-real, so the four points are not concyclic. Option (B) is the conjugate, which comes from a slip in sign.

**Q7 — (B).** Möbius maps form a group under composition, isomorphic to $PSL(2,\mathbb{C})$, and they preserve generalised circles. For III, $T(z) = z$ gives a quadratic $cz^2 + (d-a)z - b = 0$, which has at most 2 roots unless $T$ is the identity.

**Q8 — (C).** $(e^z)' = e^z \ne 0$ everywhere, so $e^z$ is conformal everywhere. But $e^z$ has period $2\pi i$, so it is not injective. Conformality is a local property and does not need injectivity.

**Q9 — (C).** (a) $e^{x+iy}$ with $0 \lt  y \lt  \pi/2$ covers all arguments in $(0,\pi/2)$ and all moduli, giving the first quadrant. (b) $\operatorname{Arg} \in (0,\pi)$ gives the strip. (c) is the Cayley map: points of the UHP are closer to $i$ than to $-i$. (d) $0 \mapsto 1$ and $|z| = 1 \mapsto i\mathbb{R}$, so the image is the right half-plane.

**Q10 — (D).** A circle through the pole $-d/c$ goes onto a straight line. Q5 is an example. The correct statement is that circles go to circles *or lines*.

**Q11 — (C).** $ad - bc = -3 + 4 = 1$ and the trace is $a + d = 3 - 1 = 2$, so $(a+d)^2 = 4$, which is parabolic. The fixed points satisfy $z^2 - 4z + 4 = 0$, giving the double root $z = 2$. For a normalised map, elliptic means $(a+d)^2 \in [0,4)$, hyperbolic means $(a+d)^2 \gt  4$, and loxodromic means $(a+d)^2 \notin [0,\infty)$.

**Q12 — (D).** $f = e^{i\theta}\frac{z-a}{1-\bar az}$ with $a = 1/2$, so $|f'(a)| = \frac{1}{1-|a|^2} = \frac{1}{1-1/4} = \frac43$. Option (A) is $|(f^{-1})'(0)| = 1 - |a|^2$.

**Q13 — (A).** $T = e^{i\theta}\frac{z-2i}{z+2i}$, and $T(\infty) = 1$ forces $e^{i\theta} = 1$. Then $T'(z) = \frac{4i}{(z+2i)^2}$, so $|T'(2i)| = \frac{4}{16} = \frac14$. In general, $|T'(a)| = \frac{1}{2\operatorname{Im} a}$. Option (D) inverts this.
