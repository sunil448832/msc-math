# Unit 4 · Topic 03 — Zeros, Taylor and Laurent Series, Singularities
> Syllabus coverage: Zeros of analytic functions, Taylor series, Laurent series (incl. identity theorem, order of zeros, radius of convergence, classification of isolated singularities, Casorati–Weierstrass, argument principle and Rouché's theorem)
> Cheatsheet: [../Cheatsheets/03-Zeros-Taylor-Laurent-Singularities.md](../Cheatsheets/03-Zeros-Taylor-Laurent-Singularities.md)

**Q1.** `[Numerical]` ★ The radius of convergence of the Taylor series of $f(z) = \dfrac{1}{z^{2}+4}$ about $z_0 = 1$ is

(A) $\sqrt5$

(B) $2$

(C) $1$

(D) $\sqrt3$

**Q2.** `[Numerical]` ★ The order of the zero of $f(z) = \sin z - z + \dfrac{z^{3}}{6}$ at $z = 0$ is

(A) 3

(B) 4

(C) 5

(D) 7

**Q3.** `[Concept]` ★ Suppose the Laurent series $`\sum_{n=-\infty}^{\infty}a_n(z-a)^n`$ of $`f`$ in $`0 \lt  |z - a| \lt  r`$ has $`a_n \ne 0`$ for infinitely many negative $`n`$. Then $`z = a`$ is

(A) a removable singularity

(B) a pole of infinite order, which counts as a pole

(C) a non-isolated singularity

(D) an essential singularity

**Q4.** `[Numerical]` ★★ The radius of convergence of $\displaystyle\sum_{n\ge1}\frac{n!}{n^{n}}z^{n}$ is

(A) $e$

(B) $1$

(C) $1/e$

(D) $\infty$

**Q5.** `[Numerical]` ★★ In the Taylor expansion $\dfrac{e^{z}}{1-z} = \sum c_n z^n$ about $0$, the coefficient $c_4$ is

(A) $\dfrac{1}{24}$

(B) $\dfrac{65}{24}$

(C) $\dfrac{8}{3}$

(D) $e$

**Q6.** `[Numerical]` ★★ For $f(z) = \dfrac{1}{(z-1)(z-2)}$, the coefficient of $z^{-1}$ in its Laurent series valid in $1 \lt  |z| \lt  2$ is

(A) $0$

(B) $1$

(C) $-1$

(D) $-\tfrac12$

**Q7.** `[Match]` ★★ Match each function with the nature of its singularity at $z = 0$:

| List-I | List-II |
|---|---|
| (a) $\dfrac{\sin z}{z}$ | 1. simple pole |
| (b) $\dfrac{1-\cos z}{z^{4}}$ | 2. essential singularity |
| (c) $e^{1/z}$ | 3. removable singularity |
| (d) $\dfrac{1}{e^{z}-1}$ | 4. pole of order 2 |

(A) a-3, b-1, c-2, d-4

(B) a-3, b-4, c-2, d-1

(C) a-1, b-4, c-2, d-3

(D) a-3, b-4, c-1, d-2

**Q8.** `[Multi-Statement]` ★★ Let $`a`$ be an isolated singularity of $`f`$. Consider the statements:

I. If $a$ is an essential singularity, then $f(\lbrace 0 \lt  |z-a| \lt  \delta\rbrace )$ is dense in $\mathbb{C}$ for every $\delta \gt  0$.

II. If $`|f(z)| \to \infty`$ as $`z \to a`$, then $`a`$ is a pole of $`f`$.

III. If $`a`$ is a pole of $`f`$, then $`a`$ is a pole of $`e^{f(z)}`$.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q9.** `[Assertion-Reason]` ★★ 
**Assertion (A):** $z = 0$ is an isolated singularity of $f(z) = \dfrac{1}{\sin(1/z)}$.
**Reason (R):** The poles $`z = \dfrac{1}{n\pi}`$ ($`n\in\mathbb{Z}\setminus\lbrace 0\rbrace`$) of $`f`$ accumulate at $`0`$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) The zeros of a non-constant analytic function on a domain are isolated.

(B) A power series converges uniformly on every compact subset of its open disc of convergence.

(C) A function that is analytic on $\mathbb{C}$ except for finitely many poles, and has at most a pole at $\infty$, is rational.

(D) A power series either converges at every point of its circle of convergence or diverges at every point of it.

**Q11.** `[Application]` ★★★ Which of the following can hold for some function $`f`$ analytic on the open unit disc?

(A) $f\negthinspace \left(\tfrac1n\right) = \dfrac{1}{n+1}$ for all $n \ge 2$

(B) $f\negthinspace \left(\tfrac1n\right) = \dfrac{(-1)^n}{n}$ for all $n \ge 2$

(C) $f\negthinspace \left(\tfrac1n\right) = 0$ for all $n \ge 2$, and $f \not\equiv 0$

(D) $f\negthinspace \left(\tfrac1n\right) = e^{-n}$ for all $n \ge 2$

**Q12.** `[Numerical]` ★★★ The number of zeros, counted with multiplicity, of $p(z) = z^{5} + 15z + 1$ in the annulus $1 \lt  |z| \lt  2$ is

(A) 1

(B) 3

(C) 4

(D) 5

