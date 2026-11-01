# Unit 1 · Topic 02 — Group Action, Class Equation, Sylow Theorems
> Syllabus coverage: Group action, class equation, Sylow theorems and their applications
> Cheatsheet: [../Cheatsheets/02-Group-Action-Class-Equation-Sylow.md](../Cheatsheets/02-Group-Action-Class-Equation-Sylow.md)

**Q1.** `[Concept]` ★ The number of Sylow 3-subgroups of $S_4$ is

(A) 1

(B) 3

(C) 4

(D) 6

**Q2.** `[Numerical]` ★ The number of conjugacy classes in $S_5$ is

(A) 5

(B) 7

(C) 6

(D) 10

**Q3.** `[Numerical]` ★★ The number of elements of $S_5$ conjugate to $(1\,2\,3)(4\,5)$ is

(A) 10

(B) 24

(C) 30

(D) 20

**Q4.** `[Multi-Statement]` ★★ Consider the statements:

I. Every group of order 15 is cyclic.

II. Every group of order 21 is cyclic.

III. Every group of order 25 is abelian.

Which of the above is/are correct?

(A) I and III only

(B) I and II only

(C) III only

(D) I, II and III

**Q5.** `[Assertion-Reason]` ★★
**Assertion (A):** Every group of order 30 has a normal subgroup of order 15.
**Reason (R):** Every group of order 30 is abelian.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q6.** `[Match]` ★★ Match the group in List-I with the number of its Sylow subgroups in List-II.

| List-I | List-II |
|---|---|
| (a) Sylow 2-subgroups of $S_3$ | 1. 1 |
| (b) Sylow 3-subgroups of $A_4$ | 2. 3 |
| (c) Sylow 5-subgroups of $A_5$ | 3. 4 |
| (d) Sylow 3-subgroups of $S_3$ | 4. 6 |

(A) a-2, b-3, c-4, d-1

(B) a-2, b-4, c-3, d-1

(C) a-3, b-2, c-4, d-1

(D) a-1, b-3, c-4, d-2

**Q7.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) A group of order $p^n$ ($p$ prime, $n\ge1$) has a non-trivial centre.

(B) If $p<q$ are primes, a group of order $pq$ has a normal Sylow $q$-subgroup.

(C) A group of order $p^2$ is abelian.

(D) Every group of order 12 has a normal Sylow 3-subgroup.

**Q8.** `[Application]` ★★★ The vertices of a square are coloured with 2 colours. Two colourings are considered the same if one can be obtained from the other by a rotation of the square. Using Burnside's lemma (counting orbits of the action of $\mathbb{Z}_4$), the number of distinct colourings is

(A) 4

(B) 6

(C) 8

(D) 16

**Q9.** `[Numerical]` ★★ The number of elements of order 7 in a simple group of order 168 is

(A) 6

(B) 8

(C) 42

(D) 48

**Q10.** `[Concept]` ★★ If $G$ is a non-abelian group of order $p^3$ ($p$ prime), then $|Z(G)|$ equals

(A) 1

(B) $p$

(C) $p^2$

(D) $p^3$

**Q11.** `[Application]` ★★★ A group of order 55 acts on a set with 18 elements. The minimum possible number of fixed points of this action is

(A) 0

(B) 1

(C) 2

(D) 3

**Q12.** `[Numerical]` ★★★ The number of elements in the conjugacy class of $(1\,2\,3\,4\,5)$ in the alternating group $A_5$ is

(A) 24

(B) 12

(C) 6

(D) 20

**Q13.** `[Concept]` ★ In the class equation $|G| = |Z(G)| + \sum [G:C(a)]$ of a finite group $G$, the number of conjugacy classes of size 1 equals

(A) the order of the centre $Z(G)$

(B) the index $[G:Z(G)]$

(C) the number of conjugacy classes of $G$

(D) the number of Sylow subgroups of $G$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Concept |
| 2 | B | Numerical |
| 3 | D | Numerical |
| 4 | A | Multi-Statement |
| 5 | C | Assertion-Reason |
| 6 | A | Match |
| 7 | D | NOT-true |
| 8 | B | Application |
| 9 | D | Numerical |
| 10 | B | Concept |
| 11 | C | Application |
| 12 | B | Numerical |
| 13 | A | Concept |

