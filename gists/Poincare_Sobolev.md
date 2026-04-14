---
title: Poinecare's Inequality (Sobolev)
subtitle:
date: 2026-04-14
---

# Theorem

Let $U \subset \mathbb R^n$ be open and bounded. For $f \in H_0^1(U)$ there exists $C >0$ such that
\[
    \|f\|_{L^2} \leq C \|\nabla f\|_{L^2}.
\]

# Proof

By way of contradiction suppose the inequality is false then there exists $(f_n)_{n \in \mathbb N}$ in $H_0^1(U)$ such that
\[
    \|f_n\|_{L_2(U)} = 1, \ \|\nabla f\|_{L_2}(U) = \frac1n.
\]
The sequence is bounded in $H_0^1(U)$ and since $H_0^1$ is reflexive
\[
    f_n \rightharpoonup f, \text{ weakly in } H_0^1(U),
\]
for some $f \in H_0^1(U)$. Applying Rellich-Kondrachov we can extract a subsequence so that
\[
    f_n \rightarrow f, \text{ strongly in } L^2(U),
\]
and we have $\|f\|_{L^2(U)} = 1$. Noting that by definition $\nabla f_n \rightarrow 0$ in $L^2(U)$ which implies that $f$ is constant almost everywhere in $U$. Since $f \in H_0^1(U)$ it must vanish near the boundary of U which forces $f \equiv 0$ -- contradicting $\|f\|_{L^2(U)} = 1$.
