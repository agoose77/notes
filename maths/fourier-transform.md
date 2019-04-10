Fourier Transform
=================
The Fourier transform decomposes a signal from the time domain into its frequencies. It is a generalisation of the complex [Fourier series](fourier-series.md#The-Complex-Exponential-Basis)

$$
\begin{aligned}
f(x) &= \sum_{n=-\infty}^\infty c_ne^{ikx}\\
     &= \sum_{n=-\infty}^\infty \frac{1}{2L}\int_{-L}^Lf(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}\,,
\end{aligned}
$$
where k=$\frac{n\pi}{L}$, as the interval $L\rightarrow \infty$.

Let $\Delta k=k_{n+1}-k_n=\frac{\pi}{L}$, such that 
$$
f(x) = \sum_{n=-\infty}^\infty \frac{\Delta k}{2\pi}\int_{-L}^Lf(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}\,.
$$

Taking the limit $L\rightarrow \infty$, it follows that
$$
\tag{a}
\begin{aligned}
\lim_{L\rightarrow\infty}f(x) &= \int_{-\infty}^\infty \frac{\mathrm{d} k}{2\pi}\int_{-\infty}^\infty f(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}\\
                              &= \frac{1}{2\pi}\int_{-\infty}^\infty \hat{f}(k)e^{ikx}\mathrm{d}k
\end{aligned}
$$

This defines the (forward) Fourier transform $\mathcal{F}_x\mathopen{}\big[f(x)\big]\mathclose{}$, and its inverse $\mathcal{F}_k^{-1}\mathopen{}\big[\hat{f}(k)\big]\mathclose{}$:
$$
\begin{aligned}
    \mathcal{F}_x\mathopen{}\big[f\big]\mathclose{} = \hat{f}(k) &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty f(t)e^{-ikt}\,\mathrm{d}t\\
    \mathcal{F}^{-1}_k\mathopen{}\big[\hat{f}\big]\mathclose{} = f(x) &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \hat{f}(k)e^{ikx}\,\mathrm{d}k\,.
\end{aligned}
$$

There are several variants of the Fourier transform, depending upon which form of the Fourier series is used.
