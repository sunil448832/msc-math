# Cheatsheet · Unit 8 · Topic 06 — Fluid Dynamics: Euler's Equation, Two-dimensional Flows, Motion of a Sphere
> Questions: [../Questions/06-Fluid-Dynamics-Euler-Equation-2D-Flows-Sphere.md](../Questions/06-Fluid-Dynamics-Euler-Equation-2D-Flows-Sphere.md)

## 1. Euler's equation (perfect = inviscid fluid)
$$\frac{D\vec q}{Dt} = \frac{\partial\vec q}{\partial t} + (\vec q\cdot\nabla)\vec q = \vec F - \frac1\rho\nabla p$$
- **Lamb form:** $\dfrac{\partial\vec q}{\partial t} - \vec q\times\vec\omega = -\nabla\left(\tfrac12q^2 + \Omega + P\right)$, where $\vec F = -\nabla\Omega$ and $P = \int dp/\rho$ (barotropic fluid).
- **Lagrangian form** (in Lagrangian variables): $\left(\ddot x - X\right)\dfrac{\partial x}{\partial a} + \ldots = -\dfrac1\rho\dfrac{\partial p}{\partial a}$.

## 2. Bernoulli's equation
| Hypotheses | Result |
|---|---|
| Steady, conservative force, barotropic | $\tfrac12q^2 + \Omega + \int dp/\rho = C$ **along each streamline** (and along vortex lines) |
| Steady **and** irrotational | the same $C$ **throughout** the fluid |
| Unsteady, irrotational ($\vec q = -\nabla\phi$) | $-\dfrac{\partial\phi}{\partial t} + \tfrac12q^2 + \Omega + \int dp/\rho = F(t)$ (pressure equation) |

- Incompressible fluid under gravity: $\dfrac p\rho + \tfrac12q^2 + gz = $ const.
- **Torricelli:** $v = \sqrt{2gh}$. Stagnation pressure $p_0 = p + \tfrac12\rho q^2$.

## 3. Circulation and vorticity theorems
- **Kelvin:** for an inviscid, barotropic fluid with conservative forces, $\dfrac{D\Gamma}{Dt} = 0$ for every closed material curve.
- **Lagrange:** under the same hypotheses, if the motion is irrotational at one instant it stays irrotational ("permanence of irrotational motion").
- **Helmholtz:** vortex lines move with the fluid and the strength of a vortex tube is constant.
- **Vorticity equation:** $\dfrac{D}{Dt}\left(\dfrac{\vec\omega}{\rho}\right) = \left(\dfrac{\vec\omega}{\rho}\cdot\nabla\right)\vec q$. In 2-D this reduces to $D\zeta/Dt = 0$.

## 4. Two-dimensional irrotational incompressible flow
- **Complex potential** $w = \phi + i\psi$ is analytic in $z = x + iy$, with $\dfrac{dw}{dz} = -u + iv$ (for $\vec q = -\nabla\phi$; for $\vec q = +\nabla\phi$ it is $u - iv$).
- **Speed** $q = |dw/dz|$. Stagnation points are where $dw/dz = 0$.
- $\phi$ and $\psi$ are harmonic and their level curves are orthogonal.

### Standard complex potentials (Milne-Thomson convention, $\vec q = -\nabla\phi$; strength $m$ means flux $2\pi m$)
| Flow | $w$ | Streamlines |
|---|---|---|
| Uniform stream $U$ along $+x$ | $-Uz$ (or $Uz$ in the other convention) | $y = c$ |
| Stream at angle $\alpha$ | $-Ue^{-i\alpha}z$ | parallel lines |
| Source of strength $m$ at $z_0$ | $-m\log(z - z_0)$ | radial lines |
| Sink | $+m\log(z - z_0)$ | radial lines |
| Doublet (strength $\mu$, axis along $x$) | $\mu/z$ (more generally $\mu e^{i\alpha}/(z - z_0)$) | circles through $O$ tangent to the axis |
| Line vortex (circulation $\Gamma$) | $\dfrac{i\Gamma}{2\pi}\log z$ ($ik\log z$) | concentric circles |
| Corner flow (angle $\pi/n$) | $Az^n$; $z^2$ is a $90^\circ$ corner | $r^n\sin n\theta = c$ |

- A **doublet** is the limit of a source $m$ at $z = \delta$ and a sink $m$ at $z = 0$ with $m\delta = \mu$ fixed.
- **Rankine half-body:** uniform stream $U$ plus a source (flux $Q$). The stagnation point is at distance $Q/(2\pi U)$ **upstream** of the source, and the half-width far downstream is $Q/(2U)$.

