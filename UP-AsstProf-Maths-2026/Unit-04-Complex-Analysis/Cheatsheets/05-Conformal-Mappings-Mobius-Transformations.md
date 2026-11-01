# Cheatsheet · Unit 4 · Topic 05 — Conformal Mappings and Möbius Transformations

## 1. Conformal maps
- $f$ is **conformal at $z_0$** if it preserves both the **size and the sense** of angles between curves through $z_0$.
- **Theorem:** if $f$ is analytic and $f'(z_0) \ne 0$, then $f$ is conformal at $z_0$.
  - Locally it rotates by $\arg f'(z_0)$ and scales lengths by $|f'(z_0)|$.
  - Areas scale by $|f'(z_0)|^2$, which is the Jacobian.
- **Critical points** ($f'(z_0) = 0$): if $f - f(z_0)$ has a zero of order $m$ there, angles are **multiplied by $m$**. For example, $z^2$ doubles angles at $0$.
- **Isogonal** maps preserve the size of angles but reverse their sense, e.g. $\bar z$.
- Conformality is **local**: $e^z$ is conformal everywhere but not injective.
- An injective analytic map has $f' \ne 0$ everywhere, so it is conformal onto its image.
- **Riemann mapping theorem:** every simply connected domain $D \subsetneq \mathbb{C}$ is conformally equivalent to the unit disc. $\mathbb{C}$ itself is not, by Liouville.

## 2. Möbius (bilinear, linear fractional) transformations
$$T(z) = \frac{az+b}{cz+d},\qquad ad - bc \ne 0.$$
- $T$ is a bijection of $\hat{\mathbb{C}}$, with $T(-d/c) = \infty$ and $T(\infty) = a/c$. Its inverse is $\frac{dz-b}{-cz+a}$.
- $T'(z) = \frac{ad-bc}{(cz+d)^2} \ne 0$, so $T$ is conformal on $\hat{\mathbb{C}}$.
- The Möbius maps form a group, isomorphic to $PSL(2,\mathbb{C}) = SL(2,\mathbb{C})/\lbrace \pm I\rbrace$. Composition corresponds to matrix multiplication.
- Every $T$ is a composition of a translation, a rotation and dilation, and an inversion $1/z$.
- $T$ maps generalised circles (circles and lines) to generalised circles. A circle through the pole $-d/c$ goes to a **line**.
- $T$ preserves **symmetric points** (inverse points) with respect to circles.
- $T$ is determined by the images of 3 distinct points.

## 3. Fixed points
- The fixed points solve $cz^2 + (d-a)z - b = 0$. A non-identity $T$ has **1 or 2** fixed points in $\hat{\mathbb{C}}$.
- $\infty$ is fixed $\iff c = 0$. If moreover $a = d$, then $T$ is a translation, with the single fixed point $\infty$.
- **Normal forms:**
  - Two fixed points $p$ and $q$: $\frac{w-p}{w-q} = k\frac{z-p}{z-q}$, where $k$ is the multiplier.
  - One fixed point $p$: $\frac{1}{w-p} = \frac{1}{z-p} + h$.

## 4. Classification
Normalise to $ad - bc = 1$ and let $\tau = a + d$.
| Type | Condition | Multiplier $k$ | Model |
|---|---|---|---|
| Parabolic | $\tau^2 = 4$, $T \ne I$ | (1 fixed point) | $z + 1$ |
| Elliptic | $\tau^2 \in [0,4)$ | $\lvert k\rvert = 1$, $k \ne 1$ | $e^{i\theta}z$ |
| Hyperbolic | $\tau^2 \in (4,\infty)$ | $k \gt  0$ real, $k \ne 1$ | $kz$ |
| Loxodromic (strict) | $\tau^2 \notin [0,\infty)$ | otherwise | $\lambda z$, $\lambda \notin \mathbb{R}\cup S^1$ |

Example: $\frac{3z-4}{z-1}$ has $\tau = 2$, so it is parabolic with fixed point $2$.

## 5. Cross ratio
Convention: $(z_1,z_2,z_3,z_4) = \dfrac{(z_1-z_3)(z_2-z_4)}{(z_1-z_4)(z_2-z_3)}$. **Always check which convention a question uses.**
- It is invariant under Möbius maps.
- $z_1, \dots, z_4$ lie on one circle or line $\iff$ the cross ratio is **real**.
- To find $T$ with $z_k \mapsto w_k$, solve $(w,w_1,w_2,w_3) = (z,z_1,z_2,z_3)$.
- Mapping $z_1, z_2, z_3 \mapsto 0, 1, \infty$: $T(z) = \frac{(z-z_1)(z_2-z_3)}{(z-z_3)(z_2-z_1)}$.

## 6. Disc and half-plane maps
| Map | Form |
|---|---|
| Automorphisms of $\mathbb{D}$ | $e^{i\theta}\dfrac{z-a}{1-\bar az}$, $\lvert a\rvert \lt  1$ |
| Automorphisms of the UHP | $\dfrac{az+b}{cz+d}$, $a,b,c,d \in \mathbb{R}$, $ad - bc \gt  0$ |
| UHP $\to \mathbb{D}$ | $e^{i\theta}\dfrac{z-a}{z-\bar a}$, $\mathop{\mathrm{Im}}\nolimits a \gt  0$ |
| Cayley map | $\dfrac{z-i}{z+i}$ |
| $\mathbb{D} \to$ right half-plane | $\dfrac{1+z}{1-z}$ |
| $\mathbb{D} \to$ UHP | $i\dfrac{1+z}{1-z}$, or $i\dfrac{1-z}{1+z}$ |

- For a disc automorphism $\varphi_a$ with $\varphi_a(a) = 0$: $|\varphi_a'(a)| = \frac{1}{1-|a|^2}$ and $|\varphi_a'(0)| = 1 - |a|^2$.
- For UHP $\to \mathbb{D}$ with $a \mapsto 0$: $|T'(a)| = \frac{1}{2\mathop{\mathrm{Im}}\nolimits a}$.
- **Schwarz–Pick:** an analytic $f:\mathbb{D}\to\mathbb{D}$ does not increase the hyperbolic distance, and $|f'(z)| \le \frac{1-|f(z)|^2}{1-|z|^2}$.

## 7. Standard elementary maps
| Map | Domain $\to$ image |
|---|---|
| $z^2$ | first quadrant $\to$ UHP; UHP $\to \mathbb{C}\setminus[0,\infty)$; hyperbolas $\leftrightarrow$ lines |
| $z^n$ | sector of angle $\pi/n$ $\to$ UHP; angles at $0$ multiplied by $n$ |
| $e^z$ | strip $0 \lt  \mathop{\mathrm{Im}}\nolimits z \lt  \pi$ $\to$ UHP; $0 \lt  \mathop{\mathrm{Im}}\nolimits z \lt  \pi/2$ $\to$ first quadrant; vertical lines $\to$ circles; horizontal lines $\to$ rays |
| $\mathop{\mathrm{Log}}\nolimits z$ | UHP $\to$ strip $0 \lt  \mathop{\mathrm{Im}}\nolimits w \lt  \pi$ |
| $\sin z$ | half-strip $-\frac\pi2 \lt  x \lt  \frac\pi2$, $y \gt  0$ $\to$ UHP |
| $\frac1z$ | circles through $0$ $\to$ lines; $\lvert z\rvert \lt  1 \to \lvert w\rvert \gt  1$ |
| $z + \frac1z$ (Joukowski) | $\lvert z\rvert = r \ne 1$ $\to$ ellipse; $\lvert z\rvert = 1$ $\to$ $[-2,2]$; exterior of $\mathbb{D}$ $\to$ $\mathbb{C}\setminus[-2,2]$ |

## Exam traps
1. The images of circles are circles **or lines**. Check whether the pole $-d/c$ lies on the circle.
2. Conformal does not mean injective ($e^z$). Isogonal does not mean conformal ($\bar z$).
3. A non-identity Möbius map has at most 2 fixed points. A map with 3 fixed points is the identity.
4. Classify with the **normalised** trace, i.e. $ad - bc = 1$. Otherwise use $\frac{(a+d)^2}{ad-bc}$.
5. Cross-ratio conventions differ between textbooks. Concyclicity ($\iff$ the cross ratio is real) holds in every convention.
6. Disc automorphisms have $|f'(a)| = \frac{1}{1-|a|^2}$, not $1 - |a|^2$.
7. At critical points angles are multiplied by the order. $z^2$ maps the quarter-plane to the half-plane.
8. $\mathbb{C}$ is not conformally equivalent to $\mathbb{D}$, so the Riemann mapping theorem needs $D \ne \mathbb{C}$.
