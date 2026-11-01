# Unit 1 · Topic 03 — Rings, Ideals, Prime and Maximal Ideals, Quotient Rings
> Syllabus coverage: Rings, ideals, prime and maximal ideals, quotient rings
> Cheatsheet: [../Cheatsheets/03-Rings-Ideals-Quotient-Rings.md](../Cheatsheets/03-Rings-Ideals-Quotient-Rings.md)

**Q1.** `[Concept]` ★ In the polynomial ring $\mathbb{Z}[x]$, the ideal $\langle x\rangle$ is

(A) maximal

(B) prime but not maximal

(C) neither prime nor maximal

(D) maximal but not prime

**Q2.** `[Numerical]` ★★ The number of nilpotent elements in $\mathbb Z_{72}$ is

(A) 6

(B) 8

(C) 12

(D) 24

**Q3.** `[Numerical]` ★ The number of idempotent elements in $\mathbb Z_{30}$ is

(A) 2

(B) 4

(C) 6

(D) 8

**Q4.** `[Numerical]` ★ The number of non-zero zero divisors in $\mathbb Z_{24}$ is

(A) 15

(B) 16

(C) 8

(D) 14

**Q5.** `[Multi-Statement]` ★★ Let $R$ denote a commutative ring with unity. Consider:

I. Every maximal ideal of $R$ is a prime ideal.

II. Every non-zero prime ideal of $\mathbb{Z}$ is maximal.

III. Every non-zero prime ideal of $\mathbb{Z}[x]$ is maximal.

Which of the above is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I and II only

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** The quotient ring $\mathbb{Z}[x]/\langle 2, x\rangle$ is a field.
**Reason (R):** $\langle 2, x\rangle$ is a principal ideal of $\mathbb{Z}[x]$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each quotient ring in List-I with the ring it is isomorphic to in List-II.

| List-I | List-II |
|---|---|
| (a) $\mathbb{R}[x]/\langle x^2+1\rangle$ | 1. $\mathbb Z_2$ |
| (b) $\mathbb{Z}[x]/\langle x\rangle$ | 2. $\mathbb{C}$ |
| (c) $\mathbb{Z}[i]/\langle 1+i\rangle$ | 3. a field with 9 elements |
| (d) $\mathbb Z_3[x]/\langle x^2+1\rangle$ | 4. $\mathbb{Z}$ |

(A) a-2, b-1, c-4, d-3

(B) a-3, b-4, c-1, d-2

(C) a-2, b-4, c-1, d-3

(D) a-2, b-4, c-3, d-1

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) Every finite integral domain is a field.

(B) Every subring of a ring is an ideal.

(C) The intersection of two ideals of a ring is an ideal.

(D) The characteristic of an integral domain is either 0 or a prime.

**Q9.** `[Application]` ★★★ The quotient ring $R=\mathbb Z_3[x]/\langle x^2+x+1\rangle$

(A) is a field with 9 elements

(B) is an integral domain that is not a field

(C) has a non-zero nilpotent element

(D) is isomorphic to $\mathbb Z_3\times\mathbb Z_3$

**Q10.** `[Numerical]` ★ The characteristic of the ring $\mathbb Z_3\times\mathbb Z_4$ is

(A) 3

(B) 12

(C) 4

(D) 7

**Q11.** `[Application]` ★★ Let $R=C[0,1]$ be the ring of real-valued continuous functions on $[0,1]$, and let $M=\lbrace f\in R: f(1/2)=0\rbrace$. Then $M$ is

(A) a maximal ideal

(B) a prime ideal that is not maximal

(C) an ideal that is not prime

(D) a subring but not an ideal

**Q12.** `[Concept]` ★★ In a commutative ring $R$ with unity, the intersection of all prime ideals of $R$ is

(A) the Jacobson radical (intersection of all maximal ideals)

(B) the set of all zero divisors of $R$

(C) always $\lbrace 0\rbrace$

(D) the set of all nilpotent elements of $R$

**Q13.** `[Numerical]` ★★★ The number of ring homomorphisms (not necessarily preserving unity) from $\mathbb Z_{12}$ to $\mathbb Z_{28}$ is

(A) 2

(B) 4

(C) 1

(D) 12

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | C | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | D | Multi-Statement |
| 6 | C | Assertion-Reason |
| 7 | C | Match |
| 8 | B | NOT-true |
| 9 | C | Application |
| 10 | B | Numerical |
| 11 | A | Application |
| 12 | D | Concept |
| 13 | A | Numerical |

## Solutions
**Q1 — (B).** $\mathbb{Z}[x]/\langle x\rangle\cong\mathbb{Z}$, which is an integral domain but not a field, so $\langle x\rangle$ is prime but not maximal. It sits strictly inside the maximal ideal $\langle 2,x\rangle$. Option (D) is impossible: in a commutative ring with $1$, maximal implies prime.

