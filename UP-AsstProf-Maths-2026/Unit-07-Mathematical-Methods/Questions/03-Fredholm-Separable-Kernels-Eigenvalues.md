# Unit 7 · Topic 03 — Fredholm Equations, Separable Kernels and Eigenvalues
> Syllabus coverage: Linear integral equations of Fredholm type, solution of integral equations with separable kernels (characteristic values, eigenfunctions, Fredholm alternative, symmetric kernels, resolvent by Neumann series)
> Cheatsheet: [../Cheatsheets/03-Fredholm-Separable-Kernels-Eigenvalues.md](../Cheatsheets/03-Fredholm-Separable-Kernels-Eigenvalues.md)

**Q1.** `[Concept]` ★ A kernel of the form $K(x,t)=\sum_{i=1}^{n}a_i(x)\thinspace b_i(t)$ (finite sum) is called

(A) a symmetric kernel

(B) a degenerate (separable) kernel

(C) a resolvent kernel

(D) a difference (convolution) kernel

**Q2.** `[Numerical]` ★ The characteristic value of $y(x)=\lambda\displaystyle\int_0^1 x t\thinspace y(t)\thinspace dt$ and a corresponding eigenfunction are

(A) $\lambda=3,\ y=x$

(B) $\lambda=\tfrac13,\ y=x$

(C) $\lambda=2,\ y=x$

(D) $\lambda=3,\ y=x^2$

**Q3.** `[Numerical]` ★★ The solution of $y(x)=x^2+\displaystyle\int_0^1 x t\thinspace y(t)\thinspace dt$ is

(A) $x^2+\dfrac{x}{4}$

(B) $x^2+\dfrac{3x}{8}$

(C) $x^2+\dfrac{3x}{4}$

(D) $x^2+\dfrac{x}{3}$

**Q4.** `[Numerical]` ★★★ The characteristic values of the kernel $K(x,t)=x+t$ on $[0,1]$ are

(A) $-6\pm4\sqrt3$

(B) $6\pm4\sqrt3$

(C) $-6\pm2\sqrt3$

(D) $2$ and $3$

**Q5.** `[Numerical]` ★★ The characteristic values of the kernel $K(x,t)=\cos(x+t)$ on $[0,2\pi]$ are

(A) $\pm\pi$

(B) $\dfrac{1}{\pi}$ only

(C) $\pm\dfrac{1}{\pi}$

(D) $\pm\dfrac{1}{2\pi}$

**Q6.** `[Multi-Statement]` ★★★ Let $K$ be a real, continuous, symmetric kernel on $[a,b]^2$, $K\not\equiv0$.

I. All characteristic values of $K$ are real.

II. Eigenfunctions belonging to distinct characteristic values are orthogonal on $[a,b]$.

III. $K$ has at least one characteristic value.

IV. If, in addition, $K$ is degenerate, then $K$ has infinitely many characteristic values.

Which are correct?

(A) I and II only

(B) I, II and III only

(C) I, II and IV only

(D) I, II, III and IV

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** The homogeneous equation $y(x)=\lambda\displaystyle\int_0^\pi \sin x\cos t\thinspace y(t)\thinspace dt$ has only the trivial solution for every $\lambda$.
**Reason (R):** $\displaystyle\int_0^\pi \sin t\cos t\thinspace dt=0$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match the kernel on $[0,1]$ (List-I) with its characteristic value (List-II).

| List-I | List-II |
|---|---|
| (a) $K=1$ | 1. $2$ |
| (b) $K=xt$ | 2. $\dfrac{2}{e^2-1}$ |
| (c) $K=x$ | 3. $1$ |
| (d) $K=e^{x+t}$ | 4. $3$ |

(A) a-3, b-4, c-2, d-1

(B) a-3, b-1, c-4, d-2

(C) a-3, b-4, c-1, d-2

(D) a-1, b-4, c-3, d-2

**Q9.** `[NOT-true / Counterexample]` ★★ For $y(x)=f(x)+\lambda\int_a^b K(x,t)y(t)\thinspace dt$ with continuous $K$, which statement is NOT true?

(A) If $\lambda$ is not a characteristic value, the equation has a unique solution for every continuous $f$.

(B) If $\lambda$ is a characteristic value, the equation is solvable iff $f$ is orthogonal to every solution of the transposed homogeneous equation $z(x)=\lambda\int_a^b K(t,x)z(t)\thinspace dt$.

(C) If $\lambda$ is a characteristic value and a solution exists, then infinitely many solutions exist.

(D) If $\lambda$ is a characteristic value, the equation has no solution for any $f\not\equiv0$.

**Q10.** `[Application]` ★★★ For which $f$ does $y(x)=f(x)+3\displaystyle\int_0^1 x t\thinspace y(t)\thinspace dt$ have a solution?

(A) $f(x)=x$

(B) $f(x)=1$

(C) $f(x)=3x-2$

(D) $f(x)=x^2$

**Q11.** `[Concept]` ★ A degenerate kernel $K(x,t)=\sum_{i=1}^{n}a_i(x)b_i(t)$ with $\lbrace a_i\rbrace$ and $\lbrace b_i\rbrace$ each linearly independent has

