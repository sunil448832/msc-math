# Cheatsheet · Unit 10 · Topic 05 — Congruences, CRT, Fermat, Euler, Wilson
> Questions: [../Questions/05-Congruences-CRT-Fermat-Euler-Wilson.md](../Questions/05-Congruences-CRT-Fermat-Euler-Wilson.md)

## 1. Basics
- $a\equiv b\pmod m$ means $m\mid a-b$. This is an equivalence relation compatible with $+$ and $\times$.
- **Cancellation:** $ca\equiv cb\pmod m \iff a\equiv b\pmod{m/\gcd(c,m)}$. You may cancel freely only when $\gcd(c,m)=1$.
- If $a\equiv b$ modulo $m_1,\dots,m_k$, then $a\equiv b\pmod{\operatorname{lcm}(m_i)}$.
- **Divisibility tests:** 3 and 9 use the digit sum. 11 uses the alternating digit sum. 7, 11 and 13 use alternating sums of 3-digit blocks (since $1001=7\cdot11\cdot13$).

## 2. Linear congruences
For $ax\equiv b\pmod m$ with $d=\gcd(a,m)$:
- the congruence is **solvable iff $d\mid b$**;
- it then has exactly **$d$ incongruent solutions** mod $m$, namely $x_0+k\frac md$ for $k=0,\dots,d-1$.

The **inverse** $a^{-1}\bmod m$ exists iff $\gcd(a,m)=1$. Find it with the extended Euclidean algorithm or as $a^{\varphi(m)-1}$.

Examples:
- $7^{-1}\equiv15\pmod{26}$ and $17^{-1}\equiv38\pmod{43}$.
- $6x\equiv4\pmod{20}$ gives $x\equiv4,14$.
- $6x\equiv4\pmod{15}$ has no solution, since $3\nmid4$.

## 3. Chinese remainder theorem
If $m_1,\dots,m_k$ are **pairwise coprime**, then the system $x\equiv a_i\pmod{m_i}$ has a **unique** solution mod $M=\prod m_i$:
$$x\equiv\sum a_iM_iy_i,\qquad M_i=M/m_i,\quad y_i\equiv M_i^{-1}\pmod{m_i}.$$
- **General version:** $x\equiv a_i\pmod{m_i}$ is solvable iff $a_i\equiv a_j\pmod{\gcd(m_i,m_j)}$ for all $i,j$. The solution is then unique mod $\operatorname{lcm}$.
- **Ring form:** $\mathbb Z_{mn}\cong\mathbb Z_m\times\mathbb Z_n$ iff $\gcd(m,n)=1$. As a consequence, $\varphi$ is multiplicative and solution counts multiply.
- **Sunzi** (*Sunzi Suanjing*, c. 3rd–5th c.): $x\equiv2\ (3)$, $3\ (5)$, $2\ (7)$ gives $x=23$ (mod 105).

## 4. Classical theorems
| Theorem | Statement | Hypothesis |
|---|---|---|
| **Fermat's little theorem** | $a^{p-1}\equiv1\pmod p$, and $a^p\equiv a$ for all $a$ | $p$ prime, $p\nmid a$ (for the first form) |
| **Euler** | $a^{\varphi(m)}\equiv1\pmod m$ | $\gcd(a,m)=1$ |
| **Wilson** | $(p-1)!\equiv-1\pmod p$ | $p$ prime. **Converse true**: for $n\gt 1$, $(n-1)!\equiv-1\ (n)\iff n$ prime |
| Corollary | $(p-2)!\equiv1$; $\left(\left(\frac{p-1}2\right)!\right)^2\equiv(-1)^{(p+1)/2}\pmod p$ | $p$ odd prime |
| **Lagrange** | A polynomial of degree $n$ has at most $n$ roots mod $p$ | $p$ prime and leading coefficient $\not\equiv0$. Fails for composite moduli: $x^2-1$ has 4 roots mod 8 |
| **Carmichael function** | $a^{\lambda(m)}\equiv1$ with $\lambda(m)$ the exponent of $U(\mathbb Z_m)$ | $\gcd(a,m)=1$ |

- **Composite $n$:** $(n-1)!\equiv0\pmod n$ for every composite $n\ne4$ ($3!\equiv2\pmod 4$).
- **Power sums:** $`\sum_{k=1}^{p-1}k^m\equiv\begin{cases}-1 & (p-1)\mid m\cr  0&\text{otherwise}\end{cases}\pmod p`$.
- **Freshman's dream:** $(a+b)^p\equiv a^p+b^p\pmod p$.

