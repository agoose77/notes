# Orbital Angular-Momentum

Classically, the orbital angular-momentum of a single particle is defined as

$$
\tag{a}
\vb{\L}=\vb{\hat{x}}\times\vb{\hat{p}}\,.
$$

Evidently, this operator satisfies the [angular-momentum commutation relations](infinitesimal-rotations.md#Infinitesimal-Rotations-in-Quantum-Mechanics), e.g[^1].

$$
\begin{aligned}
\comm{\L_x}{\L_y}
&= \comm{\y\p_z-\z\p_y}{\z\p_x-\x\p_z} \\
&= \comm{\y\p_z}{\z\p_x-\x\p_z} - \comm{\z\p_y}{\z\p_x-\x\p_z}\\
&= \comm{\y\p_z}{\z\p_x} - \comm{\y\p_z}{\x\p_z} - \comm{\z\p_y}{\z\p_x}
+ \comm{\z\p_y}{\x\p_z}\\
&= \comm{\y\p_z}{\z\p_x} - \p_z\comm{\y}{\x}\p_z - \z\comm{\p_y}{\p_x}\z
+ \comm{\z\p_y}{\x\p_z}\\
&= \comm{\y\p_z}{\z\p_x} + \comm{\z\p_y}{\x\p_z}\\
&= \y\p_x\comm{\p_z}{\z} + \x\p_y\comm{\z}{\p_z}\\
&= i\hbar\left(\x\p_y - \y\p_x\right)= i\hbar\L_z\,,
\end{aligned}
$$

and so on (under cyclical permutation). Hence, $\vb{\L}$ is an angular momentum, which is _defined_ by these commutation relations. Hence, taking the [infinitesimal form of the rotation operator](infinitesimal-rotations.md#Infinitesimal-Rotations-in-Quantum-Mechanics)

$$
1-i\frac{\delta\phi}{\hbar}\L_z\,,
$$

we expect to find that it rotates a position eigenket ket by $\delta\phi$:

$$
\tag{b}
\begin{aligned}
\left[1-i\frac{\delta\phi}{\hbar}\L_z\right]\ket{x',y',z'}
&= \left[1-i\frac{\delta\phi}{\hbar}\x\p_y + i\frac{\delta\phi}{\hbar}\y\p_x\right]\ket{x',y',z'} \\
&= \left[1-i\frac{\delta\phi}{\hbar}\p_y\x + i\frac{\delta\phi}{\hbar}\p_x\y\right]\ket{x',y',z'} \\
&= \left[1-i\frac{\delta\phi}{\hbar}\p_yx' + i\frac{\delta\phi}{\hbar}\p_xy'\right]\ket{x',y',z'} \\
&= \left[1-i\frac{\delta\phi}{\hbar}\vb{\p}\cdot\vb{\delta\mu}\right]\ket{x',y',z'}\\
&= \ket{x'-y'\delta\phi,y'+x'\delta\phi,z'}\,,
\end{aligned}
$$

where $\vb{\delta\mu} = \begin{bmatrix}-y \\ x \\ 0\end{bmatrix}$, and $\left(1-i\frac{\delta\phi}{\hbar}\vb{\p}\cdot\vb{\delta\mu}\right)$ is the [infinitesimal translation operator](infinitesimal-translations.md). Indeed, this new state is a rotated state[^2]. Similarly, for an arbitrary state ket in the position space $\ket{\alpha}$, we observe how the wavefunction behaves under rotation

$$
\begin{aligned}
\tag{c}
\bra{x',y',z'}\left[1-i\frac{\delta\phi}{\hbar}\L_z\right]\ket{\alpha}
&= \left(\left[1+i\frac{\delta\phi}{\hbar}\L_z\right]\ket{x',y',z'}\right)^\dagger\ket{\alpha} \\
&= \ket{x'+y'\delta\phi,y'-x'\delta\phi,z'}^\dagger\ket{\alpha} \\
&= \braket{x'+y'\delta\phi,y'-x'\delta\phi,z'}{\alpha} \,.
\end{aligned}
$$

It is often more convenient to inspect this expression in a different coordinate basis. Following a change of variables 
$$
\ket{x',y',z'}\rightarrow\ket{r',\theta',\phi'}\,,
$$ **(c\)** becomes

$$
\tag{d}
\bra{r,\theta,\phi}\left[1-i\frac{\delta\phi}{\hbar}\L_z\right]\ket{\alpha}
=\braket{r,\theta,\phi-\delta\phi,z'}{\alpha}\,.
$$

Under Taylor expansion, it can be seen that **(d\)** is just

$$
\braket{r,\theta,\phi-\delta\phi,z'}{\alpha} = \braket{r,\theta,\phi,z'}{\alpha} - \delta\phi\pdv{}{\phi}\braket{r,\theta,\phi,z'}{\alpha}\,,
$$

and hence

$$
\tag{e}
\bra{\vb{x}'}\L_z\ket{\alpha} =-i\hbar\pdv{}{\phi}\braket{\vb{x}'}{\alpha}\,.
$$

Let us now consider a rotation about the $\x$ and $\y$ axes. Using the same approach as **(b)** and **(c\)**, we find

$$
\tag{f}
\begin{aligned}
\bra{\vb{x}'}\L_x\ket{\alpha} &=-i \hbar\left(-\sin \phi \pdv{}{\theta}-\cot \theta \cos \phi \pdv{}{\phi}\right)\braket{\vb{x}'}{\alpha}\\
\bra{\vb{x}'}\L_y\ket{\alpha} &=-i \hbar\left(\cos \phi \pdv{}{\theta}-\cot \theta \sin \phi \pdv{}{\phi}\right)\braket{\vb{x}'}{\alpha}\,.
\end{aligned}
$$

Finding $\braket{\vb{x}'}{l,m_l}$
------------

Using the [ladder operators](angular-momentum-ladder-operators.md) $\L_\pm$, we can find $\bra{\vb{x}'}\L_\pm\ket{\alpha}$ from the inner products in **(e)**. Given that the inner product on the Hilbert space is antilinear in the second argument, and $\L_i$ are Hermitian, it follows that

$$
\begin{aligned}
\bra{\vb{x}'}\L_\pm\ket{\alpha}
&= \bra{\vb{x}'}\left(\L_x\pm i\L_y\right)\ket{\alpha}\\
&= \bra{\vb{x}'}\L_x\ket{\alpha}\pm i\L_y\bra{\vb{x}'}\L_y\ket{\alpha}\\
&= -i \hbar e^{ \pm i \phi}\left( \pm i \pdv{}{\theta}-\cot \theta \pdv{}{\phi}\right)\,.
\end{aligned}
$$

We can express $\L^2$ in terms of these ladder operators[^3]
$$
\L^2 
= \frac{1}{2}\left(\L_+\L_+^\dagger + \L_-\L_-^\dagger\right) + \L_z^2\,,
$$
which enables us to find $\bra{\vb{x}'}\L^2\ket{\alpha}$:
$$
\tag{g}
\bra{\vb{x}'}\L^2\ket{\alpha} = -\hbar^2\left[\frac{1}{\sin^2\theta}\pdv{{}^2}{\phi^2}+\frac{1}{\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{}{\theta}\right)\right]\braket{\vb{x}'}{\alpha}\,.
$$
If we take a simultaneous eigenket from the angular-momentum representation $\L^2$ and $\L_z$, we have the following inner products
$$
\begin{aligned}
\bra{\vb{x}'}\L_z\ket{l,m_l} &= m_l\hbar\braket{\vb{x}'}{l,m_l}\\
\bra{\vb{x}'}\L^2\ket{l,m_l} &= l(l+1)\hbar^2\braket{\vb{x}'}{l,m_l}\,.
\end{aligned}
$$
We can relate these equations to those given in **(e)**, **(f)**, and **(g)**:
$$
\begin{aligned}
m_l\hbar\braket{\vb{x}'}{l,m_l} &= -i\hbar\pdv{}{\phi}\braket{\vb{x}'}{l,m_l}\\
l(l+1)\hbar^2\braket{\vb{x}'}{l,m_l} &= -\hbar^2\left[\frac{1}{\sin^2\theta}\pdv{{}^2}{\phi^2}+\frac{1}{\sin\theta}\pdv{}{\theta}\left(\sin\theta\pdv{}{\theta}\right)\right]\braket{\vb{x}'}{l,m_l}\,.
\end{aligned}
$$
It can be seen that the solutions to these equations are the spherical harmonics[^4]
$$
\braket{\vb{x}'}{l,m_l} = Y_l^{m_l}\mleftright{(}{\theta,\phi}{)}\,.
$$

<!-- TODO mention CSCO -->

Any position eigenstate $\ket{\vb{x}'}$ can be 

TODO handle r dependence (<x| vs <n|)

[^1]: We extensively use the property that operators on different spaces commute _by definition_, e.g. $\hat{x}$ and $\hat{y}$, or $\hat{z}$ and $\hat{p}_y$.
[^2]: See the infinitesimal rotation matrix $R_z(\epsilon)$ in [Infinitesimal Rotations](infinitesimal-rotations.md).
[^3]: See [angular-momenum eigenvalues](angular-momentum-eigenvalues.md) for derivation.
[^4]: https://en.wikipedia.org/wiki/Spherical_harmonics#Laplace's_spherical_harmonics
<!-- TODO derive these myself -->