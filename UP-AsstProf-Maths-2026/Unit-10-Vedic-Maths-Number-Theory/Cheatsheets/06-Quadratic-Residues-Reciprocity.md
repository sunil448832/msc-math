# Cheatsheet · Unit 10 · Topic 06 — Quadratic Residues and Quadratic Reciprocity
> Questions: [../Questions/06-Quadratic-Residues-Reciprocity.md](../Questions/06-Quadratic-Residues-Reciprocity.md)

## 1. Quadratic residues
- Let $\gcd(a,m)=1$. Then $a$ is a **quadratic residue (QR)** mod $m$ if $x^2\equiv a\pmod m$ is solvable. Otherwise it is a **non-residue (QNR)**.
- For an odd prime $p$ there are exactly $\frac{p-1}2$ QRs and $\frac{p-1}2$ QNRs in $\lbrace 1,\dots,p-1\rbrace$. The QRs are $1^2,2^2,\dots,\left(\frac{p-1}2\right)^2$, all distinct mod $p$.
- QR·QR = QR, QR·QNR = QNR, and **QNR·QNR = QR** (mod $p$).
- If $g$ is a primitive root, the QRs are exactly the even powers of $g$. In particular, a primitive root is always a QNR.
- **Examples.**
  - mod 7: QRs $\lbrace 1,2,4\rbrace$.
  - mod 11: QRs $\lbrace 1,3,4,5,9\rbrace$, sum 22.
  - mod 13: QRs $\lbrace 1,3,4,9,10,12\rbrace$, sum 39.
- **Sum of QRs** in $[1,p-1]$ for $p\equiv1\pmod 4$ is $p(p-1)/4$ (the pairing $r\leftrightarrow p-r$).

## 2. Legendre symbol
$$\left(\frac ap\right)=\begin{cases}1 & a \text{ is a QR mod } p\cr  -1 & a\text{ is a QNR mod } p\cr  0 & p\mid a\end{cases}\qquad(p \text{ odd prime}).$$
- **Euler's criterion:** $\left(\frac ap\right)\equiv a^{(p-1)/2}\pmod p$.
- **Properties:**
  - completely multiplicative in $a$: $\left(\frac{ab}p\right)=\left(\frac ap\right)\left(\frac bp\right)$;
  - depends only on $a\bmod p$;
  - $\left(\frac{a^2}p\right)=1$ for $p\nmid a$.
- $\sum_{a=1}^{p-1}\left(\frac ap\right)=0$.

## 3. Gauss's lemma
Let $p\nmid a$. Let $n$ be the number of least positive residues of $a,2a,\dots,\frac{p-1}2a$ that are **greater than $p/2$**. Then
$$\left(\frac ap\right)=(-1)^n.$$
- **Example.** For $\left(\frac5{11}\right)$ the residues are $5,10,4,9,3$. Two of them ($10, 9$) exceed $5.5$, so the symbol is $+1$.
- **Eisenstein's form** (for odd $a$): $\left(\frac ap\right)=(-1)^{\sum_{k=1}^{(p-1)/2}\lfloor ka/p\rfloor}$. This is used in the lattice-point proof of reciprocity.

## 4. Supplementary laws and small cases
| Symbol | Formula | $=+1$ iff |
|---|---|---|
| $\left(\frac{-1}p\right)$ | $(-1)^{(p-1)/2}$ | $p\equiv1\pmod4$ |
| $\left(\frac{2}p\right)$ | $(-1)^{(p^2-1)/8}$ | $p\equiv\pm1\pmod8$ |
| $\left(\frac{-2}p\right)$ | product of the two rows above | $p\equiv1,3\pmod8$ |
| $\left(\frac{3}p\right)$ | from reciprocity | $p\equiv\pm1\pmod{12}$ |
| $\left(\frac{-3}p\right)$ | $=\left(\frac p3\right)$ | $p\equiv1\pmod3$ (equivalently $1 \pmod 6$) |
| $\left(\frac{5}p\right)$ | $=\left(\frac p5\right)$ | $p\equiv\pm1\pmod5$ |
| $\left(\frac{7}p\right)$ | from reciprocity | $p\equiv\pm1,\pm3,\pm9\pmod{28}$ |

## 5. Law of quadratic reciprocity (Gauss, 1796; "theorema aureum")
For **distinct odd primes** $p,q$:
$$\left(\frac pq\right)\left(\frac qp\right)=(-1)^{\frac{p-1}2\cdot\frac{q-1}2}.$$
- **Working rule:** $\left(\frac pq\right)=\left(\frac qp\right)$ unless $p\equiv q\equiv3\pmod 4$, in which case $\left(\frac pq\right)=-\left(\frac qp\right)$.
- Stated (without full proof) by Euler and Legendre. Gauss gave the first complete proof (*Disquisitiones Arithmeticae*, 1801) and eventually gave 8 proofs. Proofs use Gauss's lemma with lattice points (Eisenstein), Gauss sums, and other methods.

**Computing $\left(\frac ap\right)$**
1. Reduce $a$ mod $p$.
2. Factor $a$ and pull out $-1$, the powers of 2 and the square factors.
3. Flip each odd prime factor using reciprocity.
4. Repeat until the symbols are trivial.

