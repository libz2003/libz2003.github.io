---
title: "Eisenstein Like Series"
date: 2019-02-13T16:02:15+08:00
---

# Remark

Th 1 is one of the exercise problems in COMPLEX ANALYSIS by E.Stein(it is the last problem before the appendix). but the book only provide sketch of the solution, so I fill in details in this note.

# Th 1: $\gamma_8(n) = 16{\sigma_3}^*(n)$  
where

$\gamma_8(n) = \\#\left\\{(x_1,x_2,\ldots,x_8)\in\mathbb{Z}^8|\sum {x_i}^2=n\right\\}$  

${\sigma_3}^*(n) =
\begin{cases}
\sigma_3(n) & \text{n is odd}\newline
\sum\_{d|n}(-1)^dd^3={\sigma_3}^e(n)-{\sigma_3}^o(n) & \text{n is even}
\end{cases}$


where ${\sigma_3}^e(n)=\displaystyle\sum\_{\substack{d|n\newline d\ even}}d^3, \quad {\sigma_3}^o(n)=\displaystyle\sum\_{{\substack{d|n\newline d\ odd}}}d^3$

# Prove:
put $q=e^{i\pi\tau}$

define ${E_4}^*(\tau)=\displaystyle\sum\_{n+m\ odd}(n+m\tau)^{-4},\ \tau\in\mathbb{H}$

notice that ${E_4}^*(\tau)=$

$E_4(\tau)-2^{-4}\displaystyle\sum\_{\substack{n+m\ even\newline (n,m)\ne(0,0)}}\left(\frac{n}{2}+\frac{m}{2}\tau\right)^{-4}=E_4(\tau)-2^{-4}E_4\left(\frac{\tau-1}{2}\right)$

#Claim 1: $\gamma_8 = 16{\sigma_3}^*\Leftrightarrow \theta^8=48\pi^{-4}{E_4}^\*$ 