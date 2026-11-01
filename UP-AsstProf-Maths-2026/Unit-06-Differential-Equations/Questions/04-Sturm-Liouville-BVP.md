# Unit 6 · Topic 04 — Sturm–Liouville Boundary Value Problems
> Syllabus coverage: Sturm-Liouville boundary value problem
> Cheatsheet: [../Cheatsheets/04-Sturm-Liouville-BVP.md](../Cheatsheets/04-Sturm-Liouville-BVP.md)

**Q1.** `[Concept]` ★ The eigenvalues of $y''+\lambda y=0$, $y(0)=0$, $y(\pi)=0$ are

(A) $\lambda=n^2,\ n=0,1,2,\dots$

(B) $\lambda=(2n-1)^2/4,\ n=1,2,\dots$

(C) $\lambda=n\pi,\ n=1,2,\dots$

(D) $\lambda=n^2,\ n=1,2,3,\dots$

**Q2.** `[Numerical]` ★ The smallest eigenvalue of $y''+\lambda y=0$, $y'(0)=0$, $y'(\pi)=0$ is

(A) $0$

(B) $1/4$

(C) $1$

(D) $\pi^2$

**Q3.** `[Numerical]` ★★ The smallest eigenvalue of $y''+\lambda y=0$, $y(0)=0$, $y'(\pi)=0$ is

(A) $1$

(B) $1/2$

(C) $1/4$

(D) $\pi^2/4$

**Q4.** `[Concept]` ★★ The Hermite equation $y''-2xy'+\lambda y=0$, written in Sturm–Liouville (self-adjoint) form, is

