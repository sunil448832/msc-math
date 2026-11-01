# Unit 9 · Topic 08 — Finite Differences and Interpolation (Newton, Lagrange, Hermite, Splines)
> Syllabus coverage: Finite differences; Lagrange, Hermite and spline interpolations
> Cheatsheet: [../Cheatsheets/08-Finite-Differences-Interpolation.md](../Cheatsheets/08-Finite-Differences-Interpolation.md)

**Q1.** `[Concept]` ★ If $p_n$ interpolates a sufficiently smooth $f$ at distinct nodes $x_0,\dots,x_n$, then for some $\xi$, $f(x)-p_n(x)$ equals

(A) $\dfrac{f^{(n)}(\xi)}{n!}\prod_{i=0}^{n}(x-x_i)$

(B) $\dfrac{f^{(n+1)}(\xi)}{(n+1)!}\prod_{i=0}^{n}(x-x_i)$

(C) $\dfrac{f^{(n+1)}(\xi)}{n!}\prod_{i=0}^{n}(x-x_i)$

(D) $\dfrac{f^{(n+1)}(\xi)}{(n+1)!}\prod_{i=0}^{n}(x-x_i)^2$

**Q2.** `[Concept]` ★ To interpolate a value near the **end** of a table of equally spaced values, the most suitable formula is

(A) Newton's forward difference formula

(B) Newton's backward difference formula

(C) Gauss's forward central difference formula

(D) Bessel's formula

**Q3.** `[Numerical]` ★ With step length $h=2$, $\Delta^3(x^3)$ equals

(A) $6$

(B) $8$

(C) $24$

(D) $48$

**Q4.** `[Numerical]` ★★ The polynomial of degree $\le2$ through $(0,1),\ (1,3),\ (3,55)$ takes at $x=2$ the value

(A) $19$

(B) $21$

(C) $23$

(D) $25$

**Q5.** `[Numerical]` ★★ For $f(x)=1/x$, the divided difference $f[1,2,4]$ is

(A) $1/4$

(B) $-1/8$

(C) $1/8$

(D) $-1/4$

**Q6.** `[Numerical]` ★★★ With $h=1$, $\Delta^{10}\big[(1-x)(1-2x)(1-3x)\cdots(1-10x)\big]$ equals

(A) $10!$

(B) $(10!)^2$

(C) $2^{10}\cdot10!$

(D) $-(10!)^2$

**Q7.** `[Numerical]` ★★ The cubic Hermite interpolant $H$ with $H(0)=0,\ H'(0)=1,\ H(1)=1,\ H'(1)=0$ satisfies $H(1/2)=$

(A) $1/2$

(B) $7/8$

(C) $3/4$

(D) $5/8$

**Q8.** `[Multi-Statement]` ★★ With $E$ the shift operator ($Ef(x)=f(x+h)$), consider:

I. $\Delta-\nabla=\Delta\nabla$

II. $\mu^2=1+\tfrac14\delta^2$

III. $\nabla=E\Delta$

Which are correct?

(A) I and II only

(B) II and III only

(C) I and III only

