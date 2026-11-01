# Unit 4 · Topic 02 — Cauchy's Theorem, Integral Formula, Morera and Liouville
> Syllabus coverage: Cauchy's theorem, Morera's theorem, Liouville's theorem, Cauchy's Integral formula (incl. Cauchy estimates, maximum/minimum modulus principle, fundamental theorem of algebra)
> Cheatsheet: [../Cheatsheets/02-Cauchy-Theorem-Integral-Formula-Morera-Liouville.md](../Cheatsheets/02-Cauchy-Theorem-Integral-Formula-Morera-Liouville.md)

**Q1.** `[Concept]` ★ Morera's theorem states that if $f$ is **continuous** on a domain $D$ and $\oint_{\partial T} f(z)\,dz = 0$ for every closed triangle $T \subset D$, then

(A) $f$ has a primitive on all of $D$

(B) $f$ is analytic on $D$

(C) $f$ is constant on $D$

(D) $f$ is bounded on $D$

**Q2.** `[Numerical]` ★ $\displaystyle\oint_{|z|=2} \frac{e^{z}}{z-1}\,dz$ equals

(A) $2\pi i$

(B) $\pi i e$

(C) $0$

(D) $2\pi i e$

**Q3.** `[Numerical]` ★★ $\displaystyle\oint_{|z|=1} \frac{e^{2z}}{z^{4}}\,dz$ equals

(A) $\dfrac{8\pi i}{3}$

(B) $\dfrac{4\pi i}{3}$

(C) $16\pi i$

(D) $\dfrac{\pi i}{3}$

**Q4.** `[Application]` ★ $\displaystyle\oint_{|z|=1} \bar z\,dz$ (counter-clockwise) equals

(A) $0$, by Cauchy's theorem

(B) $2\pi$

(C) $-2\pi i$

(D) $2\pi i$

**Q5.** `[Numerical]` ★★ $\displaystyle\oint_{|z-i|=1} \frac{dz}{z^{2}+1}$ equals

(A) $0$

(B) $2\pi$

(C) $\pi$

(D) $-\pi$

**Q6.** `[Multi-Statement]` ★★ Consider the statements:

I. If $f$ is entire and $|f(z)| \le M|z|^{n}$ for all $|z| \ge R_0$, then $f$ is a polynomial of degree at most $n$.

II. $\sin z$ is a bounded entire function.

III. An entire function whose range misses some open disc is constant.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) II and III only

**Q7.** `[Assertion-Reason]` ★★ 
**Assertion (A):** $\displaystyle\oint_{|z|=2} \frac{dz}{z^{2}} = 0$.
**Reason (R):** $1/z^{2}$ is analytic inside and on $|z| = 2$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match each theorem with its conclusion:

| List-I | List-II |
|---|---|
| (a) Liouville | 1. $\lvert f^{(n)}(a)\rvert \le n!\,M/R^{n}$ |
| (b) Maximum modulus | 2. $f$ continuous with vanishing triangle integrals $\Rightarrow$ $f$ analytic |
| (c) Cauchy's estimate | 3. bounded entire $\Rightarrow$ constant |
| (d) Morera | 4. a non-constant analytic $\lvert f\rvert$ has no interior local maximum |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-4, c-2, d-1

(C) a-2, b-4, c-1, d-3

(D) a-3, b-4, c-1, d-2

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Since $1/z$ is analytic on the annulus $\tfrac12 < |z| < 2$, which contains $|z|=1$, Cauchy's theorem gives $\oint_{|z|=1} \frac{dz}{z} = 0$.

(B) If $f$ is analytic on a simply connected domain $D$, then $\oint_\gamma f\,dz = 0$ for every closed contour $\gamma$ in $D$.

(C) Every non-constant polynomial with complex coefficients has a root in $\mathbb{C}$.

(D) If $f$ is analytic on a domain $D$, then $f$ has derivatives of all orders on $D$.

**Q10.** `[Numerical]` ★★★ Let $f$ be analytic on a neighbourhood of $|z| \le 2$ with $|f(z)| \le 5$ on $|z| = 2$. The best upper bound given by Cauchy's estimate for $|f'''(0)|$ is

(A) $\dfrac{5}{8}$

(B) $\dfrac{15}{4}$

(C) $\dfrac{15}{2}$

(D) $30$

**Q11.** `[Application]` ★★★ Let $f$ be entire with $|f(z)| \le |z|^{3/2} + 5$ for all $z\in\mathbb{C}$. Then

(A) $f$ is necessarily constant

(B) $f$ is a polynomial of degree at most 1

(C) $f$ is a polynomial of degree at most 2

(D) $f$ need not be a polynomial

