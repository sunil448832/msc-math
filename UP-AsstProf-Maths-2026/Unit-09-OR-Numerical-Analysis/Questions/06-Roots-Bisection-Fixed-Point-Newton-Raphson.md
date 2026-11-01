# Unit 9 · Topic 06 — Roots of Equations: Bisection, Fixed Point Iteration, Newton–Raphson
> Syllabus coverage: Numerical solutions of algebraic equations; Fixed point iteration and Newton-Raphson methods
> Cheatsheet: [../Cheatsheets/06-Roots-Bisection-Fixed-Point-Newton-Raphson.md](../Cheatsheets/06-Roots-Bisection-Fixed-Point-Newton-Raphson.md)

**Q1.** `[Concept]` ★ The order of convergence of the Newton–Raphson method near a simple root is

(A) 1

(B) 1.618

(C) 2

(D) 3

**Q2.** `[Numerical]` ★ A root of $f(x)=0$ lies in $[1,2]$ with $f(1)f(2)\lt 0$. The least number of bisection steps $n$ that guarantees $\dfrac{b-a}{2^n}\lt 10^{-3}$ is

(A) 9

(B) 10

(C) 11

(D) 12

**Q3.** `[Numerical]` ★ One Newton–Raphson step for $x^3-2x-5=0$ starting from $x_0=2$ gives

(A) $2.1$

(B) $2.09$

(C) $2.2$

(D) $1.9$

**Q4.** `[Numerical]` ★★ Newton's iteration $x_{n+1}=\tfrac12\left(x_n+\tfrac{N}{x_n}\right)$ is used to compute $\sqrt5$ with $x_0=2$. Then $x_2$ (to 4 decimals) is

(A) $2.2361$

(B) $2.2500$

(C) $2.2333$

(D) $2.2222$

**Q5.** `[Concept]` ★★ Applying Newton–Raphson to $f(x)=\dfrac1x-N$ gives a division-free iteration for $1/N$. It is

(A) $x_{n+1}=x_n(2-Nx_n)$

(B) $x_{n+1}=x_n(2+Nx_n)$

(C) $x_{n+1}=\tfrac12\left(x_n+\tfrac{1}{Nx_n}\right)$

(D) $x_{n+1}=\tfrac12 x_n(3-Nx_n^2)$

**Q6.** `[Numerical]` ★ One step of the regula falsi (false position) method for $x^3-x-1=0$ on $[1,2]$ gives

(A) $5/4$

(B) $4/3$

(C) $3/2$

(D) $7/6$

**Q7.** `[Multi-Statement]` ★★ Let $g:[a,b]\to\mathbb R$ and consider $x_{n+1}=g(x_n)$.

I. If $g$ is continuous and $g([a,b])\subseteq[a,b]$, then $g$ has a fixed point in $[a,b]$.

II. If, in addition, $|g'(x)|\le k\lt 1$ on $[a,b]$, the fixed point is unique and the iteration converges to it for every $x_0\in[a,b]$.

III. If $\alpha$ is a fixed point with $0\lt |g'(\alpha)|\lt 1$, the convergence is quadratic.

Which are correct?

(A) I only

(B) II and III only

(C) I and II only

(D) I, II and III

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** For a polynomial $f$, the Newton–Raphson method converges to a root for every initial guess $x_0$.
**Reason (R):** Near a simple root, the Newton–Raphson method converges quadratically.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match the method with its order of convergence (to a simple root).

| List-I | List-II |
|---|---|
| A. Bisection | 1. 2 |
| B. Secant | 2. $(1+\sqrt5)/2\approx1.618$ |
| C. Newton–Raphson | 3. 1 (linear) |
| D. Chebyshev's method | 4. 3 |

(A) A-3, B-2, C-1, D-4

(B) A-3, B-1, C-2, D-4

(C) A-2, B-3, C-1, D-4

(D) A-3, B-2, C-4, D-1

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Bisection always converges if $f$ is continuous on $[a,b]$ and $f(a)f(b)\lt 0$.

(B) Regula falsi keeps the root bracketed at every step.

(C) After the start, the secant method needs only one new function evaluation per iteration.

(D) Newton–Raphson needs a bracketing interval with $f(a)f(b)\lt 0$ in order to converge.

**Q11.** `[Application]` ★★ The equation $x^2-3x+2=0$ (roots $1$ and $2$) is rewritten as $x=g(x)=\dfrac{x^2+2}{3}$. The iteration $x_{n+1}=g(x_n)$ is locally convergent

