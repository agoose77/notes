# Fourier Transform

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
\tag{b}
\begin{aligned}
    \mathcal{F}_x\mathopen{}\big[f\big]\mathclose{} = \hat{f}(k) &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty f(t)e^{-ikt}\,\mathrm{d}t\\
    \mathcal{F}^{-1}_k\mathopen{}\big[\hat{f}\big]\mathclose{} = f(x) &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty \hat{f}(k)e^{ikx}\,\mathrm{d}k\,.
\end{aligned}
$$

## Variants

There are several variants of the Fourier transform, depending upon which form of the Fourier series is used.  
For example, letting $k=2\pi\hat{k}$:

$$
\begin{aligned}
    \mathcal{F}_x\mathopen{}\big[f\big]\mathclose{} = \hat{f}(2\pi\hat{k}) &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty f(t)e^{-2\pi i\hat{k}t}\,\mathrm{d}t\\
    \mathcal{F}^{-1}_k\mathopen{}\big[\hat{f}\big]\mathclose{} = f(x) &= \sqrt{2\pi}\int_{-\infty}^\infty \hat{f}(2\pi\hat{k})e^{2\pi i\hat{k}x}\,\mathrm{d}\hat{k}\,.
\end{aligned}
$$

We can then _redefine_ $\hat{f}(\hat{k})=\sqrt{2\pi}\hat{f}(2\pi \hat{k})$, such that

$$
\begin{aligned}
    \mathcal{F}_x\mathopen{}\big[f\big]\mathclose{} = \hat{f}(\hat{k}) &= \int_{-\infty}^\infty f(t)e^{-2\pi i\hat{k}t}\,\mathrm{d}t\\
    \mathcal{F}^{-1}_k\mathopen{}\big[\hat{f}\big]\mathclose{} = f(x) &=\int_{-\infty}^\infty \hat{f}(\hat{k})e^{2\pi i\hat{k}x}\,\mathrm{d}\hat{k}\,.
\end{aligned}
$$

Similarly, an asymmetrical convention can be used to define a variant of **(b)**,

$$
\begin{aligned}
    \mathcal{F}_x\mathopen{}\big[f\big]\mathclose{} = \hat{f}(k) &= \int_{-\infty}^\infty f(t)e^{-ikt}\,\mathrm{d}t\\
    \mathcal{F}^{-1}_k\mathopen{}\big[\hat{f}\big]\mathclose{} = f(x) &= \frac{1}{2\pi}\int_{-\infty}^\infty \hat{f}(k)e^{ikx}\,\mathrm{d}k\,.
\end{aligned}
$$

It is important to note that the two transforms are defined _with respect to one another_; as evidenced by our redefinition of $\hat{f}$.
