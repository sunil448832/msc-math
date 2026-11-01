# Unit 6 · Topic 01 — Existence and Uniqueness of Solutions of IVPs
> Syllabus coverage: Existence and uniqueness of solutions of initial value problems for first order ordinary differential equations
> Cheatsheet: [../Cheatsheets/01-Existence-Uniqueness-IVP.md](../Cheatsheets/01-Existence-Uniqueness-IVP.md)

**Q1.** `[Concept]` ★ Let $f$ be continuous on $R=\lbrace |x-x_0|\le a,\ |y-y_0|\le b\rbrace$, $|f|\le M$ on $R$, and let $f$ satisfy a Lipschitz condition in $y$ on $R$. By Picard's theorem, the IVP $y'=f(x,y)$, $y(x_0)=y_0$ has a unique solution on $|x-x_0|\le h$, where

(A) $h=\max\lbrace a,\ b/M\rbrace$

(B) $h=\min\lbrace a,\ b/M\rbrace$

(C) $h=\min\lbrace a,\ M/b\rbrace$

(D) $h=ab/M$

**Q2.** `[Numerical]` ★★ For the IVP $y'=x^2+y^2$, $y(0)=0$ on the rectangle $R=\lbrace |x|\le 1,\ |y|\le 1\rbrace$, the interval of existence guaranteed by Picard's theorem is

(A) $|x|\le 1$

(B) $|x|\le 1/2$

(C) $|x|\le 1/4$

(D) $|x|\le 2$

**Q3.** `[Numerical]` ★★ For $y'=x+y$, $y(0)=1$, the second Picard iterate $y_2(x)$ (with $y_0(x)\equiv 1$) is

(A) $1+x+x^2+\dfrac{x^3}{6}$

(B) $1+x+x^2+\dfrac{x^3}{3}$

(C) $1+x+\dfrac{x^2}{2}$

(D) $1+x+\dfrac{x^2}{2}+\dfrac{x^3}{6}$

**Q4.** `[Concept]` ★ The IVP $y'=3y^{2/3}$, $y(0)=0$ has

(A) no solution

(B) exactly one solution

(C) exactly two solutions

(D) infinitely many solutions

**Q5.** `[Multi-Statement]` ★★ Consider the following statements.

I. $f(x,y)=|y|$ satisfies a Lipschitz condition in $y$ on $\mathbb R^2$.

II. $f(x,y)=y^{2/3}$ satisfies a Lipschitz condition in $y$ on $\lbrace |x|\le 1,\ |y|\le 1\rbrace$.

III. $f(x,y)=x^2y$ satisfies a Lipschitz condition in $y$ on $\lbrace |x|\le 1,\ y\in\mathbb{R}\rbrace$.

Which of the above is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** If $f$ is continuous on an open set containing $(x_0,y_0)$, then the IVP $y'=f(x,y)$, $y(x_0)=y_0$ has a unique local solution.
**Reason (R):** Peano's theorem guarantees the existence of at least one local solution when $f$ is merely continuous.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each IVP in List-I with the correct description in List-II.

| List-I | List-II |
|---|---|
| (a) $y'=y^2,\ y(0)=1$ | 1. unique solution, existing on all of $\mathbb{R}$ |
| (b) $y'=1+y^2,\ y(0)=0$ | 2. maximal interval $(-\pi/2,\pi/2)$ |
| (c) $y'=2\sqrt{\lvert y\rvert},\ y(0)=0$ | 3. maximal interval $(-\infty,1)$ |
| (d) $y'=y,\ y(0)=1$ | 4. infinitely many solutions |

(A) a-3, b-2, c-4, d-1

(B) a-2, b-3, c-4, d-1

(C) a-3, b-2, c-1, d-4

(D) a-1, b-2, c-4, d-3

**Q8.** `[NOT-true / Counterexample]` ★★ On the rectangle $\lbrace |x|\le 1,\ |y|\le 1\rbrace$, which of the following functions does **NOT** satisfy a Lipschitz condition in $y$?

(A) $f(x,y)=y^2$

(B) $f(x,y)=x\sin y$

(C) $f(x,y)=\sqrt{|y|}$

(D) $f(x,y)=e^{x}y$

**Q9.** `[Application]` ★★ The IVP $y'=\sqrt{|y|}$, $y(x_0)=y_0$ has a unique solution in some neighbourhood of $x_0$ if and only if

(A) $y_0=0$

(B) $x_0\ne 0$

(C) $y_0\gt 0$

(D) $y_0\ne 0$

**Q10.** `[Numerical]` ★★★ For $y'=y^2$, $y(0)=1$, apply Picard's theorem on rectangles $\lbrace |x|\le a,\ |y-1|\le b\rbrace$ with $a$ large. The largest $h$ obtainable by optimising over $b\gt 0$ is

(A) $1$

(B) $1/2$

(C) $1/4$

(D) $1/8$

