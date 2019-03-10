Wronskian
=========
The Wronskian for a series of differentiable functions $f_1,\,f_2,\,\dots,\,f_n$ which are $n-1$ times differentiable on an interval $I$ is defined as
$$
\tag{a}
\operatorname{W}\left[f_1,f_2,\dots,f_n\right] = 
\begin{vmatrix} 
    f_1 & f_2 & \dots & f_n\\
    f_1^{(1)} & f_2^{(1)} & \dots & f_n^{(1)}\\
    \vdots & \vdots & \ddots & \vdots\\
    f_1^{(n-1)} & f_2^{(n-1)} & \dots & f_n^{(n-1)}\\
\end{vmatrix}\,.
$$

Properties
----------
1. If $\operatorname{W}[f,g](x)\neq 0$ for $x\in I$, then $f,g$ are linearly independent on I.
1. If $f,g$ are linearly _dependent_ on I, then $\operatorname{W}[f,g](x)= 0\,\forall\, x\in I$.

Relation to Vectors of Functions
--------------------------------
The set of functions $\{\, \vec{g_1}(t),\,\vec{g_2}(t),\,\dots,\,\vec{g_n}(t)\,\}$, where $\vec{g}_i(t):\mathbb{R}\mapsto\mathbb{R}^3$, is _linearly dependent_ on $I$ if there exists $\{\,c_i\in \mathbb{R}\,\}$ not all zero such that
$$
c_1\vec{g_1}(t) + c_2\vec{g_2}(t) + \dots + c_n\vec{g_n}(t) =0 \,\forall\,t\in I\,.
$$
In matrix form, this may be written as 
$$
\tag{b}
\begin{bmatrix}
    g_{11}(t) & g_{12}(t) & \dots & g_{1n}(t)\\
    g_{21}(t) & g_{22}(t) & \dots & g_{2n}(t)\\
    \vdots & \vdots & \ddots & \vdots\\
    g_{n1}(t) & g_{n2}(t) & \dots & g_{nn}(t)\\
\end{bmatrix}
\begin{bmatrix}
c_1\\
c_2\\
\vdots\\
c_n
\end{bmatrix}=
\vec{0}\,\forall\, t\in I\,,
$$
or
$$
G(t)\vec{x}=\vec{0}\,\forall\, t\in I\,.
$$
From linear algebra, if the columns $\vec{g}_i$ of $G(t)$ are linearly dependent on $I$, then it follows from the [properties of the determinant that](linear-algebra/matrix-determinant-properties.md#Linear-Dependence) $\lvert G(t)\rvert=0\,\forall\,t\in I$. 

---
Now consider a set of real valued functions $\{\,f_1,\,f_2,\,\dots,\,f_n\,\}$. They are linearly _dependent_ on $I$ if
$$
    \tag{c}
    c_1f_1(t) + c_2f_2(t) + \dots + c_nf_n(t) =0 \,\forall\,t\in I\,,
$$
for $\{\,c_i\in \mathbb{R}\,\}$ not all zero.

If we repeatedly differentiate **(c)**, we find
$$
\begin{aligned}
    c_1f_1^{(1)}(t) + c_2f_2^{(1)}(t) + \dots + c_nf_n^{(1)}(t) &= 0 \\
    c_1f_1^{(2)}(t) + c_2f_2^{(2)}(t) + \dots + c_nf_n^{(2)}(t) &= 0 \\
    &\;\;\vdots\\
    c_1f_1^{(n-1)}(t) + c_2f_2^{(n-1)}(t) + \dots + c_nf_n^{(n-1)}(t) &= 0\,,
\end{aligned}
$$

which may also be written in the same matrix form as **(b)**
$$
\begin{bmatrix}
    f_1(t) & f_2(t) & \dots & f_n(t)\\
    f_1^{(1)}(t) & f_2^{(1)}(t) & \dots & f_n^{(1)}(t)\\
    \vdots & \vdots & \ddots & \vdots\\
    f_1^{(n-1)}(t) & f_2^{(n-1)}(t) & \dots & f_n^{(n-1)}(t)\\
\end{bmatrix}
\begin{bmatrix}
c_1\\
c_2\\
\vdots\\
c_n
\end{bmatrix}=
\vec{0}\,\forall\, t\in I\,,
$$

and we consider the linear independence of vectors 
$$
    \vec{f_i} = \begin{bmatrix}f_i\\f_i^{(1)}\\\vdots\\f_i^{(n-1)}\end{bmatrix}\,.
$$
Hence, from **(b)** it follows that the Wronskian in **(a)** is just a specific case of the linear independence of vector valued functions.