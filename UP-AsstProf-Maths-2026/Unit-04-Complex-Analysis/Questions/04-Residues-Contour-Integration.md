# Unit 4 · Topic 04 — Calculus of Residues and Contour Integration
> Syllabus coverage: Calculus of residues, Contour integration (incl. residue formulas, residue at infinity, trigonometric and rational integrals, Jordan's lemma, indented contours / principal values)
> Cheatsheet: [../Cheatsheets/04-Residues-Contour-Integration.md](../Cheatsheets/04-Residues-Contour-Integration.md)

**Q1.** `[Numerical]` ★ $\operatorname{Res}_{z=0}\dfrac{e^{z}}{z^{3}}$ equals

(A) $1$

(B) $0$

(C) $\dfrac16$

(D) $\dfrac12$

**Q2.** `[Concept]` ★ If $f$ is analytic on $\mathbb{C}$ except at finitely many isolated singularities, then the sum of the residues of $f$ at all its finite singularities **and** at $\infty$ is

(A) $2\pi i$

(B) $1$

(C) $0$

(D) not determined in general

**Q3.** `[Numerical]` ★ $\displaystyle\int_{-\infty}^{\infty}\frac{dx}{x^{2}+2x+2}$ equals

(A) $\pi$

(B) $\dfrac{\pi}{2}$

(C) $2\pi$

(D) $\dfrac{\pi}{\sqrt2}$

**Q4.** `[Numerical]` ★★ The residue of $\dfrac{1}{z^{4}+1}$ at $z = e^{i\pi/4}$ is

(A) $\dfrac{e^{i\pi/4}}{4}$

(B) $-\dfrac{e^{i\pi/4}}{4}$

(C) $\dfrac{e^{-i\pi/4}}{4}$

(D) $-\dfrac{e^{-i\pi/4}}{4}$

**Q5.** `[Numerical]` ★★ $\displaystyle\int_{0}^{2\pi}\frac{d\theta}{5+4\cos\theta}$ equals

(A) $\dfrac{2\pi}{9}$

(B) $\dfrac{2\pi}{3}$

(C) $\dfrac{\pi}{3}$

(D) $\dfrac{2\pi}{\sqrt{41}}$

**Q6.** `[Numerical]` ★★ $\displaystyle\int_{-\infty}^{\infty}\frac{\cos x}{x^{2}+1}\,dx$ equals

(A) $\pi e$

(B) $\pi\cosh 1$

(C) $\dfrac{\pi}{2e}$

(D) $\dfrac{\pi}{e}$

**Q7.** `[Multi-Statement]` ★★ Consider the statements:

I. $\operatorname{Res}_{z=0}\, z\cos(1/z) = -\tfrac12$.

II. $\operatorname{Res}_{z=0}\dfrac{\sin z}{z^{2}} = 1$.

III. $\operatorname{Res}_{z=0}\dfrac{\cot z}{z} = 1$.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q8.** `[Assertion-Reason]` ★★ Let $C_R$ be the upper semicircle $|z| = R$, $\operatorname{Im} z \ge 0$.
**Assertion (A):** $\displaystyle\lim_{R\to\infty}\int_{C_R}\frac{e^{iz}}{z}\,dz = 0$.
**Reason (R):** If $f(z) \to 0$ uniformly on $C_R$ as $R\to\infty$ and $m > 0$, then $\displaystyle\int_{C_R}e^{imz}f(z)\,dz \to 0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match each integral with its value:

| List-I | List-II |
|---|---|
| (a) $\displaystyle\int_0^{2\pi}\frac{d\theta}{2+\cos\theta}$ | 1. $\pi/4$ |
| (b) $\displaystyle\int_0^{\infty}\frac{\sin x}{x}\,dx$ | 2. $0$ |
| (c) $\displaystyle\int_0^{\infty}\frac{dx}{(1+x^2)^2}$ | 3. $2\pi/\sqrt3$ |
| (d) $\displaystyle\int_0^{\infty}\frac{\ln x}{1+x^2}\,dx$ | 4. $\pi/2$ |

(A) a-3, b-4, c-1, d-2

(B) a-3, b-1, c-4, d-2

(C) a-4, b-3, c-1, d-2

(D) a-3, b-4, c-2, d-1

**Q10.** `[NOT-true / Counterexample]` ★★★ Which of the following is NOT true?

(A) The residue of $f$ at a removable singularity is $0$.

(B) If $f$ has a pole of order $m$ at $a$, then $\operatorname{Res}_a f = \dfrac{1}{(m-1)!}\lim_{z\to a}\dfrac{d^{m-1}}{dz^{m-1}}\big[(z-a)^m f(z)\big]$.

(C) If $f$ is analytic at $\infty$, then $\operatorname{Res}_{z=\infty}f = 0$.

(D) If $f$ is even and has an isolated singularity at $0$, then $\operatorname{Res}_{z=0}f = 0$.

**Q11.** `[Application]` ★★★ $\displaystyle\oint_{|z|=2}\frac{z^{15}}{(z^{2}+1)^{2}(z^{4}+2)^{3}}\,dz$ equals

(A) $0$

(B) $-2\pi i$

(C) $2\pi i$

(D) $\pi i$

**Q12.** `[Application]` ★★★ The Cauchy principal value $\displaystyle \mathrm{P.V.}\int_{-\infty}^{\infty}\frac{dx}{(x-1)(x^{2}+1)}$ equals

(A) $\dfrac{\pi}{2}$

(B) $-\dfrac{\pi}{2}$

(C) $-\pi$

(D) $0$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Numerical |
| 2 | C | Concept |
| 3 | A | Numerical |
| 4 | B | Numerical |
| 5 | B | Numerical |
| 6 | D | Numerical |
| 7 | D | Multi-Statement |
| 8 | A | Assertion-Reason |
| 9 | A | Match |
| 10 | C | NOT-true / Counterexample |
| 11 | C | Application |
| 12 | B | Application |

## Solutions
**Q1 — (D).** $\frac{e^z}{z^3} = \sum\frac{z^{n-3}}{n!}$. The $z^{-1}$ term comes from $n = 2$, giving $\frac{1}{2!} = \frac12$. Option (C) uses $n = 3$.

**Q2 — (C).** For a large circle $C$, $\oint_C f = 2\pi i\sum_{\text{finite}}\operatorname{Res}$, and also $\oint_C f = -2\pi i\operatorname{Res}_\infty f$. So the total of all residues is $0$.

**Q3 — (A).** $x^2 + 2x + 2 = (x+1)^2 + 1$. Substituting $u = x + 1$ gives $\int\frac{du}{u^2+1} = \pi$. By residues: the pole in the upper half-plane is $-1 + i$, with residue $\frac{1}{2i}$, so the integral is $2\pi i\cdot\frac{1}{2i} = \pi$.

**Q4 — (B).** At a simple pole, $\operatorname{Res} = \frac{p(a)}{q'(a)} = \frac{1}{4a^3} = \frac{a}{4a^4} = -\frac{a}{4}$, because $a^4 = -1$. Option (A) misses the sign.

**Q5 — (B).** $\int_0^{2\pi}\frac{d\theta}{a + b\cos\theta} = \frac{2\pi}{\sqrt{a^2-b^2}}$ for $a > |b|$. Here this is $\frac{2\pi}{\sqrt{25-16}} = \frac{2\pi}{3}$. Option (D) adds instead of subtracting.

**Q6 — (D).** Integrate $\frac{e^{iz}}{z^2+1}$ over the upper half-plane. The residue at $i$ is $\frac{e^{-1}}{2i}$, so the integral is $2\pi i\cdot\frac{e^{-1}}{2i} = \frac{\pi}{e}$; take the real part. Option (A) comes from closing in the wrong half-plane, and (C) is the value of $\int_0^\infty$.

**Q7 — (D).** I: $z\cos(1/z) = z - \frac{1}{2z} + \cdots$, so the residue is $-\frac12$. II: $\frac{\sin z}{z^2} = \frac1z - \frac z6 + \cdots$, so the residue is $1$. III: $\frac{\cot z}{z} = \frac{1}{z^2} - \frac13 - \cdots$ is even, so its residue is $0$.

**Q8 — (A).** R is Jordan's lemma. With $f = 1/z$ and $m = 1$ it gives A. The ML-inequality alone does not suffice, because it only gives the bound $\frac{1}{R}\cdot\pi R = \pi$, which does not tend to $0$. So R is exactly the explanation needed.

**Q9 — (A).** (a) $\frac{2\pi}{\sqrt{4-1}} = \frac{2\pi}{\sqrt3}$. (b) is the Dirichlet integral, $\frac\pi2$. (c) is half of $\int_{\mathbb{R}} = \frac\pi2$, so $\frac\pi4$. (d) The substitution $x \mapsto 1/x$ maps the integral to its negative, so it is $0$.

**Q10 — (C).** $f = \frac1z$ is analytic at $\infty$ (it vanishes there), yet $\operatorname{Res}_\infty f = -1$. The residue at $\infty$ is $-c_{-1}$ from the expansion at $\infty$, and that coefficient can be non-zero even when $f$ is analytic at $\infty$. (D) is true: an even Laurent series has no $z^{-1}$ term.

**Q11 — (C).** All poles ($\pm i$ and the fourth roots of $-2$, with modulus $2^{1/4} \approx 1.19$) lie inside $|z| = 2$, so the integral is $-2\pi i\operatorname{Res}_\infty$. The degrees are 15 over 16, so $f = \frac1z + O(z^{-2})$ at $\infty$ and $\operatorname{Res}_\infty = -1$. The integral is $2\pi i$. Computing 7 separate residues would be far too slow; checked numerically.

**Q12 — (B).** Indent around $x = 1$:
$$\mathrm{P.V.} = 2\pi i\operatorname{Res}_{i} + \pi i\operatorname{Res}_{1}.$$
- $\operatorname{Res}_1 = \frac12$.
- $\operatorname{Res}_i = \frac{1}{(i-1)\,2i} = -\frac{1-i}{4}$.

So
$$\mathrm{P.V.} = -\frac{\pi i(1-i)}{2} + \frac{\pi i}{2} = -\frac{\pi}{2}$$
(confirmed numerically). Option (D) wrongly assumes the integrand is odd. A pole on the axis contributes $\pi i$, half of $2\pi i$.
