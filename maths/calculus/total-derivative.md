# Total Derivative
Consider some function $f(x, y)$. The quantity $\dd{f}$ given by the change in $f$ as $x\rightarrow x+\dd x$ and $y\rightarrow y+\dd y$ is defined as the _total differential_. For some small change $\delta x$ in $x$ and $\delta y$ in $y$, the change in $f$ is given as 
$$
\tag{1}
\begin{aligned}
\delta f 
&= f(x+\delta x,y+\delta y)-f(x,y)\\
&= f(x+\delta x,y+\delta y)-f(x+\delta x,y)+f(x+\delta x,y)-f(x,y)\\
\end{aligned}
$$
Recall that 
$$
\tag{2}
\pdv{f}{x}=\lim_{\delta x\rightarrow 0}\frac{f(x+\delta x,y)-f(x,y)}{\delta x}\,.
$$
From the [definition of the limit](limit.md), we have
$$\abs{x-p}<\delta\implies \abs{f(x)-L} < \epsilon\,,$$ 
for some $\delta$ determined by $\epsilon$. It follows that we can write **(2)** as
$$
f(x+\delta x,y)-f(x,y) = \pdv{f}{x}\delta x + \epsilon'\delta x\,,
$$
<!-- Change inequality to equality:
|x - y| < E becomes x = y ± E ∓ err (0 < err ⩽ E, E > 0)
                      = y ± E(1 - err/E)
                      = y ± E*k, 0 ⩽ k < 1
-->
where $\epsilon'=\pm k\epsilon$ for $k\in[0,1)$. We can therefore rewrite **(1)** as
$$
\tag{3}
\delta f = \pdv{f(x+\delta x,y)}{y}\delta y + \epsilon'_y\delta y+\pdv{f}{x}\delta x + \epsilon'_x\delta x\,.
$$
From **(2)** we can further expand **(3)**
$$
\tag{4}
\begin{aligned}
\delta f &= \pdv{}{y}\left(\pdv{f}{x}\delta x + \epsilon'_x\delta{x}+f(x,y)\right)\delta y + \epsilon'_y\delta y+\pdv{f}{x}\delta x + \epsilon'_x\delta x\\
&= \pdv{f}{y}\delta y+  \left(\pdv{\epsilon'_x}{y} + \pdv{f}{y\partial x}\right)\delta x\delta y + \epsilon'_y\delta y+\pdv{f}{x}\delta x + \epsilon'_x\delta x\,,
\end{aligned}
$$
In the limit, **(4)** becomes
$$
\begin{aligned}
\lim_{\delta_x,\delta_y\rightarrow 0}\delta f = \dd{f}=\pdv{f}{y}\dd{y} + \pdv{f}{x}\dd{x}\,,
\end{aligned}
$$ 
to first order, as $\epsilon'_x$ is *at least* first order in $\delta x$. Hence, the total differential $\dd{f}$ is the sum of the partial differentials $\pdv{f}{x}\dd{x}$.

Chain Rule
----------
Let $x=x(t)$, $y=y(t)$. Dividing **(4)** by the quantity $\delta t$, we have
$$
\frac{\delta f}{\delta t} = \pdv{f}{y}\frac{\delta y}{\delta t} + \pdv{f}{x}\frac{\delta x}{\delta t} + \epsilon'_x\frac{\delta x}{\delta t} + \epsilon'_y\frac{\delta y}{\delta t} + \frac{\delta x\delta y}{\delta t}\epsilon'_{xy}\,.
$$
Taking the limit as $\delta  t\rightarrow 0$, we have $\delta x\rightarrow 0$ and $\delta y\rightarrow 0$, and hence
$$
\dv{f}{t} = \pdv{f}{y}\dv{y}{t} + \pdv{f}{x}\dv{x}{t}\,.
$$
One can extend this approach to many dimensions, which gives the result
$$
\tag{5}
\dv{}{t}f(x_1, x_2, \dots, x_n) = \sum^n_{i=1}\pdv{f}{x_i}\dv{x_i}{t}\,.
$$
This may be used to differentiate functions with indirect dependencies, such as $L(t, x_1(t), x_2(t),\dots,x_n(t))$. From **(5)** it follows that
$$
\begin{aligned}
\dv{L}{t} 
&= \pdv{L}{t} + \sum_{i=1}^n\pdv{L}{x_i}\dv{x_i}{t}\\
&= \left(\pdv{}{t} + \sum_{i=1}^n\dv{x_i}{t}\pdv{}{x_i}\right)L\,.
\end{aligned}
$$

[^oxford-notes]: https://www.robots.ox.ac.uk/~dwm/Courses/1PD_1994/course.pdf