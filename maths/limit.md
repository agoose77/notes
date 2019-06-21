Limit
=====
Suppose that $M\subseteq A$ and $N\subseteq B$ are [subsets](set.md) of [metric spaces](https://en.wikipedia.org/wiki/Metric_space). The limit $L$ of a function $f\colon M\rightarrow N$ as $x$ *approaches* $p$ is written as 
$$
\lim_{x\rightarrow p}f(x) = L\,,
$$
if the following holds:
$$
\forall\,\epsilon>0,\exists\,\delta > 0 : \forall\,x , d_A(x,p) < \delta \implies d_B(f(x),L) < \epsilon \,,
$$
where $d_V(x,y)$ is the distance function on the metric space $V$.

Known as the $(\epsilon,\delta)$ definition of the limit, this definition *does not require* that $f$ be defined at $p$, nor on its value at $p$ if it is defined.
<!-- If we don't specify a one-sided limit x\rightarrow p^+, then by the definition above |x-p| we will have the (two-sided) limit of f at p. -->

One-Sided Limits
----------------
One may approach $p$ from above ($x>p$) denoted by $x\rightarrow p^+$, or below ($x<p$) denoted by $x\rightarrow p^-$. If both of these one-sided limits exist and are equal, then they are called **the limit of $f(x)$ at $p$**. Otherwise, the limit *does not exist*. 

Limits at Infinity
------------------
The limit of $f(x)$ as $x$ approaches infinity is denoted by
$$
\lim_{x\rightarrow\infty}f(x)=L\,,
$$
which requires that
$$
\forall\,\epsilon>0,\exists\,c:\forall\,x>c,\abs{f(x)-L}<\epsilon\,.
$$
Similarly, for the limit of $f(x)$ as $x$ approaches negative infinity, 
$$
\lim_{x\rightarrow-\infty}f(x)=L\,,
$$
it is necessary that
$$
\forall\,\epsilon>0,\exists\,c:\forall\,x<c,\abs{f(x)-L}<\epsilon\,.
$$

Continuity
----------
A function $f$ is said to be continuous at $c$ if 
* It is defined at $c$ 
* Its value at $c$ equals the (two sided[^implied]) limit of $f$ as $x$ approaches $c$, i.e.

$$
\lim_{x\rightarrow c} f(x) = f(c)\,.
$$
There are several types of discontinuity which do not satisfy these conditions:

![Types of discontinuity](https://schoolbag.info/mathematics/ap_calculus/ap_calculus.files/image262.jpg)


Properties
----------
Limits of complex or real valued functions have the following properties:[^proofs]
$$
\begin{aligned} \lim _{x \rightarrow p}(f(x)\pm g(x)) &=\lim _{x \rightarrow p} f(x)\pm\lim _{x \rightarrow p} g(x) \\ 
\lim _{x \rightarrow p} (f(x) \cdot g(x))&=\lim _{x \rightarrow p} f(x) \cdot \lim _{x \rightarrow p} g(x) \\ 
\lim _{x \rightarrow p}(f(x) / g(x)) &=\lim _{x \rightarrow p} f(x) / \lim _{x \rightarrow p} g(x) \end{aligned}
$$
[^proofs]: http://tutorial.math.lamar.edu/Classes/CalcI/LimitProofs.aspx#Extras_Limit_LimitProp
[^implied]: this is implied by the statement
    > as $x$ approaches $c$.

<!-- TODO mention squeeze theorem -->