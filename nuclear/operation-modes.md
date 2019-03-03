Operation Modes
===============

Pulse Mode
----------
Pulse mode involves recording the time-integral of the current (such as that from a [charge-sensitive preamplifier](electronics.md#Charge-Sensitive-Amplifier)). This *preserves the nature of the amplitude and timing* of the pulse.

![Pulse Mode Schematic](images/pulse-mode.png)

The voltage across the load resistor $R$ is the fundamental signal voltage, and has two extremes of operation, dependent upon the [RC circuit](rc-circuits.md#RC-Circuit) time constant $\tau=RC$.

For an RC circuit with source current $I_s=I_C+I_R$, it follows that
$$
I_s = C\frac{\mathrm{d}V_C}{\mathrm{d}t} + \frac{V_C}{R}\,.
$$

To solve this, let's introduce an function $M(t)$, and multiply through 
$$
    \tag{a}
    M(t)C\frac{\mathrm{d}V_C}{\mathrm{d}t} + M(t)\frac{V_C}{R} = M(t)\frac{I_s}{C}\,.
$$
By choosing $M(t)=e^{\int{\frac{1}{RC}\,\mathrm{d}t}}=e^{\int{\frac{1}{\tau}\,\mathrm{d}t}}$, it follows that
$$
\frac{\mathrm{d}M(t)}{\mathrm{d}t} = \frac{1}{\tau}M(t)\,,
$$

hence we can rewrite **(a)** as
$$
    \frac{\mathrm{d}}{\mathrm{d}t}\Big(M(t)V_C\Big) = M(t)\frac{I_s}{C}\,,
$$

taking the integral of both sides from $t=0$ to $t=t$ and solving for $V_C$, we find
$$
V_C(t) = \frac{1}{M(t)}\left(V_C(0)M(0) + \frac{1}{C}\int_0^t M(t^\prime)I_s\,\mathrm{d}t^\prime\right)\,.
$$

As $M(t)$ can be any function which satisfies $M^\prime = \frac{1}{\tau}M$, let $M(t) = \exp\left(\int_0^t \frac{1}{\tau}\,\mathrm{d}t\right)=\exp(\frac{t}{\tau})$,
$$
    \tag{b}
    V_C(t) = \exp\left(\frac{-t}{\tau}\right)\left(V_C(0) + \frac{1}{C}\int_0^t \exp\left(\frac{t^\prime}{\tau}\right)I_s\,\mathrm{d}t^\prime\right)\,.
$$

Evidently, at $t=0$, the voltage on the capacitor $V_C$ must be zero, hence
$$
    \tag{c}
    V_C(t) = \exp\left(\frac{-t}{\tau}\right)\frac{1}{C}\int_0^t \exp\left(\frac{t^\prime}{\tau}\right)I_s\,\mathrm{d}t^\prime\,.
$$


### Small $\tau$
Where $\tau \ll t_c$, given $t_c$ is the charge collection time, the 

### Large $\tau$
Where $\tau \gg t_c$, **(c)** approaches
$$
    V_C(t) = \frac{1}{C}\int_0^t I_s(t^\prime) \,\mathrm{d}t^\prime\,.
$$