# Integration By Substitution
Consider a transformation $T:\mathbb{R}^2\rightarrow\mathbb{R}$ which maps from $(u,v)$ to $(x,y)$, where $x=g(u,v),y=h(u,v)$. 

If $S\subseteq \mathbb{R}^2$ is a region in the $uv$ plane, on which $T$ is a one-to-one function, and $R=T(S)$, we might look to find an expression which relates an integral using $xy$ coordinates on $R$ to one using $uv$ coordinates on $S$.

Let us define a small rectangle $L$ in a region of $S$, with vertices $\vec{o},\vec{p},\vec{q}$. Under $T$, the image of $L$ may be approximated (by Taylor expansion to first order) as:

|   Vertex  	|    Coordinate    	|                                                                  Transformation                                                                 	|
|:---------:	|:----------------:	|:-----------------------------------------------------------------------------------------------------------------------------------------------:	|
| $\vec{o}$ 	|      $(u,v)$     	|                                                            $\big(g(u,v),h(u,v)\big)$                                                            	|
| $\vec{p}$ 	|  $(u+\Delta u)$  	|          $\left(g(u,v)+\frac{\partial g}{\partial u}\Big|_{u,v}\Delta u,h(u,v)+\frac{\partial h}{\partial u}\Big|_{u,v}\Delta u\right)$         	|
| $\vec{q}$ 	| $(u,v+\Delta v)$ 	| $\left(g(u,v)+\frac{\partial g}{\partial v}\Big|_{u,v}\Delta v,h(u,v)+\frac{\partial h}{\partial v}\Big|_{u,v}\Delta v\right)$ 	|

If we assume that $T$ is linear, then the image of $L$ under $T$ is a parallelogram with sides $\vec{p}-\vec{o}$, and $\vec{q}-\vec{o}$. We can find its area by calculating the cross product:
$$
\begin{vmatrix}
\vec{i} & \vec{j} & \vec{k}\\
\frac{\partial g}{\partial u}(u,v)\Delta u & \frac{\partial h}{\partial u}(u,v)\Delta u & 0\\
\frac{\partial g}{\partial v}(u,v)\Delta v & \frac{\partial h}{\partial v}(u,v)\Delta v & 0\\
\end{vmatrix} = 
\left(\frac{\partial g}{\partial u}(u,v)\frac{\partial h}{\partial v}(u,v)- \frac{\partial h}{\partial u}(u,v)\frac{\partial g}{\partial v}(u,v)\right)\Delta u \Delta v \vec{k}\,,
$$

whose $\vec{k}$ component is defined as _the Jacobian_ $J_T(u,v)$ of $T$. The Jacobian is defined as
$$
J_T(u_1, \dots, u_n)=
\begin{vmatrix}
    \frac{\partial x_1}{\partial u_1} & \frac{\partial x_2}{\partial u_1} & \dots & \frac{\partial x_n}{\partial u_1}\\
    \frac{\partial x_1}{\partial u_2} & \frac{\partial x_2}{\partial u_2} & \dots & \frac{\partial x_n}{\partial u_2}\\
    \vdots & \vdots & \ddots & \vdots\\
\frac{\partial x_1}{\partial u_n} & \frac{\partial x_2}{\partial u_n} & \dots & \frac{\partial x_n}{\partial u_n}
\end{vmatrix}\,.
$$

Evidently, the region $L$ has area $\Delta u \Delta v$ in $S$, and an area $\lvert J_T(u,v)\rvert \Delta u\Delta v$ in $T(S)$.
Hence, a double integral over $R$
$$
\iint\limits_Rf(x,y)\,\mathrm{d}A=\iint\limits_Rf(x,y)\,\mathrm{d}x\,\mathrm{d}y\,,
$$
can be transformed to an integral over $S$
$$
\iint\limits_Sf(g(u,v),h(u,v))\,\mathrm{d}A=\iint\limits_Sf(g(u,v),h(u,v))\lvert J_T(u,v)\rvert\,\mathrm{d}u\,\mathrm{d}v\,.
$$