(D) I, II and III

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** Through $n+1$ points with distinct abscissae there is exactly one polynomial of degree $\le n$, so the Lagrange and Newton divided-difference forms give the same polynomial.
**Reason (R):** A nonzero polynomial of degree $\le n$ has at most $n$ roots.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[Match]` ★★ Match each operator with its expression in terms of $E$.

| List-I | List-II |
|---|---|
| A. $\Delta$ | 1. $1-E^{-1}$ |
| B. $\nabla$ | 2. $E-1$ |
| C. $\delta$ | 3. $\tfrac12\left(E^{1/2}+E^{-1/2}\right)$ |
| D. $\mu$ | 4. $E^{1/2}-E^{-1/2}$ |

(A) A-2, B-1, C-4, D-3

(B) A-1, B-2, C-4, D-3

(C) A-2, B-1, C-3, D-4

(D) A-2, B-4, C-1, D-3

**Q11.** `[NOT-true / Counterexample]` ★★ For a natural cubic spline $S$ interpolating data at nodes $x_0<x_1<\dots<x_n$, which statement is NOT true?

(A) $S$ is a cubic on each $[x_{i-1},x_i]$ and $S\in C^2[x_0,x_n]$.

(B) $S''(x_0)=S''(x_n)=0$.

(C) Interpolation and continuity give $4n-2$ conditions on the $4n$ coefficients, so 2 end conditions are needed.

(D) $S$ is always a single cubic polynomial on the whole interval $[x_0,x_n]$.

**Q12.** `[Application]` ★★ The table $x:0,1,2,3,4$; $y:1,3,9,\,?\,,81$ has one missing entry. Assuming the data come from a polynomial of degree 3 (so $\Delta^4y_0=0$), the missing value is

(A) $27$

(B) $29$

(C) $31$

(D) $33$

**Q13.** `[Application]` ★★★ The function
$$S(x)=\begin{cases}x^3,&0\le x\le1\\[2pt] 1+3(x-1)+3(x-1)^2+c(x-1)^3,&1\le x\le2\end{cases}$$
is a cubic spline for every $c$. It is a **natural** cubic spline on $[0,2]$ exactly when $c=$

(A) $1$

(B) $0$

(C) $-1$

(D) $-2$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | B | Concept |
| 3 | D | Numerical |
| 4 | B | Numerical |
| 5 | C | Numerical |
| 6 | B | Numerical |
| 7 | D | Numerical |
| 8 | A | Multi-Statement |
| 9 | A | Assertion-Reason |
| 10 | A | Match |
| 11 | D | NOT-true / Counterexample |
| 12 | C | Application |
| 13 | C | Application |

## Solutions
**Q1 — (B).** This is the standard Cauchy remainder: derivative of order $n+1$ divided by $(n+1)!$. (D) is the Hermite form, but that one has $f^{(2n+2)}/(2n+2)!$.

**Q2 — (B).** Backward differences use $y_n,\nabla y_n,\nabla^2y_n,\dots$, which are available at the end of the table. Forward suits the beginning, and central formulas (Gauss, Stirling, Bessel) suit the middle.

**Q3 — (D).** $\Delta^n x^n=n!\,h^n$, so $\Delta^3x^3=6\cdot8=48$. (A) is the $h=1$ value.

**Q4 — (B).** $p(x)=1-6x+8x^2$ fits all three points, and $p(2)=1-12+32=21$.

**Q5 — (C).** For $1/x$, $f[a,b]=-\frac1{ab}$ and $f[a,b,c]=\frac{1}{abc}=\frac18$. Directly: $f[1,2]=-\frac12$, $f[2,4]=-\frac18$, so $f[1,2,4]=\frac{-1/8+1/2}{4-1}=\frac18$.

**Q6 — (B).** The product has degree 10 with leading coefficient $(-1)(-2)\cdots(-10)=10!$. Since $\Delta^{10}x^{10}=10!$ when $h=1$, the answer is $10!\cdot10!$. The sign is $+$ because there are ten negative factors.

**Q7 — (D).** Write $H=ax^3+bx^2+x$. Then $H(1)=1$ gives $a+b=0$, and $H'(1)=0$ gives $3a+2b+1=0$. So $b=1$, $a=-1$, and $H=-x^3+x^2+x$, giving $H(\tfrac12)=-\tfrac18+\tfrac14+\tfrac12=\tfrac58$.

**Q8 — (A).** I: $\Delta-\nabla=E-2+E^{-1}=(E-1)(1-E^{-1})$, true. II: $\mu^2=\frac14(E+2+E^{-1})=1+\frac14(E-2+E^{-1})$, true. III is false: $\nabla=E^{-1}\Delta$ (and $\Delta=E\nabla$).

**Q9 — (A).** If $p$ and $q$ both interpolate, then $p-q$ has degree $\le n$ and $n+1$ roots, so $p-q\equiv0$. R is exactly the reason for uniqueness.

**Q10 — (A).** $\Delta=E-1$, $\nabla=1-E^{-1}$, $\delta=E^{1/2}-E^{-1/2}$, $\mu=\frac12(E^{1/2}+E^{-1/2})$.

**Q11 — (D).** A spline is only *piecewise* cubic. The cubics can differ in the third derivative at the knots (as in Q13). A, B and C are true. There are $4n$ unknowns. Each piece must match the data at both of its endpoints, which gives $2n$ conditions and already makes $S$ continuous. Continuity of $S'$ and $S''$ at the $n-1$ interior knots gives $2(n-1)$ more. The total is $4n-2$, so 2 end conditions are still needed.

**Q12 — (C).** $y_4-4y_3+6y_2-4y_1+y_0=0$ gives $81-4y_3+54-12+1=0$, so $y_3=31$. (A) $27$ is the guess from the pattern $3^k$, but $3^x$ is not a cubic.

**Q13 — (C).** At $x=1$ both pieces give $S=1$, $S'=3$, $S''=6$, so $S\in C^2$ for every $c$. Natural means $S''(0)=0$ (true for $x^3$) and $S''(2)=6+6c=0$, so $c=-1$.
