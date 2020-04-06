Map
===
A *map* or function is a relation $\phi$ between [sets
](set.md) $X,Y$ which associates each element of $X$ with an element of $Y$.
The map $\phi\colon X \rightarrow Y$ has a domain $X$, codomain $Y$, and range (image) $\phi(X)$. 

Image
-----
The image $\phi(A)$ of $A\subseteq X$ under $\phi$ is the subset of the codomain $Y$ mapped to from $X$ by $\phi$:
$$
\phi(X) = \set{\phi(x) : x \in X}\,.
$$

The image $\phi(X)$ of the domain is the *range*.

Relations
---------
There are several terms used to describe the relations between the domain $X$ and codomain $Y$:

Injective *(one-to-one)*
 ~ A one-to-one mapping such that $\forall\, x\in X$ there is *at most* one element of $Y$ mapped onto by $x$.  
 E.g. $\phi(x)=x^3-x$ is not injective, as $\phi(1) = \phi(-1)$.  
 ![](https://upload.wikimedia.org/wikipedia/commons/thumb/0/02/Injection.svg/200px-Injection.svg.png)
 
Surjective *(onto)*
 ~ A one-to-one mapping such that $\forall\, y\in Y$ there is *at least* one element of $X$ mapped onto $y$.  
 E.g. $\phi=e^x$ is not surjective, as $\nexists x\in X:\phi(x)=-1$.  
 ![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6c/Surjection.svg/200px-Surjection.svg.png)

Bijective *(one-to-one and onto)*
 ~ A map which is both injective and surjective. Also known as *invertible*, i.e. there exists an *inverse map* $\phi^{-1}\colon X\rightarrow Y$ such that $\phi^{-1}(\phi(a)) = a$. A map is invertible iff. it is a bijection.[^invertible.iff]
 ![](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Bijection.svg/200px-Bijection.svg.png)
 
[^invertible.iff]: https://en.wikipedia.org/wiki/Bijection#Inverses