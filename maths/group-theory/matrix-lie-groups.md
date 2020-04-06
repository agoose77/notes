Matrix Lie Groups
=================

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
### General Linear Groups
<!-- Here the semicolon distinguishes variables but is semantically identical to a comma -->
The *general linear group* over the reals $\operatorname{GL}(n;\mathbb{R})$ is the [group](../group-theory/group.md) of all $n\times n$ invertible matrices with real entries. There is similarly the linear operator $\operatorname{GL}(n;\mathbb{C})$ defined over the complex numbers. 
    
The group property under the binary operation of matrix multiplication $(\cdot\times\cdot)$ follows from the [group axioms](../group-theory/group.md#Group-Axioms):
* Matrix multiplication is associative (*associativity*)
* The product $(\mathbf{A}\times \mathbf{B})$ of two invertible matrices $\mathbf{A},\mathbf{B}$ is itself invertible (*closure*)
* There exists an identity matrix $\mathbf{\mathbb{I}}$ (*identity element*)
* There exists an inverse (by definition) for all invertible matrices (*inverse element*)
</div>

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">

### Convergence
A matrix series $\mathbf{A_m}$ is said to converge to some matrix $\mathbf{A}$ if each element $kl$ of $\mathbf{A_m}$ converges to the corresponding element of $\mathbf{A}$, i.e. $(A_m)_{kl}\rightarrow A_{kl} \forall\,kl$.
</div>
    
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
### Matrix Lie Group
<!-- Here the semicolon distinguishes variables but is semantically identical to a comma -->
A matrix Lie group is any subgroup G of $\operatorname{GL}(n;\mathbb{C})$ which satisfies the following:
    
> If $A_m$ is a sequence of matrices in $G$ and $A_m$ converges to some matrix $A$ then either $A\in G$ or $A$ is not invertible.[^hall]
</div>

* The geometric link between a Lie group and its Lie algebra is the fact that the Lie algebra can be viewed as the tangent space to the Lie group at the identity.[^geom]
* There is a map from the tangent space to the Lie group, called the exponential map:
  $$\exp\colon \mathfrak{so}(n) \rightarrow \mathbf{SO}(n)$$
* Hence, as a tangent space the Lie algebra is a *linearisation* of the lie group
  See work on manifolds
$$\mathfrak{so}(n, \mathbb{R})$$

[^geom]: https://www.cis.upenn.edu/~cis610/geombchap14.pdf
[^loyd]: https://www.whitman.edu/documents/Academics/Mathematics/2015/Final%20Project%20-%20Lloyd.pdf
[^hall]: Brian С Hall Lie Groups, Lie Algebras, and Representations An Elementary Introduction
