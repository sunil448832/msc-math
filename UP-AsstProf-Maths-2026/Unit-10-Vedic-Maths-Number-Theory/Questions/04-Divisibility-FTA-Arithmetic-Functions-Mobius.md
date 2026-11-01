# Unit 10 · Topic 04 — Divisibility, Fundamental Theorem of Arithmetic, Arithmetical Functions, Möbius Inversion
> Syllabus coverage: Fundamental theorem of arithmetic, arithmetical functions, Mobius inversion
> Cheatsheet: [../Cheatsheets/04-Divisibility-FTA-Arithmetic-Functions-Mobius.md](../Cheatsheets/04-Divisibility-FTA-Arithmetic-Functions-Mobius.md)

**Q1.** `[Numerical]` ★ For $n = 360$, the values of $\big(d(n),\ \sigma(n),\ \varphi(n)\big)$ are

(A) $(24,\ 1170,\ 96)$

(B) $(24,\ 1170,\ 144)$

(C) $(18,\ 1170,\ 96)$

(D) $(24,\ 1092,\ 96)$

**Q2.** `[Concept]` ★ For every integer $n\gt 1$, $\displaystyle\sum_{d\mid n}\mu(d)$ equals

(A) $1$

(B) $\mu(n)$

(C) $-1$

(D) $0$

**Q3.** `[Numerical]` ★ The number of trailing zeros in $1000!$ is

(A) 200

(B) 248

(C) 249

(D) 250

**Q4.** `[Numerical]` ★★ The number of positive integers $n$ with $\varphi(n) = 12$ is

(A) 4

(B) 5

(C) 6

(D) 8

**Q5.** `[Match]` ★★ Here $\mathbf 1(n)=1$, $\mathrm{Id}(n)=n$, $\varepsilon(n)=[n=1]$, and $\ast$ is Dirichlet convolution. Match List-I with List-II.

| List-I | List-II |
|---|---|
| (a) $\mu \ast  \mathbf 1$ | 1. $\varphi$ |
| (b) $\mathbf 1 \ast  \mathbf 1$ | 2. $\sigma$ |
| (c) $\mathrm{Id} \ast  \mathbf 1$ | 3. $\varepsilon$ |
| (d) $\mu \ast  \mathrm{Id}$ | 4. $d$ |

(A) a-3, b-4, c-2, d-1

(B) a-3, b-2, c-4, d-1

(C) a-1, b-4, c-2, d-3

(D) a-3, b-4, c-1, d-2

**Q6.** `[Multi-Statement]` ★★ Consider the following statements.

I. $\varphi(n)$ is even for every $n \ge 3$.

II. $\varphi$ is completely multiplicative.

III. $\sum_{d\mid n}\varphi(d) = n$ for every $n\ge1$.

Which of the above is/are correct?

(A) I only

(B) I and III only

(C) II and III only

(D) I, II and III

**Q7.** `[Assertion-Reason]` ★★
**Assertion (A):** $d(n)$ is odd if and only if $n$ is a perfect square.
**Reason (R):** The divisors of $n$ pair off as $d \leftrightarrow n/d$, and a divisor is paired with itself only when $d = \sqrt n$.

(A) Both A and R are true and R is the correct explanation of A

(B) Both A and R are true but R is NOT the correct explanation of A

(C) A is true but R is false

(D) A is false but R is true

**Q8.** `[Application]` ★★ Let $f$ be an arithmetical function with $\sum_{d\mid n} f(d) = n^2$ for all $n\ge 1$. Then $f(12)$ equals

(A) 72

(B) 96

(C) 120

(D) 144

**Q9.** `[NOT-true / Counterexample]` ★★ Which of the following statements is NOT true?

(A) Every even perfect number has the form $2^{p-1}(2^p - 1)$ with $2^p - 1$ prime.

(B) If $n$ is perfect, then $\sum_{d\mid n} \frac1d = 2$.

(C) $2^p - 1$ is prime whenever $p$ is prime.

(D) $8128$ is a perfect number.

**Q10.** `[Numerical]` ★★★ The number of ordered pairs $(a, b)$ of positive integers with $\mathop{\mathrm{lcm}}\nolimits(a, b) = 36$ is

(A) 9

(B) 18

(C) 81

(D) 25

**Q11.** `[Numerical]` ★ The number of positive divisors of $10!$ is

(A) 240

(B) 270

(C) 256

(D) 320

**Q12.** `[Application]` ★★★ Using $\sum_{d^2\mid n}\mu(d) = \mu^2(n)$, the number of square-free integers in $\lbrace 1, 2, \dots, 100\rbrace$ is

(A) 60

(B) 61

(C) 62

(D) 64

**Q13.** `[Concept]` ★★ In which of the following rings does unique factorisation into irreducibles fail?

(A) $\mathbb Z[i]$

(B) $\mathbb Z[x]$

