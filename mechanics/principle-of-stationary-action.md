The Principle of Stationary Action
==================================

<!-- TODO generalise to many coordinates. -->

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
  
### Action
The time integral (functional) of the Lagrangian $\mathcal{L}$ of a system between times $t_1$ and $t_2$.
$$
    \tag{b}
    \mathcal{S}[\vec{q}(t), t_1, t_2]=\int^{t_2}_{t_1}\mathcal{L}\left(\vec{q}(t), \dot{\vec{q}}(t), t\right)\,\mathrm{d}{t}\,,
$$
where $\vec{q}$ are the N generalised coordinates which define the configuration of the system.
</div>

The Principle of Stationary (Least) Action states that $\delta \mathcal{S}=0$, [that is](https://en.wikipedia.org/wiki/Principle_of_least_action#cite_note-penrose-18):

>The path taken by the system between times $t_1$ and $t_2$ and configurations $x_1$ and $x_2$ is the one for which the action is stationary (no change) to first order

## Euler-Lagrange Equation
### Theorem
If the function $x(t)$ yields a stationary value of $\mathcal{S}$, then 
$$
\tag{c}
\frac{\partial\mathcal{L}}{\partial x}=\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial\mathcal{L}}{\partial\dot{x}}\right)\,.
$$

### Proof
Consider a system whose Lagrangian is defined by $\mathcal{L}(x, \dot{x}, t)$.
The Principle of Stationary Action states that the equations of motion for some system are those for which the action is _stationary to first order_.
Let us define the _true path_ taken by a particle in a 1D system as $x(t)$ where $t_1\leq t \leq t_2$. We can subsequently define a deviated path with the same end-points as
$$
  x^\prime(t)=x(t)+a\eta(t)\,,
$$
with $\eta(t)$ such that $\eta(t_1)=\eta(t_2)=0$.

From the Principle of Stationary Action, there must be no change in $\mathcal{S^\prime}$ to first order in $a$. Using the chain rule, we find that 
$$
\tag{a}
  \frac{\partial \mathcal{S}^\prime}{\partial a}=\int^{t_2}_{t_1}\left[\frac{\partial \mathcal{L}}{\partial x^\prime}\frac{\partial x^\prime}{\partial a}+\frac{\partial \mathcal{L}}{\partial \dot{x^\prime}}\frac{\partial \dot{x^\prime}}{\partial a}\right]\,\mathrm{d}t
  =\int^{t_2}_{t_1}\left[\frac{\partial\mathcal{L}}{\partial x^\prime}\eta(t)+\frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\dot{\eta}(t)\right]\,\mathrm{d}t\,.
$$

By parts, **(a)** becomes
$$
\int{\frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\dot{\eta}(t) \,\mathrm{d}{t}}= \frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\eta(t)-\int{\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\right)\eta(t)\,\mathrm{d}{t}}\,,
$$

hence
$$
\frac{\partial\mathcal{S}^\prime}{\partial a}=\int^{t_2}_{t_1}{\left(\frac{\partial\mathcal{L}}{\partial x^\prime}-\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\right)\right)\eta(t)\,\mathrm{d}{t}}+ \frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\eta(t)\Big|_{t_1}^{t_2}\,.
$$

Given that $\eta(t_2)=\eta(t_1)=0$,
$$
\frac{\partial \mathcal{S}^\prime}{\partial a}=\int^{t_2}_{t_1}{\left(\frac{\partial\mathcal{L}}{\partial x^\prime}-\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial\mathcal{L}}{\partial\dot{x^\prime}}\right)\right)\eta(t)\,\mathrm{d}{t}}\,.
$$

As we assume that $x(t)$ yields a stationary value, $\frac{\partial \mathcal{S}^\prime}{\partial a}\Big|_{a=0}$ must be zero for _any_ perturbation $\eta(t)$, hence, it follows that the term in parentheses must be zero. 

Thus we derive the Euler-Lagrange equation _for the true path $x(t)$_ (where $x^\prime=x$)
$$
\tag{c}
\frac{\partial\mathcal{L}}{\partial x}=\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\partial\mathcal{L}}{\partial\dot{x}}\right)\,.
$$

### Example
For the simple 1D system of a free particle under gravity, let $\mathcal{L}=\frac{m\dot{x^\prime}^2}{2}-mgx^\prime$. Then **(c)** gives $$
ma = -mg
$$
as expected.
<!-- \mathcal{S}(x)=\mathcal{S}(x^\prime)- -->

## Useful Links
* http://www.people.fas.harvard.edu/~djmorin/chap6.pdf
* http://www.feynmanlectures.caltech.edu/II_19.html