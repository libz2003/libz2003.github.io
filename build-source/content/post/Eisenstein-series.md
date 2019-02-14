---
title: "Eisenstein Like Series"
date: 2019-02-13T16:02:15+08:00
mathjax: true
---

# Remark

Th 1 is one of the exercise problems in COMPLEX ANALYSIS by E.Stein(it is the last problem before the appendix). but the book only provide sketch of the solution, so I fill in details in this note.

# Th 1: $r_8(n) = 16{\sigma_3}^*(n)$  
where

$r_8(n) = \\#\left\\{(x_1,x_2,\ldots,x_8)\in\mathbb{Z}^8|\sum {x_i}^2=n\right\\}$  

${\sigma_3}^*(n) =
\begin{cases}
\sigma_3(n) & \text{n is odd}\newline
\sum\_{d|n}(-1)^dd^3={\sigma_3}^e(n)-{\sigma_3}^o(n) & \text{n is even}
\end{cases}$


where ${\sigma_3}^e(n)=\displaystyle\sum\_{d|n\atop d\ even}d^3, \quad {\sigma_3}^o(n)=\displaystyle\sum\_{d|n\atop d\ odd}d^3$

## Prove:
put $q=e^{i\pi\tau}$

define ${E_4}^*(\tau)=\displaystyle\sum\_{n+m\ odd}(n+m\tau)^{-4},\ \tau\in\mathbb{H}$

notice that ${E_4}^*(\tau)=$

$E_4(\tau)-2^{-4}\displaystyle\sum\_{\substack{n+m\ even\newline (n,m)\ne(0,0)}}\left(\frac{n}{2}+\frac{m}{2}\tau\right)^{-4}=E_4(\tau)-2^{-4}E_4\left(\frac{\tau-1}{2}\right)$

# Claim 1: $r_8 = 16{\sigma_3}^*\Leftrightarrow \theta^8=48\pi^{-4}{E_4}^\*$ 

## Prove:
We have $\theta(\tau)^8=1+\displaystyle\sum\_{k=1}^\infty r_8(k)q^k$

and $E_4(\tau)=2\zeta(4)+\frac{16}{3}\pi^4\displaystyle\sum\_{k=1}^\infty\sigma_3(k)q^{2k}$  

as a result, $E_4(\tau)=2\zeta(4)+\frac{2}{3}\pi^4\sum{\sigma_3}^e(2k)q^{2k}$

$2^{-4}E_4\left(\frac{\tau-1}{2}\right)=\frac{\zeta(4)}{8}+\frac{1}{3}\pi^4\sum\sigma_3(k)(-q)^k$  

so $48\pi^{-4}{E_4}^*(\tau)=1+16\left(\displaystyle\sum\_{k\ odd}\sigma_3(k)q^k+\sum a\_{2k}q^{2k}\right)$

where $a_{2k}=2{\sigma_3}^e(2k)-\sigma_3(2k)$

$=2{\sigma_3}^e(2k)-{\sigma_3}^e(2k)-{\sigma_3}^o(2k)={\sigma_3}^e(2k)-{\sigma_3}^o(2k)$

# Claim 2: ${E_4}^\*(\tau+2)={E_4}^*(\tau)$
## Prove: clear

# Claim 3: ${E_4}^\*(\tau)=\tau^{-4}{E_4}^*(-\tau^{-1})$
## Prove:

we have $\tau^{-4}{E_4}^*(-\tau^{-1})=\tau^{-4}E_4(-\tau^{-1})-(2\tau)^{-4}E_4\left(\frac{-\tau^{-1}-1}{2}\right)$

$=E_4(\tau)-(2\tau)^{-4}E_4\left(-\frac{\tau+1}{2\tau}\right)=E_4(\tau)-(\tau+1)^{-4}E_4\left(\frac{2\tau}{\tau+1}\right)$

$=E_4(\tau)-(\tau+1)^{-4}E_4\left(-\frac{2}{\tau+1}\right)=E_4(\tau)-2^{-4}E_4\left(\frac{\tau+1}{2}\right)$

$=E_4(\tau)-2^{-4}E_4\left(\frac{\tau-1}{2}\right)={E_4}^*(\tau)$

# Claim 4: $48\pi^{-4}{E_4}^*(\tau)\to 1\ as\ \mathcal{I}(\tau) \to \infty$
## Prove:
${E_4}^*(\tau)=E_4(\tau)-2^{-4}E_4\left(\frac{\tau-1}{2}\right)$

it can be seen from $E_4(\tau)=2\zeta(4)+\frac{16}{3}\pi^4\displaystyle\sum\_{k=1}^\infty\sigma_3(k)q^{2k}$

# Claim 5: ${E_4}^*(1-\tau^{-1})=\tau^4(E_4(\tau)-E_4(2\tau))$
## Prove:
$\tau^{-4}{E_4}^*(1-\tau^{-1})=\tau^{-4}E_4(1-\tau^{-1})-(2\tau)^{-4}E_4(-(2\tau)^{-1})$

