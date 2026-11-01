# Unit 1 · Topic 01 — Groups: Cyclic, Permutation Groups, Cayley, Homomorphisms
> Syllabus coverage: Cyclic groups, permutation groups, Cayley's Theorem, Fundamental Theorem of homomorphism (with Lagrange, automorphism groups, $\mathbb Z_n$ facts)
> Cheatsheet: [../Cheatsheets/01-Groups-Cyclic-Permutation-Homomorphism.md](../Cheatsheets/01-Groups-Cyclic-Permutation-Homomorphism.md)

**Q1.** `[Concept]` ★ The number of generators of the cyclic group $\mathbb Z_{20}$ is

(A) 4

(B) 8

(C) 10

(D) 19

**Q2.** `[Numerical]` ★ The order of the permutation $\sigma = (1\thinspace 2\thinspace 3)(4\thinspace 5)(6\thinspace 7\thinspace 8\thinspace 9) \in S_9$ is

(A) 9

(B) 24

(C) 12

(D) 6

**Q3.** `[Numerical]` ★★ The number of elements of order 2 in the symmetric group $S_4$ is

(A) 6

(B) 7

(C) 3

(D) 9

**Q4.** `[Numerical]` ★★ The number of group homomorphisms from $\mathbb Z_{12}$ to $\mathbb Z_{18}$ is

(A) 6

(B) 2

(C) 12

(D) 36

**Q5.** `[Concept]` ★ The automorphism group $\operatorname{Aut}(\mathbb Z_8)$ is isomorphic to

(A) $\mathbb Z_8$

(B) $\mathbb Z_4$

(C) $\mathbb Z_2 \times \mathbb Z_2$

(D) $\mathbb Z_2$

**Q6.** `[Multi-Statement]` ★★ Consider the statements:

I. Every group of order $p^2$ ($p$ prime) is abelian.

II. Every abelian group is cyclic.

III. Every subgroup of a cyclic group is cyclic.

Which of the above is/are correct?