Examples:
- $\left(\frac{219}{383}\right)=+1$.
- $\left(\frac{31}{103}\right)=-1$.
- $\left(\frac3{7}\right)=-1$.
- $\left(\frac7{19}\right)=+1$ but $\left(\frac{19}7\right)=-1$.

## 6. Jacobi symbol
For odd $n=p_1p_2\cdots p_k$ (primes, possibly repeated): $\left(\frac an\right)=\prod_i\left(\frac a{p_i}\right)$.
- The Jacobi symbol is multiplicative in **both** $a$ and $n$. It satisfies the same reciprocity and supplementary laws, for **odd positive coprime** $m,n$: $\left(\frac mn\right)\left(\frac nm\right)=(-1)^{\frac{m-1}2\frac{n-1}2}$. This lets you compute without factoring.
- $\left(\frac an\right)=-1$ implies that $a$ is a QNR mod $n$.
- $\left(\frac an\right)=+1$ does **not** imply that $a$ is a QR. Example: $\left(\frac2{15}\right)=1$, yet $x^2\equiv2\pmod{15}$ is unsolvable. Similarly $\left(\frac5{21}\right)=1$, but 5 is not a square mod 21.
- **Euler's criterion fails for Jacobi symbols.** This is the basis of the Solovay–Strassen primality test (Euler–Jacobi pseudoprimes).

## 7. Solvability of $x^2\equiv a\pmod n$
- **Prime $p$ odd, $p\nmid a$:** there are $1+\left(\frac ap\right)$ solutions (0 or 2).
- **$p^k$, $p$ odd, $p\nmid a$:** solvable iff $\left(\frac ap\right)=1$, and then there are exactly 2 solutions (Hensel lifting).
- **$2^k$, $a$ odd:**
  - $k=1$: always solvable, 1 solution.
  - $k=2$: solvable iff $a\equiv1\pmod 4$, 2 solutions.
  - $k\ge3$: solvable iff $a\equiv1\pmod 8$, 4 solutions.
- **General $n$:** factor $n$ and apply the CRT. The number of solutions is the product of the local counts.
  - Example: $x^2\equiv11\pmod{35}$ has $2\cdot2=4$ solutions.
  - Example: $x^2\equiv2\pmod{77}$ has none, since $\left(\frac2{11}\right)=-1$.
- **Quadratic $ax^2+bx+c\equiv0\pmod p$** ($p$ odd, $p\nmid a$): it reduces to $(2ax+b)^2\equiv b^2-4ac$. So it is solvable iff $\left(\frac{b^2-4ac}p\right)\ne-1$.
  - Example: $x^2+x+1\equiv0$ is solvable iff $p\equiv1\pmod3$ (for $p\gt 3$).
- **If $p\equiv3\pmod 4$** and $a$ is a QR, then $x\equiv\pm a^{(p+1)/4}$ are the solutions.

## 8. Applications
- **Fermat's two-squares theorem:** an odd prime $p$ is $x^2+y^2$ iff $p\equiv1\pmod4$. The key step is $\left(\frac{-1}p\right)=1$. More generally, $n$ is a sum of two squares iff every prime $\equiv3\pmod4$ appears to an even power.
- **Infinitely many primes $\equiv1\pmod4$:** any prime divisor $p$ of $(2\thinspace N!)^2+1$ satisfies $\left(\frac{-1}{p}\right)=1$.
- Similarly there are infinitely many primes $\equiv1\pmod 3$ (via $x^2+x+1$) and $\equiv\pm1\pmod 8$.
- **Prime divisors of Fermat numbers:** $p\mid F_n=2^{2^n}+1$ with $n\ge2$ implies $p\equiv1\pmod{2^{n+2}}$ (uses $\left(\frac2p\right)=1$).
- **Pépin's test:** $F_n$ ($n\ge1$) is prime iff $3^{(F_n-1)/2}\equiv-1\pmod{F_n}$.
- **Mersenne:** if $p\equiv3\pmod4$ and $q=2p+1$ is prime, then $q\mid 2^p-1$. Example: $23\mid2^{11}-1$.

## 9. Exam traps
- The count of QRs mod $p$ is $\frac{p-1}2$; **0 is not counted** as a QR.
- $\left(\frac2p\right)$ depends on $p$ **mod 8**. $\left(\frac{-1}p\right)$ depends on $p$ mod 4. $\left(\frac3p\right)$ depends on $p$ mod 12. $\left(\frac{-3}{p}\right)$ depends on $p$ mod 3.
- The sign flips **only when both primes are $\equiv3\pmod 4$**.
- A Jacobi symbol of $+1$ does **not** guarantee a solution.
- **Never flip a symbol with an even top entry.** Pull out the factors of 2 first and use $\left(\frac2p\right)$.
- Mod $2^k$ ($k\ge3$) there are **4** square roots of an odd QR, and an odd number must be $\equiv1\pmod 8$ to be a square.
- $\left(\frac ap\right)$ is defined only for **odd prime** $p$. The Jacobi symbol is defined only for **odd positive** $n$.