## 5. Images
| Singularity | Boundary | Image |
|---|---|---|
| Source $m$ at $P$ | plane wall | equal source at the mirror point |
| Vortex $\Gamma$ | plane wall | vortex $-\Gamma$ at the mirror point |
| Doublet | plane wall | equal doublet, axis reflected |
| Source $m$ at $z_0$ (outside $\lvert z\rvert = a$) | circle | source $m$ at $a^2/\bar z_0$ **plus** sink $m$ at $O$ |
| Vortex $\Gamma$ at $z_0$ | circle | vortex $-\Gamma$ at $a^2/\bar z_0$ (optionally $+\Gamma$ at $O$) |
| Doublet at $z_0$ | circle | doublet at the inverse point |

- **Milne-Thomson circle theorem:** let $f(z)$ have all its singularities in $|z| > a$. Then
$$w = f(z) + \overline{f}\!\left(\frac{a^2}{z}\right)$$
  has the same singularities in $|z| > a$ and $|z| = a$ is a streamline.
- For a uniform stream this gives the flow past a cylinder, $w = U\left(z + \dfrac{a^2}{z}\right)$.
  - Surface speed $2U|\sin\theta|$, with maximum $2U$ at $\theta = 90^\circ$ and stagnation points at $\theta = 0, \pi$.
  - Surface pressure $p = p_\infty + \tfrac12\rho U^2(1 - 4\sin^2\theta)$, equal to $p_\infty$ at $\theta = 30^\circ$, $150^\circ$, ….
- With circulation, $w = U\left(z + \dfrac{a^2}{z}\right) + \dfrac{i\Gamma}{2\pi}\log z$. The stagnation points are at $\sin\theta = -\Gamma/(4\pi Ua)$ (sign by convention); they meet when $\Gamma = 4\pi Ua$.

## 6. Forces: Blasius' theorem
$$X - iY = \frac{i\rho}{2}\oint_C\left(\frac{dw}{dz}\right)^2dz,\qquad M = \text{Re}\left[-\frac\rho2\oint_C z\left(\frac{dw}{dz}\right)^2dz\right]$$
The integrals are evaluated by residues.
- **Kutta–Joukowski:** lift $= \rho U\Gamma$ per unit length, perpendicular to the stream, and zero drag.
- **d'Alembert's paradox:** a body in steady motion through an inviscid fluid with no circulation feels no resultant force.

## 7. Motion of a sphere in a perfect fluid
Sphere of radius $a$, velocity $U$, liquid at rest at infinity, $\vec q = -\nabla\phi$.
- **Moving sphere:** $\phi = \dfrac{Ua^3}{2r^2}\cos\theta$ (a 3-D doublet). This satisfies $\nabla^2\phi = 0$, $-\partial\phi/\partial r = U\cos\theta$ at $r = a$, and $\phi \to 0$ at infinity.
- **Fixed sphere in a stream $U$:** $\phi = U\left(r + \dfrac{a^3}{2r^2}\right)\cos\theta$. The surface speed is $\tfrac32U\sin\theta$, with maximum $1.5U$ (compare $2U$ for a cylinder).
- **Kinetic energy of the liquid:** $T = \tfrac14M'U^2 = \tfrac13\pi\rho a^3U^2$, where $M' = \tfrac43\pi a^3\rho$ is the mass displaced.
- **Added (virtual) mass:** $\tfrac12M'$ for a sphere, and $M'$ (per unit length) for a circular cylinder.
- **Equation of motion** (sphere of density $\sigma$ falling under gravity): $\left(\sigma + \tfrac12\rho\right)\dot U = (\sigma - \rho)g$, so
$$\dot U = \frac{\sigma - \rho}{\sigma + \rho/2}\,g .$$
  An air bubble ($\sigma \approx 0$) accelerates upward at $2g$.
- **Pressure on a moving sphere** (unsteady Bernoulli): it contains a term $\rho a\cos\theta\,\dot U/2$ that produces the added-mass force. Uniform motion gives zero net force.
- **Stokes stream function** for a sphere moving along the axis: $\psi = -\dfrac{Ua^3}{2r}\sin^2\theta$ (sign by convention).

## Exam traps
- Bernoulli's constant is the same everywhere only for **irrotational** flow; otherwise it holds along streamlines only.
- The image of a source in a circle is a source at the inverse point **and a sink at the centre**.
- $w = ik\log z$ is a vortex (circular streamlines) and $w = m\log z$ is a source (radial streamlines).
- The stagnation point of a Rankine body lies **upstream**.
- The maximum speed is $2U$ for a cylinder and $\tfrac32U$ for a sphere.
- Added mass is half the displaced mass for a sphere and the full displaced mass for a cylinder. The fluid kinetic energy for a sphere is $\tfrac14M'U^2$, not $\tfrac12M'U^2$.
- d'Alembert: zero drag, but a cylinder with circulation still has lift $\rho U\Gamma$.
- Sign conventions ($\vec q = \mp\nabla\phi$, sign of $\psi$) differ between texts; check the convention before choosing a signed answer.
