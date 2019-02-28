# Nuclear Electronics


Analogue and digital pulses
===========================

Analogue pulses are described by an instantaneous voltage amplitude
$V(t)$, and the corresponding profile drawn by $V(t)$ over a given time
interval $t_0\rightarrow t_1$.

Although analogue signals apprear continuous, there are a number of
physical constraints which determine the upper bound of the resolution
of a signal, such as the presence of interference and the physical
quantisation of charge.

Digital pulses may carry the same amount of information, but encode the
amplitude of a signal as an nbit number, conventionally in base 2.

#### Example

Let us encode an analogue signal in the range
$0\operatorname{V}\rightarrow 10\operatorname{V}$ into an integer of 16 bits.
First, we divide the amplitude range into ($2^{16}$) bins of equal
magnitude, and find the correspond bin for the input amplitude.

Let us assume an input amplitude of 5 V. This would be quantised by the
above algorithm into the $32768^{th}$ bin. This can be encoded into 16
bits as *0b1000000000000000*.

Logic
=====

There are three major conventions used to represent logic values over
analogue interfaces:

1.  Transistor-TransistorLogic (TTL)

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

Charge Collection
=================

For a silicon detector, the work function for a valence electron is
$\sim 3.3\operatorname{eV}$, so for an incident $\alpha$ particle of 5 MeV, $\sim3\times10^4$ electrons are produced,
corresponding to a charge of $\sim3\times 10^{-13}\operatorname{C}$.

Gas Ionisation Counters
-----------------------

Gas ionisation counters leverage the ionisation of gas atom/molecules as
charged particles enter the ionisation chamber, which generates
electrionion pairs.

For gas ionisation counters, the ionisation energies are much greater,
typically , and thus the measured charge is a similar factor lesser than
that of a silicon detector.

Given that the mobility of electrons and ions within a gas ionisation
counter differ, the current at the anode and cathode will differ
accordingly. Therefore, one must take the integral of the current over a
counter from each branch.


Charge Sensitive Amplifier
--------------------------

Typical amplifiers quantify the deposited energy of incident radiation
as liberated charge. Consequently, it is desirable to measure the
charge, and not the amplitude, yielded by the detector. For this, one
requires a "charge senstive amplifier".

To develop a CSP (charge sensitive preamplifier), one can replace the
second resistor $R_2$ in the previous configuration for a capacitor.

The current through a capacitor is given by the relationship
$$\begin{aligned}
Q_c(t) &= CV_c(t) \\
\frac{\mathrm{d}c}{\mathrm{d}t} = I_c(t) &= C\frac{\mathrm{d}c}{\mathrm{d}t}\,.\end{aligned}$$

Given that the virtual earth condition gives $V_-=0$, $V_c=-V_\text{out}$.
The current across the capacitor is equal to the current through $R$, as the opamp has infinite resistance, and therefore we deduce the following relation

$$
\begin{aligned}
    I_c(t) &= -C\frac{\mathrm{d}V_\text{out}}{\mathrm{d}t}\\
    \int_0^t{I_\text{in} \,\mathrm{d} t} = Q_\text{tot}^{0\rightarrow t} &= -C\int_0^V{\,\mathrm{d} V_\text{out}} = CV_\text{out}(t) \\
    V_\text{out}(t) = -\frac{Q_\text{tot}^{0\rightarrow t}}{C}\,.\end{aligned}
$$

Hence, in this configuration, the output voltage is the integral of the
current from the detector.

Finally, a resistor can be added in parallel with the capacitor to
prevent saturation of the output (by discharging the capacitor)

Filters
=======

Basic highpass and lowpass filtering can be performed with CR and RC
circuits, removing high and low frequencies respectively.

An RC circuit is in effect an integrator of the input current. In the
event that a voltage source is used, then the output voltage is
proportional to the time integral of the voltage.

A CR circuit, on the other hand, is a differentiator. Note that the
theory behind these behaviours is particular for AC circuitry.

The use of both a high and low pass filter compresses the signal within
a particular frequency range, which consequently maximises the signal to
noise ratio.

