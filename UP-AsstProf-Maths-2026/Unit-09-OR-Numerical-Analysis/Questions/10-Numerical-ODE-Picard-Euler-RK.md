# Unit 9 · Topic 10 — Numerical ODE: Picard, Euler, Modified Euler, Runge–Kutta
> Syllabus coverage: Numerical solutions of ordinary differential equation using Picard, Euler, modified Euler and Runge-Kutta methods
> Cheatsheet: [../Cheatsheets/10-Numerical-ODE-Picard-Euler-RK.md](../Cheatsheets/10-Numerical-ODE-Picard-Euler-RK.md)

**Q1.** `[Concept]` ★ The global (accumulated) error of the classical fourth-order Runge–Kutta method with step $h$ is

(A) $O(h^3)$

(B) $O(h^2)$

(C) $O(h^5)$

(D) $O(h^4)$

**Q2.** `[Numerical]` ★ Euler's method with $h=0.1$ for $y'=x+y,\ y(0)=1$ gives $y(0.2)\approx$

(A) $1.2000$

(B) $1.2200$

(C) $1.2320$

(D) $1.2428$

**Q3.** `[Numerical]` ★★ Heun's (modified Euler) method
$$y_{1}=y_0+\tfrac h2\big[f(x_0,y_0)+f\big(x_0+h,\ y_0+hf(x_0,y_0)\big)\big]$$
with $h=0.2$ for $y'=x+y,\ y(0)=1$ gives $y(0.2)\approx$

(A) $1.2000$

(B) $1.2200$

(C) $1.2400$

(D) $1.2428$

**Q4.** `[Numerical]` ★★ For $y'=x+y,\ y(0)=1$, starting from $y_0(x)=1$, the second Picard approximation $y_2(x)$ is

(A) $1+x+\dfrac{x^2}{2}$

(B) $1+x+\dfrac{x^2}{2}+\dfrac{x^3}{6}$

(C) $1+x+x^2+\dfrac{x^3}{3}$

(D) $1+x+x^2+\dfrac{x^3}{6}$

**Q5.** `[Numerical]` ★★ One step of classical RK4 with $h=1$ for $y'=y,\ y(0)=1$ gives $y(1)\approx$

(A) $e$

(B) $8/3$

(C) $65/24$

(D) $5/2$

**Q6.** `[Multi-Statement]` ★★ Consider the following statements.

I. Euler's method has local truncation error $O(h^2)$ and global error $O(h)$.

II. Heun's method is a two-stage Runge–Kutta method of order 2.

III. The classical RK4 method requires the partial derivatives $f_x$ and $f_y$ at each step.

Which are correct?

(A) I and II only

(B) I only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** Euler's method for $y'=-10y,\ y(0)=1$ with $h=0.25$ produces iterates that grow in magnitude, although the true solution decays.
**Reason (R):** For $y'=\lambda y$, Euler's method gives $y_{n+1}=(1+h\lambda)y_n$, which is stable iff $|1+h\lambda|\le1$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★★ Applied to the test equation $y'=\lambda y$ with $z=h\lambda$, each method gives $y_{n+1}=R(z)\,y_n$. Match the method with $R(z)$.

| List-I | List-II |
|---|---|
| A. Explicit Euler | 1. $\dfrac{1}{1-z}$ |
| B. Backward (implicit) Euler | 2. $1+z+\dfrac{z^2}{2}+\dfrac{z^3}{6}+\dfrac{z^4}{24}$ |
| C. Heun / RK2 | 3. $1+z$ |
| D. Classical RK4 | 4. $1+z+\dfrac{z^2}{2}$ |

(A) A-3, B-1, C-4, D-2

(B) A-1, B-3, C-4, D-2

(C) A-3, B-4, C-1, D-2

(D) A-3, B-1, C-2, D-4

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Classical RK4 uses four evaluations of $f$ per step.

(B) Runge–Kutta methods are self-starting.

(C) An explicit Runge–Kutta method of order 4 needs at least 4 stages.

(D) The explicit Euler method is A-stable.

**Q10.** `[Application]` ★ Runge–Kutta methods are applied to $y'=f(x)$ (where $f$ does not depend on $y$). Over one step, classical RK4 reduces to

