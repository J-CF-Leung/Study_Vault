>[!quote]
>"Experimental and theoretical physics attract rather different personality types, with different temperaments and abilities. Sociologists should find here a ripe field for a fruitful study."
>-Anthony Zee, 徐一鴻

## The process of experimental physics
![[Experimental methods flowchart.png]]
- Goals: _Minimise junk_ and effects _from the transducer_

- Examples of transducers: Thermocouples, photodiodes

- A common method is to convert the original effect into _electrical signals_
- In almost all cases, the measurement tool used to measure signals is the _oscilloscope_

## Circuits
- The transducer becomes a _voltage source_ in an electrical circuit
- _Thevenin's theorem_ states that _any linear electrical circuit_ can be replaced by an _equivalent circuit_, consisting of a _voltage source in series with an impedance_
- Let the corresponding _perfect voltage source_ be $V_1$

- The transducer's _output impedance_ is defined as $Z_\text{out}=V_1/i$
	- where $i$ is the current flowing when $V_1$ and the impedance are shorted

- An oscilloscope is modelled as an _input impedance_ in _parallel with an ideal voltmeter_

![[Transducer and scope.png]]