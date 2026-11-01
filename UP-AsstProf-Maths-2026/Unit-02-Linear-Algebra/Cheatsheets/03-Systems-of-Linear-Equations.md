# Cheatsheet · Unit 2 · Topic 03 — Systems of Linear Equations

## 1. Setting
$AX=B$, where $A$ is $m\times n$ ($m$ equations, $n$ unknowns) and $[A\,|\,B]$ is the augmented matrix.

## 2. Rouché–Capelli (consistency)
| Condition | Conclusion |
|---|---|
| $\operatorname{rank}A\ne\operatorname{rank}[A\,|\,B]$ | inconsistent (no solution) |
| $\operatorname{rank}A=\operatorname{rank}[A\,|\,B]=n$ | unique solution |
| $\operatorname{rank}A=\operatorname{rank}[A\,|\,B]=r<n$ | infinitely many solutions over an infinite field, with $n-r$ free parameters |

- **Homogeneous** $AX=0$ is always consistent. The solution space $N(A)$ has $\dim=n-\operatorname{rank}A$.
- $m<n$ (more unknowns than equations) $\Rightarrow$ a non-trivial solution exists.
- For square $A$: $AX=0$ has a non-trivial solution $\iff\det A=0$.
- **Structure:** if $AX=B$ is consistent, its solutions are $X_0+N(A)$, a coset or affine subspace.
  - The difference of two solutions solves $AX=0$.
  - $\sum c_iX_i$ is a solution iff $\sum c_i=1$.
- Over a finite field $\mathbb F_q$, a consistent system has exactly $q^{\,n-r}$ solutions.

## 3. Standard parametric systems
| System | det | Outcome |
|---|---|---|
| $kx+y+z=1$ (cyclic) | $(k-1)^2(k+2)$ | $k=1$: infinitely many; $k=-2$: none; otherwise unique |
| $x+y+z=6,\ x+2y+3z=10,\ x+2y+\lambda z=\mu$ | $\lambda-3$ | $\lambda\ne3$: unique; $\lambda=3,\mu=10$: infinitely many; $\lambda=3,\mu\ne10$: none |

## 4. Rank facts
- Row rank $=$ column rank $=$ size of the largest non-zero minor $=$ number of non-zero rows in echelon form.
- $\operatorname{rank}A\le\min(m,n)$, $\operatorname{rank}A=\operatorname{rank}A^T$, and $\operatorname{rank}A=\operatorname{rank}(PAQ)$ for invertible $P,Q$.
- $\operatorname{rank}(A^TA)=\operatorname{rank}(AA^T)=\operatorname{rank}A$ over $\mathbb R$, and $\operatorname{rank}(A^*A)=\operatorname{rank}A$ over $\mathbb C$.
- $\operatorname{rank}(A+B)\le\operatorname{rank}A+\operatorname{rank}B$ and $|\operatorname{rank}A-\operatorname{rank}B|\le\operatorname{rank}(A-B)$.
- **Sylvester's inequality** (for $A$ of size $m\times n$ and $B$ of size $n\times p$):
$$\operatorname{rank}A+\operatorname{rank}B-n\le\operatorname{rank}(AB)\le\min(\operatorname{rank}A,\operatorname{rank}B).$$
- **Frobenius:** $\operatorname{rank}(AB)+\operatorname{rank}(BC)\le\operatorname{rank}B+\operatorname{rank}(ABC)$.
- $AB=0$ (with $A$ of size $m\times n$) $\Rightarrow\operatorname{rank}A+\operatorname{rank}B\le n$.
- Rank 1 $\iff A=uv^T$ with $u,v\ne0$. Then $A^2=(v^Tu)A$ and $\operatorname{tr}A=v^Tu$.
- **Adjugate:** $\operatorname{rank}(\operatorname{adj}A)=n$ if $\operatorname{rank}A=n$; $1$ if $\operatorname{rank}A=n-1$; $0$ if $\operatorname{rank}A\le n-2$. Also $\det(\operatorname{adj}A)=(\det A)^{n-1}$.
- $a_{ij}=i+j$ gives rank 2; $a_{ij}=ij$ gives rank 1; $J_n$ (all ones) has rank 1.

## 5. Methods
- **Gaussian elimination:** row-reduce $[A|B]$. A row $(0\ \dots\ 0\,|\,c)$ with $c\ne0$ means the system is inconsistent.
- Elementary row operations preserve the row space and the null space, but **not** the column space (only its dimension).
- **Cramer's rule** (for $\det A\ne0$): $x_i=\det A_i/\det A$.

## Exam traps
- The dimension of the solution space is $n-r$, where $n$ is the number of **unknowns**, not the number of equations.
- $\det A=0$ alone does not decide between "none" and "infinitely many". Compare the ranks of $A$ and $[A|B]$.
- $\operatorname{rank}(AB)$ is not always $\min(\cdot,\cdot)$, and $\operatorname{rank}A^2$ can be smaller than $\operatorname{rank}A$ (nilpotents).
- The sum of two solutions of a non-homogeneous system is **not** a solution.
