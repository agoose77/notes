# Cramer's Rule
Consider a system of linear equations 
$$
\begin{aligned}
a_1x+b_1y+c_1z &= d_1\\
a_2x+b_2y+c_2z &= d_2\\
a_3x+b_3x+c_3z &= d_3
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
x \\ y \\ z
\end{bmatrix}
=
\begin{bmatrix}
d_1 \\ d_2 \\ d_3
\end{bmatrix}\,.
$$

We may write the determinant of the coefficients matrix $D$ as 
$$
D=\begin{vmatrix}
a_1 & b_1 & c_1 \\
a_2 & b_2 & c_2 \\
a_3 & b_3 & c_3
\end{vmatrix}\,.
$$

From the properties of the determinant, 
$$
xD=\begin{vmatrix}
a_1x & b_1 & c_1 \\
a_2x & b_2 & c_2 \\
a_3x & b_3 & c_3
\end{vmatrix}=\begin{vmatrix}
a_1x+b_1y+c_1z & b_1 & c_1 \\
a_2x+b_2y+c_2z & b_2 & c_2 \\
a_3x+b_3y+c_3z & b_3 & c_3
\end{vmatrix}=\begin{vmatrix}
d_1 & b_1 & c_1 \\
d_2 & b_2 & c_2 \\
d_3 & b_3 & c_3
\end{vmatrix}\,.
$$