# Unit 7 · Topic 02 — Integral Equations: Volterra Type, Successive Substitutions and Approximations
> Syllabus coverage: Linear integral equations of Fredholm and Volterra type (classification, ODE ↔ IE), solution by successive substitutions and successive approximations (Neumann series, iterated and resolvent kernels)
> Cheatsheet: [../Cheatsheets/02-Integral-Equations-Volterra-Successive-Methods.md](../Cheatsheets/02-Integral-Equations-Volterra-Successive-Methods.md)

**Q1.** `[Concept]` ★ The equation $y(x)=f(x)+\lambda\displaystyle\int_a^x K(x,t)\,y(t)\,dt$ is a

(A) Fredholm equation of the first kind

(B) Fredholm equation of the second kind

(C) Volterra equation of the first kind

(D) Volterra equation of the second kind

**Q2.** `[Numerical]` ★ The initial value problem $y''+y=0$, $y(0)=1$, $y'(0)=0$ is equivalent to the integral equation

(A) $y(x)=1-\displaystyle\int_0^x (x-t)\,y(t)\,dt$

(B) $y(x)=1+\displaystyle\int_0^x (x-t)\,y(t)\,dt$

(C) $y(x)=1-x-\displaystyle\int_0^x (x-t)\,y(t)\,dt$

(D) $y(x)=1-\displaystyle\int_0^x y(t)\,dt$

**Q3.** `[Numerical]` ★★ The resolvent kernel of the Volterra equation $y(x)=f(x)+\lambda\displaystyle\int_0^x e^{x-t}y(t)\,dt$ is

(A) $e^{\lambda(x-t)}$

(B) $\dfrac{e^{x-t}}{1-\lambda}$

(C) $e^{(1+\lambda)(x-t)}$

(D) $e^{x-t}\cosh\lambda(x-t)$

**Q4.** `[Numerical]` ★★ For the Volterra kernel $K(x,t)=x-t$, the second iterated kernel $K_2(x,t)=\displaystyle\int_t^x K(x,s)K(s,t)\,ds$ equals

(A) $\dfrac{(x-t)^2}{2}$

(B) $\dfrac{(x-t)^3}{3}$

(C) $\dfrac{(x-t)^3}{6}$

(D) $\dfrac{(x-t)^4}{24}$

**Q5.** `[Numerical]` ★★ The continuous solution of $y(x)=x+\displaystyle\int_0^x (t-x)\,y(t)\,dt$ is

(A) $\sinh x$

(B) $\sin x$

(C) $x e^{-x}$

(D) $1-\cos x$

**Q6.** `[Application]` ★★ Apply successive approximations to $y(x)=1+\displaystyle\int_0^x t\,y(t)\,dt$ starting with $y_0(x)=1$. Then $y_2(x)$ is

(A) $1+\dfrac{x^2}{2}$

(B) $1+x+\dfrac{x^2}{2}$

(C) $1+\dfrac{x^2}{2}+\dfrac{x^4}{8}$

(D) $1+\dfrac{x^2}{2}+\dfrac{x^4}{24}$

**Q7.** `[Multi-Statement]` ★★ Let $K(x,t)$ be continuous on $a\le t\le x\le b$ (and on $[a,b]^2$ where relevant), and $f$ continuous.

I. The Neumann series for $y=f+\lambda\int_a^x K y\,dt$ converges for every $\lambda$.

II. The Volterra equation of the second kind has a unique continuous solution for every $\lambda$; it has no characteristic values.

III. The Neumann series for the Fredholm equation $y=f+\lambda\int_a^b K y\,dt$ converges for every $\lambda$.

Which are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q8.** `[Assertion-Reason]` ★★
**Assertion (A):** The equation $\displaystyle\int_0^x e^{x-t}y(t)\,dt=x$ has the solution $y(x)=1-x$.
**Reason (R):** A Volterra equation of the first kind $\int_0^x K(x,t)y(t)\,dt=f(x)$ with $K(x,x)\ne0$ and $K_x,f'$ continuous can be reduced to one of the second kind by differentiation.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q9.** `[Match]` ★★ Match each Volterra equation (List-I) with its solution (List-II).

| List-I | List-II |
|---|---|
| (a) $y=1+\int_0^x y(t)\,dt$ | 1. $\cos x$ |
| (b) $y=1-\int_0^x y(t)\,dt$ | 2. $\cosh x$ |
| (c) $y=1-\int_0^x (x-t)y(t)\,dt$ | 3. $e^{x}$ |
| (d) $y=1+\int_0^x (x-t)y(t)\,dt$ | 4. $e^{-x}$ |

(A) a-3, b-4, c-2, d-1

(B) a-3, b-4, c-1, d-2

(C) a-4, b-3, c-1, d-2

(D) a-3, b-1, c-4, d-2

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Every initial value problem for a linear ODE with continuous coefficients can be written as a Volterra equation of the second kind.

(B) A two-point boundary value problem for a linear ODE leads to a Fredholm integral equation.

(C) A Volterra equation can be regarded as a Fredholm equation whose kernel vanishes for $t>x$.

(D) For a continuous kernel, the Volterra equation $y=f+\lambda\int_a^x K y\,dt$ fails to have a solution for some values of $\lambda$.

**Q11.** `[Numerical]` ★★★ The solution of Abel's equation $\displaystyle\int_0^x \frac{y(t)}{\sqrt{x-t}}\,dt=x$ is

(A) $\dfrac{2\sqrt{x}}{\pi}$

(B) $\dfrac{\sqrt{x}}{\pi}$

(C) $\dfrac{2}{\pi\sqrt{x}}$

(D) $\dfrac{\sqrt{x}}{2}$

