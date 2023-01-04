>[!quote]
>"Experimental and theoretical physics attract rather different personality types, with different temperaments and abilities. Sociologists should find here a ripe field for a fruitful study."
>-Anthony Zee, 徐一鴻

## The process of experimental physics
![[Experimental methods flowchart.png]]
- Goals: _Minimise junk_ and effects _from the transducer_

- Examples of transducers: Thermocouples, photodiodes

- A common method is to convert the original effect into _electrical signals_
- In almost all cases, the measurement tool used to measure signals is the _oscilloscope_

## Measurement circuits and oscilloscopes
- The transducer becomes a _voltage source_ in an electrical circuit
- _Thevenin's theorem_ states that _any linear electrical circuit_ can be replaced by an _equivalent circuit_, consisting of a _voltage source in series with an impedance_
- Let the corresponding _perfect voltage source_ be $V_1$

- The transducer's _output impedance_ is defined as $Z_\text{out}=V_1/i$
	- where $i$ is the current flowing when $V_1$ and the impedance are shorted

- An oscilloscope is modelled as an _input impedance_ in _parallel with an ideal voltmeter_
![[Transducer and scope.png]]
- From this, the p.d. detected by the oscilloscope is:
$$V_\text{in}=V_1\frac{Z_\text{in}}{Z_\text{in}+Z_\text{out}}$$
- For accurate measurements:
	- $Z_\text{in}$ must be high
	- $Z_\text{out}$ must be low

- In real oscilloscopes, $Z_\text{in}$ _has a capacitive component_
- This leads to _lower voltage measurement for high frequencies_

- To solve this problem, _oscilloscope probes_ are used
- Probes also contain a capacitive component to compensate

- For _current measurements_, a _low_ $Z_\text{in}$ is desired
- To _transfer maximum power_ to another system, the _impedances should match_

## Operational amplifiers
![[Op-amp.png]]
- This is what happens when you eat the silica gel packets

![[Op-amp symbol.png|]]

- $A$ is the _open loop gain_ of the amplifier, defined with:
$$V_\text{out}=A(V_+-V_-)$$

- When connected in a circuit with other components, the gain of the _entire circuit_ is known as the _closed-loop gain_

### Ideality, negative feedback, and the golden rules
- An ideal voltage amplifier has the following properties:
$$A=\infty \hspace{1cm}Z_\text{in}\equiv\pd{V_\text{in}}{i_\text{in}}=\infty \hspace{1cm} Z_\text{out}\equiv\pd{V_\text{out}}{i_\text{out}}=0$$
- Real op-amps: $A>>10^5$
- $Z_\text{in}=\infty$: The op-amp works, _even for infinitesimally small currents_
- $Z_\text{out}=0$: There is no limit to output current

- By itself, an ideal op-amp would give infinite $V_\text{out}$, or the maximum allowed by the power supply. causing _clipping_
- The _closed-loop gain_ of an op-amp circuit can be controlled with _negative feedback_
- The negative feedback eventually creates an equilibrium

- For circuits containing ideal op-amps, there are two _Golden Rules_:
1. Since $Z_\text{in}$ is infinite, _the inputs draw no current_
	- _Output current_ is derived from the power supply, and _unrelated to current input_
2. The voltages on the $+$ and $-$ inputs are _the same, unless output is saturated_
	- Negative feedback is required for this to be true
	- Due to large $A$, $V_+-V_-$ is usually negligible

#### The inverting voltage amplifier
![[Inverting voltage amplifier.png]]
- From applying _Kirchoff's rules_ plus the _Golden Rules_, the overall _closed-loop gain_ is:
$$G\equiv\frac{V_\text{out}}{V_\text{in}}=-\frac{R_2}{R_1}$$
- The gain is _purely determined by the two resistors_
- The negative feedback applies for _all frequencies_
- This value of gain is true as long as _$V_\text{out}$ does not exceed the limit set by the power supply_

#### The non-inverting voltage amplifier
![[Non-inverting amplifier.png]]
- The _closed-loop gain_ is:
$$G\equiv\frac{V_\text{out}}{V_\text{in}}=1+\frac{R_2}{R_1}$$
- The circuit can also be understood as a _potential divider_

#### More on amplifiers
- The external components _do not have to be resistors_
- Adding _inductors and capacitors_ introduces _frequency dependence_
- Potential circuits include _integrators_, _differentiators_, and _filters_
![[Filter circuit with op-amp.png]]

### Non-ideal performance
- Typical op-amps:
	- $10^4\lesssim A\lesssim10^6$, function of frequency
	- High but non-infnite $Z_\text{in}$
	- Low but non-zero $Z_\text{out}$
	- Finite _slew rate_, $dV_\text{out}/dt$

- _Bias current_: the op-amp draws a small current $(10^{-12}-10^{-7})\text{A}$
	- Sets a _limit on external resistance_ as there is a voltage _drop at the input pins_
	- There must be a path allowing the bias currents to _flow to ground_

- _Offset voltage_: Output voltage _independent of_ $(V_+-V_-)$, causing a _differential offset_ of $10^{-3}-10^{-2}\text{V}$, must be balanced with an _external potentiometer_

