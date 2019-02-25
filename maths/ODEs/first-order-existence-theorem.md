<!-- 65.4 p786 -->
# Existence and Uniqueness Theorem for $n$ Linear First-Order ODEs
## Theorem
Given a system of $n$ linear first order ODEs
$$
\begin{aligned}
\tag{a}
\frac{\mathrm{d}y_1}{\mathrm{d}t}&=f_{11}(t)y_1+f_{12}(t)y_2+\dots+f_{1n}(t)y_n+Q_1(t)\\
\frac{\mathrm{d}y_1}{\mathrm{d}t}&=f_{21}(t)y_1+f_{22}(t)y_2+\dots+f_{2n}(t)y_n+Q_2(t)\\
&\;\;\vdots\\
\frac{\mathrm{d}y_1}{\mathrm{d}t}&=f_{n1}(t)y_1+f_{n2}(t)y_2+\dots+f_{nn}(t)y_n+Q_n(t)\,,
\end{aligned}
$$
where all functions $f_{ij}$ and $Q_i$, $i=1,2,\dots,n$, $j=1,2,\dots,n$ are continuous on a common interval $I$. Then, there is on $I_0\subset I$ ($I$ without its end points) _one and only one_ set of continuous functions $y_1(t),\,y_2(t),\,\dots,\,y_n(t)$ with continuous derivatives, which satisfies the system **(a)** and the initial conditions.
    
## Proof
Let us define 
$$
\begin{aligned}
\tag{b}
f_1(t,y_1,y_2,\dots,y_n) &= f_{11}(t)y_1+f_{12}(t)y_2+\dots+f_{1n}(t)y_n+Q_1(t)\\
f_2(t,y_1,y_2,\dots,y_n) &= f_{21}(t)y_1+f_{22}(t)y_2+\dots+f_{2n}(t)y_n+Q_2(t)\\
&\;\;\vdots\\
f_n(t,y_1,y_2,\dots,y_n) &= f_{n1}(t)y_1+f_{n2}(t)y_2+\dots+f_{nn}(t)y_n+Q_n(t)\,.\\
\end{aligned}
$$
We assume that the interval $I=I^\prime$ is finite and includes its end points. If this is not the case, we take a _finite closed subinterval_ $I^\prime$ of $I$. In $I^\prime$, each function $f_{ij}(t)$ and $Q_i(T)$ is _by hypothesis_ continuous, and hence bounded, in $I^\prime$. Let $N$ be the upper bound of the $f_{ij}(t)$ on $I^\prime$, such that 
$$
    \tag{c}
    \lvert f_{ij}(t)\rvert \leq N \;\forall f_{ij}\,.
$$

Let us consider _two_ sets of values of the dependent variables $\{\,y_i \,\}$
$$
\begin{aligned}
f_i(t, y_1, y_2,\dots,y_n) &= f_{i1}(t)y_1+f_{i2}(t)y_2+\dots+f_{in}(t)y_n+Q_i(t)\\
f_i(t, \overline{y_1}, \overline{y_2},\dots,\overline{y_n}) &= f_{i1}(t)\overline{y_1}+f_{i2}(t)\overline{y_2}+\dots+f_{in}(t)\overline{y_n}+Q_i(t)\,.\\
\end{aligned}
$$
Subtracting the two, we find that 
$$
\lvert f_i(t, y_1, y_2,\dots,y_n) - f_i(t, \overline{y_1}, \overline{y_2},\dots,\overline{y_n})\rvert = \lvert f_{i1}(t)\left(y_1 -\overline{y_1}\right)+f_{i2}(t)\left(y_2 -\overline{y_2}\right)+\dots+f_{in}(t)\left(y_n -\overline{y_n}\right)\rvert \,. 
$$
    
Since $\lvert a + b \rvert \leq \lvert a \vert + \lvert b \rvert$ and $\lvert f_{ij}\rvert \leq N$, 
$$
\lvert f_i(t, y_1, y_2,\dots,y_n) - f_i(t, \overline{y_1}, \overline{y_2},\dots,\overline{y_n})\rvert \leq \lvert f_{i1}(t)\rvert\lvert y_1 -\overline{y_1}\rvert+\lvert f_{i2}(t)\rvert\lvert y_2 -\overline{y_2}\rvert +\dots+\lvert f_{in}(t)\rvert \lvert y_n -\overline{y_n}\rvert \,. 
$$
    
This inequality resembles _Lipschitz continuity_ on $I^\prime$, which in turn implies uniqueness. See [this PDF](existunique.pdf) for more.
   
