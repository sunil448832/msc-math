# Unit 3 · Topic 02 — Fourier Series
> Syllabus coverage: Fourier series (Euler coefficients, Dirichlet conditions and pointwise convergence, even/odd functions, half-range series, arbitrary period $2L$, Parseval's identity, summing numerical series using Fourier series)
> Cheatsheet: [../Cheatsheets/02-Fourier-Series.md](../Cheatsheets/02-Fourier-Series.md)

**Q1.** `[Concept]` ★ If $f$ is an odd function on $(-\pi,\pi)$, then its Fourier series contains

(A) only cosine terms, including the constant term

(B) only cosine terms, without the constant term

(C) both sine and cosine terms in general

(D) only sine terms

**Q2.** `[Numerical]` ★ In the Fourier series of $f(x)=x$ on $(-\pi,\pi)$, the coefficient of $\sin 3x$ is

(A) $-\dfrac23$

(B) $\dfrac23$

(C) $\dfrac{2}{3\pi}$

(D) $\dfrac13$

**Q3.** `[Numerical]` ★★ Given that on $[-\pi,\pi]$
$$x^2=\frac{\pi^2}{3}+4\sum_{n=1}^\infty\frac{(-1)^n\cos nx}{n^2},$$
the value of $1-\dfrac1{2^2}+\dfrac1{3^2}-\dfrac1{4^2}+\cdots$ is

(A) $\dfrac{\pi^2}{6}$

(B) $\dfrac{\pi^2}{8}$

(C) $\dfrac{\pi^2}{12}$

(D) $\dfrac{\pi^2}{24}$

**Q4.** `[Numerical]` ★★★ Applying Parseval's identity to the Fourier series of $x^2$ on $(-\pi,\pi)$ (given in Q3) gives $\displaystyle\sum_{n=1}^\infty\frac1{n^4}=$

(A) $\dfrac{\pi^4}{72}$

(B) $\dfrac{\pi^4}{90}$

(C) $\dfrac{\pi^4}{96}$

(D) $\dfrac{\pi^4}{48}$

**Q5.** `[Application]` ★★ Let $f(x)=0$ for $-\pi\lt x\lt 0$ and $f(x)=x$ for $0\lt x\lt \pi$, extended $2\pi$-periodically. The Fourier series of $f$ at $x=\pi$ converges to

(A) $0$

(B) $\pi$

(C) $\dfrac{\pi}{2}$

(D) $\dfrac{\pi}{4}$

**Q6.** `[Multi-Statement]` ★★ Consider the following statements.

I. If $f$ is $2\pi$-periodic and piecewise smooth, its Fourier series converges at every $x$ to $\tfrac12\big[f(x^+)+f(x^-)\big]$.

II. If $f$ is Riemann (or Lebesgue) integrable on $[-\pi,\pi]$, then $a_n\to0$ and $b_n\to0$.

III. The Fourier series of every continuous $2\pi$-periodic function converges at every point.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** The Fourier series of $f(x)=x$ on $(-\pi,\pi)$ converges uniformly on $\mathbb{R}$.
**Reason (R):** The Fourier coefficients of $f$ tend to $0$ as $n\to\infty$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match each function (List-I) with its Fourier series (List-II). Sums over "$`n`$ odd" mean $`n=1,3,5,\dots`$

| List-I | List-II |
|---|---|
| a. $1$, half-range **sine** series on $(0,\pi)$ | 1. $\dfrac{\pi}{2}-\dfrac4\pi\sum_{n\text{ odd}}\dfrac{\cos nx}{n^2}$ |
| b. $x$, half-range **cosine** series on $(0,\pi)$ | 2. $\dfrac{\pi^2}{3}+4\sum_{n\ge1}\dfrac{(-1)^n\cos nx}{n^2}$ |
| c. $x$ on $(-\pi,\pi)$ | 3. $\dfrac4\pi\sum_{n\text{ odd}}\dfrac{\sin nx}{n}$ |
| d. $x^2$ on $(-\pi,\pi)$ | 4. $2\sum_{n\ge1}\dfrac{(-1)^{n+1}\sin nx}{n}$ |

(A) a-3, b-1, c-4, d-2

(B) a-1, b-3, c-4, d-2

(C) a-3, b-1, c-2, d-4

(D) a-4, b-1, c-3, d-2

**Q9.** `[Numerical]` ★★ For $f(x)=x$ on $(-2,2)$ (period $4$), the coefficient $b_1$ of $\sin\dfrac{\pi x}{2}$ in its Fourier series is

(A) $\dfrac{4}{\pi}$

(B) $\dfrac{2}{\pi}$

(C) $\dfrac{8}{\pi}$

(D) $\dfrac{4}{\pi^2}$

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is **NOT** true?

(A) The half-range sine series of $f$ on $(0,\pi)$ is the Fourier series of the odd extension of $f$ to $(-\pi,\pi)$.

(B) Near a jump discontinuity, the partial sums overshoot by an amount that does not go to $0$ as $n\to\infty$ (Gibbs phenomenon).

(C) For every square-integrable $f$, $\dfrac{a_0^2}{2}+\sum_{n\ge1}(a_n^2+b_n^2)$ converges.

(D) If $\sum(|a_n|+|b_n|)\lt \infty$, then the sum of the Fourier series must be differentiable everywhere.

**Q11.** `[Numerical]` ★★★ In the Fourier series of $f(x)=|\sin x|$ on $(-\pi,\pi)$, the coefficient of $\cos 2x$ is

(A) $-\dfrac{4}{3\pi}$

(B) $\dfrac{4}{3\pi}$

(C) $-\dfrac{2}{3\pi}$

(D) $0$

**Q12.** `[Concept]` ★ For a positive integer $`n`$, $`\displaystyle\int_{-\pi}^{\pi}\sin^2 nx\thinspace dx`$ equals

(A) $0$

(B) $\pi/2$

(C) $\pi$

(D) $2\pi$

**Q13.** `[Application]` ★★★ Let $f(x)=x^2$ for $0\lt x\lt 2\pi$, extended to $\mathbb{R}$ with period $2\pi$. Its Fourier series at $x=0$ converges to

(A) $0$

(B) $\pi^2$

(C) $2\pi^2$

(D) $4\pi^2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | B | Numerical |
| 5 | C | Application |
| 6 | B | Multi-Statement |
| 7 | D | Assertion-Reason |
| 8 | A | Match |
| 9 | A | Numerical |
| 10 | D | NOT-true / Counterexample |
| 11 | A | Numerical |
| 12 | C | Concept |
| 13 | C | Application |

## Solutions
**Q1 — (D).** For odd $f$, $f\cos nx$ is odd, so every $a_n=0$, including $a_0$. Only the $b_n\sin nx$ terms survive.

**Q2 — (B).** $b_n=\frac{2}{\pi}\int_0^\pi x\sin nx\thinspace dx=\frac{2(-1)^{n+1}}{n}$. For $n=3$ this is $+\frac23$. Option (A) has the sign wrong.

**Q3 — (C).** Put $x=0$: $0=\frac{\pi^2}{3}+4\sum\frac{(-1)^n}{n^2}$, so $\sum\frac{(-1)^{n+1}}{n^2}=\frac{\pi^2}{12}$. (A) $\frac{\pi^2}{6}$ comes from $x=\pi$ instead, and gives $\sum 1/n^2$.

**Q4 — (B).** Parseval: $\frac1\pi\int_{-\pi}^{\pi}x^4dx=\frac{a_0^2}{2}+\sum a_n^2$. Here $\frac{2\pi^4}{5}=\frac{2\pi^4}{9}+16\sum\frac1{n^4}$, so $\sum\frac1{n^4}=\frac{1}{16}\cdot\frac{8\pi^4}{45}=\frac{\pi^4}{90}$. Note that $a_0=\frac{2\pi^2}{3}$, so $\frac{a_0^2}{2}=\frac{2\pi^4}{9}$. The usual error is to use $a_0^2$ in place of $\frac{a_0^2}{2}$.

**Q5 — (C).** $x=\pi$ is a jump of the periodic extension: $f(\pi^-)=\pi$ and $f(\pi^+)=f(-\pi^+)=0$. By Dirichlet's theorem the series converges to $\frac{\pi+0}{2}=\frac\pi2$.

**Q6 — (B).** I is the Dirichlet convergence theorem. II is the Riemann–Lebesgue lemma. III is false: du Bois-Reymond constructed a continuous function whose Fourier series diverges at a point (Carleson: it still converges a.e. for $L^2$ functions). Continuity alone is not enough; Dini/Lipschitz-type conditions are.

**Q7 — (D).** The series is $2\sum\frac{(-1)^{n+1}\sin nx}{n}$. Its sum is the $2\pi$-periodic extension of $x$, which jumps at $x=\pm\pi,\pm3\pi,\dots$ (the series gives $0$ there). A uniform limit of continuous partial sums would be continuous, so A is false. R is true by Riemann–Lebesgue.

**Q8 — (A).** a: $`b_n=\frac2\pi\int_0^\pi\sin nx\thinspace dx=\frac{4}{n\pi}`$ for odd $`n`$ and $`0`$ for even $`n`$, giving 3. b: $`a_0=\pi`$ and $`a_n=-\frac{4}{\pi n^2}`$ for odd $`n`$, giving 1. c gives 4 and d gives 2.

**Q9 — (A).** $b_n=\frac1L\int_{-L}^{L}x\sin\frac{n\pi x}{L}dx=\frac{2L(-1)^{n+1}}{n\pi}$. With $L=2$ and $n=1$, $b_1=\frac4\pi$. Using the $2\pi$-period formula by mistake gives $2/\pi$-type answers.

**Q10 — (D).** Absolute convergence of the coefficient series gives uniform convergence to a **continuous** function, not a differentiable one. The Weierstrass function $\sum a^n\cos(b^n x)$ ($0\lt a\lt 1$, $b$ odd, $ab\gt 1+\frac{3\pi}2$) has absolutely summable coefficients and is nowhere differentiable. (A) is the definition. (B) is Gibbs (about $9\text{ percent}$ of the jump). (C) is Bessel's inequality.

**Q11 — (A).** $|\sin x|$ is even, so $a_n=\frac2\pi\int_0^\pi\sin x\cos nx\thinspace dx$. For $n=2$ this is $\frac{2}{\pi}\cdot\left(-\frac23\right)=-\frac{4}{3\pi}$. In general $|\sin x|=\frac2\pi-\frac4\pi\sum_{m\ge1}\frac{\cos 2mx}{4m^2-1}$.

**Q12 — (C).** $\int_{-\pi}^{\pi}\sin^2nx\thinspace dx=\int_{-\pi}^{\pi}\frac{1-\cos2nx}{2}dx=\pi$. This is the normalising constant behind $a_n,b_n=\frac1\pi\int\cdots$.

**Q13 — (C).** $x=0$ is a jump of the periodic extension: $f(0^+)=0$ and $f(0^-)=\lim_{x\to2\pi^-}x^2=4\pi^2$. The average is $2\pi^2$. Answering $0$ ignores the left-hand limit coming from the previous period.
