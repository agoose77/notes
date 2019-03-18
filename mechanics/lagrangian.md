The Lagrangian
==============

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
  
#### Lagrangian
The difference between the kinetic and potential energies, $T$ and $V$ respectively, of the system, given by 
$$
  \mathcal{L}\equiv T -V\,.
$$

</div>

## Change of Coordinates
Consider the set of coordinates
$$
  x_i:(x_1,x_2,\dots,x_N)\,,
$$
where $N$ bounds the number of coordinates to fully describe the system (e.g $N=6$ for two particles in Cartesian $x,y,z$ space). Assuming that the Euler-Lagrange equations hold for these variables,
$$
  \frac{\mathrm{d}}{\mathrm{d}t}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}=\frac{\partial \mathcal{L}}{\partial x_i}\,.
$$
Let us introduce a new set of variables which are functions of $x_i$ and $t$
$$
    q_i = q_i(x_1,x_2,\dots,x_N;t)\,,
$$
and consider only the case where the $q_i$ do not depend upon the $\dot{x}_i$ (i.e $\frac{\partial q_j}{\partial  \dot{x}_k}=0\,\forall \,j,k$). One can invert these definitions such that
$$
    x_i = x_i(q_1,q_2,\dots,q_N;t)\,.
$$
We can then show that the Euler-Lagrange relations hold for the new coordinate system.
From the chain rule,
$$
\tag{a}
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
It follows that 
$$
\tag{b}
  \begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)=\sum^N_{i=1}\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\right)\frac{\partial x_i}{\partial q_m}+\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)\,.
\end{aligned}
$$

From the [Principle of Stationary Action](principle-of-stationary-action.md#Proof), it follows that **(b)** simplifies to
$$
  \begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial x_i}{\partial q_m}\right)&=\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial x_i}\frac{\partial x_i}{\partial q_m}+\sum^N_{i=1}\frac{\partial \mathcal{L}}{\partial\dot{x}_i}\frac{\partial \dot{x}_i}{\partial q_m}\\
&= \frac{\partial \mathcal{L}}{\partial q_m}\,.
\end{aligned}
$$

## Forces of Constraint
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
However, by imposing these constraints at the outset, one cannot then proceed to say anything about the constraining forces. In order to do so, one can instead define the Lagrangian in terms of a constraining potential $V(r)$,
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

### Example: Momentum Conservation in Cylindrical Coordinates
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


## Holonomic Constraints and Degrees of Freedom
Consider a system of N particles in three dimensional space, each with position vector $\vec{r}_i(t)$ for $i=1,\dots,N$. Note that each $\vec{r}_i(t)\in\mathcal{R}^3$ is a 3-vector, hence there are $3N$ coordinates which define the system.
From Newton's second law, the equation of motion for the $i^\text{th}$ particle is
$$
\tag{c}
\dot{\vec{p}}_i = F_i^\text{ext} + F_i^\text{con}\,,
$$
for $i=1,\dots,N$, where $\vec{p}=m_i\vec{v}_i$ is the linear momentum of the $i^\text{th}$ particle and $\vec{v}_i$ its velocity. Here, the net force on the $i^\text{th}$ particle is decomposed into external and constraint components, the former to describe conventional physical forces, the latter to describe some motion constraint (e.g constrained to a surface or wire). In a system of N particles which constitute a rigid body, the distances between particles are rigidly fixed, described by the constraint
$$
\lvert{\vec{r}_i(t)-\vec{r}_j(t)=c_{ij}}\rvert\,,
$$
where $c_{ij}$ is some constant for all $i,j=1,\dots,N$. Such a constraint is said to be _holonomic_.


<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
  
### Holonomic Constraints
A constraint whose function depends only upon the positional coordinates of the system, and time (i.e. of the form $g(\vec{r}_1,\vec{r}_2,\dots,\vec{r}_N,t)=0$), e.g. a pendulum of length $l$
$$
    x^2 + y^2 - l^2 = 0\,.
$$
_Non holonomic constraints_ are those constraints which cannot be written as an equation between coordinates (instead, often an inequality), e.g. a particle trapped inside a spherical shell satisfies
$$
    x^2 + y^2 + z^2 < R^2\,.
$$
</div>

For the $N$ particles there will be $m$ holonomic constraints
$$
g_k(\vec{r}_1,\dots,\vec{r}_N,t)=0
$$
for $k=1,\dots,m$. Though there are $3N$ coordinates which describe the full set of position vectors $\vec{r}_i$, due to the constraints, these are not all independent. There will instead by $3N-m$ _independent_ coordinates. The dimension of this configuration space is called the _number of degrees of freedom_.

For example, consider the above pendulum. Though there are two degrees of freedom ($x$ and $y$) which define a point in 2D space, the length of the pendulum is constant, and hence the number of degrees of freedom is $1$.
### D'Alembert's Principle
Consider a system in which the net work of the constraint forces is zero:
$$
\sum_{i=1}^N\vec{F}_i^\text{con}\cdot\,\mathrm{d}{\vec{r}_i}=0\,.
$$
In such a system, it follows from **(c\ )** that
$$
\sum_{i=1}^N\left(\dot{\vec{p}_i}-\vec{F}_i^{\text{ext}}\right)\cdot{\,\mathrm{d}{\vec{r}_i}}=0\,,
$$
which represents D'Alembert's principle.


<!-- TODO ### Energy conservation in cylindrical coordinates -->

## Useful Links
* http://www.people.fas.harvard.edu/~djmorin/chap6.pdf
* http://www.macs.hw.ac.uk/~simonm/mechanics.pdf