(C) $\mathbb Z[\omega]$, where $\omega = e^{2\pi i/3}$

(D) $\mathbb Z[\sqrt{-5}]$

---
## Answer Key
| Q | Ans | Type |
|---|---|---|
| 1 | A | Numerical |
| 2 | D | Concept |
| 3 | C | Numerical |
| 4 | C | Numerical |
| 5 | A | Match |
| 6 | B | Multi-Statement |
| 7 | A | Assertion-Reason |
| 8 | B | Application |
| 9 | C | NOT-true |
| 10 | D | Numerical |
| 11 | B | Numerical |
| 12 | B | Application |
| 13 | D | Concept |

## Solutions
**Q1 — (A).** $360 = 2^3\cdot3^2\cdot5$.
- $d = 4\cdot3\cdot2 = 24$.
- $\sigma = 15\cdot13\cdot6 = 1170$.
- $\varphi = 360\cdot\frac12\cdot\frac23\cdot\frac45 = 96$.
- (B) has the wrong $\varphi$ ($144 = 360\cdot\frac25$ is not $`\varphi(360)`$). (C) gets $d$ by multiplying the exponents plus one wrongly ($3\cdot3\cdot2$ instead of $4\cdot3\cdot2$). (D) has the wrong $\sigma$.

**Q2 — (D).** $\sum_{d\mid n}\mu(d) = \prod_{p\mid n}(1-1) = 0$ for $n\gt 1$. It equals 1 only when $n=1$.

**Q3 — (C).** $\lfloor1000/5\rfloor+\lfloor1000/25\rfloor+\lfloor1000/125\rfloor+\lfloor1000/625\rfloor = 200+40+8+1=249$. The factor 5 is the limiting one because there are more 2s than 5s.

**Q4 — (C).** $\varphi(n)=12$ for $n = 13, 21, 26, 28, 36, 42$. (14, for comparison, is a non-totient: no $n$ has $\varphi(n)=14$.)

**Q5 — (A).**
- $\mu\ast \mathbf1=\varepsilon$ (this is Q2).
- $\mathbf1\ast \mathbf1 = d$.
- $\mathrm{Id}\ast \mathbf1=\sigma$.
- $\mu\ast \mathrm{Id}=\varphi$, because $\varphi\ast \mathbf 1 = \mathrm{Id}$, followed by Möbius inversion.

**Q6 — (B).**
- I is true: $n\ge3$ has an odd prime factor $p$, which contributes the even factor $p-1$, or $4\mid n$, which contributes $2^{k-1}$ with $k\ge2$.
- II is false: $\varphi(4)=2\ne\varphi(2)^2=1$. $\varphi$ is only multiplicative.
- III is Gauss's identity.

**Q7 — (A).** If $d\ne n/d$ for every $d$, the divisors come in pairs and $d(n)$ is even. A fixed point exists only when $n=d^2$. So R proves A.

**Q8 — (B).** By Möbius inversion, $f(n)=\sum_{d\mid n}\mu(d)(n/d)^2 = n^2\prod_{p\mid n}(1-p^{-2})$ (Jordan's totient $J_2$). So $f(12) = 144\cdot\frac34\cdot\frac89 = 96$.

**Q9 — (C).** $2^{11}-1 = 2047 = 23\cdot89$ is composite even though 11 is prime. The converse is the true statement: if $2^p-1$ is prime then $p$ is prime. (A) is Euclid–Euler. (B) holds because $\sigma(n)/n=2$. (D) is true: $8128 = 2^6(2^7-1)$.

**Q10 — (D).** Write $36=2^2 3^2$. For each prime $p^k\thinspace \Vert \thinspace n$, the pair of exponents $(\alpha,\beta)$ must satisfy $\max(\alpha,\beta) = k$, which gives $2k+1$ choices. So the count is $5\cdot5=25$, which equals $d(36^2)$. (A) counts divisors only.

**Q11 — (B).** $10! = 2^8\thinspace 3^4\thinspace 5^2\thinspace 7$ (Legendre's formula: $5+2+1=8$, $3+1=4$, $2$, $1$). So $d = 9\cdot5\cdot3\cdot2 = 270$.

**Q12 — (B).** The count is $\sum_{d\le10}\mu(d)\lfloor100/d^2\rfloor$:
$$100-25-11-4-2+2+1 = 61,$$
from $d=1,2,3,5,7,6,10$ respectively ($\mu(4)=\mu(8)=\mu(9)=0$). Forgetting the $+$ terms for $d=6,10$ gives 58, and stopping after $d=5$ gives 60.

**Q13 — (D).** $6=2\cdot3=(1+\sqrt{-5})(1-\sqrt{-5})$, and these are non-associate irreducibles. $\mathbb Z[i]$ and $\mathbb Z[\omega]$ are Euclidean domains, and $\mathbb Z[x]$ is a UFD (by Gauss's lemma) although it is not a PID.
