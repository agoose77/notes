Operation Modes
===============

Pulse Mode
----------
Pulse mode involves recording the time-integral of the current (such as that from a [charge-sensitive preamplifier](electronics.md#Charge-Sensitive-Amplifier)). This *preserves the nature of the amplitude and timing* of the pulse.

![Pulse Mode Schematic](images/pulse-mode.png)

The voltage across the load resistor $R$ is the fundamental signal voltage, and has two extremes of operation, dependent upon the [RC circuit](rc-circuits.md#RC-Circuit) time constant $\tau=RC$.

For an RC circuit with source current $I_s=I_C+I_R$, it follows that
$$
\tag{a}
I_s = C\frac{\mathrm{d}V_C}{\mathrm{d}t} + \frac{V_C}{R}\,.
$$

To solve this, let's introduce an function $M(t)$, and multiply through 
$$
    \tag{b}
    M(t)C\frac{\mathrm{d}V_C}{\mathrm{d}t} + M(t)\frac{V_C}{R} = M(t)\frac{I_s}{C}\,.
$$
By choosing $M(t)=e^{\int{\frac{1}{RC}\,\mathrm{d}t}}=e^{\int{\frac{1}{\tau}\,\mathrm{d}t}}$, it follows that
$$
\frac{\mathrm{d}M(t)}{\mathrm{d}t} = \frac{1}{\tau}M(t)\,,
$$

hence we can rewrite **(b)** as
$$
    \frac{\mathrm{d}}{\mathrm{d}t}\Big(M(t)V_C\Big) = M(t)\frac{I_s}{C}\,,
$$

taking the integral of both sides from $t=0$ to $t=t$ and solving for $V_C$, we find
$$
V_C(t) = \frac{1}{M(t)}\left(V_C(0)M(0) + \frac{1}{C}\int_0^t M(t^\prime)I_s\,\mathrm{d}t^\prime\right)\,.
$$

As $M(t)$ can be any function which satisfies $M^\prime = \frac{1}{\tau}M$, let $M(t) = \exp\left(\int_0^t \frac{1}{\tau}\,\mathrm{d}t\right)=\exp(\frac{t}{\tau})$,
$$
    V_C(t) = \exp\left(\frac{-t}{\tau}\right)\left(V_C(0) + \frac{1}{C}\int_0^t \exp\left(\frac{t^\prime}{\tau}\right)I_s\,\mathrm{d}t^\prime\right)\,.
$$

Evidently, at $t=0$, the voltage on the capacitor $V_C$ must be zero, hence
$$
    \tag{c}
    V_C(t) = \exp\left(\frac{-t}{\tau}\right)\frac{1}{C}\int_0^t \exp\left(\frac{t^\prime}{\tau}\right)I_s\,\mathrm{d}t^\prime\,.
$$


### Small $\tau$
Let us rewrite **(a)** in terms of $\tau$
$$
\tag{d}
R I_s = \tau\frac{\mathrm{d}V_C}{\mathrm{d}t} + V_C\,.
$$

Taking the limit as $\tau \rightarrow 0$, it follows that $I_s \approx \frac{V_C}{R}$

### Large $\tau$
Where $\tau \rightarrow \infty$, **(c)** approaches
$$
    V_C(t) = \frac{1}{C}\int_0^t I_s(t^\prime) \,\mathrm{d}t^\prime\,.
$$

This can also be shown from **(d)**, with $I_s \approx C \frac{\mathrm{d}V_C}{\mathrm{d}t}$.