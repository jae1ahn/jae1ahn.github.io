---
layout: post
title: "coupled mode theory"
date: 2025-4-10
categories: blog
excerpt: ""
image: ""
---

<head>
<script type="text/x-mathjax-config"> MathJax.Hub.Config({ TeX: { equationNumbers: { autoNumber: "all" } } }); </script>
       <script type="text/x-mathjax-config">
         MathJax.Hub.Config({
           tex2jax: {
             inlineMath: [ ['$','$'], ["\\(","\\)"] ],
             displayMath: [['$$','$$']],
             processEscapes: true
           }
         });
       </script>
       <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
</head>


<div style="overflow-x: auto;">
$$
\left[\nabla^2 + n^2k_0^2\right]\psi = 0
$$
</div>

<div style="overflow-x: auto;">
$$
\partial_z^2\psi=\left[\nabla^2_\perp + \sum_{m}n_m^2k_0^2\right]\psi
$$
</div>

<div style="overflow-x: auto;">
$$
\beta_m^2u_m(x,y)=\left[\nabla^2_\perp + n_m^2k_0^2\right]u_m(x,y)
$$
</div>

<div style="overflow-x: auto;">
$$
\psi(x,y,z)=\sum_{m}a_m(z)u_m(x,y)e^{-i\beta_m z}=\sum_{m}A_m(z)u_m(x,y)
$$
</div>

plugging on Eq(2) and using slowly varying envelope approximation(SVEA, $\|\partial_za|>>|\partial_z^2a|$) yields

<div style="overflow-x: auto;">
$$
\sum_{m}2i\beta_m\frac{da_m(z)}{dz}u_m e^{-i\beta_m z} = -\sum_{m}\Delta n^2 k_0^2 a_m u_m e^{-i\beta_m z}
$$
</div>

now projection assuming mode orthonormality $\int u_m^*u_pdxdy=\delta_{pm}$ gives

<div style="overflow-x: auto;">
$$
i\frac{da_p(z)}{dz} = \sum_{m}\kappa_{pm} e^{i(\beta_p-\beta_m)z} a_m
$$
</div>

where $\kappa_{pm} = \frac{1}{2\beta_p}k_0^2\int dxdy (n^2-n_m^2)u^*_p(x,y)u_m(x,y) //
(n^2-n^2_m \text{ can be considered as } n_p^2)$ is coupling coefficient


with $A_m=a_me^{-i\beta_mz}$,

<div style="overflow-x: auto;">
$$
i\frac{d\bf{A}}{dz}=\bf{H}\bf{A}
$$
</div>

where $H_{pm}=\beta_p\delta_{pm} + \kappa_{pm}$

therefore supermodes satisfy 
<div style="overflow-x: auto;">
$$
\begin{align}
  \bf{A}=\bf{v}e^{-i\beta z} \\
  \bf{Hv}=\beta\bf{v} \\
  \beta \in eig(\bf{H})
\end{align}
$$
</div>