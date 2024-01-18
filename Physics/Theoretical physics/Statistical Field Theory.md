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

### Expected behaviour
- Consider _no external fields_
- At _low temperatures_, it is favourable to be _all spin up or down_
- At _high temperatures_, it is favourable to have _random spins_, or _zero magnetisation_
![[Magnetisation crit.png]]
- The _discontinuity_ of the _first derivative_ at $T=T_c$ gives a _second order phase transition_

- Given there is some _external magnetic field_:
![[Ising model B.png]]
- _Below_ the critical temperature, at _zero field_, two opposite magnetisations _co-exist_
- The magnetic field _further increases magnetisation_ in each direction
- As _temperature_ gets _closer_ to $T_c$, the discontinuity gets _smaller_
- At $T\geq T_c$, the curve is _continuous_ as spins are random at $B=0$
- At $T=T_c$, the curve has a _vertical gradient_ at $B=0$

- This _discontinuity_ of $M$ gives a _first order phase transition_

- At _critical points_ where phase transitions occur, phenomena of _all length scales_ become physically relevant

### Hamiltonian and partition function
- Let there be $d$ dimensions
	- The _lattice of spins_ is a field from $\mathbb{Z}^d$ to $\mathbb{Z}_2$
	- $\mathbb{Z}_2$: integers _modulo_ 2 (up or down)
- To make alignment _favourable_, set a _coupling constant_ $J$ in the Hamiltonian:
$$H=-\frac{J}{2}\sum_{i,\delta}s_is_{i+\delta}-\mu\sum_i s_iB$$
- $i$ sums over _all sites_, and $\delta$ sums over _nearest neighbours_ ($2d$ in a _cubic lattice_)
- The _factor_ of $1/2$ avoids _double counting_

- Then calculate the _partition function_, where one sums over _all possible spin configurations_
$$Z=\sum_{\{s_i\}}\exp[-\beta H(\{s_i\})] \hspace{1.5cm}\beta=\frac{1}{kT}$$

### Mean field theory
- Make a _mean field approximation_: there is _no quadratic term_
- It is typically _valid_ when the _fluctuations_ are _small_ relative to the _average value_

- In the case of _non-interacting spins_, one finds the Hamiltonian and partition function (with $b=\mu B$)
$$\displaylines{H_0=-\mu\sum_i s_iB\hspace{1.5cm}Z_0=\left[\exp(\beta b)+\exp(-\beta b)\right]^N}$$
- The _average spin_ on each site is then:
$$s=\mean{s_i}=\frac{\mean{U}}{-Nb}=\frac{1}{Nb}\pd{\ln Z}{\beta}=\tanh(\beta b)$$
- This _asymptotically_ approaches $\pm1$ depending on the _direction_ of $b$
- As $\beta\to\infty$, it approaches a _step function_

- Then switch on the _interactions_
- Then make the approximation such that the spin of _every site_ is _close to the average spin_:
$$s_i=s+(s_i-s)=s+\delta s$$

- Substituting this into the _interaction Hamiltonian_, and _expanding in linear order_ while _neglecting constant terms_
	- Constant term: $\propto s^2$, is a _constant_ and does _not_ involve $s_{i}$
$$H=-\frac{Js}{2}\sum_{i,\delta} s_i+s_{i,\delta}=-2dJs \sum_{i}s_{i}$$
- In ignoring second-order terms, all _surrounding spins_ effectively _have the mean spin_
- Doing the sum, one finds there is then an _additional term acting as an effective field_:
$$b_{\text{{eff}}}=b+2dJs$$

- One then finds an equation like the previous form of $\mean{s}$, where one must find a _self-consistent solution_:
$$s=\tanh[\beta (b+2dJs)]$$
- One gets the same result by assuming _each neighbouring spin_ produces an _additional field_ $J\mean{s_{i+\delta}}$

### Zero external field
- For the case of _zero field_, treating $\varepsilon=2\beta dJs$:
$$\varepsilon=2d\beta J\tanh\varepsilon$$
![[ising model self consistent.png]]
- For $T>T_c$, the _only solution_ is $\varepsilon=0$
- For $T<T_c$, there is some _spontaneous magnetisation_ as new solutions appear
- This is a _phase transition_

- $T_c$ can be found, as new solutions appear when _gradients match at $\varepsilon=0$:
$$T_c=\frac{2dJ}{k}$$

- For $T$ _near_ $T_c$, $|\varepsilon|\ll1$ and one can _expand_ the equation:
$$\varepsilon=\frac{T_c}{T}\left(\varepsilon-\frac{1}{3}\varepsilon^3+\dots\right)$$

