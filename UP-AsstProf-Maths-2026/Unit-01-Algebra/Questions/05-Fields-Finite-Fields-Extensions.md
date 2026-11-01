# Unit 1 · Topic 05 — Fields, Finite Fields, Field Extensions
> Syllabus coverage: Fields, finite fields, field extensions (with degree, algebraic elements, splitting fields, subfields of $GF(p^n)$, counting irreducible polynomials, constructibility basics)
> Cheatsheet: [../Cheatsheets/05-Fields-Finite-Fields-Extensions.md](../Cheatsheets/05-Fields-Finite-Fields-Extensions.md)

**Q1.** `[Concept]` ★ The degree $[\mathbb{Q}(\sqrt2,\sqrt3):\mathbb{Q}]$ is

(A) 2

(B) 4

(C) 6

(D) 3

**Q2.** `[Numerical]` ★★ The degree over $\mathbb{Q}$ of the splitting field of $x^3-2$ is

(A) 3

(B) 9

(C) 6

(D) 2

**Q3.** `[Numerical]` ★★ The number of subfields of the finite field $GF(p^{12})$ (including $GF(p)$ and $GF(p^{12})$ itself) is

(A) 4

(B) 12

(C) 2

(D) 6

**Q4.** `[Numerical]` ★★★ The number of monic irreducible polynomials of degree 4 over $\mathbb Z_2$ is

(A) 3

(B) 2

(C) 4

(D) 6

**Q5.** `[Multi-Statement]` ★★ Consider:

I. The multiplicative group of a finite field is cyclic.

II. There exists a field with 6 elements.

III. $GF(p^m)$ is (isomorphic to) a subfield of $GF(p^n)$ if and only if $m\mid n$.

Which of the above is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q6.** `[Assertion-Reason]` ★★
**Assertion (A):** The angle $60^\circ$ can be trisected with straightedge and compass.
**Reason (R):** $\cos 20^\circ$ is a root of $8x^3-6x-1$, which is irreducible over $\mathbb{Q}$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q7.** `[Match]` ★★ Match each extension in List-I with its degree in List-II.

| List-I | List-II |
|---|---|
| (a) $[\mathbb{Q}(\sqrt2+\sqrt3):\mathbb{Q}]$ | 1. 2 |
| (b) $[\mathbb{Q}(\zeta_7):\mathbb{Q}]$, $\zeta_7=e^{2\pi i/7}$ | 2. 4 |
| (c) $[\mathbb{Q}(\sqrt[5]{2}):\mathbb{Q}]$ | 3. 5 |
| (d) $[\mathbb{Q}(i,\sqrt2):\mathbb{Q}(i)]$ | 4. 6 |

(A) a-2, b-4, c-3, d-1

(B) a-1, b-4, c-3, d-2

(C) a-2, b-3, c-4, d-1

(D) a-4, b-2, c-3, d-1

**Q8.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) $[\mathbb{Q}(\pi):\mathbb{Q}]$ is infinite.

(B) Every finite extension is algebraic.

(C) Every algebraic extension is finite.

(D) $\mathbb{C}$ is an algebraic extension of $\mathbb{R}$.

**Q9.** `[Numerical]` ★★ The number of generators of the cyclic group $GF(16)^{\times}$ (i.e. the number of primitive elements of $`GF(16)`$) is

(A) 15

(B) 4

(C) 8

(D) 6

**Q10.** `[Concept]` ★ Which of the following can be the number of elements of a finite field?

(A) 36

(B) 64

(C) 100

(D) 6

**Q11.** `[Application]` ★★ The degree over $\mathbb{Q}$ of the splitting field of $x^4+1$ is

(A) 1

(B) 2

(C) 8

(D) 4

**Q12.** `[Concept]` ★★ The order of the group of all field automorphisms of $GF(p^n)$ is

(A) $n$

(B) 1

(C) $p$

(D) $p^n-1$

**Q13.** `[Application]` ★ The degree $[\mathbb{Q}(\sqrt2,\sqrt8):\mathbb{Q}]$ is

(A) 2

(B) 4

(C) 8

(D) 1

**Q14.** `[Application]` ★★★ Let $K$ be the smallest extension of $\mathbb Z_2$ that contains a root of $x^2+x+1$ and a root of $x^3+x+1$. The number of elements of $K$ is

(A) 32

(B) 8

(C) 64

(D) 4

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | C | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | B | Multi-Statement |
| 6 | D | Assertion-Reason |
| 7 | A | Match |
| 8 | C | NOT-true |
| 9 | C | Numerical |
| 10 | B | Concept |
| 11 | D | Application |
| 12 | A | Concept |
| 13 | A | Application |
| 14 | C | Application |

