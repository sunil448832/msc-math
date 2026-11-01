# Unit 6 · Topic 07 — Separation of Variables: Laplace, Heat and Wave Equations
> Syllabus coverage: Method of separation of variables for Laplace, Heat and Wave equations
> Cheatsheet: [../Cheatsheets/07-Separation-of-Variables-Laplace-Heat-Wave.md](../Cheatsheets/07-Separation-of-Variables-Laplace-Heat-Wave.md)

**Q1.** `[Concept]` ★ The solution of $u_{tt}=c^2u_{xx}$ on $-\infty\lt x\lt \infty$, $u(x,0)=f(x)$, $u_t(x,0)=g(x)$ is

(A) $u=\tfrac12[f(x+ct)+f(x-ct)]+\dfrac{1}{2c}\displaystyle\int_{x-ct}^{x+ct}g(s)\thinspace ds$

(B) $u=\tfrac12[f(x+ct)-f(x-ct)]+\dfrac{1}{2c}\displaystyle\int_{x-ct}^{x+ct}g(s)\thinspace ds$

(C) $u=f(x+ct)+f(x-ct)+\dfrac{1}{c}\displaystyle\int_{x-ct}^{x+ct}g(s)\thinspace ds$

(D) $u=\tfrac12[f(x+ct)+f(x-ct)]+\dfrac{c}{2}\displaystyle\int_{x-ct}^{x+ct}g(s)\thinspace ds$

**Q2.** `[Numerical]` ★★ If $u_{tt}=u_{xx}$ on $\mathbb{R}$ with $u(x,0)=x^2$ and $u_t(x,0)=2x$, then $u(1,1)=$

(A) $2$

(B) $3$

(C) $4$

(D) $5$

**Q3.** `[Numerical]` ★ Let $u_t=u_{xx}$ for $0\lt x\lt \pi$, $t\gt 0$, with $u(0,t)=u(\pi,t)=0$ and $u(x,0)=3\sin x-5\sin 4x$. Then $u(\pi/2,t)=$

(A) $3e^{-t}-5e^{-16t}$

(B) $3e^{-t}-5e^{-4t}$

(C) $3e^{-t}+5e^{-16t}$

(D) $3e^{-t}$

**Q4.** `[Numerical]` ★★ For $u_{tt}=4u_{xx}$ on $0\lt x\lt \pi$ with fixed ends, $u(x,0)=\sin 3x$ and $u_t(x,0)=0$, the solution is periodic in $t$ with (least) period

(A) $\pi/3$

(B) $2\pi/3$

(C) $\pi/6$

(D) $\pi$

**Q5.** `[Numerical]` ★★ For $u_t=u_{xx}$ on $0\lt x\lt \pi$ with $u(0,t)=u(\pi,t)=0$ and $u(x,0)=x$, the coefficient of $e^{-4t}\sin 2x$ in the series solution is

(A) $1$

(B) $-1/2$

(C) $2$

(D) $-1$

**Q6.** `[Concept]` ★★ For $u_{xx}+u_{yy}=0$ in the rectangle $0\lt x\lt a$, $0\lt y\lt b$, with $u=0$ on $x=0$, $x=a$ and $y=0$, and $u(x,b)=f(x)$, the separated solutions have the form

(A) $\sin\dfrac{n\pi x}{a}\thinspace \cosh\dfrac{n\pi y}{a}$

(B) $\sin\dfrac{n\pi x}{a}\thinspace \sinh\dfrac{n\pi y}{a}$

(C) $\sinh\dfrac{n\pi x}{a}\thinspace \sin\dfrac{n\pi y}{a}$

(D) $\sin\dfrac{n\pi x}{a}\thinspace e^{-n\pi y/a}$

**Q7.** `[Multi-Statement]` ★★ Consider:

I. For $u_t=ku_{xx}$ on $0\lt x\lt L$ with $u(0,t)=0$ and $u(L,t)=100$, the steady-state temperature is $100x/L$.

II. The solution of the heat equation on $0\lt x\lt L$ with $u(0,t)=u(L,t)=0$ tends to $0$ as $t\to\infty$.

III. For the vibrating string with fixed ends, $E(t)=\tfrac12\int_0^L(u_t^2+c^2u_x^2)\thinspace dx$ is constant in time.

IV. The bounded solution of Laplace's equation inside the unit disc contains terms $r^{-n}\cos n\theta$.

Which are correct?

(A) I and II only

(B) I, II and III only

(C) II, III and IV only

(D) I, II, III and IV

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** For $u_t=ku_{xx}$ on $0\lt x\lt L$ with insulated ends $u_x(0,t)=u_x(L,t)=0$ and $u(x,0)=f(x)$, we have $u(x,t)\to\dfrac1L\displaystyle\int_0^Lf(x)\thinspace dx$ as $t\to\infty$.
**Reason (R):** The Neumann problem has the eigenvalue $\lambda=0$ with constant eigenfunction, while all other modes carry factors $e^{-k(n\pi/L)^2t}\to0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ For separation of variables on $0\lt x\lt L$, match the boundary conditions in List-I with the spatial eigenfunctions in List-II.

| List-I | List-II |
|---|---|
| (a) $u(0)=u(L)=0$ | 1. $\cos\dfrac{n\pi x}{L},\ n\ge0$ |
| (b) $u_x(0)=u_x(L)=0$ | 2. $\sin\dfrac{(2n-1)\pi x}{2L},\ n\ge1$ |
| (c) $u(0)=0,\ u_x(L)=0$ | 3. $\sin\dfrac{n\pi x}{L},\ n\ge1$ |
| (d) $u$ periodic of period $2L$ on $[-L,L]$ | 4. $1,\ \cos\dfrac{n\pi x}{L},\ \sin\dfrac{n\pi x}{L}$ |

