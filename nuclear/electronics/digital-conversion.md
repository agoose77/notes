Digital Conversion
==================

Analogue and digital pulses
---------------------------

Analogue pulses are described by an instantaneous voltage amplitude
$V(t)$, and the corresponding profile drawn by $V(t)$ over a given time
interval $t_0\rightarrow t_1$.

Although analogue signals apprear continuous, there are a number of
physical constraints which determine the upper bound of the resolution
of a signal, such as the presence of interference and the physical
quantisation of charge.

Digital pulses may carry the same amount of information, but encode the
amplitude of a signal as an nbit number, conventionally in base 2.

Example
-------
Let us encode an analogue signal in the range
$0\operatorname{V}\rightarrow 10\operatorname{V}$ into an integer of 16 bits.
First, we divide the amplitude range into ($2^{16}$) bins of equal
magnitude, and find the correspond bin for the input amplitude.

Let us assume an input amplitude of 5 V. This would be quantised by the
above algorithm into the $32768^{th}$ bin. This can be encoded into 16
bits as `0b1000000000000000`.

Logic
-----

There are three major conventions used to represent logic values over
analogue interfaces:

1.  Transistor-Transistor Logic (TTL)
2.  Nuclear Instrument Module (NIM)
3.  Emitter Coupled Logic (ECL/CLM)

The TTL convention defines a logical true value as a potential
difference of +5 V with respect to ground, and a false value as 0 V p.d.
with respect to ground.

The NIM convention, on the other hand, defines a true value as -0.5 V
w.r.t ground, and a false value as 0 V p.d. w.r.t ground.

Finally, the ECL convention requires that two lines are used to carry a
signal, each of an amplitude between -1.75 V and -0.75 V (true, false
for A, & false, true for B)

An ADC converts an analogue pulse into a digital amplitude as follows:

1.  The peak amplitude is located using peak detection (differentiating
    to find the zerocrossing point).
2.  The peak amplitude is then held constant for processing
3.  A digitisation routine quantifies the voltage as a digital value.

There are several approaches to digitisation, Wilkinson and Successive
Approximation.

Linearity
---------

There are two aspects to the linearity of an ADC, which describe its
linear behaviour:

1.  Integral nonlinearity, the maximum deviation of the digitised vs
    amplitude curve from the line of best fit.
    $$\operatorname{INL} = \max_{0\le c\le c_\text{max}}{\lvert V_\text{out}(c)-V_\text{out}(0) - c\times m\rvert }$$
2.  Differential nonlinearity, the difference between the channel width
    and the ideal width as a fraction of the ideal.
    $$\operatorname{DNL}(i) = \frac{V_\text{out}(i+1)-V_\text{out}(i)}{\,\dd{w}_\text{ideal}} - 1$$

The Wilkinson Method
--------------------
The Wilkinson method involves charging a capacitor to the held voltage
$V$, and then counting the number of clock pulses which elapse as it
discharges through a constant current source, before a discriminator
measures a zero voltage across the capacitor.

Given that the voltage across a capacitor discharging through a constant
current source is described by the relation

$$
\begin{aligned}
            i&=i_c=c\dv{c}{t}\\
            \int_0^T{\frac{i}{C}\,\dd{t}} &= V_0 = \frac{iT}{C}\,.
        \end{aligned}
$$

The time taken for the capacitor to discharge can be used to determine
the initial voltage. Evidently the uncertainty in the digitised voltage
is dependant upon the clock frequency.

The $\operatorname{INL}$ of this method depends upon the capacitor and current source,
whilst the $\operatorname{DNL}$ depends upon, in particular, the clock characteristics.

The Successive Approximation Method
-----------------------------------
The successive approximation method uses an iterative algorithm which
utilises a fixed number of bits to encode the voltage as a digital
value. The algorithm decomposes the voltage as a sum of fractional
powers of a known maximum voltage.

Because the method uses a fixed number of iterations, independent of
voltage, it is typically fast. It also exhibits good $\operatorname{INL}$ but poor
$\operatorname{DNL}$.

The _sliding scale principle_ can be used to improve differential
nonlinearity, whilst worsening resolution. The method involves adding a
random (known) analogue voltage to the ADC input, and subtracting the
digital representation at the end.

Flash ADC
---------
This method "brute forces" the AD problem by using N window
discriminators, which correspond to N equally spaced channels.
Given that each "bin" requires a discriminator, this approach is
crude, and exhibits poor linearity and limited resolution.
