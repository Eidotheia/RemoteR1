---
title: Little Notes on Representation Theory
date: 2023-11-26 20:12:58
tags:
---


Let $G$ be a finite group and $K$ be a field. The multiplicative character of $G$ is a group homomorphism $\chi:G\to K^{\ast}$, where $K^{\ast}$ denotes the multiplicative group of non-zero elements of $K$. The trivial character is given by $\chi(g)=1$ for all $g\in G$.
Let $\chi:G\to K^{\ast}$ be a non-trivial multiplicative character, we now show that
$$
\sum_{g\in G}\chi(g)=0.
$$
$\color{skyblue}{\blacksquare}$ Since $G$ is finite, it must be finitely generated. Suppose that
$$
G=\langle g_1,\ldots,g_n\rangle.
$$
Let $s_k$ be the order of $g_k$ for $k=1,2,\ldots,n$. Then

<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Balign*%7D%0A%5Csum_%7Bg%5Cin%20G%7D%5Cchi(g)%26%3D%5Csum_%7B%5Csubstack%7B(%5Calpha_1%2C%5Cldots%2C%5Calpha_n)%20%5C%5C%200%5Cleq%5Calpha_k%5Cleq%20s_k-1%7D%7D%5Cprod_%7Bk%3D1%7D%5En%7B%5Cchi(g_k)%7D%5E%7B%5Calpha_k%7D%5C%5C%0A%26%3D%5Cprod_%7Bk%3D1%7D%5En%5Cleft(%5Csum_%7B%5Calpha_k%3D0%7D%5E%7Bs_k-1%7D%20%7B%5Cchi(g_k)%7D%5E%7B%5Calpha_k%7D%20%5Cright)%5C%5C%0A%26%3D%5Cprod_%7Bk%3D1%7D%5E%7Bn%7D%5Cleft(%5Cfrac%7B1-%7B%5Cchi(g_k)%7D%5E%7Bs_k%7D%7D%7B1-%5Cchi(g_k)%7D%5Cright)%5C%5C%0A%26%3D0.%5C%5C%0A%5Cend%7Balign*%7D%0A" alt="
\begin{align*}
\sum_{g\in G}\chi(g)&amp;=\sum_{\substack{(\alpha_1,\ldots,\alpha_n) \\ 0\leq\alpha_k\leq s_k-1}}\prod_{k=1}^n{\chi(g_k)}^{\alpha_k}\\
&amp;=\prod_{k=1}^n\left(\sum_{\alpha_k=0}^{s_k-1} {\chi(g_k)}^{\alpha_k} \right)\\
&amp;=\prod_{k=1}^{n}\left(\frac{1-{\chi(g_k)}^{s_k}}{1-\chi(g_k)}\right)\\
&amp;=0.\\
\end{align*}
" />

$\color{skyblue}{\square}$

In particular, let $\zeta_n$ $(n\geq 2)$ be the primitive $n$-th root of unity, we have
$$
\sum_{k=0}^{n-1}\zeta_n^k=0.
$$
Further more, for $n\geq 2$, 
$$
\sum \zeta=0
$$
in which $\zeta$ ranges over $n$ distinct roots of unity. 