(A) $\big(e^{x^2}y'\big)'+\lambda e^{x^2}y=0$

(B) $\big((1-x^2)y'\big)'+\lambda y=0$

(C) $\big(xy'\big)'+\lambda e^{-x}y=0$

(D) $\big(e^{-x^2}y'\big)'+\lambda e^{-x^2}y=0$

**Q5.** `[Multi-Statement]` ★★ For a regular Sturm–Liouville problem $(p y')'+(q+\lambda r)y=0$ on $[a,b]$ with separated boundary conditions ($p\gt 0$, $r\gt 0$), consider:

I. All eigenvalues are real.

II. Eigenfunctions corresponding to distinct eigenvalues are orthogonal on $[a,b]$ with respect to the weight $r(x)$.

III. Each eigenvalue has two linearly independent eigenfunctions.

IV. The eigenvalues form an increasing sequence $\lambda_1\lt \lambda_2\lt \cdots$ with $\lambda_n\to\infty$.

Which are correct?

(A) I and II only

(B) I, II and III only

(C) I, II and IV only

(D) I, II, III and IV

**Q6.** `[Assertion-Reason]` ★★★
**Assertion (A):** For $y''+\lambda y=0$ on $[-\pi,\pi]$ with periodic conditions $y(-\pi)=y(\pi)$, $y'(-\pi)=y'(\pi)$, the eigenvalue $\lambda=1$ has two linearly independent eigenfunctions.
**Reason (R):** In a regular Sturm–Liouville problem with separated boundary conditions, every eigenvalue is simple.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each equation in List-I with the weight function in List-II with respect to which its polynomial solutions are orthogonal.

| List-I | List-II |
|---|---|
| (a) Legendre $(1-x^2)y''-2xy'+n(n+1)y=0$ | 1. $e^{-x^2}$ on $(-\infty,\infty)$ |
| (b) Hermite $y''-2xy'+2ny=0$ | 2. $e^{-x}$ on $(0,\infty)$ |
| (c) Laguerre $xy''+(1-x)y'+ny=0$ | 3. $(1-x^2)^{-1/2}$ on $(-1,1)$ |
| (d) Chebyshev $(1-x^2)y''-xy'+n^2y=0$ | 4. $1$ on $(-1,1)$ |

(A) a-4, b-1, c-2, d-3

(B) a-4, b-2, c-1, d-3

(C) a-3, b-1, c-2, d-4

(D) a-4, b-1, c-3, d-2

**Q8.** `[NOT-true / Counterexample]` ★★ Consider $y''+q(x)y=0$ with $q$ continuous. Which of the following is **NOT** true?

(A) The zeros of a non-trivial solution are isolated.

(B) The zeros of two linearly independent solutions strictly interlace.

(C) If $q(x)\lt 0$ on an interval, a non-trivial solution can have infinitely many zeros there.

(D) If $q_2\gt q_1$, then between any two consecutive zeros of a non-trivial solution of $y''+q_1y=0$ there is at least one zero of every solution of $y''+q_2y=0$.

**Q9.** `[Numerical]` ★★★ The Green's function $G(x,s)$ for $-y''=f(x)$, $y(0)=y(1)=0$ (so that $y(x)=\int_0^1G(x,s)f(s)\thinspace ds$) gives $G\negthinspace \left(\tfrac14,\tfrac12\right)=$

(A) $1/8$

(B) $-1/8$

(C) $3/16$

(D) $1/16$

**Q10.** `[Application]` ★★ Let $y$ be a non-trivial solution of $y''+q(x)y=0$, where $4\le q(x)\le 9$ for all $x$. The distance $d$ between two consecutive zeros of $y$ satisfies

(A) $\pi/9\le d\le\pi/4$

(B) $\pi/3\le d\le\pi/2$

(C) $2\pi/3\le d\le\pi$

(D) $d=\pi/2$ exactly

**Q11.** `[Numerical]` ★★★ The eigenvalues of $x^2y''+xy'+\lambda y=0$, $y(1)=0$, $y(e)=0$ are

(A) $\lambda=n^2,\ n=1,2,\dots$

(B) $\lambda=n^2\pi^2,\ n=1,2,\dots$

(C) $\lambda=n^2\pi^2/e^2,\ n=1,2,\dots$

(D) $\lambda=n\pi,\ n=1,2,\dots$

**Q12.** `[Concept]` ★ The operator $L[y]=a_0(x)y''+a_1(x)y'+a_2(x)y$ is formally self-adjoint if and only if

(A) $a_0=a_1$

(B) $a_1'=a_2$

(C) $a_0''=a_2$

(D) $a_0'=a_1$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | A | Numerical |
| 3 | C | Numerical |
| 4 | D | Concept |
| 5 | C | Multi-Statement |
| 6 | B | Assertion-Reason |
| 7 | A | Match |
| 8 | C | NOT-true / Counterexample |
| 9 | A | Numerical |
| 10 | B | Application |
| 11 | B | Numerical |
| 12 | D | Concept |

## Solutions
**Q1 — (D).** For $\lambda\le0$ only the trivial solution satisfies the conditions. For $\lambda=k^2\gt 0$, $y=\sin kx$ with $\sin k\pi=0$, so $k=n\ge1$. The value $n=0$ (option A) gives $y\equiv0$, which is not an eigenfunction.

**Q2 — (A).** With Neumann conditions, $\lambda=0$ has the eigenfunction $y=1$. The eigenvalues are $n^2$ for $n=0,1,2,\dots$, with eigenfunctions $\cos nx$.

**Q3 — (C).** $y=\sin\sqrt\lambda x$ and $\cos\sqrt\lambda\thinspace \pi=0$ give $\sqrt\lambda=\frac{2n-1}{2}$. So $\lambda_1=1/4$. $\pi^2/4$ is what you get by confusing $L=\pi$ with $L=1$.

**Q4 — (D).** The integrating factor is $p=e^{\int -2x\thinspace dx}=e^{-x^2}$. Multiplying gives $e^{-x^2}y''-2xe^{-x^2}y'=(e^{-x^2}y')'$, so the weight is $e^{-x^2}$. (C) is the Laguerre form and (B) is Legendre.

**Q5 — (C).** For separated conditions, each eigenvalue is **simple** (one-dimensional eigenspace), so III is false. I, II and IV are the standard theorems.

**Q6 — (B).** With periodic conditions, $\cos x$ and $\sin x$ both belong to $\lambda=1$, so A is true. R is a true theorem, but periodic conditions are not separated, so R does not explain A. Rather, A shows that R needs the separated-BC hypothesis.

**Q7 — (A).** These are the standard weights: Legendre $1$, Hermite $e^{-x^2}$, Laguerre $e^{-x}$, Chebyshev $(1-x^2)^{-1/2}$.

**Q8 — (C).** If $q\lt 0$ and $y(x_0)=0$, then $y''=-qy$ has the sign of $y$, so $y$ is convex where it is positive and concave where it is negative. A non-trivial solution then has **at most one** zero, so it is non-oscillatory. (A) holds by uniqueness, (B) is the Sturm separation theorem, and (D) is the Sturm comparison theorem.

**Q9 — (A).** $G(x,s)=x(1-s)$ for $x\le s$ and $s(1-x)$ for $x\ge s$. Here $x=\frac14\le s=\frac12$, so $G=\frac14\cdot\frac12=\frac18$. The sign is positive because the equation is $-y''=f$; for $y''=f$ the Green's function would be $-G$.

**Q10 — (B).** By Sturm comparison with $y''+4y=0$ (zeros spaced $\pi/2$) and $y''+9y=0$ (zeros spaced $\pi/3$), the larger $q$ gives zeros that are closer together. So $\pi/3\le d\le\pi/2$.

**Q11 — (B).** Put $x=e^t$, $t\in[0,1]$. The equation becomes $\ddot y+\lambda y=0$ with $y(0)=y(1)=0$, so $\lambda=n^2\pi^2$ and $y_n=\sin(n\pi\ln x)$. These are orthogonal with weight $1/x$, since the self-adjoint form is $(xy')'+\frac{\lambda}{x}y=0$.

**Q12 — (D).** $L^\ast [y]=(a_0y)''-(a_1y)'+a_2y$, and $L^\ast =L$ iff $a_0'=a_1$. Then $L[y]=(a_0y')'+a_2y$.
