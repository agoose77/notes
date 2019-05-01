# Exponential Characterisation

From the [fundamental theorem of calculus](fundamental-theorem-of-calculus.md#First-Fundamental-Theorem-of-Calculus),

$$
\dv{}{x}\ln(x)=\dv{x}\int_1^x\frac{1}{t}\dd t=\frac{1}{x}\,.
$$

Now, let $x\in\mathbb{R}$ be some fixed constant, and

$$
y = \lim_{n\rightarrow\infty}\left(1+\frac{x}{n}\right)^m\,.
$$

We have

$$
    \begin{aligned}
    \ln{y} &= \ln\mleftright{[}{\lim_{n\rightarrow\infty}\left(1+\frac{x}{n}\right)^n}{]}\\
           &=\lim_{n\rightarrow\infty}\mleftright{[}{\ln\mleftright{(}{1+\frac{x}{n}}{)}^n}{]}\,,
    \end{aligned}
$$

where the interchange of the limit results from the continuity of $\left(1+\frac{x}{n}\right)^n$.
It then follows that

$$
    \begin{aligned}
    \ln{y} &=\lim_{n\rightarrow\infty}\mleftright{[}{n\ln\mleftright{(}{1+\frac{x}{n}}{)}}{]}\\
           &=\lim_{n\rightarrow\infty}\mleftright{[}{n\ln\mleftright{(}{1+\frac{x}{n}}{)}\frac{x/n}{x/n}}{]}\\
           &=\lim_{n\rightarrow\infty}\mleftright{[}{\frac{x\ln\mleftright{(}{1+\frac{x}{n}}{)}}{x/n}}{]}\,.\\
    \end{aligned}
$$

Now, let $h=\frac{x}{n}$, then

$$
\begin{aligned}
    \ln{y} &=\lim_{h\rightarrow 0}\frac{x\ln(1+h)}{h}\\
           &=x\lim_{h\rightarrow 0}\frac{\ln(1+h)-\ln 1}{h}\\
           &=x\dv{}{t}\Big[\ln{t}\Big]_{t=1}\\
           &=x\,.
\end{aligned}
$$

Hence,

$$
y = \exp(x)\,.
$$
