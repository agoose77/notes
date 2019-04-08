Variation of Parameters
=======================
Recall that the complementary function for some _non homogeneous_ linear ODE of second order is  $y_c = c_1y_1 + c_2y_2$ , where $y_1,\,y_2$ are linearly independent solutions of the associated _homogeneous_ equation. For a linear ODE, the [general solution](n-order-inhomogeneous-general-solution.md) is given by $y=y_c+y_p$, which reduces to $y_c$ for the homogeneous linear ODE where $y_p=0$.

For the nonhomogeneous linear ODE 
$$
    \tag{a}
    s(t)y^{\prime\prime}(t) + y'(t) p(t) + q(t)y(t) = g(t)\,,
$$
let us define 
$$
    \tag{b}
    y_p = u_1y_1 + u_2y_2\,.
$$
Taking the derivative of **(b)**, 
$$
    {y_p}' = u_1{y_1}' + {u_1}' y_1 + u_2{y_2}' + {u_2}' y_2\,,
$$
we assume that 
$$
    \tag{c}
    {u_1}' y_1 + {u_2}' y_2 = 0\,,
$$ such that
$$
\begin{aligned}
    {y_p}' &= u_1{y_1}' + u_2{y_2}'\\
    y_p^{\prime\prime} &= u_1y^{\prime\prime} + {u_1}'{y_1}' + u_2y_2^{\prime\prime} + {u_2}'{y_2}'\,.
\end{aligned}
$$
**(a)** may then be rewritten as 
$$
    s\Big(u_1y^{\prime\prime} + {u_1}'{y_1}' + u_2y_2^{\prime\prime} + {u_2}'{y_2}'\Big) + 
    p\Big(u_1{y_1}' + u_2{y_2}'\Big) + 
    q\Big(u_1y_1 + u_2y_2\Big) = g\,.
$$

Grouping terms in $u_1$, $u_2$,
$$
    \tag{d}
    s\Big({u_1}'{y_1}' + {u_2}'{y_2}'\Big) + 
    u_1\Big(s{y_1}^{\prime\prime} + p{y_1}' + qy_1\Big) + 
    u_1\Big(s{y_1}^{\prime\prime} + p{y_1}' + qy_1\Big) = g\,.
$$

As $y_1,\,y_2$ are solutions to the _homogeneous_ equation, it follows that **(d)** reduces to
$$
    {u_1}'{y_1}' + {u_2}'{y_2}'  = \frac{g}{s}\,.
$$

Let us now _redefine_ $p, q, g$ such that $s$ is divided out,
$$
    \tag{d}
    {u_1}'{y_1}' + {u_2}'{y_2}'  = g\,.
$$

From **(c\)**, ${u_1}'=\frac{-{u_2}'}{y_1}y_2$, hence **(d)** becomes
$$
\begin{aligned}
    -\frac{{u_2}'}{y_1}y_2{y_1}' + {u_2}'{y_2}' &= g(t)\\
    {u_2}' \left({y_2}'-\frac{y_2}{y_1}{y_1}'\right) &= g(t)\\
    {u_2}' \left(\frac{{y_2}' y_1-y_2{y_1}'}{y_1}\right) &= g(t)\,,
\end{aligned}
$$
Solving for ${u_1}'$ and ${u_2}'$, we find
$$
\begin{aligned}
    {u_2}' &= \frac{g(t)y_1}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,\\
    {u_1}' &= -\frac{g(t)y_2}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,.
\end{aligned}
$$

<!-- TODO: fix this hyperlink -->
Given that $y_1$ and $y_2$ form a fundamental set of solutions, it can be shown that $\operatorname W\mathopen{}\big[y_1,y_2\big]\mathclose{}$ is not zero (see [Non Vanishing Wronskian For Solutions to Non-Singular Second Order ODEs](#Non%20Vanishing%20Wronskian%20For%20Solutions%20to%20Non-Singular%20Second%20Order%20ODEs)).

Finally, taking the integral of both sides,
$$
\begin{aligned}
    u_2 &= \int\frac{g(t)y_1}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,\mathrm{d}t\,\\
    u_1 &= -\int\frac{g(t)y_2}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,\mathrm{d}t\,.
\end{aligned}
$$

We can then form the particular solution from **(b)** as
$$
y_p(t) = -y_1\int\frac{g(t)y_2}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,\mathrm{d}t + 
y_2\int\frac{g(t)y_1}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,\mathrm{d}t\,.
$$

<!--Given that $y_1,\,y_2$ form a _fundamental set of solutions_, it follows from [Abel's theorem](abels-theorem.md) that $\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}$ is exclusively either zero or non-zero for _all_ $t \in I$.-->

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">

#### Non Vanishing Wronskian For Solutions to Non-Singular Second Order ODEs
Suppose that $f$ and $g$ are linearly dependent differentiable functions on some interval $I$. Then there exist two non-zero constants $c$ and $d$ which satisfy the _two_ linear equations
$$
\begin{array}{cc}
cf(x)+dg(x) = 0\,, & cf'(x)+dg'(x)=0\,,
\end{array}
$$
identically on $I$. It then follows that the matrix of equations 
$
\begin{bmatrix}
f & g\\
f' & g'
\end{bmatrix}
$
is not invertible, and hence $\operatorname W\mathopen{}\big[f,g\big]\mathclose{}(x)=0\,\forall\,x\in I$. 
    
There is a strong converse of this lemma when $f$ and $g$ are solutions to a second order linear DE. Let $f$ and $g$ be solutions to the DE
$$
    \tag{e}
    u^{\prime\prime} + p(x)u' + q(x)u = 0\,.
$$
Suppose that the Wronskian $\operatorname W\mathopen{}\big[f,g\big]\mathclose{}(x)$ vanished at some point $x_1$. Then the system of linear equations represented by $\operatorname W$ would have a non-trivial solution, i.e. the vectors $\begin{bmatrix}f(x_1)&f'(x_1)\\\end{bmatrix}$ and $\begin{bmatrix}g(x_1)&g'(x_1)\\\end{bmatrix}$ would be linearly dependent (for $x=x_1$), with $g(x_1)=kf(x_1)$ and $g'(x_1)=kf'(x_1)$ for some constant $k$. Now consider the function $h(x)=g(x)-kf(x)$. As a linear combination of solutions, this function is also a solution to **(e)**. By [the uniqueness theorem](n-order-existence-theorem.md), there can only be _one_ solution to **(e)** with initial conditions $u(x_1)=u_1$, $u'(x_1)={u'}_1$. It then follows that, as $f$ and $kg$ satisfy the same initial conditions, $f(x)=kg(x)\,\forall\,x\in I$, and hence $u(x)$ _vanishes_ on $I$. 
    
This result concludes that if $\operatorname W\mathopen{}\big[f,g\big]\mathclose{}(x)=0$ for _any_ $x\in I$, then $f$ and $g$ _must_ be linearly dependent on $I$. If, therefore, $f$ and $g$ are linearly _independent_ on $I$, then it follows that $\operatorname W\mathopen{}\big[f,g\big]\mathclose{}(x)\neq0\,\forall\,x\in I$.
<!-- Future note to self 
That f, g are linearly dependent given W[f,g](x_i)=0 is only valid for x_i, and is implied by writing the matrix representation of a linear combination of f, g, f', g'. This matrix is non-invertible from the result that W=0, and hence there are nontrivial solutions c, d that imply linear dependence (for x=x_i). We then extend this linear dependence 
-->
</div>

<!-- Can the Wronskian be nonzero for linearly _depedendent_ fns? -->