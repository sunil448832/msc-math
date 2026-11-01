# Cheatsheet · Unit 2 · Topic 03 — Systems of Linear Equations

## 1. Setting
$AX=B$, where $A$ is $m\times n$ ($m$ equations, $n$ unknowns) and $[A\thinspace |\thinspace B]$ is the augmented matrix.

## 2. Rouché–Capelli (consistency)
| Condition | Conclusion |
|---|---|
| $\mathop{\mathrm{rank}}\nolimits A\ne\mathop{\mathrm{rank}}\nolimits[A\thinspace \vert \thinspace B]$ | inconsistent (no solution) |
| $\mathop{\mathrm{rank}}\nolimits A=\mathop{\mathrm{rank}}\nolimits[A\thinspace \vert \thinspace B]=n$ | unique solution |
| $\mathop{\mathrm{rank}}\nolimits A=\mathop{\mathrm{rank}}\nolimits[A\thinspace \vert \thinspace B]=r\lt n$ | infinitely many solutions over an infinite field, with $n-r$ free parameters |

- **Homogeneous** $AX=0$ is always consistent. The solution space $N(A)$ has $\dim=n-\mathop{\mathrm{rank}}\nolimits A$.
- $m\lt n$ (more unknowns than equations) $\Rightarrow$ a non-trivial solution exists.
- For square $A$: $AX=0$ has a non-trivial solution $\iff\det A=0$.
- **Structure:** if $AX=B$ is consistent, its solutions are $X_0+N(A)$, a coset or affine subspace.
  - The difference of two solutions solves $AX=0$.
  - $\sum c_iX_i$ is a solution iff $\sum c_i=1$.
- Over a finite field $\mathbb F_q$, a consistent system has exactly $q^{\thinspace n-r}$ solutions.

## 3. Standard parametric systems
| System | det | Outcome |
|---|---|---|
| $kx+y+z=1$ (cyclic) | $(k-1)^2(k+2)$ | $k=1$: infinitely many; $k=-2$: none; otherwise unique |
| $x+y+z=6,\ x+2y+3z=10,\ x+2y+\lambda z=\mu$ | $\lambda-3$ | $\lambda\ne3$: unique; $\lambda=3,\mu=10$: infinitely many; $\lambda=3,\mu\ne10$: none |

## 4. Rank facts
- Row rank $=$ column rank $=$ size of the largest non-zero minor $=$ number of non-zero rows in echelon form.
- $\mathop{\mathrm{rank}}\nolimits A\le\min(m,n)$, $\mathop{\mathrm{rank}}\nolimits A=\mathop{\mathrm{rank}}\nolimits A^T$, and $\mathop{\mathrm{rank}}\nolimits A=\mathop{\mathrm{rank}}\nolimits(PAQ)$ for invertible $P,Q$.
- $\mathop{\mathrm{rank}}\nolimits(A^TA)=\mathop{\mathrm{rank}}\nolimits(AA^T)=\mathop{\mathrm{rank}}\nolimits A$ over $\mathbb R$, and $\mathop{\mathrm{rank}}\nolimits(A^\ast A)=\mathop{\mathrm{rank}}\nolimits A$ over $\mathbb C$.
- $\mathop{\mathrm{rank}}\nolimits(A+B)\le\mathop{\mathrm{rank}}\nolimits A+\mathop{\mathrm{rank}}\nolimits B$ and $|\mathop{\mathrm{rank}}\nolimits A-\mathop{\mathrm{rank}}\nolimits B|\le\mathop{\mathrm{rank}}\nolimits(A-B)$.
- **Sylvester's inequality** (for $A$ of size $m\times n$ and $B$ of size $n\times p$):
$$\mathop{\mathrm{rank}}\nolimits A+\mathop{\mathrm{rank}}\nolimits B-n\le\mathop{\mathrm{rank}}\nolimits(AB)\le\min(\mathop{\mathrm{rank}}\nolimits A,\mathop{\mathrm{rank}}\nolimits B).$$
- **Frobenius:** $\mathop{\mathrm{rank}}\nolimits(AB)+\mathop{\mathrm{rank}}\nolimits(BC)\le\mathop{\mathrm{rank}}\nolimits B+\mathop{\mathrm{rank}}\nolimits(ABC)$.
- $AB=0$ (with $A$ of size $m\times n$) $\Rightarrow\mathop{\mathrm{rank}}\nolimits A+\mathop{\mathrm{rank}}\nolimits B\le n$.
- Rank 1 $\iff A=uv^T$ with $u,v\ne0$. Then $A^2=(v^Tu)A$ and $\mathop{\mathrm{tr}}\nolimits A=v^Tu$.
- **Adjugate:** $\mathop{\mathrm{rank}}\nolimits(\mathop{\mathrm{adj}}\nolimits A)=n$ if $\mathop{\mathrm{rank}}\nolimits A=n$; $1$ if $\mathop{\mathrm{rank}}\nolimits A=n-1$; $0$ if $\mathop{\mathrm{rank}}\nolimits A\le n-2$. Also $\det(\mathop{\mathrm{adj}}\nolimits A)=(\det A)^{n-1}$.
- $a_{ij}=i+j$ gives rank 2; $a_{ij}=ij$ gives rank 1; $J_n$ (all ones) has rank 1.

## 5. Methods
- **Gaussian elimination:** row-reduce $[A|B]$. A row $(0\ \dots\ 0\thinspace |\thinspace c)$ with $c\ne0$ means the system is inconsistent.
- Elementary row operations preserve the row space and the null space, but **not** the column space (only its dimension).
- **Cramer's rule** (for $\det A\ne0$): $x_i=\det A_i/\det A$.

## Exam traps
- The dimension of the solution space is $n-r$, where $n$ is the number of **unknowns**, not the number of equations.
- $\det A=0$ alone does not decide between "none" and "infinitely many". Compare the ranks of $A$ and $[A|B]$.
- $\mathop{\mathrm{rank}}\nolimits(AB)$ is not always $\min(\cdot,\cdot)$, and $\mathop{\mathrm{rank}}\nolimits A^2$ can be smaller than $\mathop{\mathrm{rank}}\nolimits A$ (nilpotents).
- The sum of two solutions of a non-homogeneous system is **not** a solution.
