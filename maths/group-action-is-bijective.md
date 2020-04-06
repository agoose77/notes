Group Action is Bijective
=========================
To prove that the group action $g \rhd x$ is [bijective](map.md#Relations) for every $g \in G$, it suffices to prove that it is both *[injective](map.md#Relations)* and *[surjective](map.md#Relations)*, i.e. $g \rhd x = g \rhd y \iff x = y$ and $g\rhd x = y\,,\forall y$ where $x,\,y \in X$.

Injectivity
-----------
Let $\phi_g(x) = g \rhd x$. Consider the case where $\phi_g(x) = \phi_g(y)$. Taking the action of $g^{-1}$, we have
$$
g^{-1}\rhd \phi_g(x) = g^{-1}\rhd \phi_g(y)\,.
$$
From the compatibility of the group action, we then have 
$$
\begin{aligned}
g^{-1}\rhd g \rhd x &= g^{-1}\rhd g \rhd y\,.\\
\pqty{g^{-1}\circ g} \rhd x &= \pqty{g^{-1}\circ g} \rhd y\\
e \rhd x &= e \rhd y\\
x &= y\,,
\end{aligned}
$$
i.e. if two elements $x,\, y$ of $X$ (the domain) map to the same value then those elements must be equal, proving injectivity.

Surjectivity
------------
Let $y = e \rhd y$. It follows that we may form $e$ from any group element $g$ and its inverse by taking $g \circ g^{-1}$. Under the compatiblity of the group action, we then have
$$
\begin{aligned}
y &= \pqty{g \circ g^{-1}}\rhd y\\
 &= g\rhd g^{-1} \rhd y\\
 &= g\rhd \pqty{g^{-1} \rhd y}\\
 &= g\rhd x\\
 &= \phi_g(x)\,,
\end{aligned}
$$
for $x = \pqty{g^{-1}\rhd y} \in X$. Evidently for each $y \in X$ (the codomain) there exists an $x$ from which it is mapped, that is, $\phi_g$ is surjective.