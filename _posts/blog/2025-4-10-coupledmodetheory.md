---
layout: post
title: "Coupled Mode Theory"
date: 2025-04-10
categories: blog
excerpt: "Derivation of CMT and Supermodes"
image: ""
---

<head>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>

Starting from the Helmholtz equation:

<div style="overflow-x: auto;">
$$\left[\nabla^2 + n^2k_0^2\right]\psi = 0$$
</div>

The propagation along $z$ can be expressed as:

<div style="overflow-x: auto;">
$$\partial_z^2\psi=\left[\nabla^2_\perp + \sum_{m}n_m^2k_0^2\right]\psi$$
</div>

The individual modes $u_m$ satisfy the eigenvalue equation:

<div style="overflow-x: auto;">
$$\beta_m^2u_m(x,y)=\left[\nabla^2_\perp + n_m^2k_0^2\right]u_m(x,y)$$
</div>

We expand the total field as a sum of these modes:

<div style="overflow-x: auto;">
$$\psi(x,y,z)=\sum_{m}a_m(z)u_m(x,y)e^{-i\beta_m z}=\sum_{m}A_m(z)u_m(x,y)$$
</div>

Plugging into Eq(2) and using the **Slowly Varying Envelope Approximation (SVEA)**, where $|\partial_z a| \gg |\partial_z^2 a|$:

<div style="overflow-x: auto;">
$$\sum_{m}2i\beta_m\frac{da_m(z)}{dz}u_m e^{-i\beta_m z} = -\sum_{m}\Delta n^2 k_0^2 a_m u_m e^{-i\beta_m z}$$
</div>

Projecting using mode orthonormality $\int u_m^*u_p dx dy = \delta_{pm}$ yields:

<div style="overflow-x: auto;">
$$i\frac{da_p(z)}{dz} = \sum_{m}\kappa_{pm} e^{i(\beta_p-\beta_m)z} a_m$$
</div>

where the coupling coefficient $\kappa_{pm}$ is defined as:

<div style="overflow-x: auto;">
$$\kappa_{pm} = \frac{k_0^2}{2\beta_p}\int (n^2-n_m^2)u^*_p(x,y)u_m(x,y) dx dy$$
</div>

Using $A_m = a_m e^{-i\beta_m z}$, we can write this in matrix form:

<div style="overflow-x: auto;">
$$i\frac{d\mathbf{A}}{dz}=\mathbf{H}\mathbf{A}$$
</div>

where $H_{pm} = \beta_p\delta_{pm} + \kappa_{pm}$. Therefore, the **supermodes** satisfy:

<div style="overflow-x: auto;">
$$
\begin{aligned}
  \mathbf{A} &= \mathbf{v}e^{-i\beta z} \\
  \mathbf{H}\mathbf{v} &= \beta\mathbf{v} \\
  \beta &\in \text{eig}(\mathbf{H})
\end{aligned}
$$
</div>