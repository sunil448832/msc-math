# Unit 9 · Topic 09 — Numerical Differentiation and Integration
> Syllabus coverage: Numerical differentiation and integration
> Cheatsheet: [../Cheatsheets/09-Numerical-Differentiation-Integration.md](../Cheatsheets/09-Numerical-Differentiation-Integration.md)

**Q1.** `[Concept]` ★ The degree of precision of Simpson's 1/3 rule is

(A) 1

(B) 2

(C) 3

(D) 4

**Q2.** `[Concept]` ★ From Newton's forward difference formula, the derivative at the tabular point $x_0$ is

(A) $\dfrac1h\left[\Delta y_0-\dfrac12\Delta^2y_0+\dfrac13\Delta^3y_0-\cdots\right]$

(B) $\dfrac1h\left[\Delta y_0+\dfrac12\Delta^2y_0+\dfrac13\Delta^3y_0+\cdots\right]$

(C) $\dfrac1h\left[\Delta y_0-\dfrac12\Delta^2y_0+\dfrac16\Delta^3y_0-\cdots\right]$

(D) $h\left[\Delta y_0-\dfrac12\Delta^2y_0+\dfrac13\Delta^3y_0-\cdots\right]$

**Q3.** `[Numerical]` ★ The trapezoidal rule with $h=0.5$ applied to $\displaystyle\int_0^1x^2\,dx$ gives

(A) $0.3333$

(B) $0.3500$

(C) $0.3750$

(D) $0.4000$

**Q4.** `[Numerical]` ★★ Simpson's 1/3 rule with $h=0.5$ applied to $\displaystyle\int_0^1\frac{dx}{1+x}$ gives (to 4 decimals)

(A) $0.6931$

(B) $0.6944$

(C) $0.7083$

(D) $0.6970$

**Q5.** `[Numerical]` ★★ For $f(x)=x^3$, the central difference approximation $\dfrac{f(1+h)-f(1-h)}{2h}$ to $f'(1)$ with $h=0.1$ gives

(A) $3.00$

(B) $2.71$

(C) $3.31$

(D) $3.01$

**Q6.** `[Numerical]` ★★ The two-point Gauss–Legendre rule $\displaystyle\int_{-1}^{1}f(x)\,dx\approx f\!\left(-\tfrac1{\sqrt3}\right)+f\!\left(\tfrac1{\sqrt3}\right)$ applied to $\displaystyle\int_{-1}^1x^4\,dx$ gives

(A) $2/5$

(B) $2/9$

(C) $1/9$

(D) $2/3$

**Q7.** `[Numerical]` ★★ Simpson's 3/8 rule with $h=1$ applied to $\displaystyle\int_0^3x^4\,dx$ (exact value $48.6$) gives

(A) $48.6$

(B) $49.5$

(C) $50.25$

(D) $51.0$

**Q8.** `[Multi-Statement]` ★★ Consider the following statements about composite rules on $n$ equal subintervals.

I. Composite Simpson's 1/3 rule requires $n$ to be even.

II. Composite Simpson's 3/8 rule requires $n$ to be a multiple of 3.

III. The trapezoidal rule integrates every polynomial of degree $\le2$ exactly.

Which are correct?

(A) I only

(B) I, II and III

(C) II and III only