**Q11.** `[Concept]` ★ Regarding uniqueness of solutions of $y'=f(x,y)$, $y(x_0)=y_0$ with $f$ continuous, the Lipschitz condition on $f$ in $y$ is

(A) necessary and sufficient

(B) necessary but not sufficient

(C) sufficient but not necessary

(D) neither necessary nor sufficient

**Q12.** `[Application]` ★ The largest open interval on which the IVP $(x^2-4)\thinspace y'+y=x$, $y(0)=1$ is guaranteed to have a unique solution is

(A) $(-2,2)$

(B) $(-\infty,\infty)$

(C) $(0,2)$

(D) $(-2,\infty)$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | B | Numerical |
| 3 | A | Numerical |
| 4 | D | Concept |
| 5 | B | Multi-Statement |
| 6 | D | Assertion-Reason |
| 7 | A | Match |
| 8 | C | NOT-true / Counterexample |
| 9 | D | Application |
| 10 | C | Numerical |
| 11 | C | Concept |
| 12 | A | Application |

## Solutions
**Q1 — (B).** $h=\min(a,b/M)$: we need $|x-x_0|\le a$ (stay in the strip), and $|y-y_0|\le M|x-x_0|\le b$ (the graph cannot leave the rectangle through its top or bottom). Option (C) inverts the ratio.

**Q2 — (B).** $M=\max_R(x^2+y^2)=2$, so $h=\min(1,1/2)=1/2$. A common slip is to take $M=1$, which gives (A).

**Q3 — (A).** $y_1=1+\int_0^x(t+1)\thinspace dt=1+x+\tfrac{x^2}{2}$. Then $y_2=1+\int_0^x\big(t+1+t+\tfrac{t^2}{2}\big)dt=1+x+x^2+\tfrac{x^3}{6}$. Option (C) is $y_1$. Option (D) is the Taylor series of $e^x$, which is the wrong guess here; the exact solution is $2e^x-x-1$.

**Q4 — (D).** $y\equiv 0$ is a solution, and so is $y=(x-c)^3$ for $x\ge c$ (with $y=0$ for $x\lt c$), for every $c\ge 0$. Shifting on the left as well gives still more solutions. Uniqueness fails because $y^{2/3}$ is not Lipschitz near $y=0$.

**Q5 — (B).** I: $\big||y_1|-|y_2|\big|\le|y_1-y_2|$, so it is Lipschitz (it need not be differentiable). II: $|f(y)-f(0)|/|y|=|y|^{-1/3}\to\infty$, so it is not Lipschitz. III: $|x^2(y_1-y_2)|\le|y_1-y_2|$ for $|x|\le1$, so it is Lipschitz with $L=1$.

**Q6 — (D).** Continuity gives existence (Peano), but it does not give uniqueness; $y'=3y^{2/3}$ is the counterexample. So A is false and R is true.

**Q7 — (A).** (a) $y=1/(1-x)$ blows up at $x=1$, so the interval is $(-\infty,1)$. (b) $y=\tan x$, so $(-\pi/2,\pi/2)$. (c) $y\equiv0$ and $y=(x-c)^2$ for $x\ge c$ are all solutions, so there are infinitely many. (d) $y=e^x$, unique on $\mathbb{R}$, since $f$ is globally Lipschitz.

**Q8 — (C).** For (A), (B) and (D), $\partial f/\partial y$ is bounded on the rectangle ($|2y|\le2$, $|x\cos y|\le1$, $e^x\le e$), and a bounded partial derivative on a convex set implies Lipschitz. For (C), $\sqrt{|y|}/|y|\to\infty$ as $y\to0$.

**Q9 — (D).** If $y_0\ne0$, then near $y_0$ the function $\sqrt{|y|}$ has bounded derivative, hence is locally Lipschitz, so the solution is unique. If $y_0=0$, both $y\equiv0$ and $y=(x-x_0)^2/4$ for $x\ge x_0$ are solutions. Option (C) omits $y_0\lt 0$, where uniqueness also holds.

**Q10 — (C).** $M=\max(1+b)^2$, so $h=\min\negthinspace \big(a,\ b/(1+b)^2\big)$. The function $b/(1+b)^2$ is maximised at $b=1$, giving $h=1/4$. Note that the true solution $1/(1-x)$ exists on $(-\infty,1)$, so Picard's $h$ is only a guaranteed lower bound.

**Q11 — (C).** Lipschitz implies uniqueness. It is not necessary: for example, $f(y)=-y\ln|y|$ (with $f(0)=0$) is not Lipschitz at $0$, yet uniqueness holds by Osgood's criterion.

**Q12 — (A).** In standard linear form, $y'+\frac{1}{x^2-4}y=\frac{x}{x^2-4}$. The coefficients are continuous except at $x=\pm2$, and the interval containing $x_0=0$ is $(-2,2)$. A linear equation has a unique solution on the whole interval where its coefficients are continuous.
