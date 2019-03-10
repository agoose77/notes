Cramer's Rule
=============

Derivation
----------
Consider a system of linear equations 
$$
\begin{aligned}
a_1x_1+b_1x_2+c_1x_3 &= d_1\\
a_2x_1+b_2x_2+c_2x_3 &= d_2\\
a_3x_1+b_3x_2+c_3x_3 &= d_3
\end{aligned}\,,
$$

which may be expressed in matrix form as
$$
\begin{bmatrix}
a_1 & b_1 & c_1 \\
a_2 & b_2 & c_2 \\
a_3 & b_3 & c_3
\end{bmatrix}
\begin{bmatrix}
x_1 \\ x_2 \\ x_3
\end{bmatrix}
=
\begin{bmatrix}
d_1 \\ d_2 \\ d_3
\end{bmatrix}\,,
$$
or
$$
M\vec{x} = \vec{d}\,.
$$

We may write the determinant $D$ of the coefficients matrix $M$ as 
$$
D=\begin{vmatrix}
a_1 & b_1 & c_1 \\
a_2 & b_2 & c_2 \\
a_3 & b_3 & c_3
\end{vmatrix}\,.
$$

From the properties of the determinant, 
$$
x_1D=\begin{vmatrix}
a_1x & b_1 & c_1 \\
a_2x & b_2 & c_2 \\
a_3x & b_3 & c_3
\end{vmatrix}=\begin{vmatrix}
a_1x_1+b_1x_2+c_1x_3 & b_1 & c_1 \\
a_2x_1+b_2x_2+c_2x_3 & b_2 & c_2 \\
a_3x_1+b_3x_2+c_3x_3 & b_3 & c_3
\end{vmatrix}=\begin{vmatrix}
d_1 & b_1 & c_1 \\
d_2 & b_2 & c_2 \\
d_3 & b_3 & c_3
\end{vmatrix}\,,
$$
hence $$
    x_1=\frac{\begin{vmatrix}
            d_1 & b_1 & c_1 \\
            d_2 & b_2 & c_2 \\
            d_3 & b_3 & c_3
            \end{vmatrix}}
            {D}\,.
$$

Solutions
---------
For a homogeneous linear equation, $\vec{d}=\vec{0}$, and hence $\vec{x}M=\vec{0}$. If the determinant $D=\lvert M\rvert$ is zero, then the system has non-degenerate solutions, otherwise $\vec{x}=\vec{0}$.  
From of the [Invertible Matrix Theorem](http://mathworld.wolfram.com/InvertibleMatrixTheorem.html), if $M$ is singular (i.e. $M^{-1}$ does not exist, $\lvert M\rvert=0$) then the columns (and rows) are _not linearly independent_, hence we can find solutions $\vec{x}$ such that
$$
\tag{a}
x_1M_{i1} + x_2M_{i2} +x_3M_{i3}=0\,\forall\,i\,.
$$

Conversely, if $\lvert M\rvert\neq 0$, then the columns (and rows) of $M$ _are linearly independent_, and thus only the trivial solution $\vec{x}=\vec{0}$ satisifes **(a)**.