(A) at both roots

(B) only at the root $1$

(C) only at the root $2$

(D) at neither root

**Q12.** `[Application]` ★★★ The iteration $x_{n+1}=x_n+\lambda\thinspace (x_n^2-3)$ converges to $\sqrt3$ at least quadratically when $\lambda$ equals

(A) $-\dfrac{1}{\sqrt3}$

(B) $\dfrac{1}{2\sqrt3}$

(C) $-\dfrac{1}{2\sqrt3}$

(D) $-\dfrac{\sqrt3}{2}$

**Q13.** `[Numerical]` ★★★ Newton–Raphson is applied to $f(x)=(x-1)^2(x+2)$ with $x_0$ close to $1$. With $e_n=x_n-1$, the limit $\lim_{n\to\infty} e_{n+1}/e_n$ is

(A) $0$

(B) $1/2$

(C) $1/3$

(D) $2/3$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Numerical |
| 3 | A | Numerical |
| 4 | A | Numerical |
| 5 | A | Concept |
| 6 | D | Numerical |
| 7 | C | Multi-Statement |
| 8 | D | Assertion-Reason |
| 9 | A | Match |
| 10 | D | NOT-true / Counterexample |
| 11 | B | Application |
| 12 | C | Application |
| 13 | B | Numerical |

## Solutions
**Q1 — (C).** For a simple root $e_{n+1}\approx \dfrac{f''(\alpha)}{2f'(\alpha)}e_n^2$, so the order is 2. 1.618 is the secant order; 3 is Chebyshev/Halley.

**Q2 — (B).** We need $2^n\gt 1000$. Since $2^9=512$ and $2^{10}=1024$, $n=10$.

**Q3 — (A).** $f(2)=8-4-5=-1$ and $f'(2)=3\cdot4-2=10$, so $x_1=2-(-1)/10=2.1$.

**Q4 — (A).** $x_1=(2+2.5)/2=2.25$ and $x_2=(2.25+5/2.25)/2=(2.25+2.2222)/2=2.23611$. (B) is only $x_1$.

**Q5 — (A).** $f'(x)=-1/x^2$, so $x-f/f'=x+x^2(1/x-N)=x(2-Nx)$. (D) is the iteration for $1/\sqrt N$, and (C) still involves a division.

**Q6 — (D).** $f(1)=-1$ and $f(2)=5$, so $x=\dfrac{1\cdot5-2\cdot(-1)}{5-(-1)}=\dfrac76$. (C) is the bisection midpoint.

**Q7 — (C).** I follows from the IVT applied to $g(x)-x$. II is the contraction mapping theorem, with $|x_n-\alpha|\le k^n|x_0-\alpha|$. III is false: when $g'(\alpha)\neq0$, $e_{n+1}\approx g'(\alpha)e_n$, which is linear. Quadratic convergence needs $g'(\alpha)=0$.

**Q8 — (D).** A is false. Newton can cycle or diverge, for example $f(x)=x^3-2x+2$ with $x_0=0$ gives $0\to1\to0\to\cdots$, and it can also land where $f'=0$. R is the standard local result, but it is local only.

**Q9 — (A).** Bisection is linear (the error bound halves each step), secant has order $\frac{1+\sqrt5}{2}$, Newton has order 2, and Chebyshev's method has order 3.

**Q10 — (D).** Newton is an open method: it needs a good starting point, not a sign-change bracket. A, B and C are true. Regula falsi always keeps a sign change, although one endpoint may stay fixed, which makes it linear.

**Q11 — (B).** $g'(x)=2x/3$, so $|g'(1)|=2/3\lt 1$ (attracting) and $|g'(2)|=4/3\gt 1$ (repelling). Starting from $x_0=1.5$, the iterates decrease to 1.

**Q12 — (C).** $g(x)=x+\lambda(x^2-3)$ gives $g'(\sqrt3)=1+2\sqrt3\lambda$. Setting this to 0 gives $\lambda=-\frac1{2\sqrt3}=-\frac{\sqrt3}{6}$, which is exactly Newton's step $-1/f'(\sqrt3)$. (B) has the wrong sign.

**Q13 — (B).** At a root of multiplicity $m$, Newton's iteration function has $g'(\alpha)=1-\frac1m$. Here $m=2$, so the ratio tends to $1/2$ and convergence is only linear. The modified method $x-mf/f'$ restores quadratic convergence. A numerical check confirms the ratio $\to0.5$.