(D) I and II only

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** If $f''>0$ on $[a,b]$, the composite trapezoidal rule overestimates $\int_a^bf$.
**Reason (R):** The composite trapezoidal error is $\int_a^bf-T_h=-\dfrac{(b-a)h^2}{12}f''(\xi)$ for some $\xi\in(a,b)$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[Match]` ★★ Match the single-panel rule with its error term (exact $-$ approximate).

| List-I | List-II |
|---|---|
| A. Trapezoidal (1 strip) | 1. $-\dfrac{3h^5}{80}f^{(4)}(\xi)$ |
| B. Simpson 1/3 (2 strips) | 2. $-\dfrac{h^3}{12}f''(\xi)$ |
| C. Simpson 3/8 (3 strips) | 3. $-\dfrac{h^7}{140}f^{(6)}(\xi)$ |
| D. Weddle (6 strips) | 4. $-\dfrac{h^5}{90}f^{(4)}(\xi)$ |

(A) A-2, B-4, C-1, D-3

(B) A-2, B-1, C-4, D-3

(C) A-4, B-2, C-1, D-3

(D) A-2, B-4, C-3, D-1

**Q11.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) The $n$-point Gauss–Legendre rule has degree of precision $2n-1$.

(B) The nodes of the $n$-point Gauss–Legendre rule are the zeros of the Legendre polynomial $P_n$.

(C) All weights of a Gauss–Legendre rule are positive.

(D) A closed Newton–Cotes rule with $n+1$ equally spaced points always has degree of precision $n+1$.

**Q12.** `[Application]` ★★★ For $\displaystyle\int_0^1x^2dx$ the trapezoidal values are $T(1)=0.5$ and $T(0.5)=0.375$. One step of Richardson (Romberg) extrapolation $\dfrac{4T(h/2)-T(h)}{3}$ gives

(A) $0.3125$

(B) $0.3542$

(C) $0.3333$

(D) $0.3750$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | A | Concept |
| 3 | C | Numerical |
| 4 | B | Numerical |
| 5 | D | Numerical |
| 6 | B | Numerical |
| 7 | B | Numerical |
| 8 | D | Multi-Statement |
| 9 | A | Assertion-Reason |
| 10 | A | Match |
| 11 | D | NOT-true / Counterexample |
| 12 | C | Application |

## Solutions
**Q1 — (C).** Simpson's rule is built from a quadratic but is exact for cubics as well: by symmetry it integrates $(x-x_1)^3$ exactly, and its error involves $f^{(4)}$. It fails for $x^4$.

**Q2 — (A).** $hD=\log(1+\Delta)=\Delta-\frac{\Delta^2}2+\frac{\Delta^3}3-\cdots$. Option (C) uses the wrong coefficient, and (D) has $h$ in the wrong place.

**Q3 — (C).** $\frac{0.5}{2}[0+2(0.25)+1]=0.25\times1.5=0.375$. It is larger than the exact $1/3$ because $x^2$ is convex (see Q9).

**Q4 — (B).** $\frac{0.5}{3}\left[1+4\cdot\frac23+\frac12\right]=\frac16(4.1667)=0.69444$. (A) is $\ln2$ (the exact value) and (C) is the trapezoidal value.

**Q5 — (D).** $(1.331-0.729)/0.2=3.01$. The error $\frac{h^2}{6}f'''=0.01$ is consistent with this. (C) is the forward difference and (B) the backward difference.

**Q6 — (B).** $2\cdot(1/\sqrt3)^4=2/9$. The rule is exact only up to degree 3, so it misses the exact value $2/5$ (A).

**Q7 — (B).** $\frac{3}{8}[0+3(1)+3(16)+81]=\frac38\cdot132=49.5$. As a check, the error formula gives $-\frac{3}{80}\cdot24=-0.9=48.6-49.5$.

**Q8 — (D).** I and II are true (Weddle needs $n$ to be a multiple of 6). III is false: the trapezoidal rule has degree of precision 1. For example, $\int_0^1x^2=1/3\ne1/2$.

**Q9 — (A).** By R, $f''>0$ gives $\int f-T_h<0$, so $T_h$ overestimates. The chord also lies above a convex curve. R directly yields A.

**Q10 — (A).** These are the standard error terms: $-\frac{h^3}{12}f''$, $-\frac{h^5}{90}f^{(4)}$, $-\frac{3h^5}{80}f^{(4)}$ and $-\frac{h^7}{140}f^{(6)}$.

**Q11 — (D).** With $n+1$ points, the degree of precision is $n+1$ only when $n$ is even (Simpson 1/3 with $n=2$ has degree 3). When $n$ is odd it is $n$ (trapezoidal with $n=1$ has degree 1, and 3/8 with $n=3$ has degree 3). A, B and C are standard.

**Q12 — (C).** $(4\cdot0.375-0.5)/3=1/3$, which is exact. One Romberg step on the trapezoidal rule reproduces Simpson's rule, which is exact for $x^2$.
