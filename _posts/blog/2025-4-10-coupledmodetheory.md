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

<img src="/study_img/cmt/1.png" alt="scheme" style="width: 50%; height: auto;"/>
<img src="/study_img/cmt/2.png" alt="effective index" style="width: 50%; height: auto;"/>


<div style="overflow-x: auto;">
$$
\left[\partial_x^2 + \partial_z^2 + n^2(x)\frac{\omega_0^2}{c^2}\right] E_y = 0
$$
</div>

<div style="overflow-x: auto;">
$$
E_y(x,z) = A(z)\psi_1(x)e^{i\beta_1 z} + B(z)\psi_2(x)e^{i\beta_2 z}
$$
</div>

<div style="overflow-x: auto;">
$$
\begin{align}
\frac{\partial A}{\partial z} + i\kappa_{12}B e^{i(\beta_1-\beta_2)z} = 0 \\
\frac{\partial B}{\partial z} + i\kappa_{21}A e^{i(\beta_2-\beta_1)z} = 0
\end{align}
$$
</div>

<div style="overflow-x: auto;">
$$
\kappa_{ij} = \frac{1}{2\beta_i}\frac{\omega^2_0}{c^2}\int n_i^2(x)\psi^*_i(x)\psi_j(x)\,dx
$$
</div>

<div style="overflow-x: auto;">
$$
A(z) = a(z)e^{i\Delta \beta z}, \quad
B(z) = b(z)e^{-i\Delta \beta z}, \quad
(\Delta \beta = \frac{\beta_1-\beta_2}{2})
$$
</div>

<div style="overflow-x: auto;">
$$
\partial_z 
\begin{pmatrix} a \\ b \end{pmatrix} 
= -i 
\mathbf{H}
\begin{pmatrix} a \\ b \end{pmatrix}
$$
</div>

<div style="overflow-x: auto;">
$$
\mathbf{H} =
\begin{pmatrix}
\Delta\beta & \kappa_{12} \\
\kappa_{21} & -\Delta\beta
\end{pmatrix}, \quad
\text{eigenvalue } \lambda = \pm \displaystyle \sqrt{(\Delta\beta)^2 + \kappa_{12}\kappa_{21}}
$$
</div>