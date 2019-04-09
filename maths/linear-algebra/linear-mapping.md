Linear Mapping
==============
A linear mapping is a mapping $V\rightarrow W$ between two [vector spaces](vector-space.md) $V$, $W$ over the same [field](../field.md) $\bm{K}$, that preserves the operations of addition and _scalar_ multiplication. In the special case that $V=W$, the map is called a linear operator.

Axioms
------
| Name                               	| Definition                                     	|
|------------------------------------	|------------------------------------------------	|
| Operation of addition              	| $f(\vec{u}+\vec{v}) = f(\vec{u}) + f(\vec{v})$ 	|
| Operation of scalar multiplication 	| $f(c\vec{u}) = cf(\vec{u})$                    	|

This may equivalently be written as 
$$
    f(c_1\vec{u_1} + c_2\vec{u_2} + \dots + c_n\vec{u_n}) = c_1f(\vec{u_1})+c_2f(\vec{u_2}) + \dots + c_nf(\vec{u_n})\,.
$$

It follows that if $\vec{0}_V$ and $\vec{0}_W$ are the zero elements of $V$ and $W$ respectively, and $\vec{v}\in V$, then 
$$
    f(\vec{0}_V) = f(0\vec{v}) = 0f(\vec{v}) =\vec{0}_W\,.
$$

Linear Functional
-----------------
A linear functional is a linear map from a vector space to its _associated field_, e.g. if $$\operatorname{I}\mathopen{}\big[f\big]\mathclose{}=\int_a^bf(x)\,\mathrm{d}x\,,$$

then $\operatorname{I}: F\rightarrow \mathbb {R}$, where $F$ is a (vector) space of continuous functions.

Properties
----------
### Null Space (Kernel)
The null space $\mathcal{N}(L)$ of a linear map $L:V\rightarrow W$ between two vector spaces $V$ and $W$ is the [set](../set.md) of vectors which lose their identity under $L$, i.e. the vectors which satisfy $L(\vec{v})=\vec{0}$ for $\vec{v}\in V$:
$$
\mathcal{N}(L) = \{\,\vec{v}\in V : L(\vec{v})=\vec{0}\,\}\,.
$$

The null space has several properties:
* It is a subspace of $V$ (a subset of $V$, and a vector space):  
  * If $\vec{v_1},\vec{v_2}\in V$, then $L(\vec{v_1}+\vec{v_2})=L(\vec{v_1})+L(\vec{v_2})=\vec{0}_W\in W$.
  * If $c\in \mathbb{R}$, then $L(c\vec{v_1})=cL(\vec{v_1})=\vec{0}_W$.
  

### Image 
The image of a linear mapping is the subset of the mapping's codomain to which maps its domain:
$$
L[V] = \{\,w\in W : w=L(v) \,\forall\, v \in V\,\}\,.
$$
$L[V]$ is a subspace of $W$.