$=E_4(\tau)-E_4(2\tau)$

# Claim 6: $\vert{E_4}^*(1-\tau^{-1})\vert\approx\vert\tau\vert^4\vert q\vert^2\ as \ \mathcal{I}(\tau) \to \infty$
where we denote $c\ f_1\le f_2\le C\ f_1 \ \mathrm{by} \ f_1 \approx f_2$

## prove:
obvious from Claim 5  
but $\theta^8$ also satisfies Claim 2, 3, 4, 6  
so we can get our result by applying  
the following lemma to $\frac{{E_4}^*}{\theta^8}(\theta\ has\ no\ root\ on\ \mathbb{H})$

# Lemma: $f$ is a holomorphic on $\mathbb{H}$ such that
$\begin{align}
\tag{i}f(\tau+2)=f(\tau)\newline
\tag{ii}f(-\tau^{-1})=f(\tau)\newline
\tag{iii}f(\tau)\ is\ bounded
\end{align}$

**then $f$ is constant**

## prove:
see COMPLEX ANALYSIS by E.Stein  
we can see from the above text that ${E_4}^*$ has no root on $\mathbb{H}$  
we want to ask the same question about other similar functions.

# Th 2: ${E_{4k}}^*(k>1)\ has\ root(s)\ on\ \mathbb{H}$
where ${E_{4k}}^*(\tau)=\displaystyle\sum\_{n+m\ odd}(n+m)^{-4k}$

## Prove:
by similar auguement we can get  
$$\begin{align}
\tag{1}{E_{4k}}^*(\tau) &= E\_{4k}(\tau)-2^{-4k}E\_{4k}\left(\frac{\tau-1}{2}\right)\newline
\tag{2}{E\_{4k}}^\*(\tau) &= {E\_{4k}}^\*(\tau+2)\newline
\tag{3}{E\_{4k}}^\*(\tau) &= \tau^{-4k}{E\_{4k}}^\*(-\tau^{-1})\newline
\tag{4}{E\_{4k}}^\*(\tau) &\to c\_{4k}\ as\ \mathcal{I}(\tau) \to \infty,\ where\ c\_{4k}=2(1-2^{-4k})\zeta(4k)\newline
\tag{5}{E\_{4k}}^\*(1-\tau^{-1}) &= \tau^{4k}(E\_{4k}(\tau)-E\_{4k}(2\tau))\newline
\tag{6}\vert{E\_{4k}}^\*(1-\tau^{-1})\vert &\approx \vert\tau\vert^{4k}\vert q\vert^2\ as\ \mathcal{I}(\tau) \to \infty
\end{align}$$

note that $\theta^{8k}$ satisfies $\left\vert\theta(1-\tau^{-1})^{8k}\right\vert \approx \vert\tau\vert^{4k}\vert q\vert^{2k}\ as\ \mathcal{I}(\tau) \to \infty$

if ${E_{4k}}^*$ has no root, then $\frac{\theta^{8k}}{{E\_{4k}}^\*}$ is holomorphic on $\mathbb{H}$,  
so must be constant by the lemma  
however, $\displaystyle\lim\_{\tau \to 1}\frac{\theta^{8k}}{{E\_{4k}}^\*}{\tau}=0,\quad \displaystyle\lim\_{\tau \to 1}\frac{\theta^{8k}}{{E\_{4k}}^\*}{\tau}=\frac{1}{c\_{4k}}$  
contradiction

# Corollary 1: 
$E\_{4k}(2\tau)-E\_{4k}(\tau)
\begin{cases}
\text{has no root on }\mathbb{H} & k=1\newline
\text{has root(s) on }\mathbb{H} & k>1
\end{cases}$

## Prove:
${E_{4k}}^*(1-\tau^{-1})=\tau^{4k}(E\_{4k}(\tau)-E\_{4k}(2\tau))$

# Th 3: 
${S\_{4k}}^{(1)} \ \\& \ {S\_{4k}}^{(2)}
\begin{cases}
\text{has no root on }\mathbb{H} & k=1\newline
\text{has root(s) on }\mathbb{H} & k>1
\end{cases}$

where  
${S_{4k}}^{(1)}(\tau)=\displaystyle\sum\_{n,m}\left(n+m\tau+\frac{1}{2}\right)^{-4k}$

${S_{4k}}^{(2)}(\tau)=\displaystyle\sum\_{n,m}\left(n+m\tau+\frac{\tau}{2}\right)^{-4k}$

## Prove:
$E\_{4k}(\tau)-E\_{4k}(2\tau)=\displaystyle\sum\_{(n,m)\ne(0,0)}(n+m\tau)^{-4k}-\displaystyle\sum\_{(n,m)\ne(0,0)}(n+2m\tau)^{-4k}$

$=\sum(n+(2m+1)\tau)^{-4k}={S_{4k}}^{(2)}(2\tau)$

we can get ${S_{4k}}^{(1)}(2\tau)$ by simply multiply a factor