**Q12.** `[Numerical]` ★★ The maximum of $|\sin z|$ over the closed square $0 \le x \le 2\pi,\ 0 \le y \le 2\pi$ is

(A) $\cosh 2\pi$

(B) $\sinh 2\pi$

(C) $1$

(D) $e^{2\pi}$

**Q13.** `[Concept]` ★ Let $D$ be a bounded domain and $f$ non-constant and analytic on $D$, continuous on $\bar D$, with **no zeros** in $D$. Then $\min_{\bar D}|f|$ is attained

(A) only at interior points of $D$

(B) on the boundary $\partial D$

(C) only where $f' = 0$

(D) possibly nowhere on $\bar D$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | D | Numerical |
| 3 | A | Numerical |
| 4 | D | Application |
| 5 | C | Numerical |
| 6 | C | Multi-Statement |
| 7 | C | Assertion-Reason |
| 8 | D | Match |
| 9 | A | NOT-true / Counterexample |
| 10 | B | Numerical |
| 11 | B | Application |
| 12 | A | Numerical |
| 13 | B | Concept |

## Solutions
**Q1 — (B).** Morera's theorem is the converse of Goursat's theorem: such an $f$ has local primitives, and a primitive is analytic, so its derivative $f$ is analytic too. Option (A), a *global* primitive, needs zero integrals over *all* closed curves (or a simply connected $D$).

**Q2 — (D).** By Cauchy's integral formula, with $1$ inside $|z| = 2$, the integral is $2\pi i\,e^{1}$.

**Q3 — (A).** $\oint \frac{f(z)}{z^{n+1}}dz = \frac{2\pi i}{n!}f^{(n)}(0)$. Here $n = 3$ and $f'''(0) = 8$, so the value is $2\pi i\cdot 8/6 = 8\pi i/3$. Option (C) forgets to divide by $3!$.

**Q4 — (D).** On $|z| = 1$ we have $\bar z = 1/z$, so the integral is $\oint dz/z = 2\pi i$. Option (A) is the trap: $\bar z$ is not analytic, so Cauchy's theorem does not apply.

**Q5 — (C).** Only $z = i$ lies inside $|z - i| = 1$; $-i$ is at distance 2. Writing $\frac{1}{z^2+1} = \frac{1/(z+i)}{z-i}$, the integral is $2\pi i\cdot\frac{1}{2i} = \pi$. Option (A) would be the answer for a large circle enclosing both poles.

**Q6 — (C).** I: Cauchy's estimate on $|z| = R$ gives $|f^{(k)}(0)| \le k!\,MR^{n}/R^{k} \to 0$ for $k > n$ (generalised Liouville). II is false: $|\sin(iy)| = \sinh|y|$. III: if $|f - a| \ge r$, then $1/(f - a)$ is bounded and entire, hence constant (Liouville).

**Q7 — (C).** A is true because $1/z^2$ has the primitive $-1/z$ on $\mathbb{C}\setminus\{0\}$ (equivalently, its residue is $0$). R is false because $1/z^2$ has a pole at $0$, inside the circle.

**Q8 — (D).** Liouville goes with 3, maximum modulus with 4, Cauchy's estimate with 1 and Morera with 2.

**Q9 — (A).** The annulus is not simply connected, and $\oint_{|z|=1} dz/z = 2\pi i \ne 0$. (B) is Cauchy's theorem, (C) is the fundamental theorem of algebra (via Liouville applied to $1/p$), and (D) follows from the integral formula for derivatives.

**Q10 — (B).** $|f'''(0)| \le \frac{3!\,M}{R^{3}} = \frac{6\cdot5}{8} = \frac{15}{4}$. Option (A) forgets the $3!$, and (D) forgets $R^3$.

**Q11 — (B).** Apply the estimate on $|z| = R$: $|f''(0)| \le 2(R^{3/2} + 5)/R^{2} \to 0$, and similarly for every $f^{(k)}(0)$ with $k \ge 2$. So $f(z) = a + bz$. For example $f(z) = z$ satisfies $|z| \le |z|^{3/2} + 5$, so $f$ need not be constant and (A) is false. Degree 2 is impossible because $|z|^2$ outgrows $|z|^{3/2}$.

**Q12 — (A).** $|\sin z|^2 = \sin^2 x + \sinh^2 y$. By maximum modulus the maximum is on the boundary, at $x = \pi/2$ and $y = 2\pi$: $\sqrt{1 + \sinh^2 2\pi} = \cosh 2\pi \approx 267.7$. Option (B) misses the $\sin^2 x$ term.

**Q13 — (B).** Apply the maximum modulus principle to $1/f$, which is analytic because $f$ has no zeros. This is the minimum modulus principle. Without the no-zero hypothesis the minimum can be interior; for example $f = z$ on the unit disc has minimum $0$ at the centre.
