---
layout: post
title: "Coupled Mode Theory"
date: 2025-04-10
categories: blog
excerpt: "An overview of mode coupling in waveguides using the slowly varying envelope approximation."
image: ""
---

<head>
  <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      TeX: { equationNumbers: { autoNumber: "all" } },
      tex2jax: {
        inlineMath: [ ['$','$'], ["\\(","\\)"] ],
        displayMath: [['$$','$$']],
        processEscapes: true
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
</head>

The starting point is the Helmholtz equation:

$$\left[\nabla^2 + n^2k_0^2\right]\psi = 0$$

Separating the propagation direction $z$ from the transverse components:

$$\partial_z^2\psi = -\left[\nabla^2_\perp + \sum_{m}n_m^2k_0^2\right]\psi$$

Each individual mode $u_m(x,y)$ satisfies the following eigenvalue equation:

$$\beta_m^2 u_m(x,y) = \left[\nabla^2_\perp + n_m^2k_0^2\right]u_m(x,y)$$

We expand the total field $\psi$ as a linear combination of these modes, where $a_m(z)$ represents the complex amplitude:

$$\psi(x,y,z) = \sum_{m}a_m(z)u_m(x,y)e^{-i\beta_m z} = \sum_{m}A_m(z)u_m(x,y)$$

### Slowly Varying Envelope Approximation (SVEA)

Plugging this into the wave equation and applying the **SVEA** ($|\partial_z a| \gg |\partial_z^2 a|$), we obtain:

$$\sum_{m}2i\beta_m\frac{da_m(z)}{dz}u_m e^{-i\beta_m z} = -\sum_{m}\Delta n^2 k_0^2 a_m u_m e^{-i\beta_m z}$$

By assuming mode orthonormality ($\int u_m^* u_p dx dy = \delta_{pm}$) and projecting the equation, we get the Coupled Mode Equations:

$$i\frac{da_p(z)}{dz} = \sum_{m}\kappa_{pm} e^{i(\beta_p-\beta_m)z} a_m$$

Where the **Coupling Coefficient** $\kappa_{pm}$ is defined as:

$$\kappa_{pm} = \frac{k_0^2}{2\beta_p}\int (n^2-n_m^2)u^*_p(x,y)u_m(x,y) dx dy$$

---

### Matrix Representation and Supermodes

Defining $A_m = a_m e^{-i\beta_m z}$, the system can be written in matrix form:

$$i\frac{d\mathbf{A}}{dz} = \mathbf{H}\mathbf{A}$$

where the Hamiltonian matrix elements are $H_{pm} = \beta_p\delta_{pm} + \kappa_{pm}$. 

The **Supermodes** of the system are found by solving the eigenvalue problem:

$$ \begin{aligned}
\mathbf{A} &= \mathbf{v}e^{-i\beta z} \\
\mathbf{H}\mathbf{v} &= \beta\mathbf{v} \\
\beta &\in \text{eig}(\mathbf{H})
\end{aligned} $$