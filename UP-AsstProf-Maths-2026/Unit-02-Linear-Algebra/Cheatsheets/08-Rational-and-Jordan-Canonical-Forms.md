# Cheatsheet · Unit 2 · Topic 08 — Rational and Jordan Canonical Forms

## 1. Jordan canonical form (JCF)
- **Jordan block:** $J_k(\lambda)=\lambda I_k+N_k$, where $N_k$ has 1's on the superdiagonal.
  - Its characteristic polynomial and minimal polynomial are both $(x-\lambda)^k$.
  - $\mathop{\mathrm{rank}}\nolimits(J_k(\lambda)-\lambda I)^j=\max(k-j,0)$.
  - Its eigenspace is 1-dimensional.
- **Theorem:** if $\chi_A$ splits over $F$ (always the case over $\mathbb C$), then $A$ is similar to $\bigoplus J_{k_i}(\lambda_i)$. This form is unique up to the order of the blocks.
- Two complex matrices are similar $\iff$ they have the same JCF.

| Quantity | What it tells you about the blocks for $\lambda$ |
|---|---|
| Algebraic multiplicity | sum of the sizes of the blocks |
| Geometric multiplicity $=n-\mathop{\mathrm{rank}}\nolimits(A-\lambda I)$ | **number** of blocks |
| Multiplicity in $m_A$ | size of the **largest** block |
| $\mathop{\mathrm{rank}}\nolimits(A-\lambda I)^{k-1}-\mathop{\mathrm{rank}}\nolimits(A-\lambda I)^{k}$ | number of blocks of size $\ge k$ |
| $r_{k-1}-2r_k+r_{k+1}$ (with $r_j=\mathop{\mathrm{rank}}\nolimits(A-\lambda I)^j$) | number of blocks of size exactly $k$ |

- $A$ is diagonalizable $\iff$ every block is $1\times1$ $\iff$ $m_A$ has distinct roots.

## 2. Counting similarity classes
- $n\times n$ nilpotent matrices: $p(n)$ classes, the number of partitions of $n$.

  | $n$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
  |---|---|---|---|---|---|---|---|
  | $p(n)$ | 1 | 2 | 3 | 5 | 7 | 11 | 15 |

- Given $\chi_A=\prod(x-\lambda_i)^{a_i}$: there are $\prod p(a_i)$ possible JCFs.
- Given both $\chi_A$ and $m_A=\prod(x-\lambda_i)^{b_i}$: the count is $\prod\sharp \lbrace \text{partitions of }a_i\text{ with largest part }b_i\rbrace$.
- Matrices with $A^k=I$ (or with any $m_A$ having distinct roots) are diagonalizable. The classes are multisets of eigenvalues: choosing $n$ eigenvalues from $k$ roots gives $\binom{n+k-1}{n}$ classes.
- $A^2=0$ in $M_n$: blocks of size $\le2$, giving $\lfloor n/2\rfloor+1$ classes.
- **Characteristic and minimal polynomials determine the JCF iff $n\le3$.** The standard 4×4 counterexample is $J_2(0)\oplus J_2(0)$ versus $J_2(0)\oplus J_1(0)\oplus J_1(0)$.
- For $n\le6$, the triple ($\chi_A$, $m_A$, geometric multiplicities) determines the JCF. At $n=7$ the partitions $3{+}3{+}1$ and $3{+}2{+}2$ of a nilpotent share all three.

## 3. Rational canonical form (RCF), valid over any field
- **Companion matrix** of $f=x^n+a_{n-1}x^{n-1}+\dots+a_0$:
```math
C(f)=\begin{pmatrix}0&0&\cdots&-a_0\cr 1&0&\cdots&-a_1\cr &\ddots&&\vdots\cr 0&\cdots&1&-a_{n-1}\end{pmatrix}
```
  Its characteristic and minimal polynomials both equal $f$. It is cyclic (non-derogatory) and has one Jordan block per eigenvalue.
- **Invariant factors:** $d_1\mid d_2\mid\cdots\mid d_k$, with $d_k=m_A$ and $\prod d_i=\chi_A$. The RCF is $C(d_1)\oplus\dots\oplus C(d_k)$, and it is unique.
- **Elementary divisors:** the prime-power factors of the $d_i$, which correspond to the Jordan blocks over $\mathbb C$.
- **From elementary divisors to invariant factors:** $d_k$ is the product of the highest power of each prime, $d_{k-1}$ the product of the next highest, and so on.
  - Example: $(x-1),(x-1)^2,(x-2)$ gives $d_2=(x-1)^2(x-2)$ and $d_1=x-1$.
- **Smith normal form** of $xI-A$ over $F[x]$ is $\mathop{\mathrm{diag}}\nolimits(1,\dots,1,d_1,\dots,d_k)$, and $d_i$ is a ratio of determinantal divisors.
- $A$ is similar to $B$ over $F$ $\iff$ they have the same invariant factors. Similarity over an extension field $K\supseteq F$ implies similarity over $F$.
- $m_A=\chi_A$ $\iff$ there is only one invariant factor $\iff A\sim C(\chi_A)$ $\iff$ $A$ is cyclic $\iff$ every eigenvalue has GM $=1$.

## 4. Useful consequences
- $A\sim A^T$ always.
- $J_k(\lambda)^m$ for $\lambda\neq0$ is similar to $J_k(\lambda^m)$, a single block.
- For a nilpotent $N$ of order $n$, $N^{n}=0$. If $N^{n-1}\ne0$, then $N\sim J_n(0)$.
- $\dim\lbrace X: AX=XA\rbrace \ge n$, with equality iff $A$ is cyclic.
- Real matrices: the real JCF uses $2\times2$ blocks $`\begin{pmatrix}a&-b\cr b&a\end{pmatrix}`$ for the eigenvalues $a\pm ib$.

## Exam traps
- **Number** of blocks = GM, and the **largest** block = exponent in $m_A$. Don't swap them.
- In counting problems, multiply the counts over different eigenvalues; do not add them.
- Same $\chi_A$ and $m_A$ does **not** imply similarity once $n\ge4$.
- Invariant factors must divide one another. Elementary divisors are the prime powers; don't confuse the two lists.
- A companion matrix with a repeated root is **not** diagonalizable.