(A) exactly $n$ characteristic values

(B) infinitely many characteristic values

(C) at least $n$ characteristic values

(D) at most $n$ characteristic values

**Q12.** `[Numerical]` ★★ For $y(x)=f(x)+\lambda\displaystyle\int_0^1 x t\thinspace y(t)\thinspace dt$ $(\lambda\ne3)$, the resolvent kernel $R(x,t;\lambda)$ is

(A) $\dfrac{3xt}{3+\lambda}$

(B) $\dfrac{xt}{3-\lambda}$

(C) $xt\thinspace e^{\lambda/3}$

(D) $\dfrac{3xt}{3-\lambda}$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | A | Numerical |
| 3 | B | Numerical |
| 4 | A | Numerical |
| 5 | C | Numerical |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | C | Match |
| 9 | D | NOT-true / Counterexample |
| 10 | C | Application |
| 11 | D | Concept |
| 12 | D | Numerical |

## Solutions
**Q1 — (B).** Finite sum of products ⇒ degenerate/separable (Pincherle–Goursat). It need not be symmetric.

**Q2 — (A).** $y=\lambda c\thinspace x$ with $c=\int_0^1 t\thinspace y\thinspace dt=\lambda c/3$ ⇒ $c\ne0$ requires $\lambda=3$; eigenfunction $x$. (B) confuses the characteristic value $\lambda$ with the eigenvalue $\mu=1/\lambda$ of the operator.

**Q3 — (B).** $y=x^2+cx$, $c=\int_0^1 t(t^2+ct)dt=\frac14+\frac c3$ ⇒ $c=\frac38$. (A) forgets the $c/3$ feedback term.

**Q4 — (A).** $y=\lambda(c_1x+c_2)$, $c_1=\int y$, $c_2=\int t y$ ⇒ $c_1=\lambda(\frac{c_1}{2}+c_2)$, $c_2=\lambda(\frac{c_1}{3}+\frac{c_2}{2})$. $`\det\begin{pmatrix}1-\lambda/2&-\lambda\cr -\lambda/3&1-\lambda/2\end{pmatrix}=0`$ ⇒ $\lambda^2+12\lambda-12=0$ ⇒ $\lambda=-6\pm4\sqrt3$.

**Q5 — (C).** $\cos(x+t)=\cos x\cos t-\sin x\sin t$; $\int_0^{2\pi}\cos^2=\int_0^{2\pi}\sin^2=\pi$, cross term $0$. Eigenfunction $\cos x$: $\lambda\pi=1$; $\sin x$: $-\lambda\pi=1$. So $\lambda=\pm1/\pi$.

**Q6 — (B).** I, II, III are the Hilbert–Schmidt facts for nonzero symmetric $L^2$ kernels. IV is false: a degenerate kernel has at most $n$ characteristic values (e.g. $xt$ has only $\lambda=3$).

**Q7 — (A).** $y=\lambda c\sin x$, $c=\int_0^\pi\cos t\thinspace y\thinspace dt=\lambda c\int_0^\pi\sin t\cos t\thinspace dt=0$ ⇒ $y\equiv0$. R is precisely the reason. (Such kernels, $\int K(t,t)dt=0$ with rank 1, are the standard "no characteristic value" example.)

**Q8 — (C).** $K=1$: $c=\lambda c$ ⇒ 1. $K=xt$: $\int t^2=\frac13$ ⇒ 3. $K=x$: $y=\lambda cx$, $c=\int y=\lambda c/2$ ⇒ 2. $K=e^{x+t}$: $\int_0^1e^{2t}=\frac{e^2-1}{2}$ ⇒ $\frac{2}{e^2-1}$. Rule for rank one $a(x)b(t)$: $\lambda=1/\int_a^b a(t)b(t)dt$.

**Q9 — (D).** By the Fredholm alternative, at a characteristic value the equation is solvable for those $f$ orthogonal to the transposed eigenfunctions (and then has infinitely many solutions). So "no solution for any $f$" is false.

**Q10 — (C).** $\lambda=3$ is the characteristic value with (symmetric) eigenfunction $x$. Solvable iff $\int_0^1 t f(t)dt=0$. Values: $x\to\frac13$, $1\to\frac12$, $3x-2\to1-1=0$, $x^2\to\frac14$. Indeed $y=f+cx$ ⇒ $c=\int tf+c$ forces $\int tf=0$.

**Q11 — (D).** The characteristic values are roots of $\det(I-\lambda A)=0$, $A_{ij}=\int b_ia_j$, a polynomial of degree $\le n$; it may have fewer roots (even none, as in Q7).

**Q12 — (D).** $K_n=\frac{xt}{3^{n-1}}$ ⇒ $R=\sum\lambda^{n-1}\frac{xt}{3^{n-1}}=\frac{xt}{1-\lambda/3}=\frac{3xt}{3-\lambda}$, valid by continuation for all $\lambda\ne3$ (Neumann series converges for $|\lambda|\lt 3$). (B) drops the factor 3.
