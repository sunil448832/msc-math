# Unit 3 · Topic 01 — Sequences and Series of Functions, Uniform Convergence
> Syllabus coverage: Sequence and series of functions, uniform convergence (with the real sequence/series basics that are usually asked: limsup/liminf, convergence tests, Weierstrass M-test, Dini's theorem, radius of convergence of power series)
> Cheatsheet: [../Cheatsheets/01-Sequences-Series-of-Functions-Uniform-Convergence.md](../Cheatsheets/01-Sequences-Series-of-Functions-Uniform-Convergence.md)

**Q1.** `[Concept]` ★ A power series $\sum a_n x^n$ has radius of convergence $R$ with $0<R<\infty$. Then the series necessarily converges uniformly on

(A) $(-R,R)$

(B) $\mathbb{R}$

(C) $[-R,R]$

(D) every closed interval $[-r,r]$ with $0<r<R$

**Q2.** `[Numerical]` ★ Let $a_n = (-1)^n\dfrac{n}{n+1} + \cos\dfrac{n\pi}{2}$. Then $\limsup a_n - \liminf a_n$ equals

(A) $1$

(B) $2$

(C) $3$

(D) $4$

**Q3.** `[Multi-Statement]` ★ Let $f_n(x)=x^n$.

I. On $[0,1]$, $(f_n)$ converges pointwise to a discontinuous function.

II. $(f_n)$ converges uniformly on $[0,a]$ for every $0<a<1$.

III. $(f_n)$ converges uniformly on $[0,1)$.

Which of the above is/are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q4.** `[Assertion-Reason]` ★★
**Assertion (A):** $\displaystyle\sum_{n=1}^\infty \frac{\sin nx}{n^2}$ converges uniformly on $\mathbb{R}$ and its sum is continuous on $\mathbb{R}$.
**Reason (R):** $\left|\dfrac{\sin nx}{n^2}\right|\le \dfrac1{n^2}$ for all $x$, and $\sum \dfrac1{n^2}<\infty$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q5.** `[Match]` ★★ Match the series in List-I with their behaviour in List-II.

| List-I | List-II |
|---|---|
| a. $\sum_{n\ge2} \dfrac{1}{n\log n}$ | 1. converges (root test gives limit $1/e$) |
| b. $\sum_{n\ge2} \dfrac{1}{n(\log n)^2}$ | 2. diverges (Cauchy condensation / integral test) |
| c. $\sum_{n\ge1} \dfrac{(-1)^n}{n}$ | 3. converges absolutely (Cauchy condensation / integral test) |
| d. $\sum_{n\ge1} \left(\dfrac{n}{n+1}\right)^{n^2}$ | 4. converges conditionally |

(A) a-2, b-3, c-4, d-1

(B) a-3, b-2, c-4, d-1

(C) a-2, b-3, c-1, d-4

(D) a-2, b-4, c-3, d-1

**Q6.** `[NOT-true / Counterexample]` ★★ Which of the following statements is **NOT** true?

(A) A uniform limit of continuous functions on a set $E\subseteq\mathbb{R}$ is continuous on $E$.

(B) A uniform limit of differentiable functions on $[-1,1]$ is differentiable on $[-1,1]$.

(C) If $f_n\to f$ uniformly on $[a,b]$ and each $f_n$ is Riemann integrable, then $\int_a^b f_n\to\int_a^b f$.

(D) If $f_n\to f$ and $g_n\to g$ uniformly on $E$, then $f_n+g_n\to f+g$ uniformly on $E$.

**Q7.** `[Application]` ★★ Which of the following sequences converges **uniformly** on $[0,1]$?

(A) $\dfrac{nx}{1+n^2x^2}$

(B) $nx^n(1-x)$

(C) $nx(1-x)^n$

(D) $\dfrac{x}{1+nx^2}$

**Q8.** `[Numerical]` ★★ Let $f_n(x)=n^2xe^{-nx}$ on $[0,1]$. Then $\displaystyle\lim_{n\to\infty}\int_0^1 f_n(x)\,dx$ equals

(A) $0$

(B) $1/e$

(C) $1$

(D) $\infty$

**Q9.** `[Numerical]` ★★ Let $a_n=2^n$ if $n$ is even and $a_n=3^n$ if $n$ is odd. The radius of convergence of $\sum a_n z^n$ is

(A) $1/2$

(B) $1/3$

(C) $1/\sqrt6$

(D) $2/5$

**Q10.** `[NOT-true / Counterexample]` ★★★ Dini's theorem: if $f_n$ are continuous on a compact set $K$, $f_n(x)\downarrow f(x)$ for every $x$ and $f$ is continuous, then $f_n\to f$ uniformly. Which sequence shows that **compactness** of $K$ cannot be dropped?

(A) $x^n$ on $[0,1)$

(B) $x^n$ on $[0,1]$

(C) $x/n$ on $[0,1]$

(D) $\dfrac{nx}{1+n^2x^2}$ on $[0,1]$

**Q11.** `[Application]` ★★★ Consider $\displaystyle S(x)=\sum_{n=0}^{\infty}\frac{x^2}{(1+x^2)^n}$, $x\in\mathbb{R}$. Which statement is correct?

(A) The series converges uniformly on $\mathbb{R}$ and $S(x)=1+x^2$ for all $x$.

(B) The series converges pointwise on $\mathbb{R}$, but not uniformly on any interval containing $0$.

(C) The series diverges at $x=0$.

(D) The series converges uniformly on $[-1,1]$ because each term is continuous and bounded by $1$.

**Q12.** `[Numerical]` ★ The interval of convergence of $\displaystyle\sum_{n=1}^\infty \frac{(x-2)^n}{n\,3^n}$ is

(A) $(-1,5)$

(B) $[-1,5)$

(C) $(-1,5]$

(D) $[-1,5]$

**Q13.** `[Multi-Statement]` ★★ Consider the following statements about real sequences.

I. Every bounded real sequence has a convergent subsequence.

II. Every Cauchy sequence of rational numbers converges to a rational number.

III. A monotone real sequence converges if and only if it is bounded.

Which of the above is/are correct?

(A) I only

(B) II and III only

(C) I and III only

(D) I, II and III

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | C | Numerical |
| 3 | D | Multi-Statement |
| 4 | A | Assertion-Reason |
| 5 | A | Match |
| 6 | B | NOT-true / Counterexample |
| 7 | D | Application |
| 8 | C | Numerical |
| 9 | B | Numerical |
| 10 | A | NOT-true / Counterexample |
| 11 | B | Application |
| 12 | B | Numerical |
| 13 | C | Multi-Statement |

## Solutions
**Q1 — (D).** On $[-r,r]$ with $r<R$, $|a_nx^n|\le |a_n|r^n$ and $\sum|a_n|r^n<\infty$, so the M-test applies. Uniform convergence on all of $(-R,R)$ can fail: $\sum x^n$ ($R=1$) is not uniformly convergent on $(-1,1)$ since the partial sums are unbounded near $1$. (C) fails because the series may diverge at $\pm R$.

**Q2 — (C).** For $n\equiv0\pmod 4$: $a_n\to 1+1=2$; $n\equiv2$: $a_n\to1-1=0$; $n$ odd: $a_n\to-1+0=-1$. So $\limsup=2$, $\liminf=-1$, and the difference is $3$. A common mistake is to treat the two terms separately and add their limsups ($1+1$) and liminfs ($-1-1$), which gives $4$.

**Q3 — (D).** Pointwise limit is $0$ on $[0,1)$ and $1$ at $x=1$, which is discontinuous. On $[0,a]$, $\sup|x^n|=a^n\to0$. On $[0,1)$, $\sup_{[0,1)}x^n=1$ for every $n$, so the convergence is not uniform there (even though the limit $0$ is continuous on $[0,1)$).

**Q4 — (A).** R is exactly the Weierstrass M-test, which gives uniform convergence. A uniform limit of continuous partial sums is continuous. So R explains A.

**Q5 — (A).** (a) Condensation: $\sum 2^k\cdot\frac{1}{2^k k\log2}=\sum\frac1{k\log 2}$ diverges. (b) Condensation gives $\sum \frac{1}{k^2(\log 2)^2}$, which converges. (c) Converges by the Leibniz test but not absolutely, so it converges conditionally. (d) $\sqrt[n]{a_n}=(1+1/n)^{-n}\to 1/e<1$.

**Q6 — (B).** $f_n(x)=\sqrt{x^2+1/n}$ is differentiable and converges uniformly to $|x|$, because $0\le f_n-|x|\le 1/\sqrt n$. But $|x|$ is not differentiable at $0$. For differentiation you need uniform convergence of $f_n'$ and convergence of $f_n$ at one point.

**Q7 — (D).** $\sup\frac{x}{1+nx^2}=\frac1{2\sqrt n}$ (at $x=1/\sqrt n$), which tends to $0$. For the others: (A) has value $1/2$ at $x=1/n$. (B) and (C) both have sup $\to 1/e$, attained near $x=\frac{n}{n+1}$ and $x=\frac1{n+1}$ respectively. All three have pointwise limit $0$, so they do not converge uniformly.

**Q8 — (C).** $\int_0^1 n^2xe^{-nx}dx = 1-(n+1)e^{-n}\to1$, although $f_n\to0$ pointwise. So the limit and the integral cannot be interchanged (the convergence is not uniform: $f_n(1/n)=n/e$). The tempting answer $0$ comes from interchanging them.

**Q9 — (B).** Cauchy–Hadamard: $\limsup|a_n|^{1/n}=\max(2,3)=3$, so $R=1/3$. The answer comes from the limsup, not from an average of $2$ and $3$.

**Q10 — (A).** On $[0,1)$ the functions $x^n$ are continuous and decrease to $0$, which is continuous, but $\sup_{[0,1)}x^n=1$. Every hypothesis except compactness holds. (B) fails a different hypothesis (the limit is discontinuous). (C) converges uniformly. (D) is not monotone in $n$.

**Q11 — (B).** For $x\ne0$ this is a geometric series with ratio $\frac{1}{1+x^2}<1$, so the sum is $x^2\cdot\frac{1}{1-1/(1+x^2)}=1+x^2$. At $x=0$ every term is $0$, so $S(0)=0$. The sum is discontinuous at $0$ while the partial sums are continuous, so the convergence cannot be uniform on any interval containing $0$. (D) is wrong because a bound by $1$ is not a summable M-test bound.

**Q12 — (B).** The ratio test gives $|x-2|<3$. At $x=5$ we get $\sum 1/n$, which diverges. At $x=-1$ we get $\sum(-1)^n/n$, which converges. So the interval is $[-1,5)$.

**Q13 — (C).** I is Bolzano–Weierstrass and III is the monotone convergence theorem. II is false: the decimal truncations of $\sqrt2$ form a Cauchy sequence in $\mathbb{Q}$ with no rational limit, because $\mathbb{Q}$ is not complete.
