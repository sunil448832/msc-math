# Unit 1 · Topic 04 — UFD, PID, Euclidean Domain, Polynomial Rings
> Syllabus coverage: Unique factorization domain, principal ideal domain, Euclidean domain, Polynomial rings
> Cheatsheet: [../Cheatsheets/04-UFD-PID-Euclidean-Polynomial-Rings.md](../Cheatsheets/04-UFD-PID-Euclidean-Polynomial-Rings.md)

**Q1.** `[Concept]` ★ If $R$ is a unique factorization domain, then the polynomial ring $R[x]$ is always

(A) a Euclidean domain

(B) a principal ideal domain

(C) a unique factorization domain

(D) a field

**Q2.** `[Numerical]` ★ The number of units in the ring of Gaussian integers $\mathbb{Z}[i]$ is

(A) 2

(B) 4

(C) 6

(D) infinitely many

**Q3.** `[Application]` ★★ The number of roots of $x^2-1$ in $\mathbb{Z}_8$ is

(A) 1

(B) 4

(C) 3

(D) 2

**Q4.** `[Multi-Statement]` ★ Consider:

I. Every Euclidean domain is a principal ideal domain.

II. Every principal ideal domain is a Euclidean domain.

III. Every unique factorization domain is a principal ideal domain.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I and III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** $\mathbb{Z}[x]$ is not a principal ideal domain.
**Reason (R):** For an integral domain $D$, the ring $D[x]$ is a PID if and only if $D$ is a field.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★★ Match each ring in List-I with its best description in List-II.

| List-I | List-II |
|---|---|
| (a) $\mathbb{Z}[x]$ | 1. Euclidean domain |
| (b) $\mathbb{Q}[x]$ | 2. PID but not a Euclidean domain |
| (c) $\mathbb{Z}[\sqrt{-5}]$ | 3. UFD but not a PID |
| (d) $\mathbb{Z}\!\left[\frac{1+\sqrt{-19}}{2}\right]$ | 4. integral domain but not a UFD |

(A) a-3, b-1, c-2, d-4

(B) a-1, b-3, c-4, d-2

(C) a-3, b-2, c-4, d-1

(D) a-3, b-1, c-4, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following polynomials is NOT irreducible over $\mathbb{Q}$?

(A) $x^4+1$

(B) $x^3-2$

(C) $x^4+4$

(D) $x^5-6x+3$

**Q8.** `[Application]` ★★ Which of the following primes remains irreducible (prime) in $\mathbb{Z}[i]$?

(A) 2

(B) 5

(C) 13

(D) 7

**Q9.** `[Numerical]` ★★ The remainder when $x^{101}+x^{50}+1$ is divided by $x^2+1$ in $\mathbb{Q}[x]$ is

(A) $x$

(B) $x+2$

(C) $1$

(D) $-x+1$

**Q10.** `[Application]` ★ The polynomial $2x+4$ is

(A) irreducible in both $\mathbb{Z}[x]$ and $\mathbb{Q}[x]$

(B) irreducible in $\mathbb{Q}[x]$ but reducible in $\mathbb{Z}[x]$

(C) irreducible in $\mathbb{Z}[x]$ but reducible in $\mathbb{Q}[x]$

(D) reducible in both $\mathbb{Z}[x]$ and $\mathbb{Q}[x]$

**Q11.** `[Concept]` ★★ The number of units in the ring $\mathbb{Z}[\sqrt2]=\{a+b\sqrt2: a,b\in\mathbb{Z}\}$ is

(A) 2

(B) 4

(C) 6

(D) infinite

**Q12.** `[Numerical]` ★★ The number of elements in the quotient ring $\mathbb{Z}[i]/\langle 2+3i\rangle$ is

(A) 5

(B) 6

(C) 13

(D) infinite

**Q13.** `[Application]` ★★★ In $\mathbb{Z}[\sqrt{-5}]$, the element $2$ is

(A) a unit

(B) prime

(C) irreducible but not prime

(D) reducible

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Numerical |
| 3 | B | Application |
| 4 | A | Multi-Statement |
| 5 | A | Assertion-Reason |
| 6 | D | Match |
| 7 | C | NOT-true |
| 8 | D | Application |
| 9 | A | Numerical |
| 10 | B | Application |
| 11 | D | Concept |
| 12 | C | Numerical |
| 13 | C | Application |

