# Unit 3 · Topic 03 — Riemann Integral and Improper Integrals
> Syllabus coverage: Riemann integral (integrability criteria, Lebesgue's criterion, properties, fundamental theorem of calculus, Riemann sums), improper integrals (convergence tests, absolute/conditional convergence, Beta and Gamma functions)
> Cheatsheet: [../Cheatsheets/03-Riemann-Integral-Improper-Integrals.md](../Cheatsheets/03-Riemann-Integral-Improper-Integrals.md)

**Q1.** `[Concept]` ★ A bounded function $f:[a,b]\to\mathbb{R}$ is Riemann integrable if and only if

(A) $f$ is continuous on $[a,b]$

(B) $f$ has only finitely many discontinuities

(C) the set of discontinuities of $f$ has Lebesgue measure zero

(D) the set of discontinuities of $f$ is countable

**Q2.** `[Concept]` ★★ Thomae's function on $[0,1]$ is $f(p/q)=1/q$ for $p/q$ in lowest terms, $f(0)=1$, and $f(x)=0$ for irrational $x$. Which statement is correct?

(A) $f$ is discontinuous everywhere and not Riemann integrable.

(B) $f$ is continuous exactly at the irrationals, and is Riemann integrable with $\int_0^1f=0$.

(C) $f$ is continuous exactly at the rationals.

(D) $f$ is continuous at the irrationals, but not Riemann integrable since it is discontinuous on a dense set.

**Q3.** `[Numerical]` ★★ $\displaystyle\lim_{x\to0}\frac{1}{x^3}\int_0^x\sin(t^2)\thinspace dt=$

(A) $0$

(B) $1/3$

(C) $1$

(D) $1/6$

**Q4.** `[Numerical]` ★ $\displaystyle\lim_{n\to\infty}\sum_{k=1}^{n}\frac{n}{n^2+k^2}=$

(A) $\log 2$

(B) $\pi/2$

(C) $1$

(D) $\pi/4$

**Q5.** `[Multi-Statement]` ★★ Consider the improper integrals

I. $\displaystyle\int_0^\infty\frac{\sin x}{x}\thinspace dx$  II. $\displaystyle\int_0^\infty\left|\frac{\sin x}{x}\right|dx$  III. $\displaystyle\int_0^\infty\sin(x^2)\thinspace dx$

Which of them converge?

(A) I only

(B) I, II and III

(C) I and II only

(D) I and III only

**Q6.** `[Assertion-Reason]` ★
**Assertion (A):** Every continuous function $f:[a,b]\to\mathbb{R}$ is Riemann integrable.
**Reason (R):** Every continuous function on $[a,b]$ is uniformly continuous.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match List-I with List-II.

| List-I | List-II |
|---|---|
| a. $\Gamma(1/2)$ | 1. $\dfrac{3\pi}{16}$ |
| b. $B(1/2,1/2)$ | 2. $\dfrac{\sqrt\pi}{2}$ |
| c. $\displaystyle\int_0^\infty e^{-x^2}dx$ | 3. $\sqrt\pi$ |
| d. $\displaystyle\int_0^{\pi/2}\sin^4x\thinspace dx$ | 4. $\pi$ |

(A) a-3, b-4, c-2, d-1

(B) a-4, b-3, c-2, d-1

(C) a-3, b-4, c-1, d-2

(D) a-2, b-4, c-3, d-1

**Q8.** `[Numerical]` ★★ $\displaystyle\int_0^1x^4(1-x)^3\thinspace dx=$

(A) $\dfrac1{140}$

(B) $\dfrac1{560}$

(C) $\dfrac1{280}$

(D) $\dfrac1{252}$

**Q9.** `[Application]` ★★★ The improper integral $\displaystyle\int_0^\infty\frac{x^{p-1}}{1+x}\thinspace dx$ converges if and only if

(A) $p\gt 0$

(B) $p\lt 1$

(C) $0\lt p\lt 1$

(D) $0\lt p\le1$

**Q10.** `[NOT-true / Counterexample]` ★★★ Let $f,g:[a,b]\to\mathbb{R}$ be bounded. Which of the following is **NOT** true in general?

(A) If $f$ is Riemann integrable, then so is $|f|$.

(B) If $|f|$ is Riemann integrable, then so is $f$.

(C) If $f$ and $g$ are Riemann integrable, then so is $fg$.

(D) If $f$ is Riemann integrable and $\phi$ is continuous on $\mathbb{R}$, then $\phi\circ f$ is Riemann integrable.

**Q11.** `[Application]` ★★ Let $f:[0,1]\to\mathbb{R}$ be continuous with $\displaystyle\int_0^xf(t)\thinspace dt=\int_x^1f(t)\thinspace dt$ for all $x\in[0,1]$. Then

(A) $f\equiv0$

(B) $f$ is a nonzero constant

(C) $f(x)=1-2x$

(D) $f(x)=x-\tfrac12$

**Q12.** `[Numerical]` ★★ $\displaystyle\int_0^\infty x^2e^{-x^2}\thinspace dx=$

(A) $\dfrac{\sqrt\pi}{2}$

(B) $\dfrac{\sqrt\pi}{4}$

(C) $\dfrac{\sqrt\pi}{8}$

(D) $\dfrac{1}{2}$

**Q13.** `[Multi-Statement]` ★★ Let $f$ be Riemann integrable on $[a,b]$ and $F(x)=\int_a^xf(t)\thinspace dt$.

I. $F$ is (uniformly) continuous on $[a,b]$.

II. $F$ is differentiable on $(a,b)$ and $F'=f$ everywhere.

III. If $f$ is continuous at $c\in(a,b)$, then $F'(c)=f(c)$.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and III only

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Concept |
| 3 | B | Numerical |
| 4 | D | Numerical |
| 5 | D | Multi-Statement |
| 6 | A | Assertion-Reason |
| 7 | A | Match |
| 8 | C | Numerical |
| 9 | C | Application |
| 10 | B | NOT-true / Counterexample |
| 11 | A | Application |
| 12 | B | Numerical |
| 13 | D | Multi-Statement |

## Solutions
**Q1 — (C).** This is Lebesgue's criterion. (A) and (B) are sufficient but not necessary (Thomae's function). (D) is neither: the indicator of the Cantor set has uncountably many discontinuities but is integrable, because they form a null set.

