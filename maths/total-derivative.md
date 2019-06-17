# Total Derivative
Consider some function $f(x, y)$. The quantity $\dd{f}$ given by the change in $f$ as $x\rightarrow x+\dd x$ and $y\rightarrow y+\dd y$ is defined as the _total differential_. For some small change $\delta x$ in $x$ and $\delta y$ in $y$, the change in $f$ is given as 
$$
\begin{aligned}
\delta f 
&= f(x+\delta x,y+\delta y)-f(x,y)\\
&= f(x+\delta x,y+\delta y)-f(x+\delta x,y)+f(x+\delta x,y)-f(x,y)\\
\end{aligned}
$$
Recall that 
$$
\pdv{f}{x}=\lim_{\delta x\rightarrow 0}\frac{f(x+\delta x,y)-f(x,y)}{\delta x}\,.
$$
It follows that 
$$
f(x+\delta x,y)-f(x,y) = \pdv{f(x,y)}{x}\delta x + \gamma_{xy}(\delta x)
$$
$$
\begin{aligned}
\delta f 
&= \pdv{f(x+\delta x,y)}{y}\delta y+\epsilon_y(\delta y)\delta y + 
   \pdv{f(x,y)}{y}\delta x+\epsilon_x(\delta x)\delta x\,,
\end{aligned}
$$
where $\epsilon_x(\delta x)$, $\epsilon_y(\delta y)$ are functions which satisfy
$$
\begin{aligned}
\lim_{\delta{x}\rightarrow 0}\epsilon_x &= 0\\
\lim_{\delta{y}\rightarrow 0}\epsilon_y &= 0\,,
\end{aligned}
$$
and hence may be Taylor expanded about $\delta x=0$, $\delta y=0$ respectively.
Similarly, the partial derivatives may be expanded about $\delta x,\delta y=0$ as
$$
\begin{aligned}
\pdv{f(x+\delta x,y)}{y} &= \pdv{f(x,y)}{y} + \mathcal{O}(\delta x)
\end{aligned}
$$