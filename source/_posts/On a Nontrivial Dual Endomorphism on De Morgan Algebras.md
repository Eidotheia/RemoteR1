Let $\mathcal{O}$ be the poset of all order-preserving maps from $\mathbb{N}$ to $\overline{\mathbb{N}}=\mathbb{N}\cup\{\infty\}$, where the order on $\mathcal{O}$ is given by pointwise comparison: $a\leq b$ iff $a_n\leq b_n$ for each $n$. $\mathcal{O}$ is a bounded distributive lattice in which
$$
a\vee b=\max\{a,b\},\: a\wedge b =\min\{a,b\}.
$$
With all elements as objects, and $\mathrm{Hom}_{\mathcal{O}}(a,b)$ is empty unless $a\leq b$, $\mathcal{O}$ becomes a category that has limits and colimits. For each $a\in\mathcal{O}$, the endofunctor $Z$ on $\mathcal{O}$ defined by
$$
{(Za)}_n=\sum_{i\in\mathbb{N}}\zeta(a_i,n).
$$
is a dual endomorphism since it's self-adjoint, and $\mathcal{O}$ thus becomes a De Morgan algebra.

Our first interest is about the functor $\Delta Z: \mathcal{O}\to\mathcal{A}$; $\Delta Za_i$ counts the frequency that the integer $i$ occurs in the sequence $\{a_n\}_0^{+\infty}$. For convenience, we sometimes denote it by $\chi$. Given $a\in\mathrm{Obj}\:\mathcal{O}$, there is a unique morphism $Z^*$ such that the following diagram commutes

$$ \require{AMScd} \begin{CD} a @>Z>> Za \\ @V{\chi}VV @V{\chi}VV \\ \chi(a) @>{Z^*}>> \chi(Za) \end{CD} $$

It's easy to show that $Z^*=\Delta Z\Delta^{-1}$, and $Z^*$ is not a dual endomorphism. As a remedy, we define $\vee^*$ to be the 2-operation on $\mathcal{A}$ such that $f\vee^* g=\max\{\bar f,\bar g\}$ where $\bar f$, $\bar g$ are the lest objects in $\mathcal{O}$ that covers $f$ and $g$. Similiarly, we can define $\wedge^*$. So that
$$
f\mapsto\sum_{i\in\mathbb{N}}\zeta(\bar{f}_i,)
$$
gives a dual endomorphism on $\mathcal{A}$ with respect to $\vee^*$ and $\wedge^*$. 

___

ALL ARE ABOUT GALOIS CORRESPONDENCE. 2023. 9. 25. 

---

The pair 
$$
(Z:\mathcal{O}\to\mathcal{O^{\mathrm{op}}},
Z:\mathcal{O}^{\mathrm{op}}\to\mathcal{O})
$$
is a antitone Galois correspondence from $\mathcal{O}$ to $\mathcal{O}^{\mathrm{op}}$. That is, 
$$
a=ZZ(a);\: a\leq Z(b)\Leftrightarrow Z(a)\geq b 
$$
for all $a$, $b\in\mathrm{Obj}\:\mathcal{O}$. 

---
October 10, 2023

__Finite case__

For $t\in\mathbb{N}$, consider the lattice $\mathcal{O}_{t}$ of all order-preserving maps from $[t]$ to $[t+1]$, it's also a category where the morphisms and objects are defined in the canonical way.  
We define $Z$ on it by
$$
{(Za)}_n=\sum_{i\in[t]}\zeta(a_i,n)
$$
for every $a\in\mathrm{Obj}\:\mathcal{O}_{t}$. The order complex $\Delta(\mathcal{O}_t)$ is an abstract simplicial complex on $\mathcal{O}_t$, could we find some Galois connection between it and another one? 

__Example__ Taking $t=1$, and determine each order-preserving map in $\mathcal{O}_1$ by a sequence with length $2$. There $6$ such maps:

<center>
<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Bcenter%7D%0A%5Cbegin%7Btabular%7D%7B%20c%7Cc%20c%20%7D%20%0A%20n%20%26%200%20%26%201%20%20%5C%5C%20%0A%5Chline%0A%20%24a%5E0%24%20%26%200%20%26%200%20%20%5C%5C%20%0A%20%24a%5E1%24%20%26%200%20%26%201%20%20%5C%5C%20%0A%20%24a%5E2%24%20%26%200%20%26%202%20%20%5C%5C%20%0A%20%24a%5E3%24%20%26%201%20%26%201%20%20%5C%5C%0A%20%24a%5E4%24%20%26%201%20%26%202%20%20%5C%5C%20%0A%20%24a%5E5%24%20%26%202%20%26%202%20%20%5C%5C%20%0A%5Cend%7Btabular%7D%0A%5Cend%7Bcenter%7D" alt="
\begin{center}
\begin{tabular}{ c|c c } 
 n &amp; 0 &amp; 1  \\ 
