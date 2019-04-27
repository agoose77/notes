# Fourier Series

A generalised Fourier series is a series expansion of a function using a complete orthogonal system of (basis) functions.

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
<!-- TODO port continuity -->
    
#### Complete Orthogonal System
A [set](set.md) of orthogonal functions $\{\,\phi_n(x)\,\}$ is complete in the closed interval $I=[a,\,b]:x\in I$ if, for _every_ [piecewise continuous](https://onedrive.live.com/redir?resid=BD289BC30A5FCA84%21107&page=Edit&wd=target%28Mathematics.one%7Cfe20c90a-2fc0-465c-90eb-c8c23e132c47%2FLniform%20Continuity.jpg%7C4df87a97-8900-438d-a3b2-6dc8f6c1ca87%2F%29&wdorigin=703) function $f(x)$ in the interval, the minimum square error
$$
E_n \equiv \lvert f - (c_1\phi_1+c_2\phi_2+\dots+c_n\phi_n)\rvert^2
$$
converges to zero as $n\rightarrow \infty$.
</div>

These functions satisfy an orthogonality relation over $I$ of the form

$$
\tag{a}
\int_I\phi_m(x)\phi_n(x)w(x)\,\mathrm{d}x=c_m\delta_{mn}\,,
$$

where $w(x)$ is a weighting function, and $c_m$ are given constants. In this basis, we can express an arbitrary function $f(x)$ as

$$
f(x) = \sum_{n=0}^\infty a_n\phi_n(x)
$$

The orthogonality relation may then be used to determine $a_n$:

$$
\tag{b}
\begin{aligned}
\int_If(x)\phi_m(x)w(x)\,\mathrm{d}x&=\int_I\sum_{n=0}^\infty a_n\phi_n(x)\phi_m(x)w(x)\,\mathrm{d}x\\
                                    &= \sum_{n=0}^\infty a_n \int_I \phi_n(x)\phi_m(x)w(x)\,\mathrm{d}x\\
                                    &= \sum_{n=0}^\infty a_n c_m \delta_{nm} \\
                                    &= a_m c_m\\
                                    a_n &= \frac{1}{c_n}\int_If(x)\phi_n(x)w(x)\,\mathrm{d}x\,.
\end{aligned}
$$

## The $\sin(nx)$ and $\cos(nx)$ Basis

The conventional Fourier series is based upon the complete orthogonal system of the $\sin(nx)$ and $\cos(nx)$ functions over the interval $I=[-\pi,\pi]$. It can be shown that $\sin(nx)$ and $\cos(mx)$ are mutually orthogonal to themselves and each other. In this basis, any $f(x)$ may be written as

$$
\begin{aligned}
f(x) &= \sum_{n=0}^\infty a_n\cos(nx) + \sum_{n=0}^\infty b_n\sin(nx)\\
     &= \frac{a_0}{2} + \sum_{n=1}^\infty a_n\cos(nx) + \sum_{n=1}^\infty b_n\sin(nx)\,,
\end{aligned}
$$

where

$$
\begin{aligned}
    a_n &= \frac{1}{\pi}\int_If(x)\cos(nx)\,\mathrm{d}x\\
    b_n &= \frac{1}{\pi}\int_If(x)\sin(nx)\,\mathrm{d}x\,.
\end{aligned}
$$

I.e. $w(x)=1$ and $c_n=\pi$ in both cases. The term $\frac{a_0}{2}$ arises from the fact that $c_0=2c_{n\neq0}$; by taking $a_n=\frac{1}{\pi}\int\dots$, $a_0$ will be twice as large.

## The Complex Exponential Basis

Another complete orthogonal system is given by $\{\,e^{inx}\,\}$. Given Euler's identity, any pair of terms $a_n\cos(nx) + b_n\sin(nx)$ can be expressed as the sum of two exponentials $p_ne^{inx} + q_ne^{-inx}$, and thus $f(x)$ may be expressed as the complex series

$$
f(x) = \sum_{i=-\infty}^\infty l_ie^{inx}\,.
$$

As before, $l_n$ are determined from the orthogonality relation

$$
l_n = \frac{1}{c_n}\int_{-\pi}^\pi f(x)e^{inx}\,\mathrm{d}x\,,
$$

where $c_n$ is given by **(a)** as

$$
    c_n = \int_{-\pi}^\pi e^{ix(n-n)}\,\mathrm{d}x=2\pi\,.
$$

## Change of Interval

Since $\sin(nx)$ and $\cos(nx)$, and $e^{inx}$, only form orthogonal systems on $[-\pi,\pi]$, in order to extend the Fourier series to a larger domain $I'$, we must use a change of variables.

More generally, let us consider a set of orthogonal functions $\{\,\phi_n(x)\,\}$ on the interval $I=[-L,L]$. Let us introduce a change of variables $x=\frac{x'L}{L'}$, which linearly scales $x'$ from $I'=[-L',L']$ to $I$. Our orthogonality relation then becomes

$$
\frac{L}{L'}\int_{I'}\phi_m\mathopen{}\left(\frac{x'L}{L'}\right)\mathclose{}\phi_n\mathopen{}\left(\frac{x'L}{L'}\right)\mathclose{}w\mathopen{}\left(\frac{x'L}{L'}\right)\mathclose{}\,\mathrm{d}x'=c_m\delta_{mn}\,,
$$

and our coefficients are determined as in **(b)**

$$
a'_n = \frac{L}{c_nL'}\int_{I'}f(x')\phi_n\mathopen{}\left(\frac{x'L}{L'}\right)\mathclose{}w\mathopen{}\left(\frac{x'L}{L'}\right)\,\mathrm{d}x'\,.
$$

For the complex exponential basis, this gives

$$
l'_n = \frac{1}{2L'}\int_{I'} f(x')e^{ix'k}\,\mathrm{d}x'\,,
$$

where $k=\frac{\pi n}{L'}$, and a function expansion

$$
f(x') = \sum_{i=-\infty}^\infty l'_ie^{ikx'}\,.
$$
