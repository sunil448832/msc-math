# Unit 3 · Topic 06 — Lebesgue Integral
> Syllabus coverage: Lebesgue integral (simple functions, MCT, Fatou's lemma, DCT), Riemann vs Lebesgue integral, $L^p$ spaces (basics)
> Cheatsheet: [../Cheatsheets/06-Lebesgue-Integral.md](../Cheatsheets/06-Lebesgue-Integral.md)

**Q1.** `[Concept]` ★ The Monotone Convergence Theorem says $\int \lim f_n = \lim \int f_n$ when $(f_n)$ is a sequence of measurable functions that is

(A) uniformly bounded and converges pointwise

(B) uniformly convergent on a set of finite measure

(C) dominated by an integrable function

(D) non-negative and pointwise increasing

**Q2.** `[Numerical]` ★ Let $f:[0,1]\to\mathbb R$ be $f(x)=1$ for rational $x$ and $f(x)=x^2$ for irrational $x$. Then $\displaystyle\int_{[0,1]} f\thinspace dm$ (Lebesgue) equals

(A) $1$

(B) $\tfrac{4}{3}$

(C) $\tfrac{1}{3}$

(D) does not exist, because $f$ is not Riemann integrable

**Q3.** `[Numerical]` ★ $\displaystyle\lim_{n\to\infty}\int_0^n\left(1-\frac{x}{n}\right)^n dx$ equals

(A) $0$

(B) $\infty$

(C) $e$

(D) $1$

**Q4.** `[Multi-Statement]` ★★ Consider the following statements.

I. Fatou's lemma: if $f_n\ge 0$ are measurable, then $\int \liminf f_n \le \liminf \int f_n$.

II. The inequality in Fatou's lemma can be strict.

III. Fatou's lemma remains true for arbitrary real-valued measurable $f_n$ (no sign condition).

Which is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** $f(x)=\dfrac{\sin x}{x}$ is not Lebesgue integrable on $(0,\infty)$, although the improper Riemann integral $\int_0^\infty \frac{\sin x}{x}dx$ converges.
**Reason (R):** A measurable function $f$ is Lebesgue integrable if and only if $|f|$ is Lebesgue integrable.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ All functions are on $\mathbb R$ (or the indicated interval) with Lebesgue measure. Match the sequence with its behaviour.

| List-I | List-II |
|---|---|
| (a) $f_n=n\thinspace \chi_{(0,1/n)}$ | 1. $f_n\to 0$ uniformly on $\mathbb R$, but $\int f_n=1$ for all $n$ |
| (b) $f_n=\chi_{[n,n+1]}$ | 2. $f_n\to0$ pointwise, $\int f_n=1$; the mass concentrates near $0$ |
| (c) $f_n=\tfrac1n\chi_{[0,n]}$ | 3. DCT applies and $\int f_n\to 0$ |
| (d) $f_n=x^n$ on $[0,1]$ | 4. $f_n\to0$ pointwise, $\int f_n=1$; the mass "escapes to infinity" |

(A) a-2, b-4, c-1, d-3

(B) a-1, b-4, c-2, d-3

(C) a-2, b-1, c-4, d-3

(D) a-4, b-2, c-1, d-3

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) Every bounded Riemann integrable function on $[a,b]$ is Lebesgue integrable, and the two integrals agree.

(B) A bounded function on $[a,b]$ is Riemann integrable if and only if its set of discontinuities has Lebesgue measure zero.

(C) Every bounded Lebesgue integrable function on $[a,b]$ is Riemann integrable.

(D) The Dirichlet function $\chi_{\mathbb Q}$ is Lebesgue integrable on $[0,1]$ with integral $0$.

**Q8.** `[Concept]` ★★ Which inclusion is correct for $1\le p\lt q\lt \infty$?

(A) $L^p[0,1]\subseteq L^q[0,1]$

(B) $L^q(\mathbb R)\subseteq L^p(\mathbb R)$

(C) $L^p(\mathbb R)\subseteq L^q(\mathbb R)$

(D) $L^q[0,1]\subseteq L^p[0,1]$

**Q9.** `[Numerical]` ★★ The number of integers $p\ge 1$ for which $f(x)=x^{-1/3}$ belongs to $L^p(0,1)$ is

(A) $2$

(B) $1$

(C) $3$

(D) infinitely many

**Q10.** `[Application]` ★★★ $\displaystyle\lim_{n\to\infty}\int_0^\infty \frac{n\sin(x/n)}{x(1+x^2)}\thinspace dx$ equals

(A) $0$

(B) $1$

(C) $\dfrac{\pi}{2}$

(D) $\pi$

**Q11.** `[Application]` ★★ Let $f\in L^2[0,1]$ with $\int_0^1 f\thinspace dx=1$. The minimum possible value of $\int_0^1 f^2\thinspace dx$ is

(A) $0$

(B) $\tfrac12$

(C) $1$

(D) $2$

**Q12.** `[Concept]` ★ For which $p\in[1,\infty]$ is $L^p[0,1]$ a Hilbert space (norm coming from an inner product)?

(A) every $p\in[1,\infty]$

(B) only $p=2$

(C) every $p\in[1,\infty)$

(D) only $p=1$ and $p=2$

**Q13.** `[Concept]` ★★ If $f_n\to f$ in $L^1[0,1]$, then necessarily

(A) $f_n\to f$ almost everywhere

(B) some subsequence $f_{n_k}\to f$ almost everywhere

