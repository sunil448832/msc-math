# Unit 10 · Topic 06 — Quadratic Residues and the Quadratic Reciprocity Law
> Syllabus coverage: Quadratic reciprocity law and its applications
> Cheatsheet: [../Cheatsheets/06-Quadratic-Residues-Reciprocity.md](../Cheatsheets/06-Quadratic-Residues-Reciprocity.md)

**Q1.** `[Concept]` ★ For an odd prime $p$, the number of quadratic residues among $1, 2, \dots, p-1$ is

(A) $\dfrac{p-1}{2}$

(B) $\dfrac{p+1}{2}$

(C) $p-1$

(D) $\dfrac{p-1}{4}$

**Q2.** `[Numerical]` ★ The Legendre symbol $\left(\dfrac{3}{7}\right)$ equals

(A) $1$

(B) $-1$

(C) $0$

(D) $3$

**Q3.** `[Concept]` ★ For an odd prime $p$, the congruence $x^2 \equiv -1 \pmod p$ is solvable if and only if

(A) $p \equiv 3 \pmod 4$

(B) $p \equiv 1 \pmod 3$

(C) $p \equiv \pm1 \pmod 8$

(D) $p \equiv 1 \pmod 4$

**Q4.** `[Match]` ★★ For odd primes $p$ (with $p \ne 5$ in (d)), match each Legendre symbol in List-I with the condition in List-II under which it equals $+1$.

| List-I | List-II |
|---|---|
| (a) $\left(\frac{-1}{p}\right)$ | 1. $p\equiv 1, 3 \pmod 8$ |
| (b) $\left(\frac{2}{p}\right)$ | 2. $p\equiv \pm1 \pmod 5$ |
| (c) $\left(\frac{-2}{p}\right)$ | 3. $p\equiv 1 \pmod 4$ |
| (d) $\left(\frac{5}{p}\right)$ | 4. $p\equiv \pm1 \pmod 8$ |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-4, c-1, d-2

(C) a-4, b-3, c-1, d-2

(D) a-3, b-4, c-2, d-1

**Q5.** `[Numerical]` ★★★ ($383$ is prime.) The Legendre symbol $\left(\dfrac{219}{383}\right)$ equals

(A) $1$

(B) $-1$

(C) $0$

(D) It cannot be determined because $219$ is composite.

**Q6.** `[Multi-Statement]` ★★ Let $p$ be an odd prime and $n$ an odd positive integer. Consider the following statements.

I. The product of two quadratic non-residues mod $p$ is a quadratic residue mod $p$.

II. If the Jacobi symbol $\left(\frac{a}{n}\right) = 1$, then $x^2 \equiv a \pmod n$ is solvable.

III. If the Jacobi symbol $\left(\frac{a}{n}\right) = -1$, then $x^2 \equiv a \pmod n$ has no solution.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) I, II and III