**Pseudoprimes and Carmichael numbers**
- **Fermat pseudoprime to base $a$:** a composite $n$ with $a^{n-1}\equiv1\pmod n$. The smallest for base 2 is $341=11\cdot31$.
- **Carmichael number:** a composite $n$ that is a pseudoprime to every coprime base. The smallest is $561=3\cdot11\cdot17$; the next are $1105$ and $1729$.
- **Korselt's criterion:** $n$ is a Carmichael number iff $n$ is square-free and $p-1\mid n-1$ for every $p\mid n$. Every Carmichael number has at least 3 prime factors. There are infinitely many (Alford–Granville–Pomerance, 1994).

## 5. Order and primitive roots
- $\operatorname{ord}_m a$ is the least $k\ge1$ with $a^k\equiv1$.
- $a^n\equiv1\iff\operatorname{ord}_m a\mid n$. In particular $\operatorname{ord}_m a\mid\varphi(m)$.
- $\operatorname{ord}(a^k)=\dfrac{\operatorname{ord}a}{\gcd(k,\operatorname{ord}a)}$.
- A **primitive root** mod $m$ is an element $g$ with $\operatorname{ord}_m g=\varphi(m)$.
- **Primitive roots exist iff $m=1,2,4,p^k,2p^k$** ($p$ an odd prime). Then $U(\mathbb Z_m)$ is cyclic and there are **$\varphi(\varphi(m))$** primitive roots.
- No primitive root exists mod 8, 12, 15, 16, 20, 21, 24, …
- **Test:** $g$ is a primitive root mod $p$ iff $g^{(p-1)/q}\not\equiv1$ for every prime $q\mid p-1$.
- Least primitive roots: 2 for $p=3,5,11,13,19,29$; 3 for $p=7,17,31$; 5 for $p=23$. (2 is **not** a primitive root mod 7 or 17.)
- If $g$ is a primitive root mod $p$ and $g^{p-1}\not\equiv1\pmod{p^2}$, then $g$ is a primitive root mod $p^k$ for all $k$.
- $U(\mathbb Z_{2^k})\cong\mathbb Z_2\times\mathbb Z_{2^{k-2}}$ for $k\ge3$, and $x^2\equiv1\pmod{2^k}$ has 4 solutions.
- **Decimal periods:** the period of $1/p$ is $\operatorname{ord}_p10$. Examples: $1/7$ has period 6, $1/13$ period 6, $1/17$ period 16, $1/19$ period 18.

## 6. Counting solutions of $x^2\equiv1\pmod n$
For $n=2^e p_1^{a_1}\cdots p_r^{a_r}$, the number of solutions is $2^r\cdot c(e)$, where
$$c(e)=1\ (e\le1),\quad 2\ (e=2),\quad 4\ (e\ge3).$$
Examples: mod 120 there are $4\cdot2\cdot2=16$; mod 15 there are 4; mod 8 there are 4.

## 7. Last digits and remainders
- Reduce the exponent modulo the order, or modulo $\varphi(m)$ or $\lambda(m)$.
- $3^{100}\equiv4\pmod7$.
- $7^{2026}\equiv49\pmod{100}$ (since $7^4\equiv1$).
- $2^{100}\equiv3\pmod{13}$.
- $\lambda(100)=20$, so $a^{20}\equiv1\pmod{100}$ for $\gcd(a,10)=1$.
- The last digit of $17^{17}$ is 7. The last digit of $3^{2026}$ is 9.
- $2^{1000}\equiv376\pmod{1000}$.
- For a tower $a^{b^c}\bmod m$, reduce $b^c$ modulo $\varphi(m)$ (when $\gcd(a,m)=1$).

## 8. Exam traps
- A linear congruence with $d\mid b$ has **$d$ solutions mod $m$**, not one.
- The CRT needs **pairwise coprime** moduli for existence for every choice of the $a_i$.
- The **converse of Fermat** is false (pseudoprimes, Carmichael numbers). The **converse of Wilson** is true.
- Lagrange's root bound holds only for a **prime** modulus.
- There is **no primitive root mod 8** (or mod $2^k$ for $k\ge3$), even though $8$ is a prime power. Primitive roots do exist mod $2p^k$.
- $99!\bmod101=1$, while $100!\bmod101=100$.
- Fermat needs $p\nmid a$. Euler needs $\gcd(a,m)=1$.
