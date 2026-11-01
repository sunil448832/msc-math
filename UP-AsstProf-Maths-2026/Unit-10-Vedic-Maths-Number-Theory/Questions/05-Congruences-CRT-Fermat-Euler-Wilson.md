# Unit 10 · Topic 05 — Congruences, Chinese Remainder Theorem, Fermat, Euler, Wilson
> Syllabus coverage: Congruences, Chinese remainder theorem
> Cheatsheet: [../Cheatsheets/05-Congruences-CRT-Fermat-Euler-Wilson.md](../Cheatsheets/05-Congruences-CRT-Fermat-Euler-Wilson.md)

**Q1.** `[Numerical]` ★ The remainder when $3^{100}$ is divided by 7 is

(A) 1

(B) 2

(C) 4

(D) 6

**Q2.** `[Numerical]` ★ The last two digits of $7^{2026}$ are

(A) 01

(B) 07

(C) 43

(D) 49

**Q3.** `[Numerical]` ★★ The number of incongruent solutions of $6x \equiv 4 \pmod{20}$ is

(A) 0

(B) 1

(C) 2

(D) 4

**Q4.** `[Numerical]` ★★ (Sunzi's problem) The least positive integer $x$ with $x \equiv 2 \pmod 3$, $x \equiv 3 \pmod 5$ and $x \equiv 2 \pmod 7$ is

(A) 23

(B) 53

(C) 68

(D) 128

**Q5.** `[Concept]` ★ For an integer $n \gt  1$, the congruence $(n-1)! \equiv -1 \pmod n$ holds if and only if

(A) $n$ is odd

(B) $n$ is prime

(C) $n$ is prime or $n = 4$

(D) $n$ is square-free

**Q6.** `[Application]` ★★ The remainder when $99!$ is divided by $101$ is

(A) 1

(B) 50

(C) 99

(D) 100

**Q7.** `[Match]` ★★ Match each modulus in List-I with the number of primitive roots modulo it in List-II.

| List-I (modulus) | List-II (number of primitive roots) |
|---|---|
| (a) 13 | 1. 0 |
| (b) 8 | 2. 8 |
| (c) 18 | 3. 4 |
| (d) 25 | 4. 2 |

(A) a-3, b-1, c-4, d-2

(B) a-3, b-4, c-1, d-2

(C) a-2, b-1, c-4, d-3

(D) a-3, b-1, c-2, d-4

**Q8.** `[Multi-Statement]` ★★ Consider the following statements.

I. $561$ is a Carmichael number.

II. $341$ is a pseudoprime to the base 2.

III. If $a^{n-1} \equiv 1 \pmod n$ for some $a$ with $\gcd(a,n)=1$, then $n$ is prime.

Which of the above is/are correct?

(A) I only

(B) I and II only

(C) II and III only

(D) I, II and III

**Q9.** `[Assertion-Reason]` ★★
**Assertion (A):** There is no primitive root modulo 8.
**Reason (R):** $x^2 \equiv 1 \pmod 8$ for every odd integer $x$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q10.** `[NOT-true / Counterexample]` ★★ Which of the following is NOT true?

(A) The order of 2 modulo 11 is 10.

(B) 2 is a primitive root modulo 13.

(C) The order of 10 modulo 7 is 6.

(D) 2 is a primitive root modulo 7.

**Q11.** `[Numerical]` ★★ The multiplicative inverse of 17 modulo 43 is

(A) 5

(B) 38

(C) 18

(D) 30

**Q12.** `[Numerical]` ★★★ The number of solutions of $x^2 \equiv 1 \pmod{120}$ in $\lbrace 0, 1, \dots, 119\rbrace$ is

(A) 4

(B) 8

(C) 12

(D) 16

**Q13.** `[Application]` ★★★ The remainder when $1^{100} + 2^{100} + \cdots + 100^{100}$ is divided by $101$ is

(A) 0

(B) 1

(C) 100

(D) 50

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | C | Numerical |
| 2 | D | Numerical |
| 3 | C | Numerical |
| 4 | A | Numerical |
| 5 | B | Concept |
| 6 | A | Application |
| 7 | A | Match |
| 8 | B | Multi-Statement |
| 9 | A | Assertion-Reason |
| 10 | D | NOT-true |
| 11 | B | Numerical |
| 12 | D | Numerical |
| 13 | C | Application |

## Solutions
**Q1 — (C).** $3^6\equiv1\pmod 7$ by Fermat, and $100 = 6\cdot16+4$. So $3^{100}\equiv3^4=81\equiv4$.

**Q2 — (D).** $7^4 = 2401\equiv1\pmod{100}$ and $2026\equiv2\pmod4$, so $7^{2026}\equiv49$. (Using $\varphi(100)=40$ also works, but the order 4 is quicker.)

**Q3 — (C).** $d=\gcd(6,20)=2$ divides 4, so there are exactly 2 solutions mod 20. Reduce to $3x\equiv2\pmod{10}$, which gives $x\equiv4$, so $x\equiv4, 14\pmod{20}$. Choosing (B) means forgetting that a solution mod 10 splits into $d$ classes mod 20.

**Q4 — (A).** $x\equiv2\pmod{21}$ (from the mod 3 and mod 7 conditions) and $x\equiv3\pmod5$ give $x = 23$, unique mod 105. $128 = 23+105$ is also a solution but not the least. $53$ and $68$ fail the mod 7 condition.

**Q5 — (B).** This is Wilson's theorem together with its converse. If $n$ is composite, then $\gcd((n-1)!, n) \gt  1$, so $(n-1)!\not\equiv -1$. For $n=4$: $3!=6\equiv2\pmod 4$. In fact $(n-1)!\equiv0\pmod n$ for every composite $n\ne4$.

**Q6 — (A).** Wilson: $100!\equiv-1\pmod{101}$. Since $100\equiv-1$, we get $99!\cdot(-1)\equiv-1$, so $99!\equiv1$. In general $(p-2)!\equiv1\pmod p$. (D) is the value of $100!$ mod 101.

**Q7 — (A).** If primitive roots exist mod $m$, there are $\varphi(\varphi(m))$ of them.
- $m=13$: $\varphi(12)=4$.
- $m=8$: none, since 8 is not of the form $1,2,4,p^k,2p^k$.
- $m=18$: $\varphi(\varphi(18))=\varphi(6)=2$.
- $m=25$: $\varphi(20)=8$.

**Q8 — (B).**
- I: $561=3\cdot11\cdot17$, and $2, 10, 16$ all divide $560$ (Korselt's criterion).
- II: $341=11\cdot31$, and $2^{10}\equiv1$ modulo both 11 and 31, so $2^{340}\equiv1\pmod{341}$.
- III is false: 341 with $a=2$ is a counterexample.

**Q9 — (A).** $\varphi(8)=4$, but every unit mod 8 has order at most 2 because $x^2\equiv1$. So no unit has order 4. R gives exactly this reason.

**Q10 — (D).** $2^3=8\equiv1\pmod7$, so $`\mathop{\mathrm{ord}}\nolimits_7 2=3\ne6`$. The others are true: $`\mathop{\mathrm{ord}}\nolimits_{11}2=10`$; $\mathop{\mathrm{ord}}\nolimits_{13}2=12$; and 10 is a primitive root mod 7, which is why $1/7$ has period 6.

**Q11 — (B).** $17\cdot38=646=15\cdot43+1$. The Euclidean algorithm gives this directly: $43=2\cdot17+9$, $17=9+8$, $9=8+1$.

**Q12 — (D).** $120=8\cdot3\cdot5$. The congruence $x^2\equiv1$ has 4 solutions mod 8, 2 mod 3 and 2 mod 5. By the CRT the total is $4\cdot2\cdot2=16$. Answer (B) treats the modulus-8 part as having 2 roots.

**Q13 — (C).** For prime $p$, $\sum_{k=1}^{p-1}k^m\equiv -1\pmod p$ if $(p-1)\mid m$, and $\equiv 0$ otherwise. Here $m=100=p-1$, so every term is $\equiv1$ by Fermat. The sum is $\equiv100\equiv-1$. (A) is the answer when $(p-1)\nmid m$.
