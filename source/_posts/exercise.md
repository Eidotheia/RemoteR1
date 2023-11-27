---
title: A Little Note on Representation Theory
date: 2023-7-10 13:42:58
Categories: 
- [Algebra]
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

$$
\begin{aligned}
\sum_{g\in G}\chi(g)&=\sum_{\substack{(\alpha_1,\ldots,\alpha_n) \\ 0\leq\alpha_k\leq s_k-1}}\prod_{k=1}^n{\chi(g_k)}^{\alpha_k}\\
&=\prod_{k=1}^n\left(\sum_{\alpha_k=0}^{s_k-1} {\chi(g_k)}^{\alpha_k} \right)\\
&=\prod_{k=1}^{n}\left(\frac{1-{\chi(g_k)}^{s_k}}{1-\chi(g_k)}\right)\\
&=0.\\
\end{aligned}
$$

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
