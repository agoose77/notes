Fourier Transform
=================
The Fourier transform decomposes a signal from the time domain into its frequencies. It is a generalisation of the complex [fourier series](series.md#Complex-Fourier-Series), as the interval $L\rightarrow \infty$: <!-- TODO define series.md -->

$$
\begin{aligned}
f(x) &= \sum_{n=-\infty}^\infty c_ne^{ikx}\\
     &= \sum_{n=-\infty}^\infty \frac{1}{2L}\int_{-L}^Lf(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}
\end{aligned}
$$
where k=$\frac{n\pi}{L}$.

Let $\Delta k=k_{n+1}-k_n=\frac{\pi}{L}$, such that 
$$
f(x) = \sum_{n=-\infty}^\infty \frac{\Delta k}{2\pi}\int_{-L}^Lf(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}\,.
$$

Taking the limit $L\rightarrow \infty$, 
$$
\lim_{L\rightarrow\infty}f(x) = \sum_{n=-\infty}^\infty \frac{\Delta k}{2\pi}\int_{-L}^Lf(t)e^{-ikt}\,\mathrm{d}t\, e^{ikx}\,.
$$

