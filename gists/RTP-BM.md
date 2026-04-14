---
title: MFPT Derivation
subtitle: 
date: 
---

We consider a run-and-tumble particle with additional translational diffusion:
\[
dX_t = v\sigma_t\,dt + \sqrt{2D}\,dW_t,
\]
where $\sigma_t \in \{+1,-1\}$ switches at rate $\alpha$. The particle is confined to $[0,L]$, with
- absorbing boundary at $x=0$,
- reflecting boundary at $x=L$.

Define the mean first passage times
\[
m_\pm(x) = \mathbb{E}_{x,\pm}[\tau_0],
\]
where $\tau_0$ is the first hitting time of $x=0$.

## Backward Equations

Using a standard backward argument, the MFPT satisfies
\[
D m_+''(x) + v m_+'(x) + \alpha (m_-(x) - m_+(x)) = -1,
\]
\[
D m_-''(x) - v m_-'(x) + \alpha (m_+(x) - m_-(x)) = -1.
\]

At the absorbing boundary,
\[
m_+(0) = 0, \qquad m_-(0) = 0.
\]

The reflecting boundary condition requires more care and is derived below.

## Derivation of Reflecting Boundary Conditions

### Forward Flux Condition

Let $p_\pm(x,t)$ denote the forward densities. The fluxes are
\[
J_+ = v p_+ - D \partial_x p_+,
\qquad
J_- = -v p_- - D \partial_x p_-.
\]

Reflection imposes zero total flux at $x=L$:
\[
J_+(L,t) + J_-(L,t) = 0.
\]

Additionally, specular reflection implies
\[
p_+(L,t) = p_-(L,t).
\]

Substituting, we obtain
\[
\partial_x p_+(L,t) + \partial_x p_-(L,t) = 0.
\]

### Backward Boundary Conditions via Duality

Using integration by parts (adjoint relationship between forward and backward generators), the backward test functions must satisfy dual conditions:
\[
m_+(L) = m_-(L),
\]
\[
m_+'(L) + m_-'(L) = 0.
\]

These are the correct reflecting boundary conditions.

## Reduction via Sum and Difference

Define
\[
s(x) = m_+(x) + m_-(x), \qquad d(x) = m_+(x) - m_-(x).
\]

Then
\[
m_\pm(x) = \frac{1}{2}(s(x) \pm d(x)).
\]

Adding and subtracting the equations gives
\[
D s''(x) + v d'(x) = -2,
\]
\[
D d''(x) + v s'(x) - 2\alpha d(x) = 0.
\]

Boundary conditions become
\[
s(0) = 0, \quad d(0) = 0,
\]
\[
d(L) = 0, \quad s'(L) = 0.
\]

## Solving for $d(x)$

From the first equation,
\[
D s'(x) + v d(x) = 2(L - x).
\]

Substitute into the second equation to obtain
\[
D^2 d''(x) - (v^2 + 2\alpha D)d(x) + 2v(L - x) = 0.
\]

Define
\[
\gamma = \sqrt{v^2 + 2\alpha D}, \qquad \beta = \frac{\gamma}{D}.
\]

Then
\[
d''(x) - \beta^2 d(x) = -\frac{2v}{D^2}(L - x).
\]

Solving,
\[
d(x) = \frac{2v}{\gamma^2}
\left[
L - x - L \frac{\sinh(\beta(L-x))}{\sinh(\beta L)}
\right].
\]

## Solving for $s(x)$

Using
\[
s'(x) = \frac{2(L-x) - v d(x)}{D},
\]
and integrating,
\[
s(x)
=
\frac{2\alpha}{\gamma^2} x(2L - x)
+
\frac{2Lv^2}{\gamma^3 \sinh(\beta L)}
\Big[
\cosh(\beta L) - \cosh(\beta(L - x))
\Big].
\]

## Final Expression for MFPT

Combining,
\[
m_\pm(x)
= \frac{Lv^2}{\gamma^3 \sinh(\beta L)}
\Big[
\cosh(\beta L) - \cosh(\beta(L - x))
\Big]
+ \frac{\alpha}{\gamma^2} x(2L - x)
\]
\[
\qquad \pm \frac{v}{\gamma^2}
\left[
L - x - L \frac{\sinh(\beta(L - x))}{\sinh(\beta L)}
\right].
\]

## Consistency Check

As $D \to 0$, we recover the pure run-and-tumble result:
\[
m_+(x) = \frac{2L - x}{v} + \frac{\alpha}{v^2} x(2L - x),
\]
\[
m_-(x) = \frac{x}{v} + \frac{\alpha}{v^2} x(2L - x).
\]