**Q13.** `[Application]` ★★★ The value of $\displaystyle\frac{1}{2\pi i}\oint_{|z|=2}\frac{f'(z)}{f(z)}\thinspace dz$ for $f(z) = \tan z$ is

(A) $1$

(B) $-1$

(C) $3$

(D) $0$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Numerical |
| 2 | C | Numerical |
| 3 | D | Concept |
| 4 | A | Numerical |
| 5 | B | Numerical |
| 6 | C | Numerical |
| 7 | B | Match |
| 8 | B | Multi-Statement |
| 9 | D | Assertion-Reason |
| 10 | D | NOT-true / Counterexample |
| 11 | A | Application |
| 12 | C | Numerical |
| 13 | B | Application |

## Solutions
**Q1 — (A).** The radius is the distance from the centre to the nearest singularity. The singularities are $\pm 2i$, and $|1 - 2i| = \sqrt5$. Option (B) is the radius about $0$.

**Q2 — (C).** $\sin z = z - \frac{z^3}{6} + \frac{z^5}{120} - \cdots$, so $f(z) = \frac{z^5}{120} - \cdots$, a zero of order 5.

**Q3 — (D).** An infinite principal part is the definition of an essential singularity. A pole has a *finite* principal part, so (B) is wrong; there is no "pole of infinite order". (C) is wrong because the singularity is isolated by hypothesis.

**Q4 — (A).** By the ratio test, $\frac{a_n}{a_{n+1}} = \frac{(n+1)^n}{n^n} = \left(1 + \frac1n\right)^n \to e$. Option (C) inverts the ratio.

**Q5 — (B).** Multiplying by $\frac{1}{1-z}$ gives partial sums: $c_n = \sum_{k=0}^{n}\frac{1}{k!}$. So $c_4 = 1 + 1 + \frac12 + \frac16 + \frac1{24} = \frac{65}{24}$. Option (A) is only the $e^z$ coefficient.

**Q6 — (C).** $`f = \frac{1}{z-2} - \frac{1}{z-1}`$. In $`|z| \lt  2`$, $`\frac{1}{z-2} = -\frac12\sum(z/2)^n`$, which has no negative powers. In $`|z| \gt  1`$, $`-\frac{1}{z-1} = -\sum_{n\ge0}z^{-n-1}`$, which contributes $`-1`$ to the $`z^{-1}`$ coefficient. Option (A) is the trap "$`f`$ is analytic at $`0`$, so there is no $`z^{-1}`$ term", but the annulus encloses the pole at $`1`$.

**Q7 — (B).** $\frac{\sin z}{z} \to 1$, so it is removable. $\frac{1-\cos z}{z^4} = \frac{1}{2z^2} - \frac{1}{24} + \cdots$ has a pole of order 2. $e^{1/z} = \sum \frac{z^{-n}}{n!}$ is essential. $e^z - 1$ has a simple zero at $0$, so $\frac{1}{e^z-1}$ has a simple pole there.

**Q8 — (B).** I is the Casorati–Weierstrass theorem. II: $`f`$ is non-zero near $`a`$, $`1/f \to 0`$ there, so $`1/f`$ has a removable zero at $`a`$ and $`f`$ has a pole. III is false: $`f = 1/z`$ gives $`e^{1/z}`$, which is essential, not a pole.

**Q9 — (D).** The poles $1/(n\pi) \to 0$, so every punctured disc around $0$ contains singularities. Hence $0$ is a *non-isolated* singularity, A is false and R is true.

**Q10 — (D).** $\sum \frac{z^n}{n}$ has $R = 1$. It diverges at $z = 1$ but converges at $z = -1$, and in fact at every other point of $|z| = 1$ by Dirichlet's test. (C) is true: subtract the principal parts, including the polynomial part at $\infty$, and Liouville leaves a constant.

**Q11 — (A).** $f(z) = \frac{z}{1+z}$ is analytic on $|z| \lt  1$ and gives $f(1/n) = \frac{1}{n+1}$. For (B), the identity theorem along even $n$ forces $f = z$, and along odd $n$ forces $f = -z$, a contradiction. (C) is impossible, because zeros accumulating at $0 \in D$ force $f \equiv 0$. For (D), $f(0) = 0$; if the zero had finite order $k$, then $|f(1/n)| \sim c\thinspace n^{-k}$, which decays too slowly to equal $e^{-n}$. So $f \equiv 0$, which contradicts $e^{-n} \ne 0$.

**Q12 — (C).** On $|z| = 2$: $|z^5| = 32 \gt  |15z + 1| \le 31$, so there are 5 zeros in $|z| \lt  2$. On $|z| = 1$: $|15z| = 15 \gt  |z^5 + 1| \le 2$, so there is 1 zero in $|z| \lt  1$. The annulus has $5 - 1 = 4$ zeros. Numerically, the moduli are about $0.067$, $1.956$ (twice) and $1.980$ (twice).

**Q13 — (B).** By the argument principle the integral equals $Z - P$ inside $|z| = 2$. The only zero of $\tan z$ there is $0$ ($\pm\pi$ lie outside since $\pi \gt  2$). The poles are $\pm\pi/2$ ($\pi/2 \approx 1.57 \lt  2$). So $Z - P = 1 - 2 = -1$. Option (A) counts zeros only.