- Express $s$ in terms of the _reduced temperature_ $t\equiv T/T_c-1$:
$$s\approx \pm\sqrt{3}\left(\frac{T_c-T}{T_c}\right)^{1/2}\equiv\pm\sqrt{3}|t|^{1/2}$$
- $\pm$: at $t>0$, the spin takes _two different branches_
	- At $t<0$, $s=0$

- The _order_ of this parameter is characterised by the _critical exponent_ $\beta=1/2$
$$M(B\to0)\propto |t|^\beta$$

### Magnetic susceptibility
- Consider the _magnetic susceptibility_, the _response_ of $s$ in response to $B$, in the limit of _small_ $B$:
$$\chi=\frac{ds}{db}\Bigg|_{b=0}$$
- One then finds, for $T>T_c$, or $t>0$:
$$\chi=\frac{1}{kT_c}\left(\frac{T_c-T}{T_c}\right)^{-1}$$
- The susceptibility always _diverges_ as $t$ approaches $0$ (approaching critical temperature)

- For $T<T_c$, one must take the _spontaneous magnetisation_ $s_0=\pm\sqrt{3}|t|^{1/2}$ into account
- By _expanding_ the $\tanh$:
$$\chi=\frac{1}{2kT_c}\left(\frac{T-T_c}{T_c}\right)^{-1}$$

- Characterise by _another critical exponent_, with $\gamma=-1$ in this case:
$$\chi\propto |t|^{-1}$$

- The _scaling behaviour_ is the _same in both regimes_

- At _exactly_ the critical temperature, one can get the _critical isotherm_
	- _Ignore_ $b^2, bs$ terms but _not_ $s^3$
$$\displaylines{s\approx (\beta_cb+s)-\frac{1}{3}(\beta_cb+s)^3 \\ s(T=T_c,b)\approx\left(\frac{3b}{k_BT_c}\right)^{1/3}}$$
- This is characterised by _another critical exponent_, with $\delta=3$ in this case
$$M(T_c)\propto B^{1/\delta}$$

### Critical behaviour and universality class
- Typically, in _mean field theories_, properties _near critical points_ obey _power laws_:
$$\displaylines{M\propto|t|^\beta \\ \chi\propto|t|^\gamma \\ M(T_c)\propto B^{1/\delta}}$$
- Mean field theories are typically only accurate when a system has a _large number of neighbouring sites near each site_
	- Typically more accurate for high $d$
	- The _fluctuations become irrelevant_

- Systems with the _same set of critical exponents_ are said to be in the _same universality class_
	- Example: Ising model and _liquid-gas transition_

- System which are _scale invariant_ (all length scales are involved) are studied in _conformal field theories_

## Heisenberg model
- Also consider a _square lattice of identical spins_
- However, they are _free to rotate in three dimensions_ $\bm{s}_i=(\sin\theta\cos \phi,\sin \theta\sin \phi, \cos\theta)$
	- Only realistic for $d=3$
- The _Hamiltonian_ is then:
$$H=-\frac{J}{2}\sum_{i,\delta}\bm{s}_i\cdot\bm{s}_\delta-B\sum_i\hat{z}\cdot\bm{s}_i$$
- wlog, set $\mean{\bm{s}_i}\equiv\boldsymbol{s}=s\hat{z}$

- In the _mean field approximation_, with approximations $|\boldsymbol{s}_{i}-\boldsymbol{s} |\ll 1$, the Hamiltonian:
$$H=-(2dJs+B)\sum_{i} \hat{z}\cdot \boldsymbol{s}_{i}$$

- One then has to set the _partition function_ as:
$$\begin{aligned}
Z&=\sum_{\{s_{i}\}}\exp[-\beta H(\{s_{i}\})]\approx\left[\int  \exp[(2d\beta Js+\beta B)\cos\theta]\,d\cos\theta\,d\phi  \right]^N \\ &=(2\pi)^N \left[\int_{-1}^1 \exp
[(2d\beta Js+\beta B)x]dx \right]^N
\end{aligned}$$

- One can then get the _average spin_:
$$\begin{aligned}
\left<\boldsymbol{s}_{i}\cdot\hat{ z}\right> &=\frac{(2\pi)^N}{Z}\left[ \int_{-1}^1 \exp[(2d\beta Js+\beta B)x] \, dx  \right]^{N-1}\left[ \int_{-1}^1 x \exp[(2d\beta Js+\beta B)x]\, dx  \right] \\ &=\frac{\int  x \exp[(2d\beta Js+\beta B)x]\, dx }{\int \exp[(2d\beta Js+\beta B)x] \, dx }=-\frac{1}{\varepsilon+\beta B}+\coth(\varepsilon+\beta B) 
\end{aligned}
$$
- Here, $\varepsilon=2d\beta Js$

