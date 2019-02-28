Digital Conversion
==================

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
    $$\operatorname{DNL}(i) = \frac{V_\text{out}(i+1)-V_\text{out}(i)}{\,\mathrm{d}{w}_\text{ideal}} - 1$$

The Wilkinson Method
--------------------

The Wilkinson method involves charging a capacitor to the held voltage
$V$, and then counting the number of clock pulses which elapse as it
discharges through a constant current source, before a discriminator
measures a zero voltage across the capacitor.

Given that the voltage across a capacitor discharging through a constant
current source is described by the relation 
$$\begin{aligned}
            i&=i_c=c\frac{\mathrm{d}c}{\mathrm{d}t}\\
            \int_0^T{\frac{i}{C}\,\mathrm{d}{t}} &= V_0 = \frac{iT}{C}\,.
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

The *sliding scale principle* can be used to improve differential
nonlinearity, whilst worsening resolution. The method involves adding a
random (known) analogue voltage to the ADC input, and subtracting the
digital representation at the end

Flash ADC
---------

This method "brute forces" the AD problem by using N window
discriminators, which correspond to N equally spaced channels.

Given that each "bin" requires a discriminator, this approach is
crude, and exhibits poor linearity and limited resolution.
