# The Lagrangian

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
  
#### Lagrangian
The difference between the kinetic and potential energies, $T$ and $V$ respectively, of the system, given by 
$$
  \mathcal{L}\equiv T -V\,.
$$

</div>

## Change of coordinates
Consider the set of coordinates
$$
  x_i:(x_1,x_2,\dots,x_N)\,,
$$
where $N$ bounds the number of coordinates to fully describe the system (e.g $N=6$ for two particles in Cartesian $x,y,z$ space). Assuming that the Euler-Lagrange equations hold for these variables,
$$
  \frac{\mathrm{d}}{\mathrm{d}t}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}=\frac{\partial \mathcal{L}}{\partial x_i}\,.
$$
Let us introduce a new set of variables which are a function of the $x_i$ and $t$
$$
    q_i = q_i(x_1,x_2,\dots,x_N;t)\,,
$$
and consider only the case where the $q_i$ do not depend upon the $\dot{x}_i$ (i.e $\frac{\partial q_j}{\partial  \dot{x}_k}=0\,\forall j,k$). One can invert these definitions such that
$$
    x_i = x_i(q_1,q_2,\dots,q_N;t)\,.
$$
We can then show that the Euler-Lagrange relations hold for the new coordinate system.
From the chain rule,
$$
\tag{DIFF}
  \frac{\partial \mathcal{L}}{\partial\dot{q}_m}=\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\frac{\partial \dot{x}_i}{\partial \dot{q}_m}\,.
$$
To find $\frac{\partial \dot{x}_i}{\partial \dot{q}_m}$, we can find the total derivative of $\dot{x_i }$
$$
  \dot{x_i}=\sum^N_{i=1}\frac{\partial x_i}{\partial q_m}\dot{q}_m+\frac{\partial x_i}{\partial t}\,,
$$
which then gives
$$
  \frac{\partial \dot{x}_i}{\partial \dot{q}_m}=\frac{\partial x_i}{\partial q_m}\,.
$$
We cam tjem 
$$
\tag{CRD}
  \begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)=\sum^N_{i=1}\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\right)\frac{\partial x_i}{\partial q_m}+\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)\,.
\end{aligned}
$$

From the [Principle of Stationary Action](principle-of-stationary-action.md#Proof), it follows that **(CRD)** simplifies to
$$
  \begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)&=\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial x_i}\frac{\partial x_i}{\partial q_m}+\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\frac{\partial \dot{x}_i}{\partial q_m}\\
&= \frac{\partial \mathcal{L}}{\partial q_m}\,.
\end{aligned}
$$

## Forces of constraint
Euler-Lagrange equations can be used to solve motion without the need to consider force balances, which in some cases can be complex.
With the use of the Lagrangian, one can introduce constraints from the beginning of the problem in order to reduce the number of variables.
Consider the motion of a particle sliding down the surface of a frictionless hemisphere of radius $R$. By constraining the particle to the surface of the hemisphere, the Lagrangian is as follows:
$$
  \mathcal{L} = \frac{mR^2\dot{\theta}^2}{2}-mgR\cos{\theta}\,.
$$

From the [Euler-Lagrange equation](principle-of-stationary-action.md#Euler-Lagrange-Equation)
$$
  \ddot{\theta} = \frac{g}{R}\sin{\theta}\,.
$$
However, by imposing these constraints at the outset, one cannot then proceed to say anything about the constraining forces. In order to do so, one can define the Lagrangian in terms of a constraining potential $V(r)$,
$$
  \mathcal{L} = \frac{m(\dot{r}^2+r^2\dot{\theta}^2)}{2}-mgr\cos{\theta}-V(r)\,.
$$
The Euler-Lagrange equation then gives
$$
  \begin{aligned}
  mr^2\ddot{\theta}+2mr\dot{r}\dot{\theta} &= mgr\sin{\theta} \\
  m\ddot{r} &= mr\dot{\theta}^2-mg\cos{\theta} - V^\prime(r) \,.
  \end{aligned}
$$

After finding the equations of motion, one can then apply the constraint condition $r=R$ (and hence, $\ddot{r}=\dot{r}=0$):
$$
  \begin{aligned}
  \ddot{\theta} &= \frac{g}{R}\sin{\theta} \\
   \frac{\mathrm{d}}{\mathrm{d}V}{r}\Big|_{r=R} &= mR\dot{\theta}^2-mg\cos{\theta} \,,
  \end{aligned}
$$
which yields the normal constraint force $F_N(\theta, \dot{\theta})=- \frac{\mathrm{d}}{\mathrm{d}V}{r}\Big|_{r=R}$.

## Conservation Laws
Consider the case where the Lagrangian does not depend upon a certain coordinate $q_k$. It then follows that
$$
\begin{aligned}
  \frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial \mathcal{L}}{\partial\dot{q}_k}\right)=\frac{\partial L}{\partial q_k}=0\quad\Longrightarrow \quad\frac{\partial \mathcal{L}}{\partial\dot{q}_k} = C\,,
\end{aligned}
$$
where $C$ is some time independent constant. In this case, $q_k$ is referred to as a _cyclic coordinate_, and $\frac{\partial \mathcal{L}}{\partial\dot{q}_k}$ is a _conserved quantity_.

### Example: momentum conservation in cylindrical coordinates
For example, for some potential which only depends upon distance to the $z$ axis, the Lagrangian is
$$
  \mathcal{L} = \frac{m}{2}(\dot{r}^2+r^2\dot{\theta}^2+\dot{z}^2)-V(r)\,.
$$
The Euler-Lagrange equations give
$$
  \begin{aligned}
    \frac{\partial \mathcal{L}}{\partial\theta}&=\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial \mathcal{L}}{\partial\dot{\theta}}\right)=mr^2\dot{\theta}=I\omega\\
      \frac{\partial \mathcal{L}}{\partial z}&=\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial \mathcal{L}}{\partial\dot{z}}\right)=m\dot{z}=\rho_z\,,
  \end{aligned}
$$
and hence angular momentum is conserved around the $z$ axis, and linear momentum along the $z$ axis.

<!-- TODO ### Energy conservation in cylindrical coordinates -->

## Useful Links
* http://www.people.fas.harvard.edu/~djmorin/chap6.pdf