(A) I and II only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** The group $U(8) = \lbrace 1,3,5,7\rbrace$ under multiplication modulo 8 is not cyclic.
**Reason (R):** Every non-identity element of $U(8)$ has order 2.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Match]` ★★ Match List-I with List-II.

| List-I | List-II |
|---|---|
| (a) Maximum order of an element of $S_5$ | 1. 60 |
| (b) Number of 3-cycles in $S_4$ | 2. 9 |
| (c) Order of $A_5$ | 3. 6 |
| (d) Number of subgroups of $\mathbb Z_{36}$ | 4. 8 |

(A) a-3, b-4, c-1, d-2

(B) a-4, b-3, c-1, d-2

(C) a-3, b-2, c-1, d-4

(D) a-1, b-4, c-3, d-2

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) $S_3 \cong D_3$ (dihedral group of order 6)

(B) $\mathbb Z_6 \cong \mathbb Z_2 \times \mathbb Z_3$

(C) $\mathbb Z_4 \cong \mathbb Z_2 \times \mathbb Z_2$

(D) $(\mathbb{Z},+) \cong (2\mathbb{Z},+)$

**Q10.** `[Application]` ★★★ By Cayley's theorem the quaternion group $Q_8$ embeds in $S_8$. The smallest $n$ such that $Q_8$ is isomorphic to a subgroup of $S_n$ is

(A) 4

(B) 6

(C) 8

(D) 5

**Q11.** `[Application]` ★★ Using the Fundamental Theorem of Homomorphism, the quotient group $(\mathbb{Z}\times\mathbb{Z})/\langle(1,1)\rangle$ is isomorphic to

(A) $\mathbb{Z}\times\mathbb{Z}$

(B) $\mathbb Z_2$

(C) the trivial group

(D) $\mathbb{Z}$

**Q12.** `[Numerical]` ★★ The number of elements of order 5 in $\mathbb Z_{25}\times\mathbb Z_5$ is

(A) 4

(B) 20

(C) 25

(D) 24

**Q13.** `[Concept]` ★ Which of the following permutations in $S_6$ is even?

(A) $(1\thinspace 2\thinspace 3\thinspace 4)$

(B) $(1\thinspace 2)(3\thinspace 4\thinspace 5\thinspace 6)$

(C) $(1\thinspace 2\thinspace 3\thinspace 4\thinspace 5\thinspace 6)$

(D) $(1\thinspace 2)(3\thinspace 4)(5\thinspace 6)$

**Q14.** `[Numerical]` ★★★ The order of the automorphism group $\operatorname{Aut}(\mathbb Z_2\times\mathbb Z_4)$ is

(A) 4

(B) 8

(C) 6

(D) 2

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | B | Concept |
| 2 | C | Numerical |
| 3 | D | Numerical |
| 4 | A | Numerical |
| 5 | C | Concept |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | A | Match |
| 9 | C | NOT-true |
| 10 | C | Application |
| 11 | D | Application |
| 12 | D | Numerical |
| 13 | B | Concept |
| 14 | B | Numerical |

## Solutions
**Q1 — (B).** The generators of $\mathbb Z_n$ are the $k$ with $\gcd(k,n)=1$, so there are $\varphi(20)=20\cdot\frac12\cdot\frac45=8$. 19 counts all the non-zero elements, and 10 is $n/2$.

**Q2 — (C).** The cycles are disjoint, so the order is $\operatorname{lcm}(3,2,4)=12$. Option (B), 24, is the product of the cycle lengths, which is the usual mistake.

**Q3 — (D).** The elements of order 2 are the transpositions, $\binom42=6$ of them, and the double transpositions $(ab)(cd)$, $3$ of them, giving $6+3=9$. Option (A) forgets the double transpositions.

**Q4 — (A).** $\sharp \operatorname{Hom}(\mathbb Z_m,\mathbb Z_n)=\gcd(m,n)=\gcd(12,18)=6$. The image of $1$ must be an $a$ with $12a\equiv0 \pmod{18}$.

**Q5 — (C).** $\operatorname{Aut}(\mathbb Z_8)\cong U(8)=\lbrace 1,3,5,7\rbrace$, and every element squares to $1$, so the group is the Klein four-group. Order 4 alone does not make it $\mathbb Z_4$, and $U(n)$ is cyclic only for $n=1,2,4,p^k,2p^k$.

**Q6 — (B).** I holds because $G/Z(G)$ cyclic forces $G$ abelian, and $Z(G)\ne 1$ for $p$-groups. III is standard. II is false: $\mathbb Z_2\times\mathbb Z_2$ and $(\mathbb{Q},+)$ are abelian but not cyclic.

**Q7 — (A).** $3^2\equiv5^2\equiv7^2\equiv1\pmod 8$. A cyclic group of order 4 needs an element of order 4, and $U(8)$ has none, so R is exactly why A holds.

**Q8 — (A).** In $S_5$ the possible orders are $`\operatorname{lcm}`$s of the cycle types of 5, and the maximum is $\operatorname{lcm}(2,3)=6$ (a). There are $\binom43\cdot2=8$ 3-cycles in $S_4$ (b). $|A_5|=60$ (c). The number of subgroups of $\mathbb Z_{36}$ is $d(36)=9$ (d).

**Q9 — (C).** $\mathbb Z_4$ has an element of order 4 and $\mathbb Z_2\times\mathbb Z_2$ does not. $\mathbb Z_m\times\mathbb Z_n\cong\mathbb Z_{mn}$ iff $\gcd(m,n)=1$, which gives (B). In (D) the map $n\mapsto2n$ is an isomorphism. (Note that $\mathbb{Z}\cong 2\mathbb{Z}$ as groups but not as rings.)

**Q10 — (C).** A faithful action of $Q_8$ on a set needs a family of point-stabilizers whose cores intersect trivially. Every non-trivial subgroup of $Q_8$ contains the normal subgroup $\lbrace \pm1\rbrace$, so some stabilizer must be trivial, which gives an orbit of size 8. So $n=8$: here Cayley's regular representation is already the smallest one. Option (A), 4, is the trap of thinking "order 8 group fits in $S_4$" because $|S_4|=24$ is divisible by 8. The Sylow 2-subgroup of $S_4$ is $D_4$, not $Q_8$.

**Q11 — (D).** The map $\phi(a,b)=a-b$ is an onto homomorphism $\mathbb Z^2\to\mathbb{Z}$ with kernel $\lbrace (a,a)\rbrace =\langle(1,1)\rangle$. By the First Isomorphism Theorem the quotient is $\cong\mathbb{Z}$.

**Q12 — (D).** The elements with $5x=0$ are $\lbrace (a,b): 5a\equiv0\ (25)\rbrace$. There are $5$ choices for $a$ and $5$ for $b$, so 25 such elements. Removing the identity leaves $24$. Option (A), 4, counts only the order-5 elements inside $\mathbb Z_{25}$. Option (C) forgets to remove the identity.

**Q13 — (B).** A $k$-cycle has sign $(-1)^{k-1}$. In (B) the transposition is odd and the 4-cycle is odd, so the product is even. (A) and (C) are cycles of even length, so they are odd. (D) is three transpositions, so it is odd.

**Q14 — (B).** An automorphism sends the generator $u$ of order 2 to an element of order $\le 2$ and $v$ (of order 4) to an element of order 4, with the images generating the group. There are 4 choices for $v$'s image, namely $(0,1),(0,3),(1,1),(1,3)$, and then 2 valid choices for $u$'s image, namely $(1,0),(1,2)$. That gives $4\times2=8$, and $\operatorname{Aut}(\mathbb Z_2\times\mathbb Z_4)\cong D_4$. (Verified by enumeration.) Option (C), 6, is $|\operatorname{Aut}(\mathbb Z_2\times\mathbb Z_2)|$.
