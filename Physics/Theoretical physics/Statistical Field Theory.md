- The same mathematical tools as [[Classical Field Theory]]
- There is _no time dependence_, as one studies systems in _equilibrium_
- Instead, one uses _temperature_ as the variable

- Characterise the system under some _coordinates_ $x^i$ and $\varphi(x^i,t)$
- One can study _phase transitions_

- The information of the system is contained in the _partition function_
- For a large number of particles, one uses an _integral_ to calculate it
# Models of a ferromagnet

## Ising model
- Have a _square lattice of spins_
	- Spin: up or down
- Model the Hamiltonian such that it is _energetically favourable to be aligned_

- At _low temperatures_, it is favourable to be _all spin up or down_
- At _high temperatures_, it is favourable to have _random spins_, or _zero magnetisation_
![[Magnetisation crit.png]]
- The _discontinuity_ of the _first derivative_ at $T=T_c$ gives a _second order phase transition_

- Given there is some _external magnetic field_:
![[Ising model B.png]]
- As _temperature_ increases _above_ $T_c$, the _size of discontinuity increases_

- Let there be $d$ dimensions
- Describe the _Hamiltonian_ as a _field_ from $\mathbb{Z}^d$ to
- To make alignment _favourable_:
$$H=-\frac{J}{2}\sum_{i,\delta}$$
- Then calculate the _partition function_, where one sums over _all possible spin configurations_

- Make a _mean field approximation_: there is _no quadratic term_
- Then one finds the partition function:
$$Z_0=\left[\right]^N$$
- The _average spin_ on each site is then:

- Then make the approximation such that the spin of _every site_ is _close to the average spin_:
$$s_i=$$

- Substituting this into the Hamiltonian, and _expanding in linear order_

- One then finds a _self-consistent solution_:
$$s=$$

- For the case of _zero field_, treating $\varepsilon=$:
$$\varepsilon=\tanh$$
![[ising model self consistent.png]]
- For $T>T_c$, the _only solution_ is $\varepsilon=0$
- For $T<T_c$, there is some _spontaneous magnetisation_ as new solutions appear
- This is a _phase transition_

- For $T$ _near_ $T_c$, $|\varepsilon|\ll1$ and one can _expand_

- Express $s$ in terms of the _reduced temperature_ $t$:

- The _order_ of this parameter is characterised by the _critical exponent_

- Consider the _magnetic susceptibility_, the _response_ of $s$ in response to $B$, in the limit of _small_ $B$
- One then finds:
$$\chi=\frac{}{}$$
- The susceptibility always _diverges_ as $t$ approaches $0$ (approaching critical temperature)
- The _scaling behaviour_ is the _same in both regimes_

- At _exactly_ the critical temperature:
$$s(T=T_c,b)\approx\left(\frac{3b}{k_BT_c}\right)^{1/3}$$

- Universality class

- Wtf is a conformal field theory

## Heisenberg model
- Also consider a _square lattice of identical spins_
- However, they are _free to rotate in three dimensions_ $\bm{s}_i=$
	- Only realistic for $d=3$
- The _Hamiltonian_ is then:
$$H=-\frac{J}{2}\sum_{i,\delta}\bm{s}_i\cdot\bm{s}_\delta-B\sum_i\hat{z}\cdot\bm{s}_i$$
- wlog, set $\mean{\bm{s}_i}=$

- In the _mean field approximation_, the Hamiltonian:

- One then has to set the _partition function_ as:
$$Z=\left[\right]$$

# Ginzburg-Landau theory
- One must describe the _degrees of freedom_ in the system
- Then specify the _symmetries_ and how they act upon the degrees of freedom

- One typically looks for _low energy degrees of freedom_
- Typically described by [[Classical Field Theory#Symmetry breaking|symmetry breaking]]
- This leads to an _order parameter_