## Solutions
**Q1 — (C).** By Gauss's theorem, $R$ a UFD implies $R[x]$ a UFD. It need not be a PID or ED: $\mathbb{Z}[x]$ is neither.

**Q2 — (B).** A unit has norm $a^2+b^2=1$, so the units are $\pm1,\pm i$, four in all.

**Q3 — (B).** $1^2,3^2,5^2,7^2$ are all $\equiv1\pmod8$, so there are 4 roots. A degree-$n$ polynomial has at most $n$ roots only over an **integral domain**, and $\mathbb{Z}_8$ is not one. Option (D) applies the field bound wrongly.

**Q4 — (A).** ED ⊂ PID ⊂ UFD, and both inclusions are strict. $\mathbb{Z}[\tfrac{1+\sqrt{-19}}2]$ is a PID that is not an ED, so II fails. $\mathbb{Z}[x]$ is a UFD that is not a PID, so III fails.

**Q5 — (A).** If $D[x]$ is a PID then $\langle x\rangle$ is a non-zero prime ideal, hence maximal, so $D\cong D[x]/\langle x\rangle$ is a field. The converse is standard. Since $\mathbb{Z}$ is not a field, $\mathbb{Z}[x]$ is not a PID, and $\langle2,x\rangle$ is the explicit witness. R directly explains A.

**Q6 — (D).** $\mathbb{Z}[x]$: UFD by Gauss, not a PID. $\mathbb{Q}[x]$: polynomial ring over a field, Euclidean with $\deg$ as the norm. $\mathbb{Z}[\sqrt{-5}]$: $6=2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5})$, so it is not a UFD. $\mathbb{Z}[\frac{1+\sqrt{-19}}2]$: the classic PID that is not an ED.

**Q7 — (C).** By the Sophie Germain identity, $x^4+4=(x^2+2x+2)(x^2-2x+2)$. (A): $(x+1)^4+1$ is Eisenstein at 2, so $x^4+1$ is irreducible over $\mathbb{Q}$, even though it is reducible mod every prime. (B) has no rational root and degree 3. (D) is Eisenstein at $p=3$.

**Q8 — (D).** A rational prime $p$ stays prime in $\mathbb{Z}[i]$ iff $p\equiv3\pmod4$. $2=-i(1+i)^2$, $5=(2+i)(2-i)$ and $13=(3+2i)(3-2i)$ all split. 7 does not, since $7\neq a^2+b^2$.

**Q9 — (A).** Modulo $x^2+1$ we have $x^2\equiv-1$. Then $x^{101}=x(x^2)^{50}\equiv x$ and $x^{50}=(x^2)^{25}\equiv-1$. The remainder is $x-1+1=x$.

**Q10 — (B).** In $\mathbb{Z}[x]$, $2x+4=2(x+2)$ with $2$ a non-unit, so it is reducible. In $\mathbb{Q}[x]$, $2$ is a unit and the polynomial is a degree-1 polynomial, hence irreducible. The point is that an irreducible element of $\mathbb{Z}[x]$ must be **primitive**.

**Q11 — (D).** $(1+\sqrt2)(-1+\sqrt2)=1$, so $1+\sqrt2$ is a unit of infinite order and $\pm(1+\sqrt2)^n$ are all units (Pell's equation $a^2-2b^2=\pm1$). The trap is to think of $\mathbb{Z}[i]$ (4 units) or of the imaginary quadratic rings, which have only finitely many units.

**Q12 — (C).** $|\mathbb{Z}[i]/\langle a+bi\rangle|=a^2+b^2=4+9=13$. Since 13 is prime, the quotient is $\cong\mathbb{Z}_{13}$, a field. This agrees with $2+3i$ being a Gaussian prime.

**Q13 — (C).** With $N(a+b\sqrt{-5})=a^2+5b^2$, a factorization $2=\alpha\beta$ into non-units would need $N(\alpha)=2$, which is impossible. So $2$ is irreducible. But $2\mid 6=(1+\sqrt{-5})(1-\sqrt{-5})$ while $2\nmid1\pm\sqrt{-5}$, so 2 is not prime. In a UFD irreducible = prime, so this is another proof that $\mathbb{Z}[\sqrt{-5}]$ is not a UFD.
