---
title: A Proof of Yoneda Lemma
date: 2023-7-8 16:30:58
tags: 
Categories: Category Theory  
---



Let $\mathcal{C}$ be a category and $\mathrm{Set}$ be the category of sets. For any (covariant) functor $F$ from $\mathcal{C}$ to $\mathrm{Set}$, the Yoneda lemma states that for each object $A$ in $\mathcal{C}$, the set $\mathrm{Nat}(\mathrm{Hom}(A,\cdot),F)$ of all natural transformations from the functor $\mathrm{Hom}(A,\cdot)$ to $F$ is isomorphic to the set $F(A)$. 

Recall that a natural transformation $\lambda$ from a functor $H$ to a functor $G$ is a collection $\{\lambda_X\}$ of morphisms such that for each pair $(X, Y)$ of objects in $\mathcal{C}$,   
$$
\lambda_X Hf=Gf\lambda_Y 
$$
for all morphism $f:X\to Y$. To prove that two natural transformations $\lambda$ and $\mu$ are equal is to prove that the collections $\{\lambda_X\}$ and $\{\mu_X\}$ are the same, i.e., 
$$
\lambda_X=\mu_X
$$
for each $X$ in $\mathcal{C}$. 

Now consider the map $\phi:\mathrm{Nat}(\mathrm{Hom}(A,-),F)\to F(A)$ given by
$$
\phi (\lambda)=\lambda_A(1_A),
$$
this map is called the _Yoneda representative map_, while $\lambda_A(1_A)$ is the _Yoneda representative_ of $\lambda$. We prove that $\phi$ is an isomorphism. Denote by $f_A^{\leftarrow}$ the "follow by $f$" map $\mathrm{Hom}(A,f),$ it satisfies the formula
$$
f_A^{\leftarrow}(u)=f\circ u
$$
for each $u\in\mathrm{Hom}(A,A)$. 

For each object $X$ and natural transformations $\lambda$ and $\mu$, if $\lambda_A(1_A)=\mu_A(1_A)$, then 
$$
\begin{aligned}
\lambda_X(f)&=\lambda_X\circ f_A^{\leftarrow}(1_A)\\
&=Ff(\lambda_A(1_A))\\
&=Ff(\mu_A(1_A))\\
&=\mu_X\circ f_A^{\leftarrow}(1_A)\\
&=\mu_X(f)\\
\end{aligned}
$$
for every $f\in\mathrm{Hom}(A,X)$. Thus $\lambda=\mu$ and hence $\phi$ is injective. However, for each $f\in\mathrm{Hom}(A,X)$, 
$$
f=f_A^{\leftarrow}(1_A)
$$
follows that $\phi$ is surjective. All in all, $\phi$ is an bijection. We have thus proved the covariant version of Yoneda lemma. 

___

In a more modern language, we call a functor $F$ from the opposite category $\mathcal{C}^{\mathrm{op}}$   to $\mathrm{Set}$ a _presheaf_ on $\mathcal{C}$. The set of all preshesves together with the natural transformations between them forms a category, called the category of presheaves on $\mathcal{C}$ and denoted by $\hat{\mathcal{C}}$. The contravariant version of Yoneda lemma states that 
$$
\mathrm{Hom}_{\hat{\mathcal{C}}}\left(\mathrm{Hom}(\cdot,A),F\right)\cong F(A).
$$
The proof is similiar. 

In particular, we have
$$
\mathrm{Hom}_{\hat{\mathcal{C}}}\left(\mathrm{Hom}(\cdot,A),\mathrm{Hom}(\cdot,B)\right) \cong\mathrm{Hom}(A,B).
$$

