# Unit 6 · Topic 03 — General Theory of Linear ODEs
> Syllabus coverage: General theory of homogeneous and non-homogeneous linear ordinary differential equations
> Cheatsheet: [../Cheatsheets/03-Linear-ODE-General-Theory.md](../Cheatsheets/03-Linear-ODE-General-Theory.md)

**Q1.** `[Concept]` ★ Let $y_1,y_2$ be solutions of $y''+p(x)y'+q(x)y=0$ on an interval $I$, where $p,q$ are continuous on $I$. Then their Wronskian $W(x)$ on $I$ is

(A) either identically zero or never zero

(B) always identically zero

(C) zero at exactly one point if the solutions are linearly independent

(D) a constant

**Q2.** `[Numerical]` ★★ Let $y_1,y_2$ be solutions of $x\thinspace y''+2y'+xe^{x}y=0$ on $(0,\infty)$ with $W(y_1,y_2)(1)=2$. Then $W(y_1,y_2)(2)$ equals

(A) $1$

(B) $1/2$

(C) $8$

(D) $2e^{-2}$

**Q3.** `[Numerical]` ★★ A particular integral of $y''-3y'+2y=e^{x}$ is

(A) $e^{x}$

(B) $-\tfrac12 e^{x}$

(C) $x e^{x}$

(D) $-x e^{x}$

**Q4.** `[Numerical]` ★ The general solution of $x^2y''-3xy'+4y=0$ on $x\gt 0$ is

(A) $(c_1+c_2\ln x)\thinspace x^2$

(B) $c_1x^2+c_2x^{-2}$

(C) $c_1x+c_2x^4$

(D) $(c_1+c_2x)\thinspace e^{2x}$

**Q5.** `[Multi-Statement]` ★★ Consider the following statements.

I. $\sin x$ and $\cos x$ are linearly independent on $\mathbb{R}$.

II. $x^2$ and $x|x|$ are linearly independent on $\mathbb{R}$, although their Wronskian vanishes identically.

III. $x$ and $x^2$ cannot both be solutions on $\mathbb{R}$ of an equation $y''+p(x)y'+q(x)y=0$ with $p,q$ continuous on $\mathbb{R}$.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★★
**Assertion (A):** The functions $x^3$ and $|x|^3$ are linearly independent on $[-1,1]$.
**Reason (R):** If the Wronskian of two differentiable functions vanishes identically on an interval, the functions are linearly dependent there.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each equation in List-I with the correct form of trial particular solution (method of undetermined coefficients) in List-II.

| List-I | List-II |
|---|---|
| (a) $y''+y=\sin x$ | 1. $Ax+B$ |
| (b) $y''-y=e^{x}$ | 2. $Ax^2e^{x}$ |
| (c) $y''-2y'+y=e^{x}$ | 3. $x(A\cos x+B\sin x)$ |
| (d) $y''+y=x$ | 4. $Axe^{x}$ |

(A) a-3, b-2, c-4, d-1

(B) a-3, b-4, c-2, d-1

(C) a-1, b-4, c-2, d-3

(D) a-3, b-4, c-1, d-2

**Q8.** `[NOT-true / Counterexample]` ★★ For $y''+p(x)y'+q(x)y=0$ with $p,q$ continuous on an interval $I$, which of the following is **NOT** true?

(A) The solution space is a two-dimensional vector space.

(B) If a solution satisfies $y(x_0)=y'(x_0)=0$ for some $x_0\in I$, then $y\equiv0$.

(C) Two solutions having a common zero in $I$ are linearly dependent.

(D) Two linearly independent solutions can have a common zero in $I$.

**Q9.** `[Numerical]` ★★★ $y_1=x$ is a solution of Legendre's equation $(1-x^2)y''-2xy'+2y=0$ on $(-1,1)$. A second, linearly independent solution obtained by reduction of order is

(A) $x\ln\dfrac{1+x}{1-x}$

(B) $\dfrac{x}{2}\ln\dfrac{1+x}{1-x}-1$

(C) $\dfrac{1}{1-x^2}$

(D) $\dfrac{3x^2-1}{2}$

**Q10.** `[Numerical]` ★★ By variation of parameters, a particular solution of $y''+y=\sec x$ on $(-\pi/2,\pi/2)$ is

(A) $x\cos x+\sin x\thinspace \ln|\cos x|$

(B) $x\sin x-\cos x\thinspace \ln|\cos x|$

(C) $x\sin x+\cos x\thinspace \ln|\cos x|$

(D) $\sin x\thinspace \ln|\sec x+\tan x|$

**Q11.** `[Application]` ★★ The functions $x$, $x+e^{x}$ and $1+x+e^{x}$ are solutions of a non-homogeneous equation $y''+p(x)y'+q(x)y=r(x)$. Its general solution is

(A) $x+c_1e^{x}+c_2$

(B) $c_1x+c_2e^{x}$

(C) $c_1x+c_2(x+e^{x})+c_3(1+x+e^x)$