(A) the trapezoidal rule

(B) Simpson's 1/3 rule

(C) Simpson's 3/8 rule

(D) the midpoint rule

**Q11.** `[Application]` ★★★ Heun's method is applied to $y'=-20y$. The largest step size $h$ for which the numerical solution does not grow is

(A) $0.05$

(B) $0.1$

(C) $0.139$

(D) $0.2$

**Q12.** `[Application]` ★★ A problem is solved on a fixed interval with RK4 and step $h$, and the global error at the endpoint is $E$. If the computation is repeated with step $h/2$, the error is expected to be about

(A) $E/2$

(B) $E/4$

(C) $E/16$

(D) $E/32$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | D | Concept |
| 2 | B | Numerical |
| 3 | C | Numerical |
| 4 | D | Numerical |
| 5 | C | Numerical |
| 6 | A | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | A | Match |
| 9 | D | NOT-true / Counterexample |
| 10 | B | Application |
| 11 | B | Application |
| 12 | C | Application |

## Solutions
**Q1 — (D).** The local truncation error is $O(h^5)$. Over $(b-a)/h$ steps this accumulates to a global error of $O(h^4)$. (C) is the local error.

**Q2 — (B).** $y_1=1+0.1(0+1)=1.1$ and $y_2=1.1+0.1(0.1+1.1)=1.22$. (D) is the exact value $2e^{0.2}-1.2$.

**Q3 — (C).** $k_1=f(0,1)=1$. The predictor is $y^*=1.2$, so $k_2=f(0.2,1.2)=1.4$. Then $y_1=1+0.1(1+1.4)=1.24$, which is close to the exact $1.2428$. (A) is the Euler step alone.

**Q4 — (D).** $y_1=1+\int_0^x(t+1)\,dt=1+x+\frac{x^2}{2}$. Then $y_2=1+\int_0^x\left(t+1+t+\frac{t^2}{2}\right)dt=1+x+x^2+\frac{x^3}{6}$. (A) is $y_1$. (B) is the $e^x$ partial sum, which comes from Picard iteration for $y'=y$ and ignores the $x$ term in $f$.

**Q5 — (C).** $k_1=1$, $k_2=1.5$, $k_3=1.75$, $k_4=2.75$, so $y_1=1+\frac16(1+3+3.5+2.75)=\frac{65}{24}\approx2.7083$. This equals the Taylor polynomial $1+1+\frac12+\frac16+\frac1{24}$, because RK4 reproduces the Taylor series up to $h^4$.

**Q6 — (A).** I and II are standard. III is false: the whole point of Runge–Kutta methods (in contrast to Taylor-series methods) is that they use only values of $f$.

**Q7 — (A).** $1+h\lambda=1-2.5=-1.5$, so $|y_n|=1.5^n$ grows with oscillating sign. R is exactly the reason. Stability needs $h\le 2/10=0.2$.

**Q8 — (A).** Explicit Euler gives $1+z$. Backward Euler, from $y_{n+1}=y_n+zy_{n+1}$, gives $1/(1-z)$. A $p$-stage explicit RK method of order $p\le4$ gives the Taylor polynomial of $e^z$ of degree $p$.

**Q9 — (D).** The stability region of explicit Euler is the disc $|1+z|\le1$, which does not contain the whole left half-plane, so it is not A-stable. Backward Euler is A-stable. A, B and C are true: four stages are necessary and sufficient for order 4, and order 5 needs 6 stages.

**Q10 — (B).** If $f=f(x)$, then $k_2=k_3=hf(x_n+h/2)$, and $y_{n+1}-y_n=\frac h6[f(x_n)+4f(x_n+\frac h2)+f(x_n+h)]$. This is Simpson's rule on two half-steps. (Heun reduces to the trapezoidal rule.)

**Q11 — (B).** On the negative real axis $|1+z+z^2/2|\le1$ iff $-2\le z\le0$, so $h\le 2/20=0.1$. (C) uses the RK4 real-axis bound $2.785/20$.

**Q12 — (C).** The global error is $\approx Ch^4$, so halving $h$ divides it by $2^4=16$. (D) is what you get if you use the local order 5.