**Q2 — (B).** At an irrational $x$, only finitely many $p/q$ with $q\le N$ lie near $x$, so $f(y)\to0=f(x)$. At a rational, $f\gt 0$ but irrationals arbitrarily close give $0$. The discontinuity set $\mathbb{Q}\cap[0,1]$ is countable, hence null, so $f$ is integrable. Every lower sum is $0$, so $\int f=0$. (D) confuses "dense" with "positive measure".

**Q3 — (B).** By L'Hôpital and the FTC, the limit is $\lim\frac{\sin x^2}{3x^2}=\frac13$. Alternatively, $\int_0^x\sin t^2\thinspace dt\approx\frac{x^3}{3}$.

**Q4 — (D).** $\sum\frac{n}{n^2+k^2}=\frac1n\sum\frac{1}{1+(k/n)^2}\to\int_0^1\frac{dx}{1+x^2}=\frac\pi4$.

**Q5 — (D).** I converges (Dirichlet test), with value $\pi/2$. II diverges: $\int_{k\pi}^{(k+1)\pi}\frac{|\sin x|}{x}dx\ge\frac{2}{(k+1)\pi}$, and the harmonic series diverges. So I converges only conditionally. III converges (substitute $x^2=u$ to get $\int\frac{\sin u}{2\sqrt u}du$; Fresnel value $\frac12\sqrt{\pi/2}$). The integrand of III does not tend to $0$, but the integral still converges.

**Q6 — (A).** Uniform continuity makes the oscillation on every sub-interval smaller than $\varepsilon$ once the mesh is small, so $U(P,f)-L(P,f)\lt \varepsilon(b-a)$. This is the standard proof, so R explains A.

**Q7 — (A).** $\Gamma(\frac12)=\sqrt\pi$; $B(\frac12,\frac12)=\Gamma(\frac12)^2/\Gamma(1)=\pi$; $\int_0^\infty e^{-x^2}dx=\frac12\Gamma(\frac12)=\frac{\sqrt\pi}2$; by Wallis, $\int_0^{\pi/2}\sin^4x\thinspace dx=\frac34\cdot\frac12\cdot\frac\pi2=\frac{3\pi}{16}$.

**Q8 — (C).** $B(5,4)=\frac{\Gamma(5)\Gamma(4)}{\Gamma(9)}=\frac{24\cdot6}{40320}=\frac{1}{280}$. A common slip is to use $B(4,3)$, which gives $\frac{1}{60}$, or to mix up the factorials.

**Q9 — (C).** Near $0$ the integrand is $\sim x^{p-1}$, which needs $p-1\gt -1$, i.e. $p\gt 0$. Near $\infty$ it is $\sim x^{p-2}$, which needs $p-2\lt -1$, i.e. $p\lt 1$. So $0\lt p\lt 1$, where the value is $B(p,1-p)=\frac{\pi}{\sin p\pi}$. At $p=1$, $\int^\infty\frac{dx}{1+x}$ diverges.

**Q10 — (B).** Let $f=1$ on $\mathbb{Q}$ and $f=-1$ off $\mathbb{Q}$. Then $|f|\equiv1$ is integrable but $f$ is discontinuous everywhere. (A), (C) and (D) all follow from Lebesgue's criterion, because the discontinuity sets stay inside null sets. Note that $f\circ\phi$ (in the reverse order) can fail.

**Q11 — (A).** Differentiate using the FTC: $f(x)=-f(x)$, so $f\equiv0$. (Check with $x=0$: $\int_0^1f=0$.) (C) and (D) satisfy $\int_0^1f=0$ but not the identity for all $x$.

**Q12 — (B).** Put $x^2=u$: $\int_0^\infty x^2e^{-x^2}dx=\frac12\int_0^\infty u^{1/2}e^{-u}du=\frac12\Gamma(\frac32)=\frac12\cdot\frac{\sqrt\pi}{2}=\frac{\sqrt\pi}4$.

**Q13 — (D).** $|F(x)-F(y)|\le M|x-y|$ with $M=\sup|f|$, so I holds. III is FTC-I. II fails: for $f=\chi_{[1/2,1]}$ on $[0,1]$, $F(x)=(x-\frac12)^+$ is not differentiable at $\frac12$.