(D) $1+c_1x+c_2e^{x}$

**Q12.** `[Concept]` ★ Under the substitution $x=e^{t}$ with $\theta=\dfrac{d}{dt}$, the operator $x^2\dfrac{d^2}{dx^2}$ becomes

(A) $\theta^2$

(B) $\theta(\theta+1)$

(C) $\theta(\theta-1)$

(D) $e^{2t}\theta^2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | B | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | D | Multi-Statement |
| 6 | C | Assertion-Reason |
| 7 | B | Match |
| 8 | D | NOT-true / Counterexample |
| 9 | B | Numerical |
| 10 | C | Numerical |
| 11 | A | Application |
| 12 | C | Concept |

## Solutions
**Q1 — (A).** Abel's formula $W(x)=W(x_0)\exp\negthinspace \big(-\int_{x_0}^x p\big)$ shows that $W$ is either $\equiv0$ (when $W(x_0)=0$) or never zero. (D) holds only when $p\equiv0$.

**Q2 — (B).** In normal form, $p(x)=2/x$. Abel's formula gives $W=Ce^{-\int 2/x\thinspace dx}=C/x^2$. From $W(1)=2$ we get $C=2$, so $W(2)=2/4=1/2$. Forgetting to divide by the leading coefficient $x$ gives wrong answers like $2e^{-2}$.

**Q3 — (D).** The roots are $1$ and $2$. Since $e^{x}$ solves the homogeneous equation, try $Axe^{x}$. Substituting gives $A\thinspace e^x[(2+x)-3(1+x)+2x]=-Ae^x$, so $A=-1$. (A) and (B) ignore resonance.

**Q4 — (A).** The indicial equation is $m(m-1)-3m+4=m^2-4m+4=0$, so $m=2$ is a double root. Hence $y=(c_1+c_2\ln x)x^2$. Option (D) is the analogue for a constant-coefficient equation, which is the wrong pattern for Cauchy–Euler.

**Q5 — (D).** I: $W=-1\ne0$. II: on $x\ge0$ we have $x|x|=x^2$, and on $x\lt 0$ we have $x|x|=-x^2$. The equation $c_1x^2+c_2x|x|\equiv0$ forces $c_1+c_2=0$ and $c_1-c_2=0$, so the functions are independent. But $W\equiv0$, as checked on each side. III: $W(x,x^2)=x^2$, which vanishes at $0$ but not identically. This is impossible for solutions (Q1).

**Q6 — (C).** Here $|x|^3=x^3$ for $x\ge0$ and $-x^3$ for $x\lt 0$, so the functions are independent on $[-1,1]$, while $W\equiv0$. So A is true, and this same pair is a counterexample showing R is false. R holds only for **solutions** of a linear ODE with continuous coefficients.

**Q7 — (B).** (a) $\pm i$ are roots, so multiply by $x$: $x(A\cos x+B\sin x)$. (b) $1$ is a simple root, so $Axe^x$. (c) $1$ is a double root, so $Ax^2e^x$. (d) $0$ is not a root, so $Ax+B$.

**Q8 — (D).** If $y_1(x_0)=y_2(x_0)=0$, then $W(x_0)=0$, so $W\equiv0$ and the solutions are dependent. Hence (C) is true and (D) is false. (A) and (B) follow from existence and uniqueness.

**Q9 — (B).** Reduction of order gives $y_2=y_1\int\frac{e^{-\int p}}{y_1^2}dx$ with $p=\frac{-2x}{1-x^2}$, so $e^{-\int p}=\frac{1}{1-x^2}$. Then $y_2=x\int\frac{dx}{x^2(1-x^2)}=x\Big(-\frac1x+\frac12\ln\frac{1+x}{1-x}\Big)=\frac{x}{2}\ln\frac{1+x}{1-x}-1$. This is $-Q_1(x)$, a Legendre function of the second kind, so it is equally valid; it was verified symbolically. (D) is $P_2$, which solves the $n=2$ equation, not this one.

**Q10 — (C).** With $y_1=\cos x$, $y_2=\sin x$ and $W=1$, we get $u_1=-\int\sin x\sec x\thinspace dx=\ln|\cos x|$ and $u_2=\int\cos x\sec x\thinspace dx=x$. So $y_p=\cos x\ln|\cos x|+x\sin x$. Option (B) has a sign error.

**Q11 — (A).** Differences of solutions of the non-homogeneous equation solve the homogeneous equation. So $e^{x}$ and $1$ are independent homogeneous solutions, and $y=x+c_1e^x+c_2$. Option (C) wrongly uses an arbitrary linear combination of non-homogeneous solutions, which does not satisfy the equation unless the coefficients sum to $1$.

**Q12 — (C).** $x\frac{d}{dx}=\theta$ and $x^2\frac{d^2}{dx^2}=\theta(\theta-1)$. In general, $x^nD^n=\theta(\theta-1)\cdots(\theta-n+1)$.
