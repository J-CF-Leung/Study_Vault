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

### Ideality and the golden rules
- An ideal voltage amplifier has the following properties:
$$A=\infty \hspace{1cm}Z_\text{in}\equiv\pd{V_\text{in}}{i_\text{in}}=\infty \hspace{1cm} Z_\text{out}\equiv\pd{V_\text{out}}{i_\text{out}}=0$$