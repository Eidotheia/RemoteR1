---
title: Uniqueness of Direct Sums in an Additive Category
date: 2023-7-23 10:21:00
tags: 
Category: Category Theory
---


$\color{skyblue}{\blacksquare}$ For any objects $X_1$, $X_2$ in an additive category $\mathcal{C}$, there exists an object $Y$ and morphisms $p_n:Y\to X_n$; $i_n:X_n\to Y$ $(n=1,2)$ such that $p_n i_n=1_{X_n}$ and $i_1 p_1+i_2 p_2=1_Y$. 

To prove that such a $Y$ is unique up to a unique isomorphism, we first show that
$$
p_1 i_2=p_2 i_1=0.
$$
However, since
$$
\begin{aligned}
p_1&=p_1 1_Y\\
&=p_1(i_1 p_1+i_2 p_2)\\
&=p_1+p_1 i_2 p_2,\\
\end{aligned}
$$
we have $p_1 i_2 p_2=0$. Thus
$$
\begin{aligned}
p_1 i_2&=p_1 i_2 1_{X_2}\\
&=p_1 i_2 p_2 i_2\\
&=0.\\
\end{aligned}
$$
Similiary, $p_2 i_1=0$. 

Suppose that there is a $Y'$ together with morphisms $p'_n:Y'\to X_n$ and $i'_n: X_n\to Y'$ such that $p'_n i'_n=1_{X_n}$ and $i'_1 p'_1+i'_2 p'_2=1_{Y'}$. By the same way we have $p'_1 i'_2=p'_2 i'_1=0$. 

Consider the morphisms $i_1 p'_1+i_2 p'_2:Y'\to Y$ and $i'_1 p_1+i'_2 p_2:Y\to Y'$. One can find that
$$
\begin{aligned}
(i_1 p'_1+i_2 p'_2)(i'_1 p_1+i'_2 p_2)
&=i_1 p_1+i_2 p_2\\
&=1_Y
\end{aligned}
$$
and similiary
$$
(i'_1 p_1+i'_2 p_2)(i_1 p'_1+i_2 p'_2)=1_{Y'}.
$$
Thus $i'_1 p_1+i'_2 p_2:Y\to Y'$ is an isomorphism and it follows that
$$
Y\cong Y'.
$$
$\color{skyblue}{\square}$ 