## Solutions
**Q1 — (C).** $|S_4|=24=2^3\cdot3$, so $n_3\mid 8$ and $n_3\equiv1\pmod 3$, which allows $n_3\in\{1,4\}$. The 8 three-cycles generate 4 distinct subgroups of order 3, so $n_3=4$. Option (B), 3, is $n_2(S_4)$.

**Q2 — (B).** Conjugacy classes of $S_n$ correspond to cycle types, i.e. partitions of $n$, and $p(5)=7$.

**Q3 — (D).** The class size is $\dfrac{5!}{|C(\sigma)|}$. The centralizer of a $3$-cycle times a disjoint transposition is $\langle(123)\rangle\times\langle(45)\rangle$, of order $3\cdot2=6$, so the class has $120/6=20$ elements. Directly: choose the 3-cycle ($\binom53\cdot2=20$ ways) and the transposition is then forced.

**Q4 — (A).** Groups of order $pq$ with $p<q$ and $p\nmid q-1$ are cyclic: $15=3\cdot5$ with $3\nmid4$, so I holds. Order $25=p^2$ is abelian, so III holds. For $21=3\cdot7$ we have $3\mid 6$, and a non-abelian group $\mathbb{Z}_7\rtimes\mathbb{Z}_3$ exists, so II fails.

**Q5 — (C).** For order 30, if neither $n_3=1$ nor $n_5=1$ we would have $n_3=10$ and $n_5=6$, giving $20+24>30$ elements. So $P_3$ or $P_5$ is normal, and then $P_3P_5$ is a subgroup of order 15 and index 2, hence normal. So A is true. R is false: $D_{15}$ and $S_3\times\mathbb{Z}_5$ are non-abelian groups of order 30.

**Q6 — (A).** $S_3$ has 3 subgroups of order 2 and a single (normal) $A_3$. $A_4$ has $8$ elements of order 3, giving $4$ subgroups. $A_5$ has $24$ five-cycles, giving $6$ subgroups. So the match is a-2, b-3, c-4, d-1.

**Q7 — (D).** $A_4$ (order 12) has $n_3=4$. (A) follows from the class equation. (B) holds because $n_q\mid p<q$ and $n_q\equiv1 \pmod q$ force $n_q=1$. (C) holds because $Z(G)\neq1$ and $G/Z(G)$ cyclic imply abelian.

**Q8 — (B).** The rotation by $0$ fixes $2^4=16$ colourings, the rotations by $90^\circ$ and $270^\circ$ fix $2$ each, and the rotation by $180^\circ$ fixes $2^2=4$. The number of orbits is $(16+2+4+2)/4=6$. Option (D), 16, ignores the action, and option (C), 8, is $16/2$.

**Q9 — (D).** $168=2^3\cdot3\cdot7$, so $n_7\mid 24$ and $n_7\equiv1\pmod 7$, giving $n_7\in\{1,8\}$. Simplicity rules out $1$, so $n_7=8$. Distinct subgroups of prime order meet trivially, so there are $8\times6=48$ elements of order 7. Option (B), 8, is the number of subgroups, not of elements.

**Q10 — (B).** $Z(G)\neq1$, and $|Z(G)|\neq p^2$ because then $G/Z(G)$ would be cyclic of order $p$, forcing $G$ abelian. $|Z(G)|\neq p^3$ since $G$ is non-abelian. So $|Z(G)|=p$.

**Q11 — (C).** Orbit sizes divide 55, so they are $1,5,11,55$. Writing $18=5a+11b+f$, where $f$ is the number of fixed points: $b=1,a=1$ gives $f=2$; $b=0,a=3$ gives $f=3$; and $f=0$ or $1$ is impossible because $17,18$ are not of the form $5a+11b$. $f=2$ is attained, for example by $\mathbb{Z}_{55}$ acting on cosets of subgroups of orders 5 and 11 plus two fixed points. Option (A) is the trap answer: the key point is that a fixed point is forced.

**Q12 — (B).** In $S_5$ the 5-cycles form one class of size 24. Their centralizer in $S_5$ is $\langle\sigma\rangle\subset A_5$, so the class splits into two $A_5$-classes of size 12. This is consistent with the class equation $60=1+15+20+12+12$. Option (A), 24, is the $S_5$-class.

**Q13 — (A).** $|\mathrm{cl}(a)|=1$ iff $a\in Z(G)$, so the singleton classes are exactly the central elements.