#### Revisiting the non-inverting amplifier
- What a non-inverting amplifier actually looks like:
![[Non-ideal non-inverting amplifier.png]]

- The circuit can be treated as a _system_ with _open-loop gain_ $A'$ and _output impedance_ $Z_\text{out}$:
$$V_\text{out}=A'V_\text{in}-Z_\text{out}i_\text{out}$$
- As usual, for accuracy, _overall_ $Z_\text{in}=V_\text{in}/i_\text{in}$ should be high and $Z_\text{out}$ should be low
![[Op-amp circuit systems approach.png]]

- Taking _$A$ and $r_\text{in}$ to be very large_, $V_\text{out}/V_\text{in}$ is equal to $1+R_2/R_1$, _same as the ideal case_
- Taking the same limit, and low $R_\text{out}$, the impedances approach:
$$Z_\text{out}\approx\frac{R_\text{out}}{A}\left(1+\frac{R_2}{R_1}\right) \hspace{1cm}Z_\text{in}\approx\frac{r_\text{in}A}{1+R_2/R_1}$$
- The circuit has a _higher $Z_\text{in}$_, and _lower_ $Z_\text{out}$ than $r_\text{in}$ and $R_\text{out}$ _of the op-amp_ respectively

- Therefore, the limits _required for close to ideal behaviour_ are:
	- Large $A$
	- High $r_\text{in}$
	- Low $R_\text{out}$

- A useful case of the non-inverting amplifier is the _buffer/follower circuit_
- The buffer circuit has $R_2/R_1=0$
![[Buffer circuit.png]]
- Its characteristics are:
$$V_\text{out}=V_\text{in} \hspace{1cm} Z_\text{in}=Ar_\text{in} \hspace{1cm} Z_\text{out}=\frac{R_\text{out}}{A}$$
- This is very useful for connecting circuits

#### Revisiting the inverting amplifier
- Taking the same limits as before, the characteristics of the circuit are:
$$\frac{V_\text{out}}{V_\text{in}}=-\frac{R_2}{R_1} \hspace{1cm} Z_\text{out}=\frac{R_\text{out}}{A}f\left(\frac{R_2}{R_1}\right) \hspace{1cm} Z_\text{in}=R_1+f\left(\frac{R_1}{A},\frac{R_2}{A},\frac{r_\text{in}}{A}\right)$$
- Here, $Z_\text{in}$ becomes _dependent on external components_
- For high $Z_\text{in}$, it is better to use a _non-inverting amplifier_

### Frequency-dependent behaviour
- Overall, the gain of the circuit is _frequency dependent_
- For _high frequencies_, due to capacitive components in $R$, _a phase shift is introduced_
- At a phase shift of $\pi$, _feedback becomes positive_, causing saturation and oscillation

- Practically, _all signals have some high frequency components_
- Therefore, op-amps are designed to _lower gain at high frequencies_
- Typically, after some threshold, $A\propto 1/f$

- _Decoupling capacitors_ are also connected between the op-amp and the power supply
- They _stop spontaneous oscillations_

## Feedback in systems
- In general, systems with feedback built in can be represented as:
![[System with feedback.png]]
- The input and output are related by:
$$\text{Output}=A(\text{Input}+\beta\times\text{Output})$$
- Here, $\beta$ is the fraction of the output fed back
- For _negative feedback_, $\beta<0$

- For the _non-inverting amplifier_, $\beta=-R_1/(R_1+R_2)$
- For the _inverting amplifier_, $\beta=(1+|-Z_2/Z_1|)^{-1}$

- The _closed-loop gain_ in the general case is:
$$G\equiv\frac{\text{Output}}{\text{Input}}=\frac{A}{1-A\beta}$$
- If $A\beta=1$, the output "explodes"
- For _large $A$_, the gain becomes _independent of $A$_:
$$G\approx-\frac{1}{\beta}$$
- In most systems, $A$ _depends on external conditions_, will _fluctuate_, be _frequency-dependent_, and in some cases, _non-linear_
	- Examples: Biological buffers, stellar burning
- Hence, $|A\beta|>>1$ will be advantageous, especially for signal measurement

### Negative feedback
- In general, negative feedback _stanilises a system against perturbations_
- For a perturbation to the output $\delta$, after one cycle, the increase in output is $\delta/(1-A\beta)$

- In the context of circuits, like the _non-inverting amplifier_:
$$Z_\text{in}=r_\text{in}(1+|A\beta|)\hspace{1cm} Z_\text{out}=R_\text{out}/(1+|A\beta|)$$
- This is desirable for accurate measurement
- Does not apply for the inverting amplifier

### Positive feedback
- Positive feedback often causes _saturation or oscillation_
- If $\beta$ is _frequency dependent_, $A\beta$ can be $\approx 1$ for _only a specific frequency_
- This generates _spontaneous oscillations_ at that frequency

- For example, a circuit can be made to have a _$\pi$ phase shift_ at a specific $\omega_0$
- This acts as both an _oscillator_ and a _filter_ at $\omega_0$
	- Other components may be fed back but _not reinforced_ as much as $\omega_0$