(A) a-3, b-1, c-4, d-2

(B) a-1, b-3, c-2, d-4

(C) a-3, b-1, c-2, d-4

(D) a-3, b-2, c-1, d-4

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following statements is **NOT** true?

(A) A harmonic function in a bounded domain, continuous up to the boundary, attains its maximum on the boundary.

(B) The value of a harmonic function at the centre of a disc equals its average over the boundary circle.

(C) Like the heat equation, the wave equation smooths out discontinuities in the initial data for $t\gt 0$.

(D) The heat equation $u_t=ku_{xx}$ ($k\gt 0$) on a bounded interval with zero Dirichlet data has a unique solution for given continuous initial data.

**Q11.** `[Application]` ★★★ Let $u$ be harmonic in the unit disc with boundary values $u(1,\theta)=\cos^2\theta$. Then the value of $u$ at the point with polar coordinates $r=\tfrac12$, $\theta=0$ is

(A) $1/2$

(B) $1/4$

(C) $3/4$

(D) $5/8$

**Q12.** `[Numerical]` ★★★ A string of length $\pi$ with fixed ends satisfies $u_{tt}=u_{xx}$, $u(x,0)=0$, $u_t(x,0)=\sin 2x$. The maximum displacement (over $t$) of the point $x=\pi/4$ is

(A) $1$

(B) $1/2$

(C) $1/4$

(D) $2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | C | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | D | Numerical |
| 6 | B | Concept |
| 7 | B | Multi-Statement |
| 8 | A | Assertion-Reason |
| 9 | C | Match |
| 10 | C | NOT-true / Counterexample |
| 11 | D | Application |
| 12 | B | Numerical |

## Solutions
**Q1 — (A).** This is d'Alembert's formula. Check: at $t=0$ it gives $f$, and $u_t(x,0)=\frac{c}{2}[f'-f']+\frac{1}{2c}\cdot 2c\thinspace g=g$. Option (D) has $c/2$ instead of $1/(2c)$.

**Q2 — (C).** $u=\frac12[(x+t)^2+(x-t)^2]+\frac12\int_{x-t}^{x+t}2s\thinspace ds=x^2+t^2+2xt=(x+t)^2$, so $u(1,1)=4$. Ignoring $g$ gives $x^2+t^2=2$ (option A).

**Q3 — (D).** $u=3e^{-t}\sin x-5e^{-16t}\sin 4x$. At $x=\pi/2$, $\sin 2\pi=0$, leaving $3e^{-t}$. Option (A) forgets to evaluate $\sin 4x$. Option (B) uses $e^{-nt}$ instead of $e^{-n^2t}$.

**Q4 — (A).** $u=\sin 3x\cos(3\cdot2\thinspace t)=\sin3x\cos6t$, with period $2\pi/6=\pi/3$. Forgetting $c=2$ gives $2\pi/3$ (option B).

**Q5 — (D).** $b_n=\frac2\pi\int_0^\pi x\sin nx\thinspace dx=\frac{2(-1)^{n+1}}{n}$, so $b_2=-1$, and $u=\sum b_ne^{-n^2t}\sin nx$.

**Q6 — (B).** $X''+\lambda X=0$ with $X(0)=X(a)=0$ gives $X=\sin\frac{n\pi x}{a}$. Then $Y''=\left(\frac{n\pi}{a}\right)^2Y$ with $Y(0)=0$ gives $\sinh\frac{n\pi y}{a}$. Finally, $B_n\sinh\frac{n\pi b}{a}=\frac2a\int_0^af\sin\frac{n\pi x}{a}dx$. Option (A) violates $u(x,0)=0$.

**Q7 — (B).** IV is false: $r^{-n}$ is unbounded at $r=0$. Those terms appear only for the exterior problem or an annulus. I: $u''=0$ with the given end values. II: every mode decays exponentially. III: $E'(t)=\int(u_tu_{tt}+c^2u_xu_{xt})=c^2[u_xu_t]_0^L=0$.

**Q8 — (A).** $u=\frac{a_0}{2}+\sum a_ne^{-k(n\pi/L)^2t}\cos\frac{n\pi x}{L}$, and $\frac{a_0}{2}=\frac1L\int_0^Lf$. R is exactly why the limit is the mean. Physically, insulated ends conserve heat.

**Q9 — (C).** Dirichlet conditions give sines, Neumann conditions give cosines (including the constant), mixed conditions give odd quarter-wave sines, and periodic conditions give the full Fourier system.

**Q10 — (C).** The wave equation **propagates** discontinuities along the characteristics $x\pm ct=$ const, and they are not smoothed. The heat equation, by contrast, makes $u$ smooth ($C^\infty$) for $t\gt 0$. (A) is the maximum principle, (B) is the mean value property, and (D) holds by the energy or maximum principle.

**Q11 — (D).** $\cos^2\theta=\frac12+\frac12\cos2\theta$, so $u=\frac12+\frac12r^2\cos2\theta$. At $r=\frac12$, $\theta=0$ this gives $\frac12+\frac18=\frac58$. In Cartesian form $u=\frac12+\frac12(x^2-y^2)$, which is harmonic. Option (A) is the value at the centre (the mean of the boundary data). Option (C) wrongly uses $r$ instead of $r^2$.

**Q12 — (B).** $u=\sum B_n\sin nx\sin nt$ with $nB_n=$ the Fourier sine coefficient of $\sin2x$. So $B_2=\frac12$ and $u=\frac12\sin2x\sin2t$. At $x=\pi/4$ this is $\frac12\sin2t$, with maximum $\frac12$. Forgetting to divide by $nc$ gives $1$ (option A).
