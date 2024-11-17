---
title: On Counting and Involutions on Posets
date: 2024-11-03
categories: 
- [Combinatorics]
---

Let $P$ be a finite poset of $n$ elements. For each $a\in P$, denote by $\iota_P(a)$ the number of elements in $P$ that are less than $a$. When the context is clear, we will simply write $\iota$ instead of $\iota_P$. 

For each order-preserving map $f$ from $P$ to the chain $[n]:=\{0,1,\ldots,n\}$, let $f_S$ be the restriction of $f$ to $S\subset P$ and let $Z_Sf(a)$ be the number of elements in $S$ whose values under $f$ are less than or equal to $\iota(a)$. Then
$$
    Z_Sf(a)=\sum_{t\leq\iota(a)}\left\vert f_S^{-1}(t)\right\vert.
$$

For convenience, let $\chi_S^a f$ be the characteristic function such that for any $x\in P$, $\chi_S^a f(x)=1$ if $x\in f_S^{-1}\left([\iota(a)]\right)$ and $=0$ if not. And for $X\subset P$ let $\chi_S^a f(X)=\prod_{x\in X}\chi_S^a f(x)$. By definition, $Z_Sf(a)$ is just the size of the preimage of $[\iota(a)]$ under $f_S$. Covering $S$ by a finite collection $\{S_i\}_{i\in I}$, then
$$
    \sum_{J\subset I}{(-1)}^{\vert J\vert}Z_{S_J}f(a)=0,
$$
where $S_J$ denotes the intersection $\bigcap_{j\in J}S_j$. In particular, 
$$
    Z_Sf(a)=\sum_{s\in S}\chi_S^a f(s).
$$


We now study the structure of $\mathrm{Hom}_{\mathsf{Pos}}\left(P,[n]\right)$ the set of all order-preserving maps from $P$ to $[n]$.

When considering the special case where $S = P$, we simplify the notation by omitting the subscript$\:_P$. For $f$, $g\in\mathrm{Hom}_{\mathsf{Pos}}\left(P,[n]\right)$, define $f_S\leq g_S$ if $f(s)\leq g(s)$ for all $s\in S$. Notice that $Z_S f$ is also order-preserving. 


__Lemma 1__ If $f_S\leq g_S$, then $Z_S f\geq Z_S g$. 


_Proof_ Suppose that $f_S\leq g_S$. If $g_S(x)=k\in [n]$, then $f_S(x)\leq k$. Which means that $g_S^{-1}(k)\subset\bigcup_{i\leq k}f_S^{-1}(i)$. Thus
$$
\begin{aligned}
        Z_S g(s)&=\sum_{i\leq\iota(s)}\left\vert g_S^{-1}(i)\right\vert \\
        &=\left\vert\bigcup_{i\leq\iota(s)}g_S^{-1}(i)\right\vert \\
        &\leq\left\vert\bigcup_{i\leq\iota(s)}\bigcup_{j\leq i}f_S^{-1}(i)\right\vert \\
        &=\left\vert\bigcup_{i\leq\iota(s)}f_S^{-1}(i)\right\vert \\
        &=Z_S f(s)
\end{aligned}
$$
for all $s\in S$. In particular, if $f\leq g$, then $Zf\geq Zg$. $\blacksquare$
 
For each order-preserving map $f$, denote by $\partial f$ the M\"{o}bius inversion of $f$. 
Since $Zf$ is also an order-preserving map, for all $a\in P$ we have
$$
    Zf(a)=\sum_{b\leq a}\partial Zf(b).
$$

Let $C_n$ denote a chain of $n$ elements. Since $\iota$ is an isomorphism between $C_n$ and $[n-1]$, for each $a\in C_n$, we have the following results.

__Lemma 2__ For every order-preserving map $f:C_n\to [n]$,
$$
\partial Zf(a)=\left\vert f^{-1}(\iota(a))\right\vert
$$
for all $a\in C_n$.

__Lemma 3__ For every order-preserving map $f:C_n\to [n]$,
$$
ZZf=f.
$$

Lemma 3 indicates that if $P$ is a chain, then $Z$ is an order-reversing involution on $\mathrm{Hom}_{\mathsf{Pos}}\left(C_n,[n]\right)$ in which the maps are ordered by pointwise comparison. 

Consider the set $\underline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right)$ consist of all order-preserving maps from $P$ to $[n]$ for which 0 has a nonempty preimage, and let $\overline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right)$ be the complement of it in $\mathrm{Hom}_{\mathsf{Pos}}\left(P,[n]\right)$. It's not hard to show that 
$$
Z\left(\underline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right)\right)\subset\overline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right)
$$
and
$$
Z\left(\overline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right)\right)\subset\underline{\mathrm{Hom}}_{\mathsf{Pos}}\left(P,[n]\right).
$$

Thus for any $f\in\mathrm{Hom}_{\mathsf{Pos}}\left(P,[n]\right)$, if there exists a $t>0$ which is the least integer such that $Z^{t}(f)=f$, then $t$ must be even. 

We conjecture that for any finite poset $P$, there exists an $N\in\mathbb{N}$ such that $Z^{r+2}(f)=Z^r(f)$ whenever $r>N$.