**Q2 — (C).** $a\in\mathbb Z_n$ is nilpotent iff $a$ is divisible by $\mathop{\mathrm{rad}}\nolimits(n)$. Here $72=2^3\cdot3^2$ has radical $6$, so the nilpotents are the multiples of 6: $72/6=12$ of them, including 0.

**Q3 — (D).** $\mathbb Z_{30}\cong\mathbb Z_2\times\mathbb Z_3\times\mathbb Z_5$, and each field factor contributes the idempotents $0,1$. So there are $2^{\omega(30)}=2^3=8$. Option (A) is the field answer.

**Q4 — (A).** In $\mathbb Z_n$ every non-zero element is either a unit or a zero divisor. So the count is $24-1-\varphi(24)=24-1-8=15$. Option (B), 16, forgets that 0 is excluded.

**Q5 — (D).** I: $R/M$ is a field, hence an integral domain. II: the non-zero primes of $\mathbb{Z}$ are $p\mathbb{Z}$, which are maximal ($\mathbb{Z}$ is a PID). III fails: $\langle x\rangle$ is a non-zero prime ideal of $\mathbb{Z}[x]$ that is not maximal.

**Q6 — (C).** Evaluating at $x=0$ and reducing mod 2 gives $\mathbb{Z}[x]/\langle2,x\rangle\cong\mathbb Z_2$, a field, so A is true. R is false: $\langle 2,x\rangle$ is the standard example of a non-principal ideal, since a generator would have to divide both $2$ and $x$, hence be $\pm1$, but $1\notin\langle2,x\rangle$.

**Q7 — (C).** (a) $x\mapsto i$ gives $\mathbb{C}$. (b) $x\mapsto0$ gives $\mathbb{Z}$. (c) $N(1+i)=2$, so the quotient has 2 elements and is $\mathbb Z_2$. (d) $x^2+1$ has no root in $\mathbb Z_3$ ($0,1,2\mapsto1,2,2$), so it is irreducible and the quotient is a field of order $3^2=9$.

**Q8 — (B).** $\mathbb{Z}$ is a subring of $\mathbb{Q}$ but not an ideal, since $\tfrac12\cdot1\notin\mathbb{Z}$. (A) is Wedderburn's little theorem in its easy commutative form ($x\mapsto ax$ is injective, hence onto). (D) holds because $\mathop{\mathrm{char}}\nolimits=mn$ would give $(m1)(n1)=0$. (C) is standard.

**Q9 — (C).** Over $\mathbb Z_3$, $x^2+x+1=x^2-2x+1=(x-1)^2$. So $\bar x-1\ne0$ but $(\bar x-1)^2=0$: a non-zero nilpotent. The ring is therefore not a field or an integral domain, and not $\mathbb Z_3\times\mathbb Z_3$, which is reduced. The trap is (A): "$`x^2+x+1`$ is irreducible" is true over $\mathbb Z_2$ and $\mathbb{Q}$ but not over $\mathbb Z_3$.

**Q10 — (B).** $\mathop{\mathrm{char}}\nolimits(R\times S)=\mathop{\mathrm{lcm}}\nolimits(\mathop{\mathrm{char}}\nolimits R,\mathop{\mathrm{char}}\nolimits S)=\mathop{\mathrm{lcm}}\nolimits(3,4)=12$. Option (D), 7, adds the characteristics, and (A) and (C) take a single factor.

**Q11 — (A).** Evaluation $f\mapsto f(1/2)$ is an onto ring homomorphism $C[0,1]\to\mathbb{R}$ with kernel $M$. Then $R/M\cong\mathbb{R}$ is a field, so $M$ is maximal. (In fact every maximal ideal of $C[0,1]$ has this form.)

**Q12 — (D).** The nilradical equals the intersection of all prime ideals (Krull). The Jacobson radical, the intersection of the maximal ideals, contains the nilradical and can be strictly larger: e.g. in $\mathbb Z_{(p)}$ the nilradical is $0$ but the Jacobson radical is $p\mathbb Z_{(p)}$.

**Q13 — (A).** A ring homomorphism $\mathbb Z_m\to\mathbb Z_n$ is determined by $e=\phi(1)$, which must satisfy $e^2=e$ and $me=0$ in $\mathbb Z_n$. The idempotents of $\mathbb Z_{28}$ are $0,1,8,21$. Of these only $0$ and $21$ satisfy $12e\equiv0\pmod{28}$, since $12\cdot21=252=9\cdot28$. So there are 2. (Verified by enumeration.) Option (B), 4, is $\gcd(12,28)$, which is the number of *group* homomorphisms.
