Tensors
=======
To summarise tensors in a simple paragraph[^1]:
> Simply put, a tensor is a mathematical construction that “eats” a bunch of vectors, and “spits out” a scalar.
The central principle of tensor analysis lies in the simple, almost trivial fact that scalars are unaffected by
coordinate transformations. From this trivial fact, one may obtain the main result of tensor analysis: an
equation written in tensor form is valid in any coordinate system.

Covariant and Contravariant Vectors
-----------------------------------
Consider a change of basis transformation, where the basis vectors $\set{\vb{b}_i}$ transform to the new basis $\set{\vb{b}_i'}=\set{2\vb{b}_i}$. Clearly, our basis vectors have doubled in length. Now consider a *coordinate vector*. For a point given by
$$
\vb{v} = \sum_i v^{i} \vb{b}_i\,,
$$
it follows that in the new basis, the same point is 
$$
\begin{aligned}
\vb{v} 
&= \sum_i v^{i\,'} \vb{b}_i'\\
&= \sum_i v^{i\,'} 2\vb{b}_i\,,
\end{aligned}
$$
which implies that $v^{i\,'}=\frac{1}{2}v^{i}$ i.e. the coordinate vectors transform inversely to the basis vectors. Vectors which transform like the basis (covariant) are called *co-vectors*, whilst those which transform like coordinates (contravariant) remain *vectors*.

The gradient $\grad f(\vb{v})$ of a function $f$ is a co-vector, as 
$$
\grad f = \pdv{f}{x}\vu{x}+\pdv{f}{y}\vu{y}+\pdv{f}{z}\vu{z}\,.
$$
If the $\vu{x}$ basis vector doubles, $\partial x$ halves, and thus $\pdv{f}{x}$ doubles, like the basis.


Index Notation
--------------
Unlike other formalisms, in tensor index notation, **coordinate indices are given by superscripts**, e.g.
$$
\begin{aligned}
v^1 &= v_x\\
v^2 &= v_y\\
v^2 &= v_z \,.
\end{aligned}
$$

Superscript indices are referred to as *raised indices*, whilst subscript indices are *lowered*.

$\gdef\tens#1#2{{}^{#1}_{\,#2}}$

Matrices are written as $M^i_j$, e.g. the [eigenvalue equation](eigenvectors-and-eigenvalues.md):
$$
\sum_{j}M\tens{i}{j}v^j=\lambda_iv^i\,,
$$
explicitly, *they have a raised-lowered index pair*.

The identity matrix in index notation is simply given by the Kronecker delta 
$$
\delta^i_j=\begin{cases}1 & \text{if } i=j\,,\\
0 & \text{else }\end{cases}\,.
$$

Einstein summation convention (E.S.C) states that wherever an expression in indexed form is written, it is implied that it is a sum over the common index. For example, 
$$
M\tens{i}{j}v_j \equiv \sum_j M\tens{i}{j}v_j\,.
$$
One can define the index pairs which are not summed over by underlining the subscripts
$$
M\tens{i}{\underline{j}}v_j \equiv M\tens{i}{\underline{j}}v_j\,.
$$

This notation is *unambiguous*, for performing a tensor calculation, the indices over which the sum is performed are always defined in a pair, one raised and one lowered. Expressions which do not satisfy this requirement, or repeat an index more than once, are malformed.

Contravariant (Tangent) Vectors
-------------------------------
<!-- TODO link directional derivative -->
Given a [manifold](https://en.wikipedia.org/wiki/Manifold) in $\mathbb{R}^N$, with a curve defined by $x^i = x^i(t)$. At every point $x^i$ there exists a [vector space](vector-space.md) (the [*tangent* space](https://en.wikipedia.org/wiki/Tangent_space)) in which an arbitrary vector may be represented. This tangent space varies from point to point. There are several definitions of the tangent space, including [the velocity of curves](https://en.wikipedia.org/wiki/Tangent_space#Definition_as_the_velocity_of_curves) and [derivatives](https://en.wikipedia.org/wiki/Tangent_space#Definition_via_derivations).

Consider the directional derivative $\grad_vf(x^a)\colon M\rightarrow \mathbb{R}$ of a curve $f(x^a)$, where $x^a$ represent Cartesian coordinates on Euclidean space.[^2] Removing the function from the equation, we have in E.S.C[^3]
$$
\tag{1}
\begin{aligned}
    \grad_v = \vu{v}\cdot\grad 
    &= v^i\pdv{}{x^i}\\
    &= v^1\pdv{}{x^1} + v^2\pdv{}{x^2} + v^3\pdv{}{x^3}\,.
\end{aligned}    
$$
If we define $\grad_u$ such that
* $(\grad_u+\grad_v)(f)=\grad_u(f)+\grad_v(f)$
* $(\lambda \grad_u)f = \lambda \grad_u(f)$,

then $\grad_u$ form a vector space according to the axioms. 
Note that earlier we demonstrated that derivatives of scalar functions are *covectors*, rather than classical vectors. Hence, the members of the tangent space are *covectors*.

Evidently, given **(1)**, we can find a basis in this vector space at any point $x'$ as $\pdv{}{x^i}\Big|_{x'}$. If we let 
$$
    v(\cdot) = \vu{v}\cdot\grad\,,
$$
then it follows that
$$
    v(x^i) = \vu{v}\cdot\grad x^i = v^i\,.
$$
A final remark is that the derivative of a scalar function $\phi(x^a(t))$ with respect to $t$ is a vector in this space:
$$
\begin{aligned}
\dv{\phi(x^a(t))}{t} 
&= \dv{x^i}{t}\pdv{\phi}{x^i}\\
&= v^i\pdv{\phi}{x^i}\,,
\end{aligned}
$$
where $\dv{x^i}{t}$ is the tangent vector $v^i$ to the curve $x^i(t)$ by definition.

[^1]: https://web2.ph.utexas.edu/~jcfeng/notes/Tensors_Poor_Man.pdf
[^2]: Note that often indices are implicit in the function arguments, that is $f(x)\equiv f(x^a)$.
[^3]: In E.S.C the index $i$ in a partial derivative $\pdv{}{x^i}$ is treated as though it were a *lowered index*.
[^4]: https://math.stackexchange.com/questions/1588854/use-of-partial-derivatives-as-basis-vector

<!--

A tangent vector can be defined as a *directional derivative*. To support this statement, let us note that
* Directional derivatives may be added together.
* Directional derivatives may be multiplied by scalars.

From these statements, it is clear that directional derivatives form a [vector space](vector-space.md) (given that they satisfy the axioms). Note that earlier we demonstrated that derivatives of scalar functions are *covectors*, rather than classical vectors.

Now, let us c
-->