(D) I and III only

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** $\left(\dfrac{7}{19}\right) = 1$.
**Reason (R):** Since $7 \equiv 19 \equiv 3 \pmod 4$, quadratic reciprocity gives $\left(\dfrac{7}{19}\right) = \left(\dfrac{19}{7}\right)$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[NOT-true / Counterexample]` ★ Which of the following is NOT a quadratic residue modulo 13?

(A) 3

(B) 4

(C) 5

(D) 10

**Q9.** `[Application]` ★★ Gauss's lemma is applied to $\left(\frac{5}{11}\right)$: let $n$ be the number of least positive residues of $5, 10, 15, 20, 25 \pmod{11}$ that exceed $11/2$. Then $\big(n, \left(\frac{5}{11}\right)\big)$ is

(A) $(2, +1)$

(B) $(3, -1)$

(C) $(1, -1)$

(D) $(2, -1)$

**Q10.** `[Numerical]` ★★ The number of solutions of $x^2 \equiv 11 \pmod{35}$ in $\lbrace 0, 1, \dots, 34\rbrace$ is

(A) 0

(B) 2

(C) 4

(D) 8

**Q11.** `[Application]` ★★★ For a prime $p \gt  3$, the congruence $x^2 + x + 1 \equiv 0 \pmod p$ has a solution if and only if

(A) $p \equiv 1 \pmod 4$

(B) $p \equiv 1 \pmod 3$

(C) $p \equiv \pm1 \pmod{12}$

(D) $p \equiv \pm1 \pmod 8$

**Q12.** `[Numerical]` ★★ The sum of all quadratic residues of 13 lying in $\lbrace 1, 2, \dots, 12\rbrace$ is

(A) 26

(B) 39

(C) 42

(D) 78

**Q13.** `[Numerical]` ★★ By Euler's criterion, the least non-negative residue of $5^{6} \pmod{13}$ is

(A) 0

(B) 1

(C) 5

(D) 12

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Concept |
| 2 | B | Numerical |
| 3 | D | Concept |
| 4 | B | Match |
| 5 | A | Numerical |
| 6 | D | Multi-Statement |
| 7 | C | Assertion-Reason |
| 8 | C | NOT-true |
| 9 | A | Application |
| 10 | C | Numerical |
| 11 | B | Application |
| 12 | B | Numerical |
| 13 | D | Numerical |

## Solutions
**Q1 — (A).** Squaring maps $U(\mathbb Z_p)$ onto the residues 2-to-1 (since $x$ and $-x$ have the same square), so there are $(p-1)/2$ residues. (B) counts 0 as well.

**Q2 — (B).** Both 3 and 7 are $\equiv 3\pmod 4$, so $\left(\frac37\right) = -\left(\frac73\right) = -\left(\frac13\right) = -1$. Directly: the squares mod 7 are $\lbrace 1,2,4\rbrace$, which does not contain 3.

**Q3 — (D).** $\left(\frac{-1}{p}\right) = (-1)^{(p-1)/2}$ by Euler's criterion. This is $+1$ iff $p\equiv1\pmod4$. (C) is the condition for $\left(\frac2p\right)$.

**Q4 — (B).**
- $\left(\frac{-1}p\right)=1$ iff $p\equiv1\ (4)$.
- $\left(\frac2p\right)=1$ iff $p\equiv\pm1\ (8)$.
- $\left(\frac{-2}p\right)=\left(\frac{-1}p\right)\left(\frac2p\right)=1$ iff $p\equiv1,3\ (8)$.
- $\left(\frac5p\right)=\left(\frac p5\right)=1$ iff $p\equiv\pm1\ (5)$, using reciprocity with $5\equiv1\pmod 4$.

**Q5 — (A).** $219=3\cdot73$.
- $\left(\frac3{383}\right)$: both are $\equiv3\pmod 4$, so it equals $-\left(\frac{383}3\right)=-\left(\frac23\right)=-(-1)=1$.
- $\left(\frac{73}{383}\right)$: $73\equiv1\pmod 4$, so it equals $\left(\frac{383}{73}\right)=\left(\frac{18}{73}\right)=\left(\frac2{73}\right)\left(\frac9{73}\right)=1$, since $73\equiv1\pmod 8$.

The product is $+1$. (D) is wrong because the Legendre symbol is multiplicative in its top entry.

**Q6 — (D).**
- I is true: the Legendre symbol is multiplicative and $(-1)(-1)=1$.
- II is false: $\left(\frac2{15}\right)=\left(\frac23\right)\left(\frac25\right)=(-1)(-1)=1$, yet $x^2\equiv2\pmod{15}$ has no solution (2 is not a square mod 3).
- III is true: $\left(\frac an\right)=-1$ means $\left(\frac ap\right)=-1$ for some $p\mid n$, so there is already no solution mod $p$.

**Q7 — (C).** A is true: $7\equiv 8^2=64\pmod{19}$, since $64-57=7$. R is false: when both primes are $\equiv3\pmod4$, reciprocity gives $\left(\frac7{19}\right) = -\left(\frac{19}7\right)$. Indeed $\left(\frac{19}{7}\right)=\left(\frac57\right)=-1$.

**Q8 — (C).** The squares mod 13 are $1,4,9,3,12,10$, i.e. $\lbrace 1,3,4,9,10,12\rbrace$. So 5 is a non-residue. (Also $\left(\frac5{13}\right)=\left(\frac{13}5\right)=\left(\frac35\right)=-1$.)

**Q9 — (A).** The residues are $5,10,4,9,3$. Those exceeding $5.5$ are $10$ and $9$, so $n=2$ and $\left(\frac5{11}\right)=(-1)^2=+1$. Check: $4^2=16\equiv5\pmod{11}$.

**Q10 — (C).** $11\equiv1\pmod5$, which gives 2 roots, and $11\equiv4\pmod7$, which gives 2 roots. Both are nonzero residues, so by the CRT there are $2\cdot2=4$ solutions mod 35.

**Q11 — (B).** Multiply by 4: $(2x+1)^2\equiv-3\pmod p$. So the congruence is solvable iff $\left(\frac{-3}{p}\right)=1$. By reciprocity $\left(\frac{-3}p\right)=\left(\frac p3\right)$, which is $1$ iff $p\equiv1\pmod 3$. (C) is the condition for $\left(\frac3p\right)$, which does not account for the factor $-1$.

**Q12 — (B).** $1+3+4+9+10+12=39$. For $p\equiv1\pmod4$, the residues pair as $r \leftrightarrow p-r$, giving the sum $p(p-1)/4=39$. (D) is the sum of all of $1,\dots,12$.

**Q13 — (D).** $5^{(13-1)/2}\equiv\left(\frac5{13}\right)=-1\equiv12\pmod{13}$. Directly: $5^2=25\equiv-1$, so $5^6\equiv(-1)^3=-1$. (B) would mean 5 is a residue, which Q8 shows it is not.
