---
title: Hille-Yosida for Parabolic PDEs
date: 2026-04-27
---

Need to show that $A: D(A) \to L^2(U)$ is closed.

# Proof

Let $(u_n)_{n \in \mathbb N}$ be a sequence in $D(A)$ such that 
\[
    u_n \longrightarrow u, \ Au_n \longrightarrow v \ \text{ in } L^2(U).
\]
By elliptic regularity
\[
    \|u_n - u_m\|_{H^2} \lesssim \|Au_n - Au_m\|_{L^2} + \|u_n - u_m\|_{L^2} \longrightarrow 0,
\]
as $n, m \to \infty$. Since $H^2$ is a Hilbert space there exists $\tilde{u} \in H^2$ such that $u_n \to \tilde{u}$ in $H^2$. $H^2$ convergence implies $L^2$ convergence so in fact $\tilde{u} = u$, moreover, $H^2$ convergence implies $H^1$ convergence. Recall the trace operator $T: H^1 \to L^2(\partial U)$, it is a bounded linear operator and since $Tu_n = 0$ we must also have $Tu = 0$ hence $u \in D(A)$. $A$ as a mapping between the Hilbert space $(D(A), (\cdot,\cdot)_{H^2})$ and $L^2$ is bounded so it follows that $Au_n \to Au$ in $L^2$. Therefore $A$ is closed.