**Q12.** `[Concept]` ★ For the Volterra kernel $K(x,t)$, the iterated kernels are defined by $K_1=K$ and $K_{n}(x,t)=$

(A) $\displaystyle\int_a^b K(x,s)\,K_{n-1}(s,t)\,ds$

(B) $\displaystyle\int_t^x K(x,s)\,K_{n-1}(s,t)\,ds$

(C) $\displaystyle\int_0^x K(x,s)\,K_{n-1}(x,s)\,ds$

(D) $\displaystyle\int_x^t K(s,x)\,K_{n-1}(t,s)\,ds$

**Q13.** `[Numerical]` ★★★ The boundary value problem $y''+\lambda y=0$, $y(0)=y(1)=0$ is equivalent to $y(x)=\lambda\displaystyle\int_0^1 G(x,t)\,y(t)\,dt$, where

(A) $G(x,t)=\begin{cases}t(1-x), & t\le x\\ x(1-t), & t\ge x\end{cases}$

(B) $G(x,t)=\begin{cases}x(1-t), & t\le x\\ t(1-x), & t\ge x\end{cases}$

(C) $G(x,t)=\begin{cases}t(x-1), & t\le x\\ x(t-1), & t\ge x\end{cases}$

(D) $G(x,t)=x-t$ for all $t,x$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | A | Numerical |
| 3 | C | Numerical |
| 4 | C | Numerical |
| 5 | B | Numerical |
| 6 | C | Application |
| 7 | D | Multi-Statement |
| 8 | A | Assertion-Reason |
| 9 | B | Match |
| 10 | D | NOT-true / Counterexample |
| 11 | A | Numerical |
| 12 | B | Concept |
| 13 | A | Numerical |

## Solutions
**Q1 — (D).** Variable upper limit ⇒ Volterra; unknown appears outside the integral ⇒ second kind.

**Q2 — (A).** Put $y''=-y$. Integrating twice with $y(0)=1,y'(0)=0$: $y=1+\int_0^x(x-t)y''(t)dt=1-\int_0^x(x-t)y(t)dt$. (C) wrongly adds the $y'(0)x$ term with $y'(0)=-1$; (B) has the wrong sign.

**Q3 — (C).** $K_n=e^{x-t}\frac{(x-t)^{n-1}}{(n-1)!}$, so $R=\sum_{n\ge1}\lambda^{n-1}K_n=e^{x-t}e^{\lambda(x-t)}$. (A) is the resolvent of $K\equiv1$.

**Q4 — (C).** $\int_t^x(x-s)(s-t)ds=\frac{(x-t)^3}{6}$ (a Beta integral $B(2,2)=1/6$). In general $K_n=\frac{(x-t)^{2n-1}}{(2n-1)!}$, so for $\lambda=1$, $R=\sinh(x-t)$.

**Q5 — (B).** Differentiate: $y'=1-\int_0^x y\,dt$, $y''=-y$, with $y(0)=0,y'(0)=1$ ⇒ $y=\sin x$. Laplace check: $Y=\frac1{s^2}-\frac{Y}{s^2}$ ⇒ $Y=\frac1{s^2+1}$. (A) comes from a sign error in the kernel.

**Q6 — (C).** $y_1=1+\int_0^x t\,dt=1+\frac{x^2}{2}$; $y_2=1+\int_0^x t(1+\frac{t^2}{2})dt=1+\frac{x^2}{2}+\frac{x^4}{8}$ — partial sums of $e^{x^2/2}$. (D) uses $x^4/4!$ wrongly.

**Q7 — (D).** For Volterra, $|K_n|\le M^n\frac{(x-a)^{n-1}}{(n-1)!}$, so the series converges for all $\lambda$ (entire resolvent) ⇒ I, II true. For Fredholm it converges only for $|\lambda|<\frac{1}{M(b-a)}$ (or $|\lambda|<1/\|K\|_2$) in general; e.g. $K\equiv1$ on $[0,1]$ has characteristic value $\lambda=1$. III false.

**Q8 — (A).** Differentiating: $y(x)+\int_0^x e^{x-t}y\,dt=1$ ⇒ $y(x)+x=1$ ⇒ $y=1-x$. Check: $\int_0^x e^{x-t}(1-t)dt=x$. R is exactly the method used.

**Q9 — (B).** (a) $y'=y,\,y(0)=1$ ⇒ $e^x$. (b) $y'=-y$ ⇒ $e^{-x}$. (c) $y''=-y,\,y(0)=1,y'(0)=0$ ⇒ $\cos x$. (d) $y''=y$ ⇒ $\cosh x$.

**Q10 — (D).** A second-kind Volterra equation with continuous kernel has a unique solution for **every** $\lambda$ (no characteristic values). (A), (B), (C) are standard facts.

**Q11 — (A).** Laplace: $Y(s)\cdot\Gamma(\tfrac12)s^{-1/2}=s^{-2}$ ⇒ $Y=\frac{s^{-3/2}}{\sqrt\pi}$ ⇒ $y=\frac{x^{1/2}}{\sqrt\pi\,\Gamma(3/2)}=\frac{2\sqrt x}{\pi}$. Check: $\int_0^x\frac{\sqrt t}{\sqrt{x-t}}dt=\frac{\pi}{2}x$.

**Q12 — (B).** For Volterra kernels the intermediate variable runs between $t$ and $x$ (the kernels vanish outside $t\le s\le x$). (A) is the Fredholm definition.

**Q13 — (A).** Green's function of $-y''$ with $y(0)=y(1)=0$: $G=t(1-x)$ for $t\le x$, $x(1-t)$ for $t\ge x$ (symmetric, $G\ge0$, kink at $t=x$). Check: $y=\sin\pi x$, $\lambda=\pi^2$ satisfies it. (C) is $-G$ (Green's function of $+y''$).