- One then gets the _self-consistent condition_:
$$
\varepsilon=2d\beta J\left[ -\frac{1}{\varepsilon+\beta B}+\coth(\varepsilon+\beta B) \right]
$$

- For $B=0$, using the same graphical technique, one finds:$$
T_{c}=\frac{2dJ}{3k_{B}}
$$
- One can find _the same critical exponents as the Ising model_
# Ginzburg-Landau theory
- One must describe the _degrees of freedom_ in the system
- Then specify the _symmetries_ and how they act upon the degrees of freedom

- One typically looks for _low energy degrees of freedom_
	- Takes less energy to _excite_
- Typically described by [[Classical Field Theory#Symmetry breaking|spontaneous symmetry breaking]]
	- If symmetry is broken by a state _in vacuo_, it costs _very little energy to fluctuate in symmetry directions_
- This leads to specification of an _order parameter_ for the system
	- _Macroscopically_ defined, corresponding to some _broken symmetry_
	- It is also a _field_ for the system
- This allows the tools of [[Classical Field Theory]] to be used
	- Lagrangian density $\to$ Hamiltonian
	- Action $\to$ Free Energy

- The _second-order phase transition_ is when a _disordered phase_ develops _continuously_ into some phase with _broken symmetry_
	- There are _many equivalent states_ with the same broken symmetry
- The _extent of broken symmetry_ is given by the _temperature_ $T$

- Example: in the Ising model, the _disordered phase_ is _invariant_ under $s_i\to-s_i$, and as $T<T_c$, the existence of _spontaneous magnetisation_ will _break_ this symmetry

## The free energy for a second-order phase transition
- Take some order parameter $m(\bm{x})\in\mathbb{R}$
- There should be some _symmetry_ such that $m\to-m$, the system is _invariant_

- Around the _phase transition_, assume $m$ and its derivatives are _small_
- Assume temperature is _near critical temperature_
- Assume the medium is _homogeneous_ and _isotropic_

- The most _general form_ of the _free energy_ $F$:
$$F=f(T)+\alpha(T)m^2+\frac{1}{2}\beta(T)m^4+\gamma(T)|\nabla m|^2$$
- Unlike in classical field theory, _all terms are positive-definite_
- Therefore at the _minimum_, $|\nabla m|=0$
![[Second order phase transition.png]]

- So at the _minimum_, one finds:
$$\overline{m}=0\;\;\;\text{ or }\;\;\;\overline{m}=\pm\sqrt{-\alpha/\beta}$$

- Expand functions in terms of $t=T/T_c-1$:
$$\displaylines{\alpha(t)=at+\dots \\ \beta(t)=b+\dots \\ c(t)=c+\dots}$$
- At $\alpha=0$, $T=T_c$, hence there is _no constant term_
	- Constructed _such that_ the transition occurs at $T=T_{c}$

- One then finds:
$$\overline{m}=\pm\left(\frac{a}{b}\right)^{1/2}\sqrt{T_c-T}\;\;\;\text{ for }\;T<T_c$$

- Add some _external field_ $B$:
$$F=f(T)+\alpha(T)m^2+\frac{1}{2}\beta(T)m^4+\gamma(T)|\nabla m|^2-mB$$
- This gives:
$$\displaylines{2a(T-T_c)\overline{m}+2b\overline{m}^3-B=0 \\ \chi=\begin{cases}1/[2a(T-T_c)]&\text{for }T>T_c\;\; (\overline{m}=0) \\ 1/[4a(T-T_c)] &\text{for }T<T_c\end{cases}}$$
- Similarly, one gets:
$$\overline{m}|_{T_c}\propto B^{1/3}$$
- One obtains the _same critical exponents_ as in the [[#Ising model]]

## Asymmetric first order phase transition
- Another free energy, with _no symmetry in reversing the order parameter_
- wlog, set _linear term to zero_
$$f=f_0+a(T-T_c)\rho^2+c\rho^3+\frac{b}{2}\rho^4$$
- $\rho$ can take _positive or negative values_

- As a function of _temperature_
![[Asymmetric free energy.png]]

- This gives a _discontinuous transition in order parameter_
	- Example: _melting_

## Symmetric first order phase transition
- Let there be a _negative quartic term_
- To ensure free energy is bounded above zero, include a _sextic term_:
$$f=f_0+a(T-T_c)m^2-\frac{b}{2}m^4+\frac{c}{3}m^6$$
![[Symmetric first order transition.png]]