\hline
 $a^0$ &amp; 0 &amp; 0  \\ 
 $a^1$ &amp; 0 &amp; 1  \\ 
 $a^2$ &amp; 0 &amp; 2  \\ 
 $a^3$ &amp; 1 &amp; 1  \\
 $a^4$ &amp; 1 &amp; 2  \\ 
 $a^5$ &amp; 2 &amp; 2  \\ 
\end{tabular}
\end{center}" />
</center>
its Hasse diagram is

![[Pasted image 20231010191106.png]]

and, if we draw all the chains expresively, then we get

![[Pasted image 20231010193018.png]]

If we draw the diagram of the $Za$'s then the resoult is trivial since $Z$ is an isomorphism on $\mathcal{O}_t$ for each $t$. 

So, instead considering $\mathcal{O}_t$, we are interested in some nonempty $S\subset {[t+1]}^{[t]}$. 
Since $S$ is finite, we can define two different $Z$ on it. One of each is to compute the $Z$-dual of each __increasing closure__ (the lest order-preserving map that is larger than or equal to it), another is to follow the usual method. $Z$ may not admit enough good propertis in the first case, and would be an endomorphism in the second case. Before this, we consider a nonempty subset of $\mathcal{O}_t$.  

---
23.10.26

To count the number of order-preserving maps in the lattice ${[t+1]}^{[t]}$, notice that $ZZ(x)=x$ iff $x$ is order-preserving. So that it's given by the following formula
$$
\sum_{x\in{[t+1]}^{[t]}}\mathbb{I}\left(ZZ(x),x\right)
$$
where $\mathbb{I}(x,y)=1$ if $x=y$; and $=0$ if not. For any principal ideal $\downarrow\{a\}$ of ${[t+1]}^{[t]}$, denoted by $\pi_{\mathrm{od}}(a)$ the number of order-preserving maps in ${[t+1]}^{[t]}$ that are less than or equal to $a$; and denoted by $p_{\mathrm{od}}(n)$ the $n$th order-preserving map. By definition,
$$
\begin{align}
\pi_{\mathrm{od}}(a)&=\sum_{i\in[{(t+1)}^t]}\zeta(p_{\mathrm{od}}(i),a)\\
&=Z(p_{\mathrm{od}})(a)
\end{align}
$$
for all $a\in{[t+1]}^{[t]}$. (For some specific order, here may be the lexicographic order) We have 
$$
p_{\mathrm{od}}(n)=Z(\pi_{\mathrm{od}})(n).
$$

The only problem here is to prove that $Z$ is also an involution. A question naturally arises: under which conditions a lattice or poset could have $Z$-transform? 

For any nonempty subset $A$ of $\mathbb{N}$, let $\chi_A$ be its index function, $\pi_A(n)$ be the number of elements in $A$ that are less than or equal to $n$, and $a(n)$ be the $n$th element of $A$. Then
$$
\begin{align}
\pi_A(n)&=\sum_{i\in[n]}\chi_A(i)\\
&=\sum_{i\in[n]}\zeta(a(i),n)\\
&=Z(a)(n),
\end{align}
$$
thus
$$
a(n)=Z(\pi_A)(n).
$$

__Example__  Denoting by $\pi(n)$ the prime counting function while let $p_n$ be the $n$th prime. Wilson's theorem said that $(n-1)!+1\equiv 0 \bmod n$ iff $n$ is a prime or $n=1$. It's easy to show that the correspond characteristic function $\chi(n)$ can be expressed by
$$
\chi(n)=\left\lfloor\cos^2\pi\frac{(n-1)!+1}{n}\right\rfloor
-\left\lfloor\frac{1}{n}\right\rfloor,
$$
thus
$$
\pi(n)=-1+\sum_{i=1}^{n}\left\lfloor\cos^2\pi\frac{(i-1)!+1}{i}\right\rfloor.
$$
C. P. Willans (Dec, 1964) showed that for $(x,y)\in\mathbb{N}\times\mathbb{N}_+$, the zeta function can be given by
$$
\zeta(x,y)=\left\lfloor\sqrt[y]{\frac{y}{1+x}}\right\rfloor.
$$
We have
$$
p_n=1+\sum_{i=1}^{2^n}\left\lfloor
\sqrt[n]{n}{\left(\sum_{j=1}^{i}\left\lfloor\cos^2\pi\frac{(j-1)!+1}{j}\right\rfloor\right)}^{-\frac{1}{n}}
\right\rfloor
$$
since $p_n\leq 2^n$ for all $n\in\mathbb{N}_+$.