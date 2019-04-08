<!-- 65.3 p783 -->
Existence and Uniqueness Theorem for a Linear ODE of Order $n$
==============================================================
## Theorem
Consider a non-homogeneous linear ODE of the form
$$
   f_n(x)y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=Q(x)\,.
$$
    
Dividing through by $f_n(x)$, and redefining the terms, it follows that
$$
    \tag{a}
     y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=Q(x)\,.
$$
    
If the coefficients $f_0(x),\,f_1(x),\,\dots,\,f_{n-1}(x)$ and $Q(x)$ in the linear ODE **(a)** are continuous functions of $x$ on a common interval $I$, then for each point $x_0\in I$ and for each set of constants $a_0,\,a_1,\,\dots,\,a_{n-1}$ there is one _and only one_ function $y(x)$ that satisfies **(a)** and the initial conditions 
$$
\begin{aligned}
y(x_0)&=a_0\\
y^\prime(x_0)&=a_1\\
&\;\;\vdots\\
y^{(n-1)}(x_0)&=a_{n-1}\,.
\end{aligned}
$$
## Proof
Assume that $y(x)$ is a solution. We may then reduce the ODE to a series of coupled first order ODEs by defining some additional functions $y_1(x),\,y_2(x),\,\dots,\,y_n(x)$:
$$
\begin{aligned}
\tag{b}
y(x) &= y_1(x)\\
y^\prime(x) &= y_1^\prime(x)=y_2(x)\\
y^{\prime\prime}(x) &= y_1^{\prime\prime}(x)=y_2(x)\\
\vdots \\
y^{(n-1)}(x) &= y_1^{(n-1)}(x)=y_2^{(n-2)}(x)=y_n(x)\,.
\end{aligned}
$$

The above relations may be summarised as 
$$
    \tag{c}
    y_n(x) = y_{n-1}^\prime(x)\,
$$ 
and therefore, $y^{(n)}(x) = y_n^\prime(x)$. 
    
With these relations, **(a)** may be rewritten as 
$$
\tag{d}
    y_n^\prime(x) + f_{n-1}(x)y_n(x) + \dots + f_1(x)y_2(x) + f_0(x)y_1(x) = Q(x)\,,
$$
which gives
$$
    y_n^\prime(x) = -f_{n-1}y_n - \dots - f_1y_2 - f_0y_1 = Q\,.
$$
    
Hence, the set of functions $y_1,\,y_2,\,\dots,\,y_n$ satisfies the system of linear first order differential equations
$$
\begin{aligned}
\tag{e}
y_1^{\prime}(x) &= y_2(x)\\
y_2^{\prime}(x) &= y_3(x)\\
&\;\;\vdots\\
y_{n-1}^\prime(x) &= y_n(x)\\
y_n^\prime(x) &= -f_{n-1}(x)y_n(x) - \dots - f_1(x)y_2(x) - f_0(x)y_1(x) = Q(x)\,.
\end{aligned}
$$
    
Using **(b)**, the following set of initial conditions,
$$
\begin{aligned}
    y(x_0) &= a_0 \\
    y^\prime(x_0) &= a_1 \\
&\;\;\vdots\\
    y^{(n-1)}(x_0) &= a_{n-1} \\
\end{aligned}
$$
may be restated as
$$
\begin{aligned}
\tag{f}
    y_1(x_0) &= a_0 \\
    y_2(x_0) &= a_1 \\
&\;\;\vdots\\
    y_n(x_0) &= a_{n-1}\,.
\end{aligned}
$$
___
Here, we have shown that starting with solution $y(x)$ to **(a)**, some additional functions may be defined according to **(b)** which satisfy the first-order ODEs in **(e)**, and the initial conditions in **(f)**.  
    
Conversley, if some functions $y_1,\,y_2,\,\dots,\,y_n$ are solutions to the system **(e)**, satisfying **(f)**, then _$y_1(x)$ satisfies the same constraints that $y(x)$ satisfies_, the final term in **(e)** becomes equivalent to **(a)**, and hence $y_1(x)$ is a solution to **(a)**. It is easy to see that by letting $y(x) = y_1(x)$, as a solution to **(e)** it satisfies **(b)**, **(c\)**, and **(d)**. 
    
Since their derivatives exist, all of $y_1,\,y_2,\,\dots,\,y_n$ are continuous on $I$. By assumption, $f_0,\,f_1,\,\dots,\,f_{n-1}$ are also continuous. Hence, if $I$  is closed, from [the earlier proof for linear first-order ODEs](first-order-existence-theorem.md#Existence-and-Uniqueness-Theorem-for-%24n%24-Linear-First-Order-ODEs) only _and only one_ set of particular solutions $y_1,\,y_2,\,\dots,\,y_n$ exists and satisfies **(e)** and **(f)**. Given that we can let $y(x)=y_1(x)$, it follows that _$y(x)$ exists, and is unique_.