## Solutions
**Q1 — (B).** $\sqrt3\notin\mathbb{Q}(\sqrt2)$, so the degree is $2\cdot2=4$ by the tower law. A basis is $\lbrace 1,\sqrt2,\sqrt3,\sqrt6\rbrace$.

**Q2 — (C).** The splitting field is $\mathbb{Q}(\sqrt[3]2,\omega)$. Here $[\mathbb{Q}(\sqrt[3]2):\mathbb{Q}]=3$, and $\omega\notin\mathbb{R}\supset\mathbb{Q}(\sqrt[3]2)$ adds degree 2, so the total is $6$ (Galois group $S_3$). Option (A) forgets the complex roots.

**Q3 — (D).** Subfields of $GF(p^n)$ correspond one-to-one with the divisors of $n$, and $d(12)=|\lbrace 1,2,3,4,6,12\rbrace |=6$.

**Q4 — (A).** By Gauss's formula, $N_q(n)=\frac1n\sum_{d\mid n}\mu(d)q^{n/d}$. So $N_2(4)=\frac14(16-4)=3$: these are $x^4+x+1$, $x^4+x^3+1$, $x^4+x^3+x^2+x+1$. (Verified by enumeration.) $x^4+x^2+1=(x^2+x+1)^2$ is a trap.

**Q5 — (B).** I: a finite subgroup of $F^{\times}$ is cyclic. II: finite fields have prime-power order, and $6$ is not a prime power. III: the standard subfield criterion.

**Q6 — (D).** $\cos3\theta=4\cos^3\theta-3\cos\theta$ with $\theta=20^\circ$ gives $4c^3-3c=\frac12$, i.e. $8c^3-6c-1=0$. That cubic has no rational roots ($\pm1,\pm\frac12,\pm\frac14,\pm\frac18$ fail), so it is irreducible. So $[\mathbb{Q}(\cos20^\circ):\mathbb{Q}]=3$, which is not a power of 2, and $\cos 20^\circ$ is not constructible. So A is false and R is true. (R is in fact the reason A fails.)

**Q7 — (A).** (a) $\mathbb{Q}(\sqrt2+\sqrt3)=\mathbb{Q}(\sqrt2,\sqrt3)$, with minimal polynomial $x^4-10x^2+1$, so the degree is 4. (b) $\varphi(7)=6$. (c) $x^5-2$ is Eisenstein, so the degree is 5. (d) $x^2-2$ stays irreducible over $\mathbb{Q}(i)$ because $\sqrt2\notin\mathbb{Q}(i)$, so the degree is 2.

**Q8 — (C).** The field $\overline{\mathbb{Q}}$ of algebraic numbers, or $\mathbb{Q}(\sqrt2,\sqrt3,\sqrt5,\dots)$, is algebraic over $\mathbb{Q}$ of infinite degree. (A): $\pi$ is transcendental, so $1,\pi,\pi^2,\dots$ are independent. (B) is standard. (D): $[\mathbb{C}:\mathbb{R}]=2$.

**Q9 — (C).** $GF(16)^{\times}$ is cyclic of order 15, so it has $\varphi(15)=8$ generators. Option (A), 15, counts all the non-zero elements.

**Q10 — (B).** A finite field has order $p^n$, and only $64=2^6$ is a prime power. $36$, $100$ and $6$ are not.

**Q11 — (D).** The roots are the primitive 8th roots of unity $\zeta_8^{1,3,5,7}$, all of which lie in $\mathbb{Q}(\zeta_8)=\mathbb{Q}(i,\sqrt2)$, of degree $\varphi(8)=4$. Option (C), 8, is the trap of multiplying $4\times 2$ as if it were $x^4-2$, whose splitting field does have degree 8.

**Q12 — (A).** $\mathop{\mathrm{Aut}}\nolimits(GF(p^n))=\mathop{\mathrm{Gal}}\nolimits(GF(p^n)/GF(p))$, because every automorphism fixes the prime field. This group is cyclic of order $n$, generated by the Frobenius map $a\mapsto a^p$. Option (D) is $|GF(p^n)^{\times}|$.

**Q13 — (A).** $\sqrt8=2\sqrt2\in\mathbb{Q}(\sqrt2)$, so the field is just $\mathbb{Q}(\sqrt2)$, of degree 2. Option (B) blindly multiplies the degrees.

**Q14 — (C).** Both polynomials are irreducible over $\mathbb Z_2$, since neither has a root. Their roots generate $GF(2^2)$ and $GF(2^3)$. The smallest field containing both is $GF(2^{\mathop{\mathrm{lcm}}\nolimits(2,3)})=GF(2^6)$, which has $64$ elements. Option (A), 32, adds the exponents ($2+3=5$), and option (B) is $GF(8)$, which does not contain $GF(4)$ because $2\nmid3$.
