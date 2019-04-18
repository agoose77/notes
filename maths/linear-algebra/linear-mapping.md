Linear Mapping
==============
A linear mapping is a mapping $V\rightarrow W$ between two [vector spaces](vector-space.md) $V$, $W$ over the same [field](../field.md) $\bm{K}$, that preserves the operations of addition and _scalar_ multiplication. In the special case that $V=W$, the map is called a linear operator.

Axioms
------
| Name                               	| Definition                                     	|
|------------------------------------	|------------------------------------------------	|
| Operation of addition              	| $f(\vb{u}+\vb{v}) = f(\vb{u}) + f(\vb{v})$ 	|
| Operation of scalar multiplication 	| $f(c\vb{u}) = cf(\vb{u})$                    	|

This may equivalently be written as 
$$
    f(c_1\vb{u_1} + c_2\vb{u_2} + \dots + c_n\vb{u_n}) = c_1f(\vb{u_1})+c_2f(\vb{u_2}) + \dots + c_nf(\vb{u_n})\,.
$$

It follows that if $\vb{0}_V$ and $\vb{0}_W$ are the zero elements of $V$ and $W$ respectively, and $\vb{v}\in V$, then 
$$
    f(\vb{0}_V) = f(0\vb{v}) = 0f(\vb{v}) =\vb{0}_W\,.
$$

Properties
----------
### Null Space (Kernel)
The null space $\mathcal{N}(L)$ of a linear map $L:V\rightarrow W$ between two vector spaces $V$ and $W$ is the [set](../set.md) of vectors which lose their identity under $L$, i.e. the vectors which satisfy $L(\vb{v})=\vb{0}$ for $\vb{v}\in V$:
$$
\mathcal{N}(L) = \set{\vb{v}\in V : L(\vb{v})=\vb{0}}\,.
$$

The null space has several properties:
* It is a subspace of $V$ (a subset of $V$, and a vector space):  
  * If $\vb{v_1},\vb{v_2}\in V$, then $L(\vb{v_1}+\vb{v_2})=L(\vb{v_1})+L(\vb{v_2})=\vb{0}_W\in W$.
  * If $c\in \mathbb{R}$, then $L(c\vb{v_1})=cL(\vb{v_1})=\vb{0}_W$.
  

### Image 
The image of a linear mapping is the subset of the mapping's codomain to which maps its domain:
$$
L[V] = \set{w\in W : w=L(v) \,\forall\, v \in V}\,.
$$
$L[V]$ is a subspace of $W$.


---

Linear Functional
-----------------
A linear functional is a linear map from a vector space to its _associated field_, e.g. if $$\operatorname{I}\mathopen{}\big[f\big]\mathclose{}=\int_a^bf(x)\,\mathrm{d}x\,,$$

then $\operatorname{I}: F\rightarrow \mathbb {R}$, where $F$ is a (vector) space of continuous functions.