(C) $f_n\to f$ uniformly outside a set of measure zero

(D) $\Vert f_n\Vert _\infty\to\Vert f\Vert _\infty$

**Q14.** `[Numerical]` ★★★ $\displaystyle\lim_{n\to\infty}\int_0^1 \frac{n\thinspace x^{n-1}}{1+x}\thinspace dx$ equals

(A) $0$

(B) $\tfrac12$

(C) $\ln 2$

(D) $1$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Numerical |
| 3 | D | Numerical |
| 4 | B | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | A | Match |
| 7 | C | NOT-true / Counterexample |
| 8 | D | Concept |
| 9 | A | Numerical |
| 10 | C | Application |
| 11 | C | Application |
| 12 | B | Concept |
| 13 | B | Concept |
| 14 | B | Numerical |

## Solutions
**Q1 — (D).** MCT needs only $0\le f_1\le f_2\le\cdots$ (measurable). No integrable bound is needed, and the limit may be $+\infty$. (C) is the hypothesis of DCT, not MCT.

**Q2 — (C).** $\mathbb Q\cap[0,1]$ has measure zero, so $f=x^2$ a.e. and $\int f=\int_0^1x^2=\tfrac13$. (D) is wrong: $f$ is not Riemann integrable, but its Lebesgue integral exists.

**Q3 — (D).** Write $f_n=(1-x/n)^n\chi_{[0,n]}$. Then $0\le f_n\le e^{-x}$ and $f_n\uparrow e^{-x}$, so by MCT (or DCT) the limit is $\int_0^\infty e^{-x}dx=1$. Directly: $\int_0^n(1-x/n)^ndx=\frac{n}{n+1}\to1$.

**Q4 — (B).** I is Fatou's lemma. II: $f_n=n\chi_{(0,1/n)}$ gives $0\lt 1$. III is false: $f_n=-n\chi_{(0,1/n)}$ gives $\int\liminf f_n=0\gt -1=\liminf\int f_n$.

**Q5 — (A).** $\int_0^\infty|\sin x|/x\thinspace dx=\infty$ (compare with $\sum \frac{c}{k}$ over the intervals $[k\pi,(k+1)\pi]$). The Lebesgue integral is absolute, so $f\notin L^1$ exactly because $|f|\notin L^1$. R is the reason.

**Q6 — (A).** (a) is a tall thin spike at $0$, so 2. (b) is a bump sliding to infinity, so 4. (c) satisfies $\sup|f_n|=1/n\to0$ (uniform convergence) yet $\int f_n=1$, so 1; uniform convergence is not enough on a set of infinite measure. (d) is dominated by $1\in L^1[0,1]$, so DCT gives $\int x^n=\frac1{n+1}\to0$, which is 3.

**Q7 — (C).** $\chi_{\mathbb Q}$ is bounded and Lebesgue integrable, but it is discontinuous everywhere, so it is not Riemann integrable. (A), (B) (Lebesgue's criterion) and (D) are true.

**Q8 — (D).** On a finite measure space, Hölder gives $`\Vert f\Vert _p\le \mu(X)^{1/p-1/q}\Vert f\Vert _q`$, so $`L^q\subseteq L^p`$ for $`p\lt q`$. On $`\mathbb R`$ neither inclusion holds: $`x^{-1/2}\chi_{(0,1)}\in L^1\setminus L^2`$ and $`\frac{1}{x}\chi_{(1,\infty)}\in L^2\setminus L^1`$.

**Q9 — (A).** $\int_0^1x^{-p/3}dx\lt \infty\iff p/3\lt 1\iff p\lt 3$, so $p=1,2$. The tempting answer $3$ fails because $\int_0^1x^{-1}dx$ diverges.

**Q10 — (C).** $\left|\frac{n\sin(x/n)}{x}\right|\le1$, so the integrand is dominated by $\frac{1}{1+x^2}\in L^1$, and it tends to $\frac{1}{1+x^2}$ pointwise. By DCT the limit is $\int_0^\infty\frac{dx}{1+x^2}=\frac\pi2$.

**Q11 — (C).** By Cauchy–Schwarz, $1=\left(\int f\cdot1\right)^2\le\int f^2\cdot\int1^2=\int f^2$, with equality for $f\equiv1$. (A) is impossible because $\int f^2=0$ forces $f=0$ a.e.

**Q12 — (B).** The $L^p$ norm satisfies the parallelogram law only for $p=2$. Every $L^p$, $1\le p\le\infty$, is a Banach space (Riesz–Fischer), but only $L^2$ is a Hilbert space.

**Q13 — (B).** The "typewriter" sequence (indicators of dyadic intervals sweeping $[0,1]$ repeatedly) tends to $0$ in $L^1$ but converges at no point, so (A) fails. Convergence in $L^1$ implies convergence in measure, and that yields an a.e. convergent subsequence (Riesz).

**Q14 — (B).** Integrate by parts: $\int_0^1\frac{nx^{n-1}}{1+x}dx=\left[\frac{x^n}{1+x}\right]_0^1+\int_0^1\frac{x^n}{(1+x)^2}dx=\frac12+O\negthinspace \left(\frac1{n+1}\right)\to\frac12$. The measures $nx^{n-1}dx$ concentrate at $x=1$, so the limit is $g(1)=\frac12$ for $g(x)=\frac{1}{1+x}$. The answer is not $0$, even though the integrand $\to0$ pointwise on $[0,1)$, because there is no integrable dominating function.
