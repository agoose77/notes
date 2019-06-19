# Differentiating Under the Integral

Leibniz's rule for differentiation under the integral sign states that for an integral of the form

$$
    \int _{a(x)}^{b(x)}f(x,t)\,\mathrm{d}t\,,
$$

the derivative may be expressed as

$$
{\frac {\mathrm{d}}{\mathrm{d}x}}\left(\int _{a(x)}^{b(x)}f(x,t)\,\,\mathrm{d}t\right)=f\big (x,b(x)\big )\cdot {\frac {\mathrm{d}}{\mathrm{d}x}}b(x)-f\big (x,a(x)\big )\cdot {\frac {\mathrm{d}}{\mathrm{d}x}}a(x)+\int _{a(x)}^{b(x)}{\frac {\partial }{\partial x}}f(x,t)\,\,\mathrm{d}t,
$$

## Proofs

### Constant Limits $(a,b)$

Let us use the [Fundamental Theorem of Calculus](fundamental-theorem-of-calculus.md#First-Fundamental-Theorem-of-Calculus) as an identity operator:

$$
\int_a^b\frac{\partial f(x,t)}{\partial x}\,\mathrm{d}t=\frac{\mathrm{d}}{\mathrm{d}x}\int_k^x\left(\int_a^b\frac{\partial f(s,t)}{\partial s}\,\mathrm{d}t\right)\mathrm{d}s\,.
$$

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7;border-color:#bce8f1;">

#### Fubini's Theorem

<!-- Note that this is quite a trivial definition, it doesn't look at measure theory -->

If $f(x,y)$ is continuous on $R=X\times Y\equiv[a, b]\times[c,d]$, then it holds that

$$
\begin{aligned}
\iint\limits_{X\times Y}f(x,y)\,\mathrm{d}x\,\mathrm{d}y &=
\int\limits_X\int\limits_Yf(x,y)\,\mathrm{d}y\,\mathrm{d}x\\
&=
\int\limits_Y\int\limits_Xf(x,y)\,\mathrm{d}x\,\mathrm{d}y\,.
\end{aligned}
$$

Which gives the result that $\iint\limits_R(x,y)\,\mathrm{d}x\,\mathrm{d}y$ can be computed using _iterated integrals_, whose order may be interchanged.

</div>

Using Fubini's theorem, we can interchange the order of integration:

$$
\begin{aligned}
\int_a^b\frac{\partial f(x,t)}{\partial x}\,\mathrm{d}t &=\frac{\mathrm{d}}{\mathrm{d}x}\int_a^b\left(\int_k^x\frac{\partial f(s,t)}{\partial s}\,\mathrm{d}s\right)\mathrm{d}t \\
&= \frac{\mathrm{d}}{\mathrm{d}x}\int_a^b\Big[f(s,t)+g(t)\Big]_{s=k}^{s=x}\\
&= \frac{\mathrm{d}}{\mathrm{d}x}\left(\int_a^bf(x,t)\,\mathrm{d}t-\int_a^bf(k,t)\,\mathrm{d}t\right)\,.
\end{aligned}
$$

The second term does not depend upon $x$, so this simplifies to

$$
\int_a^b\frac{\partial f(x,t)}{\partial x}\,\mathrm{d}t =\frac{\mathrm{d}}{\mathrm{d}x}\int_a^bf(x,t)\,\mathrm{d}t\,.
$$

### Variable Limits $\big(a(x),b(x)\big)$

Let us consider

$$
F(x, y, z) = \int_y^zf(x,t)\,\mathrm{d}t\,.
$$

The total derivative of $F$ is given by

$$
\mathrm{d}F=
\frac{\partial{F}}{\partial{y}}\,\mathrm{d}y+
\frac{\partial{F}}{\partial{x}}\,\mathrm{d}x+
\frac{\partial{F}}{\partial{z}}\,\mathrm{d}x\,.
$$

As shown [above](<#Constant-Limits-%24(a%2Cb)%24>),

$$
\frac{\partial{F}}{\partial{x}}=\int_y^z\frac{\partial f(x,t)}{\partial x}\,\mathrm{d}t\,,
$$

and we can use the Fundamental Theorem of Calculus to find $\frac{\partial F}{\partial z}$ and $\frac{\partial F}{\partial y}$:

$$
\begin{aligned}
 \frac{\partial F}{\partial z} &= f(x, z)\\
 \frac{\partial F}{\partial y} &= -f(x, y)
\end{aligned}\,.
$$

This leaves us with

$$
\frac{\mathrm{d}F}{\mathrm{d}x}=\int_y^z\frac{\partial f(x,t)}{\partial x}\,\mathrm{d}t + f(x, z)\cdot\frac{\mathrm{d}z}{\mathrm{d}x} - f(x, y)\cdot\frac{\mathrm{d}y}{\mathrm{d}x}\,,
$$

as required.