Typically the RC/CR time constants $\tau$ are set equal to one another,
and in the range for silicon detectors. It is important to choose a
sensible value for $\tau$, as it defines both the bandwidth and the
integration period of the amplifier. Where $\tau$ is less than the
charge collection time of the detector, a phenomenon known as *ballistic
deficit* is observed.

Amplifier Pulse Shape
---------------------

For a preamplifier signal with a long decay time and short rise time
(e.g 50, 1), it can be first approximated to a step function.

The first derivative of a step function *using a CR filter* gives a step
with an exponential tail.

Integrating that signal with an RC filter yields a unipolar pulse, which
can then be differentiated to give a bipolar pulse.

### The Undershoot Problem

In reality, however, preamplifier pulses have the form of a step rise
and exponential tail. When using a differentiation network where the
time constant $\tau_d < \tau_p$ (time constants of differentiation
network and preamplifier pulse), an undershoot is formed after the
initial peak. If subsequent pulses arrive on the tail of the pulse, low
energy peaks will be formed in the pulse height spectrum, degrading the
resolution.

This can be solved with the addition of an extra resistor in parallel
with the capacitor in the differentiation network, which modifiers the
response to regain the exponential decay as follows
$$\tau^\prime = \tau \frac{R}{R+R_\text{pz}}\,.$$

With too much compensation, $\tau_d$ is modified such that it is greater
than $\tau_p$, which leads to a deformed exponential tail, rather than a
symmetrical unipolar pulse.

Pile Up
-------

At high count rates, subsequent pulses can form on the tail of an
initial pulse, which leads to increasing pulse amplitudes. This
phenomenon, known as *pile up*, depends upon the event rate and pulse
length, and gives rise to high energy tails on peaks in energy spectra.

Pile up can be rejected, if a *pile up rejection* pulse is generated
when the incident pulse crosses a threshold in the positive direction.
Where two rejection pulses appear in coincidence, the event is rejected

A CR and RC circuit can be combined to form an RC shaping amplifier,
with the use of an x1 Buffer amplifier to decouple the two circuits (it
has a very high input impedance)

Baseline shift
--------------

Because capacitors cannot conduct direct current, the *average* dc
voltage at any point behind the capacitor in an RC/CR circuit must be
zero.

The mean value of a function can be defined in the form of an integral
of the function over a bounded range (if $f$ is continuous), as

$$\langle{V}\rangle = \frac{1}{b-a}\int_{t=a}^{t=b}{V(t)\,\mathrm{d}{t}}\,.$$

Hence, for $\langle{V}\rangle=0$, it must be that the integral of $V(t)$ over
the appropriate integration period is zero.

Given this constraint, it can be seen that the baseline against which an
incoming pulse train is set must be depressed below the true "zero",
such that the areas above and below the zero axis are equal.

To satisfy this constraint, the baseline shift must be dependant upon
the pulse frequency. Hence, with signals from real detectors
(preamplifiers), energy resolution will be degraded ($E\propto V$).

One can satisfy the necessary equal areas criterion whilst avoiding
baseline shift by using bipolar pulses, whch have equal areas above and
below the baseline. Another solution is to use a baseline restoration
circuit, which resets the dc level to zero after each pulse

Discriminators
==============

First Level Discriminators
--------------------------

Discriminators are used to detect pulses within a signal. A naive
amplitudedependant trigger such as a "window discriminant" will
trigger at different points along the pulse profile, depending upon the
pulse shape and amplitude, in a phenomenon known as *time walk*. See for
more.

Second Level Discriminators
---------------------------

Second level discriminators use comparisons *between logic pulses*,
rather than a single pulse and some constant criterion.

Coincidence units produce a logic pulse from each amplified signal
branch, and then feed them into a coincidence unit. These units can
perform AND/OR tests to reject or accept the event.

Some coincidence units have *veto* inputs, which overrides the
coincidence logic to reject an event, provided that the pulse spans the
pulses from both A and B.

This feature is typically used by the data acquisition system (DAS),
which is unable to process further events whilst active (corresponding
to the DAS *dead time*, often in the range of depending upon DAS
complexity).
