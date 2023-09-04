- To describe states and the effect of _reactions_, one needs the tools of [[Classical Thermodynamics]]
- To understand what is happening and make calculations based on the states of _molecules_, one needs the tools of [[Statistical thermodynamics]]

# State variables and reversibility

## The first and second laws
- The _Second Law_ states that _any spontaneous process carries an increase in entropy_
- For an _infinitesimal process_, the change in entropy is:
$$dS=\frac{dq_\text{rev}}{T}$$
- $\dbar q_\text{rev}$ is the _heat under reversible conditions_
- For a reaction, one can separate the universe into the _system_ and the _surroundings_:
$$dS_\text{univ}=dS_\text{sys}+dS_\text{surr}$$

- The _First Law_ defines a state function, _internal energy_ $U$
- The differential is given by:
$$dU=\dbar q+\dbar w$$
- Here, $\dbar w$ is the work done _on_ the system
- $\dbar$ indicates that they are _path variables_, not state variables

- Linking to other state variables gives the _Master equation_, given _only in terms of state variables_
$$dU=TdS-pdV$$
- The _heat capacity at constant volume_ is defined as a partial derivative of $U$ w.r.t. $T$:
$$C_V=\left(\pd{U}{T}\right)_V$$
- Likewise, at _constant energy_, one gets:
$$\left(\pd{S}{V}\right)_U=\frac{p}{T}$$

## Thermodynamic functions

### Enthalpy
- One can define a new function, _enthalpy_:
$$\displaylines{H=U+pV \\ dH=T\,dS+V\,dp}$$
- From this, one can get that _$dH$ at constant pressure is equivalent to heat exchanged_

### Gibbs Free Energy
- If one considers breaking the universe into _system_ and _surroundings_, then consider the fact that _the surroundings are infinitely large_, hence _all heat exchanges are irrversible w.r.t. the surroundings_, hence:
$$dS_\text{surr}=-\frac{\dbar q_\text{sys}}{T}$$
- From this, one can define another thermodynamic function, the _Gibbs Free Energy_:
$$\displaylines{G=H-TS \\ dG=dH-T\,dS-S\,dT=V\,dp-S\,dT}$$
- Then, at _constant pressure and temperature_:
$$-\frac{dG_\text{sys}}{T}=dS_\text{sys}-\frac{\dbar q_\text{sys}}{T}=dS_\text{univ}$$
- From this, for a _spontaneous process at constant pressure and temperature_, $G$ _decreases_
- At _equilibrium_, $S$ is at a maximum and $G$ is at a minimum

### Helmholtz Free Energy
- The _Helmholtz Free Energy_ is defined as:
$$\displaylines{A=U-TS \\ dA=dU-T\,dS-S\,dT=-p\,dV-S\,dT}$$
- Following similar logic to above, at _constant volume and temperature_:
$$-\frac{dA_\text{sys}}{T}=dS_\text{sys}-\frac{dU}{T}=dS_\text{univ}$$
- From this, for a _spontaneous process at constant volume and temperature_, $A$ _decreases_

## Gibbs-Helmholtz relations
- From the definitions of $F$ and $G$, one can [[Classical Thermodynamics#Gibbs-Helmholtz relations|derive]] the _Gibbs-Helmholtz relations_:
$$\displaylines{U=-T^2\left(\pd{(A/T)}{T}\right)_V \\ H=-T^2\left(\pd{(G/T)}{T}\right)_p}$$

# Statistics and the Boltzmann distribution
- Detail: [[Statistical thermodynamics]]

## Microstates and macrostates
- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of _microstates_
	- The number of microstates is denoted $\Omega$
- Overall, the microstate of the system is the _multi-particle wave function_

- A *macrostate* is defined by the _bulk properties_ of the system, and _incorporates many microstates_
- Macrostates are described by _thermodynamic variables_ such as $U, N, V, S, T, p, \mu$
- For a macrostate with a particular $U$, there is a _very large number of microstates_ with different _distributions_ of energy among particles
- _Macrostates_ with energy more or less _equally shared_ among particles become way more likely (have _more microstates_)
	- Consequence of the equal probabilities postulate

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_ as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely 

- _Microstates_ can evolve _reversibly and deterministically with time_
- As time goes on, a _macrostate irreversibly tends to its mean_, which defines _statistical equilibrium_
- The _final_ macrostate will tend to be one with _the most number of microstates_
	- Consequence of the equal probabilities postulate, as the system _spends much more time_ in that macrostate

## Entropy
- The Boltzmann definition of entropy is:
$$S=k_B\ln\Omega$$
- Here, $\Omega$ is the _number of microstates_

- If two sub-systems $A,B$ have $\Omega_A$ and $\Omega_B$ microstates respectively, then $\Omega_\text{tot}=\Omega_A\Omega_B$
- Then, the entropy is _additive_: $S=S_A+S_B$

- Consider a system going from an _initial macrostate_ with $\Omega_\text{i}$ to a _final macrostate_ with $\Omega_\text{f}$
- The _ratio of probabilities_ for finding the system in the corresponding microstates is:
$$\begin{aligned}\frac{P_f}{P_i}=\frac{\Omega_f}{\Omega_i} =\exp(-\Delta S/k)\end{aligned}$$
- For $\sim1$ moles of gas, this would be the order of $\exp(-N_A)$

## Temperature
- Temperature is a variable _only defined at thermal equilibrium_
- A _statistical definition_: [[Statistical thermodynamics#Statistical view of temperature]]
$$\begin{aligned}\frac{1}{k_BT}&=\frac{d(\ln\Omega)}{dU} \\ T&=\left(\pd{U}{S}\right)_V\end{aligned}$$

## The Boltzmann distribution
- In chemistry, one usually considers a system _in thermal equilibrium with surroundings_
- This can be considered a small system _able to exchange energy with a much larger reservoir at constant temperature_

- Let the _energy including the reservoir_ be $E_\text{tot}$, and energy _of the system_ be $E_i<<E_\text{tot}$
- The _probability_ that the system has energy $\varepsilon$ is _proportional to the number of microstates of the reservoir_
- Using this fact, and doing a Taylor expansion:
$$\displaylines{\ln\Omega(E_\text{tot}-E_i)\approx\ln\Omega(E_\text{tot}) -E_i\frac{d\ln\Omega}{dE_\text{tot}}=\ln\Omega(E_\text{tot})-\frac{E_i}{k_BT} \\ P(E_i)\propto\exp\left(-\frac{E_i}{k_BT}\right)}$$
- The exponential $\exp(-E_i/k_BT)$ is known as the _Boltzmann factor_

- Using the fact that the probability is _normalised_:
$$\displaylines{P(E_i)=\frac{1}{Q_N}\exp\left(-\frac{E_i}{k_BT}\right) \\ Q_N=\sum_i\exp\left(-\frac{E_i}{k_BT}\right)}$$
- $Q_N$ is known as the _partition function_ of the system

- This expression for probability applies to the _microstate_ of the _entire system_
- It applies to _molecular energy levels if and only if_ the particles _do not interact_ (the energies are _independent_ of each other) 

# The partition function
- For a system with energy levels $\{E_i\}$, the _partition function_ $Q_N$ is:
$$Q_N=\sum_i\exp\left(-\frac{E_i}{k_BT}\right)$$

## Thermodynamic functions in terms of partition function
- The _internal energy_ $U$ is written as:
$$U=\sum_i P_iE_i=\frac{1}{Q_N}\sum_iE_i\exp\left(-\frac{E_i}{k_BT}\right)=k_BT^2\left(\pd{\ln Q_N}{T}\right)_V$$
- Thus, internal energy _can be derived from the partition function_

- Meanwhile, _entropy_ $S$ can be written as:
$$S=\frac{U}{T}+k_B\ln{Q_N}=k_BT\left(\pd{\ln Q_N}{T}\right)_V+k_B\ln Q_N$$
- This is proven from _another definition of entropy_, given [[Statistical thermodynamics|here]]
- From this, one can derive the expression for _Helmholtz Free Energy_ $A$:
$$A=-k_BT\ln{Q_N}$$
## Multi-particle systems
- In almost all cases, the system considered is one with _many particles_, each with _their own degrees of freedom and energy levels_

### Non-interacting, distinguishable particles
- If the energies of the particles are _independent of each other_:
$$E_\text{sys}=\varepsilon_i^{(A)}+\varepsilon_j^{(B)}+\varepsilon_k^{(C)}+\dots$$
- The _subscript_ is the _state of the particle_, while the _superscript_ is the _particle index_
- This is generally _only applicable to gases_
- In terms of the wave function, the system is _separable_:
$$\psi_\text{tot}=\psi_A\psi_B\psi_C\dots$$

- Then, the _partition function_ becomes:
$$Q_N=\sum_{i,j,k,\dots}\exp\left(-\frac{E_{\text{sys},i,j,k\dots}}{k_BT}\right)=\prod_\text{particles}\sum_i\exp\left(-\frac{\varepsilon_i}{k_BT}\right)=\prod_\text{particles}q$$
- Here, $q$ is the _molecular partition function_:
$$q=\sum_i\exp\left(-\frac{\varepsilon_i}{k_BT}\right)$$
- If there are $N$ _molecules with identical energy levels_:
$$Q_N=q^N$$

### Indistinguishable particles
- If the particles are _identical_, then for _every microstate with identical populations of each energy level_ will be the _same_
- For this reason, the partition function in this case is the one for _distinguishable particles_, _divided_ by the number of permutations:
$$Q_N=\frac{q^N}{N!}$$
- This generally applies to _molecules and atoms of the same type_
- This _does not apply to solids_, as the _lattice sites_ are distinguishable

## Effect of temperature and accessible states
- Express the energy levels in terms of difference from the _ground state_ energy $\varepsilon_0$:
$$\displaylines{\varepsilon_i=\varepsilon_0+\Delta_i \\ \begin{aligned}q&=\exp\left(-\frac{\varepsilon_0}{kT}\right)\left[1+\exp\left(-\frac{\varepsilon_1}{kT}\right)+\exp\left(-\frac{\varepsilon_2}{kT}\right)+\dots\right]\\&=\exp\left(-\frac{\varepsilon_0}{kT}\right)q' \\ q'&=1+\exp\left(-\frac{\varepsilon_1}{kT}\right)+\exp\left(-\frac{\varepsilon_2}{kT}\right)+\dots\end{aligned} \\ }$$
- For _high temperatures_, where $\Delta_i<<kT$, the _Boltzmann factors are nearly all $1$_
	- _All levels_ are roughly _equally populated_
	- Therefore, $q'\approx N$
- For _low temperatures_, where $\Delta_i>>kT$, the _Boltzmann factors nearly vanish_
	- Only the _ground state_ contributes significantly
	- Therefore, $q'\approx 1$

- Therefore, $q'$ is known as _the number of accessible states_
	- It is _roughly equal_ to the number of states that are _significantly populated_

### Approximation via integration
- Let the energy levels be some _function of a variable_ $i$:
$$\displaylines{\epsilon(i)=\epsilon_0+\Delta(i) \\ \\ q'=\sum_{i=0}^\infty \exp\left(-\frac{\Delta(i)}{k_BT}\right)}$$
- If the _temperature is high_, $k_BT>>\Delta(i)$, then the error from converting from a sum to integration becomes _less significant_:
$$q'\approx\int_0^\infty \exp\left(-\frac{\Delta(i)}{k_BT}\right)\,di \hspace{0.5cm}\text{ assuming } k_BT>>\Delta(i)$$
- This necessitates that $q'>>1$

## Thermodynamic quantities for multiple particles

### Distinguishable particles
- Using the expressions above:
$$\displaylines{\begin{aligned}Q_N&=q^N \\ \\ A&=-kT\ln Q_N \\ &=-NkT\ln q \\ \\ S&=-\left(\pd{A}{T}\right)_V \\ &=Nk\ln q+NkT\left(\pd{\ln q}{T}\right)_V \\ \\ U&=kT^2\left(\pd{\ln Q_N}{T}\right)_V \\ &=NkT^2\left(\pd{\ln q}{T}\right)_V\end{aligned}}$$
- This verifies the fact that $A,S,U$ are _extensive properties_, as they _scale with the number of particles_

### Indistinguishable particles
- For this, one needs to use _Stirling's approximation_:
$$\ln N!\approx N\ln N-N$$
- Using the expressions above:
$$\begin{aligned}Q_N&=\frac{q^N}{N!} \\ \\ A&=-kT\ln Q_N \\ &=-NkT\ln q+kT(N\ln N-N) \\ \\ S&=-\left(\pd{A}{T}\right)_V \\ &=Nk\ln q-Nk\ln N+Nk+NkT\left(\pd{\ln q}{T}\right)_V \\ \\ U&=kT^2\left(\pd{\ln Q_N}{T}\right)_V \\ &=NkT^2\left(\pd{\ln q}{T}\right)_V\end{aligned}$$
- Only _internal energy_ remains the same
- The additional terms in $A$ and $S$ represent a _loss in configurational entropy_ as there are _fewer microstates_

## Choice of energy zero
- Sometimes, one may want to express energies _relative to a ground state_, with energy $\varepsilon^0$:
$$\varepsilon_i'=\varepsilon_i-\varepsilon^0$$
- In this case, the partition function _gains a multiplicative factor_:
$$q=q'\exp\left(-\frac{\varepsilon^0}{k_BT}\right)$$
- The effect on _internal energy_ is:
$$U=NkT^2\left(\pd{\ln q}{T}\right)_V=NkT^2\left(\pd{\ln q'}{T}\right)_V+N\varepsilon^0$$
- The internal energy is simply _shifted_ by $N\epsilon^0$, since _nothing about the system itself has changed_, only the _reference energy_
- $N\epsilon^0$ can be identified as _the energy of the system at absolute zero_

- The _Helmholtz free energy_ has the same _corrective term_:
$$A=-NkT\ln q'+kT(N\ln N-N)+N\varepsilon^0$$

- Meanwhile, _entropy is unchanged_:
$$S=Nk\ln q'-Nk\ln N+Nk+NkT\left(\pd{\ln q'}{T}\right)_V$$
- This is expected as _choice of reference energy does not influence disorder_

## Degeneracy
- Many systems show _degeneracy_, where _distinct wave functions have the same energy_
	- Example: _multi-dimensional_ particle in a box, or harmonic oscillator

- The previous expression for partition function is a _sum over states_, so it still holds

- However, it is often evaluated as a _sum over energies_
- In this case, if energy $\varepsilon_j$ has _degeneracy_ $g_j$:
$$q=\sum_{\text{states }i} \exp\left(-\frac{\varepsilon_i}{k_BT}\right)=\sum_{\text{energies }j}g_j\exp\left(-\frac{\varepsilon_j}{k_BT}\right)$$
- In this case, the _number of accessible levels_ is still valid, as _degenerate levels are still distinct_

# Calculating the partition function
- To derive the properties of a multi-molecular system, one will need to compute the _partition function_, taking into account the _overall motion_ of the molecules, as well as their _internal degrees of freedom_

## Molecular degrees of freedom
- In general, all _degrees of freedom_ within the system consist of:
	- _Translational_ motion of the _molecules_ in space
	- _Rotational_ motion of the molecules themselves
	- _Vibrational_ motion of the _bonds_ in a molecule
	- _Electronic_ interactions between _electrons and nuclei_ in the molecule
- By the [[Molecular quantum mechanics#The Born-Oppenheimer approximation|Born-Oppenheimer approximation]], these modes are assumed to be _independent_
	- For example, the rotational constant is assumed to be _constant_ despite vibration
- In terms of the _wave function_ and _energies_:$$\displaylines{\psi_\text{mol}=\psi_\text{trans}\psi_\text{rot}\psi_\text{vib}\psi_\text{elec}\\ \varepsilon_\text{tot}=\varepsilon_\text{trans}+\varepsilon_\text{rot}+\varepsilon_\text{vib}+\varepsilon_\text{elec}}$$
	- Ignoring [[#Nuclear spin statistics|nuclear spin]]

- As the energies are _additive_, like the multi-particle case, the _molecular partition function_ becomes:
$$q_\text{tot}=q_\text{trans}\,q_\text{rot}\,q_\text{vib}\,q_\text{elec}$$

## Dealing with indistinguishable particles
- As $Q_N$ is a product of all of these functions, _thermodynamic functions_ such as $A$ and $S$ become _additive_:
$$A=-kT\ln Q^N=-kT\ln\frac{q^N}{N!}=A_\text{trans}+A_\text{rot}+A_\text{vib}+A_\text{elec}$$
- Usually, the $N!$ factor is _associated with_ $q_\text{trans}$:
$$\displaylines{A_\text{trans}=-kT\ln\frac{q_\text{trans}^N}{N!}=-NkT\ln q_\text{trans}+kT(N\ln N-N) \\ A_\text{rot}=-kT\ln q_\text{rot}^N=-NkT\ln q_\text{rot}}$$
	- Similarly for _vibrational_ and _electronic_ degrees of freedom

- Similarly, for _entropy_:
$$\displaylines{\begin{aligned}S_\text{trans} &=k\ln\frac{q_\text{trans}^N}{N!}+kT\left(\pd{\ln q_\text{trans}^N/N!}{T}\right)_V \\ &=Nk\ln q_\text{trans} -Nk\ln N+Nk+NkT\left(\pd{\ln q_\text{trans}}{T}\right)_V\end{aligned} \\ \\  S_\text{rot}=Nk\ln q_\text{rot}+NkT\left(\pd{\ln q_\text{rot}}{kT}\right)_V}$$
- For _internal energy_, the $N!$ _disappears after differentiation_:
$$U=kT^2\left(\pd{\ln q^N/N!}{T}\right)_V=NkT^2\left(\pd{\ln q}{T}\right)_V$$
- Hence, _all contributions have a similar formula_:
$$U_\text{trans}=NkT^2\left(\pd{\ln q_\text{trans}}{T}\right)_V$$

## Choice of energy zero
- For _translation_ and _rotation_, all _types_ of molecules _have a common energy zero_
- For _vibration_ and _electronic_, the _ground state energy_ relative to their "zero" _depends on the molecule_

## Translational partition function
- Model the _translational wave functions_ of the particles as the eigenstates of the [[Molecular quantum mechanics#Particle in a box|particle in a box]]
- In _one dimensional box_ of length $a$, for a particle of mass $m$, the energies are:
  $$E_n=\frac{n^2h^2}{8ma^2}$$
- To make calculating the partition function easier, _estimate_ how many levels will be _significantly occupied_:
$$\frac{n_\text{max}^2h^2}{8ma^2}\sim kT$$
- In typical conditions, $n\sim 10^9$
- Hence, replace the sum by an _integral_:
$$q_\text{trans, 1D}=\sum_{n=1}^\infty\exp\left(-\frac{E_n}{kT}\right) \approx \int_0^\infty \exp\left(-\frac{E_n}{kT}\right)\,dn$$
- The limit is _replaced_ with $0$ to simplify the integral
- The _hypothetical_ state with $n=0$ has zero energy, so no correction is required

- This gives:
$$q_\text{trans, 1D}=\frac{1}{2}\left(\frac{8mkT a^2\pi}{h^2}\right)^{1/2}=\left(\frac{2\pi mkT}{h^2}\right)^{1/2}a\equiv\frac{a}{\Lambda}$$
- $\Lambda$ is known as the _thermal wavelength_ of the system
- A _typical value_ for $\Lambda$ would be about $\sim 10^{-11}\,\text{m}=0.1\text{Å}$
 
- For a _three-dimensional_, _symmetrical_ box with sides of length $a$:
$$q_\text{trans,3D}=\left(\frac{2\pi mkT}{h^2}\right)^{3/2}a^3\equiv\frac{V}{\Lambda^3}$$
- As volume _increases_, the levels are _less densely spaced_, and _more levels are occupied_

## Rotational partition function for diatomics
- Here, the molecule is modelled as a [[Molecular quantum mechanics#The Rigid Rotor|Rigid Rotor]]:
$$\displaylines{E_J=BJ(J+1) \\ B\equiv\frac{\hbar^2}{2I}=\frac{\hbar^2}{2\mu R^2}}$$
- Here, $B$ is the _rotational constant_, $\mu$ is the _reduced mass_, and $R$ is the _bond length_
- $J$ is the _quantum number_, an integer dictating the _angular momentum_

- At each energy, there is a _degeneracy_ of $(2J+1)$ based on the _orientation_ of the molecule
- Hence, the partition function is:
$$\begin{aligned}q_\text{rot}&=\sum_{J=0}^\infty\,(2J+1)\exp\left(-\frac{BJ(J+1)}{kT}\right) \\ &=1+3\exp\left(-\frac{2B}{kT}\right)+5\exp\left(-\frac{6B}{kT}\right)+\dots\end{aligned}$$
- Assuming a _high temperature_ and integrating w.r.t. $dJ$, one gets:
$$\displaylines{q_\text{rot}=\frac{kT}{B}\equiv\frac{T}{\theta_\text{rot}} \\ \theta_\text{rot}\equiv\frac{B}{k}}$$
- $\theta_\text{rot}$ is known as the _rotational temperature_
- A typical value for diatomics is about $\sim 1-10\text{K}$

- This approximation is _only valid if_ $T>\theta_\text{rot}$
- Otherwise, the partition function must be evaluated using a _sum_

- For _homonuclear_ diatomics, as the nuclei are _indistinguishable_, this requires the introduction of a _symmetry parameter_:
$$q_\text{rot}=\frac{kT}{\sigma B}\equiv\frac{T}{\sigma\theta}$$
- The symmetry parameter is $1$ for _heteronuclear_ diatomics, and $2$ for _homonuclear_ diatomics
- Behaviour of the rotational partition function:
![[Rotational partition function.png|350]]

## Rotational partition function for non-linear molecules
- For all non-linear molecules, there are _three rotational constants_, each associated with a _principal axis_ of the molecule:
$$A=\frac{\hbar^2}{2I_a} \hspace{1cm} B=\frac{\hbar^2}{2I_b} \hspace{1cm} C=\frac{\hbar^2}{2I_c}$$
- Each rotational constant is _associated with a rotational temperature_:
$$\theta_{\text{rot},a}=\frac{A}{k}$$
- Then, for $T>>\theta_\text{rot}$, it can be shown that:
$$q_\text{rot}=\frac{1}{\sigma}\sqrt{\frac{\pi T^3}{\theta_{\text{rot,}a}\theta_{\text{rot,}b}\theta_{\text{rot,}c}}}$$

## Vibrational partition function
- Vibrating molecules are modelled as the [[Molecular quantum mechanics#Harmonic oscillator|quantum harmonic oscillator]]:
$$E=\left(\nu+\frac{1}{2}\right)\hbar\omega$$
- The _ground state_ has energy $\hbar\omega/2$

- If the energies are evaluated _relative to the ground state_:
$$q'_\text{vib}=1+\exp\left(-\frac{\hbar\omega}{kT}\right)++\exp\left(-\frac{2\hbar\omega}{kT}\right)+\dots$$
- By summing this up as a _geometric series_:
$$\displaylines{q_\text{vib}'=\frac{1}{1-\exp(-\hbar\omega/kT)}\equiv\frac{1}{1-\exp(-\theta_\text{vib}/T)} \\ \theta_\text{vib}=\frac{\hbar\omega}{k}}$$
- Here, $\theta_\text{vib}$ is the _vibrational temperature_
- Values have a _large range_ depending on the vibrational mode

- If the energies are summed up from the _bottom of the potential well_:
$$q_\text{vib}=\frac{\exp(-\hbar\omega/2kT)}{1-\exp(-\hbar\omega/kT)}\equiv\frac{\exp(-\theta_\text{vib}/2T)}{1-\exp(-\theta_\text{vib}/T)}$$
- This is an _exact formula_

- This is only the partition function for _one normal mode_
- For a _non-linear_ molecule with $N$ atoms, there are $3N-6$ vibrational modes
- For a _linear_ molecule with $N$ atoms, there are $3N-5$ vibrational modes

- Each normal mode has _its own set of energy levels_ which the molecule can occupy
- Hence, the _total vibrational partition function_ is:
$$q_\text{vib}=\prod_\text{modes} q_{\text{vib},j}$$
- If a mode is _degenerate_, it contributes _multiple identical partition functions_

### High and low temperature limits
- At low temperatures, $T<<\theta_\text{vib}$, the partition function is:
$$q_\text{vib}'(T\to0)\approx 1$$
- All particles are _at the ground state_

- At high temperatures, $T>>\theta_\text{vib}$, the partition function is _approximately linear_:
$$q_\text{vib}'(T>>\theta_\text{vib})\approx\frac{1}{1-(1-\theta_\text{vib}/T)}=\frac{T}{\theta_\text{vib}}$$
- At this point, $kT$ is _much larger than the energy spacing_, and the particles are able to occupy _many levels_

## Electronic partition function
- The set of energy levels must be determined by [[Molecular spectroscopy#Electronic spectroscopy|spectroscopy]]
- Many molecules have _degenerate electronic energy levels_
- Hence, the partition function can be written as:
$$q_\text{elec}=\sum_j g_j\exp\left(-\frac{E_{\text{elec},j}}{kT}\right)$$
- If they are measured _from the ground state_:
$$q_\text{elec}'=g_0+g_1\exp\left(-\frac{E_{\text{elec},1}}{kT}\right) +g_2\exp\left(-\frac{E_{\text{elec},2}}{kT}\right)+\dots$$
- In many cases, the temperature is not high enough to excite up to most states, and _only the ground state is significantly occupied_, hence $q_\text{elec}'\approx g_0$

- The _ground state energy_ will _depend on the molecule_
- This becomes important when calculating the [[#Chemical equilibrium|equilibrium constant]]

### Atoms
- The electronic states of atoms are characterised by the [[Molecular quantum mechanics#Terminology and term symbols|term symbols]]:
$$^{2S+1}L_J$$
- $L$ is the _total orbital angular momentum_, determined by the _subshell_
- $S$ is the _total spin angular momentum_
- $J$ is the _total angular momentum_
- Origins and details given [[Molecular quantum mechanics#Electron correlation|here]]

- The degeneracy of such a state is $2J+1$
	- Energy does not depend on $M_J$
- This will often be $q_\text{elec}'$ at reasonable temperatures

### Molecules
- Molecules also have [[Bonding in molecules#Molecular term symbols|term symbols]]:
$$^{2S+1}\Lambda_{g/u}^{\pm}$$
- Most molecules have _closed-shell configurations_, giving a degeneracy of 1
- However, there are exceptions, such as oxygen:
$$^3\Sigma_g^-$$
- It is _triply degenerate_

# Internal energy and heat capacity
- Each _degree of freedom_ of the molecules have _their own contributions_ to internal energy and heat capacity
- _Measuring_ heat capacity (at _constant volume_) throughout a _range of temperatures_ gives a series of _plateaus_:
![[Heat capacities.png]]

- These value on these plateaus are _the same for all diatomic molecules_
- However, the _temperatures_ at which they appear _vary_ according to the molecule

- At _low temperatures_, only the _translational_ energy levels can be significantly occupied
- As temperature rises, higher energy _degrees of feedom_ are excited

## Classical behaviour
- From [[Statistical thermodynamics|classical statistical thermodynamics]], the _equipartition principle_ states that for _each independent quadratic term in energy_, there is an _equal contribution_ to internal energy
	- Quadratic in terms of _position_ or _velocity_
- This assumes the energy spectrum is _continuous_, and all potentials are _quadratic_
- If a system has $N$ _quadratic terms in energy_, the internal energy _per mole_ is:
$$U=\frac{N}{2}RT=C_VT$$

- The three _translational_ kinetic energy components give $(3/2)RT$
- For a _diatomic_, the two _rotational_ kinetic energy components give $RT$
- For a _diatomic_, the _vibrational_ kinetic and potential energy components give $RT$

- Hence, at _high temperatures_, the expected heat capacity at _constant volume_ is:
$$C_V=\frac{7}{2}RT$$


## Translational contribution
- The [[#Translational partition function|translational partition function]] at temperature $T$ is:
$$q_\text{trans}=\left(\frac{2\pi mkT}{h^2}\right)^{3/2}\propto T^{3/2}$$
- Then calculating the internal energy:
$$U_\text{trans}=NkT^2\left(\pd{\ln q_\text{trans}}{T}\right)_V=\frac{3}{2}NkT$$
- This _matches_ the _equipartition_ prediction, as the partition function is _calculated with the assumption_ that $kT$ is much larger than the energy spacing

## Rotational contribution
- The [[#Rotational partition function|rotational partition function]] at temperature $T$ is:
$$q_\text{rot}=\frac{T}{\sigma\theta_\text{rot}}\propto T$$
- This gives the internal energy contribution:
$$U_\text{rot}=NkT$$
- This partition function is also calculated from the assumption that $kT$ is _much larger than energy spacing_

- At _very low temperatures_, as all particles are only at the _lowest_ energy level, the system _cannot absorb energy_, and heat capacity is near zero
- At _intermediate temperatures_, the heat capacity must be calculated _numerically_
![[Rotational heat capacity.png|500]]

- For _polyatomic molecules_, one needs to take into account that there are _three rotational degrees of freedom_, making the equipartition value $(3/2)NkT$

## Vibrational contribution
- The [[#Vibrational partition function|vibrational partition function]], measuring energy _from the ground state_, is:
$$q_\text{vib}'=\frac{1}{1-\exp(-\theta_\text{vib}/T)}$$
- This expression is _exact_ at any temperature
- This gives the internal energy:
$$U_\text{vib}'=\frac{Nk\theta_\text{vib}}{\exp(\theta_\text{vib}/T)-1}$$
- If measured _from the bottom of the well_, there is an extra term of $Nk\theta_\text{vib}/2$
- This has _no effect on heat capacity_, which can be evaluated to be:
$$C_{V,\text{vib}}=\frac{Nk\theta_\text{vib}^2}{T^2}\frac{\exp(\theta_\text{vib}/T)}{\left[\exp(\theta_\text{vib}/T)-1\right]^2}$$
### High and low temperature limits
- At _low temperature_, $T<<\theta_\text{vib}$, all particles are _at the ground state_, and are _unable to absorb energy_
$$U_\text{vib}'(T\to0)\approx 0 \hspace{1cm} C_{V,\text{vib}}(T\to0)\approx 0$$

- At _high temperature_, the internal energy and heat capacity _reach the equipartition values_:
$$U_\text{vib}'(T>>\theta_\text{vib})\approx NkT \hspace{1cm} C_{V,\text{vib}}(T>>\theta_\text{vib})\approx Nk$$
![[Rotational energy.png]]

## Electronic contribution
- At most _reasonable_ temperatures, only the _electronic ground state_ at energy $\varepsilon^0$ is ocupied
- Hence, the electronic contribution is simply:
$$U_\text{elec}\approx N\varepsilon^0 \hspace{1cm} C_{V,\text{elec}}\approx 0$$
# Entropy
- From the [[Classical Thermodynamics|Third Law]], the entropy of a _perfect crystal_ at _abolute zero_ is zero
- From that, the entropy is calculated by the definition of its infinitesimal:
$$dS=\frac{\dbar Q_\text{rev}}{T}$$
- From statistical thermodynamics, it can be derived from the partition function:
$$S=k\ln Q_N+T\left(\pd{\ln Q}{T}\right)_V=k\ln Q_N+\frac{U}{T}$$

## Different contributions
- As the partition function is multiplicative and energy is additive, entropy can be separated into _additive contributions_:
$$S_\text{tot}=S_\text{trans}+S_\text{rot}+S_\text{vib}+S_\text{elec}$$
- As the $1/N!$ factor is associated with the _translational partition function_, it is associated with _translational entropy_ as well

### Translational entropy
- Due to the $1/N!$ factor, the _translational entropy_ in terms of the _molecular translational partition function_, and _translational internal energy_ is:
$$\begin{aligned} S_\text{trans} &= Nk\ln q_\text{trans}-Nk\ln N+Nk+\frac{U_\text{trans}}{T} \\ &= Nk\left[\ln\left(\frac{2\pi mkT}{h^2}\right)^{3/2}V-\ln N+\frac{5}{2}\right]\end{aligned}$$
- This is also under the assumption that $kT$ is _much larger than energy spacing_

### Rotational entropy
- Again, assuming that $T>>\theta_\text{vib}$:
$$\begin{aligned}S_\text{rot} &= Nk\ln q_\text{rot}+\frac{U_\text{rot}}{T} \\ &= Nk\left(\ln\frac{T}{\sigma\theta_\text{rot}}+1\right)\end{aligned}$$
- This also only applies to _diatomics_

- For _polyatomics_, one needs to use the corresponding expressions for the [[#Rotational partition function for non-linear molecules|rotational partition function]] and internal energy

### Vibrational entropy
- As the expressions for the vibrational partition function and energy are more complicated, it is better to _calculate them separately_ before substituting:
$$S_\text{vib}=Nk\ln q_\text{vib}'+\frac{U_\text{vib}'}{T}$$
- If there are _multiple vibrational modes_, then the entropy of each mode is _additive_
- The entropy is _unaffected by the reference energy_, as long as $q$ and $U$ _share the same reference_

- If $T<<\theta_\text{vib}$, then as $q_\text{vib}'\approx 1$ and $U_\text{vib}'\approx0$, there is _zero entropy_

### Electronic entropy
- At reasonable temperatures, _approximately all particles are at electronic ground state_
- Hence, the entropy is:
$$S_\text{elec}=Nk\ln q_\text{elec}'+\frac{U_\text{elec}'}{T}\approx Nk\ln g_0$$
- This is the _configurational entropy_ from the number of degeneracies at the ground state

## Calorimetry
- The value of entropy can be obtained by _calorimetry_, which measures the _heat capacity_ at constant pressure for a _large range of temperatures_
- In addition, the material may undergo _phase changes_, such as melting or boiling, which take place at _constant temperature_, with an _enthalpy change_ $\Delta H_{pc}$ for the change
- The entropy change of this phase transition is:
$$\Delta S_\text{pc}=\frac{\Delta H_\text{pc}}{T_{pc}}$$
- Then, the value is given by a _numerical integration_, relative to _absolute zero_:
$$S(T)=\int_0^T \frac{C_p(T')}{T'}\,dT'+\sum_\text{pc} \frac{\Delta H_\text{pc}}{T_\text{pc}}$$

## Behaviour at low temperatures
- At low temperatures, it becomes _difficult to measure_ $C_p$
- However, in most cases, the heat capacity at temperatures near absolute zero follow the [[Electrons in solids|Debye Law]]:
$$C_p=\alpha T^3$$
- Hence, $\alpha$ is extrapolated and used to calculate $\Delta S$ at low temperatures

- Aside from this, for many _asymmetrical molecules_, there is a _residual entropy_ that causes an _underestimation in the calorimetric value_ compared to the computational value

- This is due to the fact that even at low temperatures, there is some _randomness in the crystal structure_ that is "frozen-in"
	- Theoretically, the _ordered structure_ is only attainable at _absolute zero_, which is unreachable
![[Residual entropy.png]]

- The residual _configurational_ entropy is given by:
$$S_\text{res}=k\ln n_g^N=Nk\ln n_g$$
- Here, $n_g$ is the _number of configurations_ a molecule can take in a crystal
	- Example: $2$ for _asymmetrical diatomics_ like $\text{CO}$, $4$ for $\text{CH}_3\text{Cl}$

# Nuclear spin statistics
- The total _molecular wave function_ does not only of _molecular motion_ and the _electronic wave function_, but also _nuclear spin_ as well
- From the [[Molecular quantum mechanics#The Born-Oppenheimer approximation|Born-Oppenheimer approximation]], all the wave functions are _separable_:
$$\Psi=\psi_\text{trans}\psi_\text{rot}\psi_\text{vib}\psi_\text{elec}\psi_\text{nuc, spin}$$
- Discussion is restricted to _homonuclear diatomics_ and _symmetric, linear triatomics_

## Nuclear spin wave functions
- A nucleus is characterised by a _nuclear spin quantum number $I$_, which can have _integer or half-integer_ values
- The nuclear spin has a _component_ along some direction, characterised by quantum number $m_I$, which can take $(2I+1)$ values from $-I$ to $I$

- From the [[Molecular quantum mechanics#Pauli Principle|Pauli Principle]], for molecules with _equivalent nuclei_, with respect to the operation of _swapping nuclei_, the _overall_ wave function must be _symmetric_ if the nuclei are _bosons_, and _antisymmetric_ if the nuclei are _fermions_

- For a _homonuclear diatomic_, there are a total of $(2I+1)^2$ nuclear spin states
	- $(I+1)(2I+1)$ are _symmetric_, including $(2I+1)$ where the nuclei have identical $m_I$
	- $I(2I+1)$ are _antisymmetric_

## Swapping nuclei
- The operation of _swapping labels of nuclei_ must also _keep all other labels and coordinates the same_
- Hence, _multiple symmetry operations_ are required to do this:
![[Nuclei swap.png]]

- The _vibrational_ and _translational_ wave functions are _wholly unaffected_ by any of these operations
	- For _diatomics_, the vibrational wave function is always _totally symmetric_
- The _nuclear spin_ wave function is _only affected by_ $p_\text{nuc}$, which has the effect of _swapping labels in the spin wave function only_
	- Depends on if the spin wave function is _symmetric_ or _antisymmetric_
- The _rotational_ wave function is _only affected by_ $C_2$
	- Since the _angular part_ is a _spherical harmonic_, it is _symmetric_ w.r.t. _even_ $J$, and being _antisymmetric_ w.r.t. _odd_ $J$
- The _electronic_ wave function is affected by $i_\text{elec}$ and $\sigma_\text{v, elec}$
	- The effect of $i_\text{elec}$ is dependent on the $g/u$ label in the [[Bonding in molecules#Molecular term symbols|molecular term symbol]]
	- Similarly, the effect of $\sigma_\text{v, elec}$ is given by the $\pm$ label

## Spin $1/2$: Ortho- and para-hydrogen
- _Hydrogen nuclei_ have a nuclear spin of $1/2$, making them _fermions_, so that the _overall_ wave function must be _anti-symmetric w.r.t. swapping nuclei_
- This gives _one anti-symmetric_, and _three symmetric spin states_
- It has a ground state molecular term symbol of $^1\Sigma_g^+$, making it _symmetric_ with respect to $i_\text{elec}$ and $\sigma_\text{v, elec}$
- Hence, the only wave functions which are _antisymmetric w.r.t. swapping nuclei_ are:
	- An _even_ $J$ with an _antisymmetric nuclear spin function_, known as _para-hydrogen_
	- An _odd_ $J$ with a _symmetric nuclear spin function_, known as _ortho-hydrogen_

- Typically, while hydrogen molecules can _change rotational energy levels_, the _nuclear spin state is unchangeable_ without breaking the $\text{H}-\text{H}$ bond
- As they occpy _different energy levels_, they end up with _different physical properties_, such as internal energy and heat capacity
- Therefore, ortho- and para-hydrogen are _separable_

- By using a _paramagnetic catalyst_ that can break the $\text{H}-\text{H}$ bond, at _low temperatures_, one can make a sample of _pure para-hydrogen_, as it occupies the _lower energy_ $J=0$ state

- The _populations_ of ortho- and para-hydrogen as a function of the values of $J$ are:
$$\begin{aligned}N(\text{ortho, odd J})&\propto 3(2J+1)\exp\left(-\frac{BJ(J+1)}{kT}\right) \\ N(\text{para, even J})&\propto (2J+1)\exp\left(-\frac{BJ(J+1)}{kT}\right)\end{aligned}$$
- A consequence of this is _peaks of alternating $3:1$ intensity in the Raman spectrum_, modulated by an _envelope_
	- As $\Delta J=\pm2$ in Raman spectra, the _symmetry of the wave function does not change_
- This behaviour can also be seen in $^{15}\text{N}$, which also has a spin of $1/2$
- Comparing the Raman spectra of $^{14}\text{N}^{15}\text{N}$ and $^{15}\text{N}_2$:
![[Nitrogen Raman spectra.png]]

## Spin $1$: $^{14}\text{N}_2$
- $^{14}\text{N}$ nuclei have a spin of 1
- This gives $6$ _symmetric_ and $3$ _anti-symmetric spin states_
- Since the nuclei are _bosons_, this means the _overall wave function is symmetric_
- It also has an electronic ground term of $^1\Sigma_g^+$

- Hence, _even_ $J$ accompany _symmetric nuclear spin states_, and _odd_ $J$ accompany _anti-symmetric nuclear spin states_

- This gives an alternating $6:3:6:3$ intensity ratio in the Raman spectrum

## Spin zero: $^{16}\text{O}_2$
- In the case of $I=0$ (such as in $^{16}\text{O}$ and $^{12}\text{C}$), _there is no nuclear spin state_
	- Therefore, the effect of $p_\text{nuc}$ is entirely _omitted_
- Spin zero nuclei are always _bosons_

- The term symbol for the electronic ground state is $^3\Sigma_g^-$
	- Symmetric w.r.t. $i_\text{elec}$, anti-symmetric w.r.t. $\sigma_\text{v, elec}$
- From the fact that the nuclei are bosons, _only states with odd $J$ are allowed to exist_
- Hence, in the Raman spectrum, _only lines of odd $J$ are seen_

## A more complex case: $^{12}\text{C}^{16}\text{O}_2$
- Only the _oxygen nuclei are equivalent_ and should be considered when swapping
- The term symbol for the electronic ground state is $^1\Sigma_g^+$
- Hence, _only states with even $J$ are allowed to exist_ in the vibrational _ground state_

- The _symmetric stretch_ is Raman active, and as the _vibrational_ wave function in this case is _symmetric_, lines of _even $J$_ are seen
- The _antisymmetric stretch_ is IR active, and as the _vibrational_ wave function transitions from _symmetric to antisymmetric_ (and vice versa), $\Delta J=\pm1$ lines can be seen in the _rotational fine structure_

## Rotational partition function
- When considering _homonuclear diatomics_, the _nuclear spin partition function_ is "intertwined" with the _rotational partition function_, therefore they are often _considered together_
- For _heteronuclear diatomics_, they are _separable_:
$$\begin{aligned}q_{NS}q_\text{rot}&=(2I_1+1)(2I_2+1)\left[\sum_J(2J+1)\exp\left( -\frac{BJ(J+1)}{kT}\right) \right] \\ &=(2I_1+1)(2I_2+1)\frac{T}{\theta_\text{rot}}\end{aligned}$$

- For _homonuclear diatomics_, odd and even $J$ values have to be considered _separately_:
$$\begin{aligned} q_{NS}q_\text{rot}&=g_{NS\text{, even}}\sum_\text{even J}(2J+1)\exp\left( -\frac{BJ(J+1)}{kT}\right) \\ &\hspace{0.4cm}+ g_{NS\text{, odd}}\sum_\text{odd J}(2J+1)\exp\left( -\frac{BJ(J+1)}{kT}\right) \end{aligned}$$
- Here, $g_{NS}$ is the number of _spin states compatible with even or odd $J$_

- In the _high temperature limit_ $T>>\theta_\text{rot}$, the two sums are _equal_ and equal to $T/(2\theta_\text{rot})$:
$$q_{NS}q_\text{rot}=(g_{NS\text{, odd}}+g_{NS,\text{ even}})\frac{T}{2\theta_\text{rot}}$$

- In most cases, $g_\text{NS}$ is _not considered_, as it _does not affect energy and entropy_, and _cancels out in equilibrium constants_
- Hence, the _symmetry factor_ $\sigma$ is introduced in the rotational partition function to account for this:
$$q_\text{rot}=\frac{T}{\sigma\theta_\text{rot}}$$
- The symmetry factor is equal to _the number of equivalent nuclei_ in the molecule
- The _more equivalent nuclei_, the _fewer rotational states_ are available to the molecule

# Reactions and equilibrium
- Consider the reaction below:
$$\ce{\nu_AA + \nu_BB<=> \nu_MM + \nu_NN}$$
- Starting from a mixture of $A$ and $B$, the reaction will _proceed until equilibrium is reached_, with some _mixture_ of $A$, $B$, $M$, and $N$
- Equilibrium is reached at constant pressure when _Gibbs Free Energy is at a minimum_
	- [[Classical Thermodynamics#Availability and variational principles|Variational Principles in Classical Thermodynamics]]

- Assume each component is _non-interacting_, hence the Gibbs Free Energy is _additive_

## Chemical potential and equilibrium
- Given a _mixture_ of components, each with number of moles $n_i$, the _Gibbs Free Energy_ of the whole mixture is:$$G=\sum_i \mu_in_i \hspace{1cm} dG=\sum_i \mu_i\,dn_i$$
	- $\mu_i$ is the _chemical potential_ of the component
	 - Gibbs Free Energy is _additive_, and $G=\mu n$ for one component
		- [[Classical Thermodynamics#Scaling the system|Derivation]]

- The chemical potential can also be defined using the _Helmholtz Free Energy_:
$$\mu_i=\left(\pd{A}{N_i}\right)_{V,T,n_j}$$
- All components in the mixture have _different ground state energies_
- When considering a reaction, one must use a _common origin for all components_
	- Hence, the equilibrium depends on the _energy difference_

- A ground state energy $\varepsilon^{0,i}$ gives an _additive constant_ $N_i\varepsilon^{0,i}$ to $A$

- As the _particles for each component are indistinguishable_, the chemical potential _per particle_ is:
$$\begin{aligned} \mu_i&=\pd{}{N_i}\left[-N_ikT\ln q_i+kT(N_i\ln N_i-N_i)+N_i\varepsilon^{0,i}\right] \\ &= -kT\ln\frac{q_i}{N_i}+\varepsilon^{0,i}\end{aligned}$$

### Changes in chemical potential and solution activity
- Modelling species $i$ as an _ideal gas_, at _constant $T$ and $N_i$_, the _change in $G$_ due to a change in its _partial pressure_ $p_i$ is:
$$\Delta G=\int V\,dp=nRT\ln\frac{p_{i,2}}{p_{i,1}}$$
- By setting $p_{i,1}$ as the _standard pressure_ $p^⦵=1\,\text{bar}$ , with a corresponding $G^0$, and dividing by $n$, the _change in chemical potential per mole_ can be written as:
$$\mu_i=\mu^⦵_i+RT\ln\frac{p_i}{p^⦵}$$

- This formula can also be applied to _solutions_, defining the quantity known as _activity_ $a_i$:
$$\mu_i=\mu^⦵_i+RT\ln a_i$$
- For _low concentrations_, the activity can be approximated as _concentration relative to a standard_ $c^⦵=1 \,\text{molecule m}^{-3}$:
$$a_i\approx\frac{c_i}{c^⦵}$$
- This _standard $c^⦵$_ is chosen as the partition functions and chemical potentials are _defined per molecule_

## The reaction
- Suppose there is an _arbitrary mixture_, which is _not at equilibrium_
- Let the reaction proceed by some _amount_ $dz$, with $n_A$ _decreasing_ by $\nu_A\,dz$, similarly for other species
- Hence, the _rate of change of Gibbs energy_ is:
$$\frac{dG}{dz}=+\nu_M\mu_M+\nu_N\mu_N-\nu_A\mu_A-\nu_B\mu_B$$
- At _equilibrium_, Gibbs energy is at a _minimum_, and $dG/dz=0$:
$$\nu_M\mu_M^\text{eq}+\nu_N\mu_N^\text{eq}=\nu_A\mu_A^\text{eq}+\nu_B\mu_B^\text{eq}$$
- All of the chemical potentials are at their _equilibrium values_

### Change in Gibbs Free Energy
- By using the formula for chemical potentials in terms of $p$ or $a\approx c/c^⦵$:
$$\displaylines{\Delta_rG=\Delta_rG^⦵+RT\ln Q \\ \Delta_rG^⦵=\nu_M\mu_M^⦵+\nu_N\mu_N^⦵-\nu_A\mu_A^⦵-\nu_B\mu_B^⦵ \\ Q=\frac{p_M^{\nu_M}p_N^{\nu_N}}{p_A^{\nu_A}p_B^{\nu_B}}\left(\frac{1}{p^⦵}\right)^{\Delta\nu} \text{ or } \frac{c_M^{\nu_M}c_N^{\nu_N}}{c_A^{\nu_A}c_B^{\nu_B}} \left(\frac{1}{c^⦵}\right)^{\Delta\nu}}$$
- The quantity in the natural logarithm is the _reaction quotient_, $Q$
- $\Delta\nu$ is defined as:
$$\Delta\nu\equiv\nu_M+\nu_N-\nu_A-\nu_B$$

- As long as $\Delta_rG<0$, the reaction will _proceed forwards_ in order to _minimise_ $G$

## Equilibrium constants
- Given the _concentrations_ of each species at _equilibrium_, the _equilibrium constant_ is a _dimensionless quantity_, which gives an _indication_ of the equilibrium position

- In _equilibrium_, $\Delta_rG=0$, so there is _no driving force_ for the reaction:
$$\Delta_rG^⦵=-RT\ln K$$
- $K$, which is the _reaction quotient at equilibrium_, is defined as the _equilibrium constant_
- It can be written as $K_c$ or $K_p$:
$$K_p=\frac{p_M^{\nu_M}p_N^{\nu_N}}{p_A^{\nu_A}p_B^{\nu_B}}\left(\frac{1}{p^⦵}\right)^{\Delta\nu} \hspace{1cm} K_c=\frac{c_M^{\nu_M}c_N^{\nu_N}}{c_A^{\nu_A}c_B^{\nu_B}} \left(\frac{1}{c^⦵}\right)^{\Delta\nu}$$
- The relation between them can be written as:
$$K_c=K_p\left(\frac{p^⦵}{c^⦵kT}\right)^{\Delta\nu}$$

### van't Hoff equation
- Using the definition of $G$, $\Delta_rG$ can also be written as:
$$\Delta_rG^⦵=\Delta_rH^⦵-T\Delta_rS^⦵$$
- Using the [[#Gibbs-Helmholtz relations]]:
$$\left(\pd{(\Delta_r G^⦵/T)}{T}\right)_p=-\frac{\Delta_rH^⦵}{T^2}$$
- This then gives the _van't Hoff equation_:
$$\frac{d\,\ln K}{dT}=\frac{\Delta_rH^⦵}{RT^2}$$
- Here, $K_c$ should be used for _solutions_ and $K_p$ should be used for _gases_

- Using the relation between $K_c$ and $K_p$, one can write that in a _gaseous medium_:
$$\frac{d\,\ln K_c}{dT}=\frac{\Delta_rH^⦵-\Delta\nu RT}{RT^2}$$


### K_c and K_p in terms of partition functions
- In order to rewrite chemical potential _in terms of concentration_:
$$\mu_i= -kT\ln\frac{q_i}{N_i}+\varepsilon^{0,i}= -kT\ln\frac{f_i}{c_i}+\varepsilon^{0,i}$$
- Here, $f_i$ is the _volume-independent partition function_:
$$f=\frac{q}{V}=\frac{q_\text{trans}}{V} q_\text{rot} q_\text{vib} q_\text{elec}=\left(\frac{2\pi mkT}{h^2}\right)^{3/2}q_\text{rot}q_\text{vib}q_\text{elec}$$
- One must choose a _common origin in energy_, in this case it is chosen to be the _energy of dissociated atoms_
- For convenience, take $q_\text{vib}$ _from the bottom of the vibrational energy well_, which, relative to the dissociated atoms, has the _ground state electronic energy_:
$$q_\text{vib}=\frac{\exp(-\theta_\text{vib}/2T)}{1-\exp(-\theta_\text{vib}/T)}$$

- Then, defining the _difference in ground state electronic energy_: $$\Delta \varepsilon_0=\nu_M\varepsilon^{0,M}+\nu_N\varepsilon^{0,N}-\nu_A \varepsilon^{0,A}-\nu_B\varepsilon^{0,B}$$
	- This takes into account the _energy zeroes in_ $q_\text{elec}$

- One can then _rewrite concentrations in terms of $\mu$_, then find $K_c$:
$$K_c=\frac{f_M^{\nu_M}f_N^{\nu_N}}{f_A^{\nu_A}f_B^{\nu_B}}\left(\frac{1}{c^⦵}\right)^{\Delta\nu} \exp\left(-\frac{\Delta\varepsilon_0}{kT}\right)$$

- Alternatively, for $K_p$, using the _standard chemical potential per mole_:
$$\mu_i^⦵=-RT\ln\frac{q_i^⦵}{N_A}+N_A\varepsilon^{0,i}$$
- Here, the partition function is _in the standard state_:
$$q_i^⦵=\left(\frac{2\pi mkT}{h^2}\right)^{3/2}\left(\frac{RT}{p^⦵}\right)q_\text{rot}q_\text{vib}q_\text{elec}$$
- Then, one can obtain an expression for $K_p$:
$$K_p=\frac{(q_M^⦵)^{\nu_M}(q_N^⦵)^{\nu_N}}{(q_A^⦵)^{\nu_A}(q_B^⦵)^{\nu_B}}\left(N_A\right)^{-\Delta\nu}\exp\left(-\frac{\Delta\varepsilon_0}{kT}\right)$$

### Interpretation
- Consider a simple reaction: $$\ce{A<=>M}$$
- The equilibrium constant is then:
$$K_c=\frac{f_M}{f_A}\exp\left(-\frac{\varepsilon^{0,M}-\varepsilon^{0.A}}{kT}\right)$$
- At _low temperatures_: 
	- $f_M\approx f_A\approx1$, as molecules only occupy their respective _ground states_
	- Molecules are _unlikely to interconvert_ due to the large _ground state energy difference_

- As temperature _rises_: 
	- $\exp(-\Delta\varepsilon_0/kT)$ becomes _less significant_
	- The $f_M/f_A$ factor starts to _dominate_
	- Molecules are more likely to interconvert to the _side with more densely packed states_, in order to _maximise entropy_

### Example: Dissociation of a diatomic
- Consider the reaction: $$\ce{A_2<=>2A}$$
- The expression for $K_c$ is then:
$$K_c=\frac{f_\ce{A}^2}{f_\ce{A_2}}\frac{1}{c^⦵}\exp\left(-\frac{D_e}{kT}\right)$$
- Measuring energy _relative to that of two dissociated atoms_, $\Delta\varepsilon_0=D_e$

### Example: Ionisation of atoms
- Consider the _gas phase ionisation_ of a metal ion:
$$\ce{M(g)<=>M+(g) +e-}$$
- The difference in ground state energies is simply the _ionisation energy_ $E_I$:
$$K_c=\frac{f_\ce{e}f_{\ce{M+}}}{f_\ce{M}}\frac{1}{c^o}\exp\left(-\frac{E_I}{kT}\right)$$
- The _translational_ partition functions of the atom and the ion _approximately cancel_
- One only has to consider their _electronic ground state degeneracies_
- For the electron, its degeneracy is 2 due to _spin_
- Taking its translational partition function into account as well:
$$K_c=\left(\frac{2\pi m_e kT}{h^2}\right)^{3/2}\frac{2g_{0,\ce{M+}}}{g_{0,\ce{M}}}\exp\left(-\frac{E_I}{kT}\right)$$

## Adsorption of a gas and the Langmuir isotherm
- Consider the _adsorption_ of a gas onto some surface
- Assumptions:
	- The surface has a _fixed number_ of sites $M$, which can only absorb _one molecule each_

- Let there be $N$ adsorbed molecules at one time
- In _equilibrium_, the _rates of adsorption and desorption are equal_
- The rate of adsorption is proportional to pressure, hence one can write:
$$k_a(M-N)p=k_dN$$
- Defining $\theta=N/M$ as the _proportion of sites occupied_:
$$\theta=\frac{K_\text{ads}p}{1+K_\text{ads}p} \hspace{1cm} K_\text{ads}=\frac{k_a}{k_d}$$
- At _large pressures_, or $pK_\text{ads}>>1$, _most sites are occupied_

- At equilibrium, the _chemical potentials are equal_:
$$\mu(\text{ads})=\mu(\text{g})$$
- For the _free gas_, assume it is _monoatomic_, hence:
$$\mu(\text{g})=-kT\left(\frac{q_\text{trans}}{N_\text{gas}}\right)+\varepsilon_\text{free}^0=-kT\ln\left(\frac{kT}{p\Lambda^3}\right)+\varepsilon_\text{free}^0$$
- As for the _adsorbed gas_, consider the _number of ways $N$ molecules can be adsorbed_, and assume they _all have the same energy_:
$$Q_N=\frac{M!}{N!(M-N)!}$$
- Then the chemical potential can be derived:
$$\displaylines{A=-kT\ln Q_N \\ \mu(\text{ads})=\left(\pd{A}{N}\right)_V+\varepsilon_\text{ads}^0=kT\ln\left(\frac{\theta}{1-\theta}\right)+\varepsilon_\text{ads}^0}$$
- Rearranging, this gives:
$$\displaylines{\Delta\varepsilon^0=\varepsilon_\text{ads}^0-\varepsilon_\text{free}^0 \\ \theta=\frac{bp}{1+bp} \hspace{1cm} b=\frac{\Lambda^3}{kT}\exp\left(-\frac{\Delta\varepsilon^0}{kT}\right)}$$
- If the molecules had _internal degrees of freedom_, the form of $\theta$ would likely be different
- This is the _same form_ as from the kinetics argument

- As $\Lambda=h/\sqrt{2\pi mkT}$, $b$ _decreases for larger atoms_
	- This is an _entropic effect_ as the energy levels of the gas are _closer_ and its entropy increases
- In most cases, the _exponential term dominates_ in $b$
- As $\Delta\varepsilon^0$ becomes _more negative_, $b$ increases

# Kinetics
- Thermodynamics deals with _what the equilibrium state is like_
- Kinetics deals with _how fast equilibrium is reached_

## Potential energy surfaces and transition states
- As a reaction between molecules proceeds, and electrons and nuclei _rearrange_, the _potential energy changes_
- The _potential energy surface_ (PES) of the system specifies the _potential energy as a function of nuclear coordinates_
	- Often _multi-dimensional_, as each additional atom adds 3 additional _degrees of freedom_

- The surface will have _minima_, which correspond to _arrangements that give stable molecules_
	- The molecule can _oscillate_ sround the stable position
- As the nuclei are _infnitely far apart_, the molecule has _zero energy_
- As any nuclei become _close to each other_, the energy _tends to infinity_

- _Example_: $$\ce{A +BC->AB +C}$$
	![[PES.png]]
	- One can draw a perspective view, or a _contour plot_, where paths _perpendicular_ to the contours are _uphill/downhill_
	- There are "valleys" corresponding to an _equilibrium bond length_ for either $r_\ce{AB}$ or $r_\ce{BC}$
	- They _connect_ at one point to form a "pass", which has a _higher energy_ than all other points in the valley
	- For _large internuclear distances_, there is a _plateau_ in energy
	- Any _cross-section_ at _constant_ $r_\ce{AB}$ or $r_\ce{BC}$ will form a familiar _PE curve_

- The _reaction pathway_ of two molecules can be charted as a _path on the PES_
- The _starting_ and _end-points_ are the _potential minima corresponding to reactants and products_, with many _possible paths_ connecting them
- Example: $$\ce{A +BC->AB +C}$$
	![[PES possible paths.png]]
	- Path 1: _Dissociation_ of the atoms before forming the product
	- Path 2: _Compressing_ both distances before dissociating into the product
	- Path 3: Around the _side_ of the valley
	- Path 4: Through the _centre_ of the "valley", taking the _last energy_ pathway

- For each reaction, there is a _pathway with least expenditure of energy_

- The least-energy pathway will still involve some _potential maximum_
	- It may be a _saddle point_ overall, but _along the path_, it is a maximum
- This is the _transition state_, corresponding to _partial breakage and formation of bonds_
	- It _does not correspond to a stable molecule_, and exists for $\sim 10^{-13}\,\text{s}$
	- It is distinct from the _reaction intermediate_, which exists in a _minimum_ and is an actual molecule
- The _vast majority_ of molecules will travel via this pathway, as any _alternative route_ will require more energy that the molecules do not have

- The _coordinate_ which maps the _least-energy pathway_ is the _reaction coordinate_
- It is some _linear combination of nuclear displacements_
- The PES _along the reaction coordinate_ is known as the _reaction profile_:
![[Reaction coordinate.png|500]]


## Transition state theory
- Since the _activation energy_ is high, _very few molecules_ actually get there
- Once the reactants _reach the transition state_, it takes _a smaller, but finite time_ to transform into the _products_
- In that time, the transition state is also _likely to transform back into the reactants_
- In other words, the reactants reach an _equilibrium with the transition state_
- This can be expressed as follows:
$$\ce{A + BC<=> TS-> AB + C}$$

- Assuming _equilibrium_ between the reactants and transition state:
$$K^*=\frac{c^⦵[\ce{TS}]}{[\ce{A}][\ce{BC}]}$$
- The _rate of conversion to products_ is assumed to be _first-order_ w.r.t. $\text{TS}$:
$$r=k_\text{1st}[\ce{TS}]=k_\text{1st}\frac{K^*}{c^⦵}[\text{A}][\text{BC}]$$
- Hence, one can define a _second-order rate constant_:
$$\displaylines{r=k_\text{2nd}[\ce{A}][\ce{BC}] \\ k_\text{2nd}\equiv \frac{1}{c^⦵}k_\text{1st}K^*}$$

## Deriving the rate constant
- From the expression for the equilibrium constant:
$$K^*=\frac{c^⦵f_\text{TS}}{f_\ce{A}f_\ce{BC}}\exp\left(-\frac{\Delta\varepsilon_0^\ddagger}{RT}\right)$$
- For $f_\ce{TS}$, one note that one of its _vibrational normal modes_ corresponds to _motion along the reaction coordinate_
	- Since it is at a _maximum_, there is _no restoring force_, and the molecule simply _transforms into the product_
	- For $\ce{A +BC->AB +C}$, this corresponds to the _asymmetric stretch_ 
- Let the frequency of this normal mode be $\nu^\ddagger$, and _factor out its vibrational partition function_:
$$\displaylines{K^*=\frac{c^⦵q^\ddagger f_\ce{TS}'}{f_\ce{A}f_\ce{BC}}\exp\left(-\frac{\Delta\varepsilon_0^\ddagger}{RT}\right)\equiv q^\ddagger K^\ddagger \\ q^\ddagger=\frac{\exp(-h\nu^\ddagger/2kT)}{1-\exp(-h\nu^\ddagger/kT)} \hspace{1cm} }$$
- As this frequency corresponds to _dissociation_. $h\nu^\ddagger<<kT$, hence one gets:
$$K^*=\frac{kT}{h\nu^\ddagger}\frac{c^⦵f'_\text{TS}}{f_\ce{A}f_\ce{BC}}\exp\left(-\frac{\Delta\varepsilon_0^\ddagger}{RT}\right)$$
- The _first-order rate constant_ is the _rate of dissociation_, hence:
$$k_\text{1st}=\nu^\ddagger$$
- From this:
$$\displaylines{r=k_\text{1st}[\ce{TS}]=k_\text{2nd}[\ce{A}][\ce{BC}] \\ k_\text{2nd}=\frac{1}{c^⦵}k_\text{1st}K^*=\frac{kT}{h}\frac{f'_\text{TS}}{f_\ce{A}f_\ce{BC}}\exp\left(-\frac{\Delta\varepsilon_0^\ddagger}{RT}\right)}$$
- This has _units_ of $\text{molecule m}^{3}\,\text{s}^{-1}$
- For units of $\text{mol}^{-1}\, \text{m}^{3}\,\text{s}^{-1}$, the first factor is $RT/h$

## Applications of transition state theory
- $f_\ce{TS}'$ is often _hard to compute_, but can be used to make _approximate predictions_

### Steric factors
- Consider two reactions, one with a _diatomic_, the other with a _shapeless molecule_:
$$\displaylines{\ce{A +BC-> AB +C} \\ \ce{A +D->AD}}$$
![[Steric factor.png]]
- Assume the same _type of partition function_ have _similar magnitudes_, and:
$$q_\text{trans}>>q_\text{rot}>>q_\text{vib}$$
- Notation for clarity:
$$q_\text{trans}\to\{\text{trans}\}$$
- Comparing the _starting materials_, as well as the two _transition states_:
$$\displaylines{\frac{f'_\ce{A-B-C}}{f'_\ce{A}f'_\ce{B-C}}=\frac{\{\text{trans}\}^3\{\text{rot}\}^2\{\text{vib}\}^3}{\{\text{trans}\}^3\{\text{trans}\}^3\{\text{rot}\}^2\{\text{vib}\}}=\frac{\{\text{vib}\}^2}{\{\text{trans}\}^3} \\ \frac{f'_\ce{A-D}}{f'_\ce{A}f'_\ce{D}}=\frac{\{\text{trans}\}^3\{\text{rot}\}^2}{\{\text{trans}\}^3\{\text{trans}\}^3}=\frac{\{\text{rot}\}^2}{\{\text{trans}\}^3}}$$
- The _steric factor_ is then defined as the _ratio of the rate constants_:
$$p=\frac{k_\text{end}(\ce{A +BC})}{k_\text{2nd}(\ce{A+D})}=\frac{\{\text{vib}\}^2}{\{\text{rot}\}^2}$$

### Kinetic isotope effect
- Consider _replacing an $\ce{H}$ atom with a deuterium $\ce{D}$ atom_ at position $*$:
![[Kinetic isotope effect.png]]
- The _ratio of frequencies_ between molecules $A$ and $B$ is simply:
$$\frac{\nu_\ce{A}}{\nu_\ce{B}}=\sqrt{\frac{\mu_\ce{B}}{\mu_\ce{A}}}$$
- Given that the hydrogen is a light atom is attached to a _heavy molecule_:
$$\displaylines{h\nu>>kT \\ q_\text{vib}=\frac{\exp(-h\nu/2kT)}{1-\exp(-h\nu/kT)}\approx \exp(-h\nu/2kT)}$$
- The _ratio of rate constants_ is then:
$$\frac{k_\text{2nd}(\ce{H})}{k_\text{2nd}(\ce{D})}=\frac{q_\text{vib}(\ce{D})}{q_\text{vib}(\ce{H})}\approx\exp\left(-\frac{h(\nu_\ce{D}-\nu_\ce{H})}{2kT}\right)>1$$

- This can be interpreted as the _difference in vibrational ground states_
- The vibration with $\ce{D}$ has the _lower ground state energy_

- For the reaction above, _deuterating reduces the rate_ by a factor of $\approx7$

## The thermodynamic formulation
- Starting from transition state theory:
$$k_\text{2nd}=\frac{1}{c^⦵}k_\text{1st}K^*=\frac{1}{c^⦵} \nu^\ddagger (q^\ddagger K^\ddagger)$$
- Then, using the expression for $q^\dagger$, one gets the _Eyring equation_:
$$k_\text{2nd}=\frac{1}{c^⦵} \frac{kT}{h}K^\ddagger$$

- Then, relating $K^\ddagger$ to the [[#Equilibrium constants|Gibbs Free Energy]], in _solutions_, and adjusting the _unit_:
$$k_\text{2nd}=\frac{1}{[]^⦵} \frac{kT}{h}\exp\left(-\frac{\Delta_r G^{⦵,\ddagger}}{RT}\right)$$
- Here, $\Delta_r G^{⦵,\ddagger}$ is the _Gibbs Energy change_ from the reactants _to the transition state_
- $[]^⦵$ is a _standard concentration_ of $\text{mol dm}^{-3}$

- For reactions in the _gas phase_:
$$k_\text{2nd}=\frac{1}{p^⦵} \frac{kT}{h}\exp\left(-\frac{\Delta_r G^{⦵,\ddagger}}{RT}\right)$$
- The _factors_ of $[]^⦵$ and $p^⦵$ ensure $k_\text{2nd}$ are in the correct _units_
	- Solution: $\text{mol}^{-1}\,\text{dm}^3\,\text{s}^{-1}$
	- Gas: $\text{N}^{-1}\,\text{m}^2\,\text{s}^{-1}$

- Then using the _definition_ of $\Delta_rG$:
$$k_\text{2nd}=\frac{1}{[]^⦵} \frac{kT}{h}\exp\left(\frac{\Delta_r S^{⦵,\ddagger}}{R}\right)\exp\left(-\frac{\Delta_r H^{⦵,\ddagger}}{RT}\right)$$
- To _experimentally determine_ the parameters, _rearrange_ into a straight line equation:
$$\ln\frac{k_\text{2nd}}{T}=\ln\frac{k}{h[]^⦵}+\frac{\Delta_r S^{⦵,\ddagger}}{R}-\frac{\Delta_r H^{⦵,\ddagger}}{R}\left(\frac{1}{T}\right)$$
- A plot of $\ln(k_\text{2nd}/T)$ as a _function of_ $1/T$ then gives $\Delta_rS^\ddagger$ and $\Delta_rH^\ddagger$
- Typically, measurements are done for a _small temperature range_

### Relation to the Arrhenius equation
- The _Arrhenius equation_ for the rate constant:
$$k_\text{2nd}=A\exp\left(-\frac{E_a}{RT}\right)$$
- This _defines_ $E_a$, or the _activation energy_ of the reaction
- Rates must also be recorded at _constant volume_
- This can be put into a more useful form:
$$\left(\pd{\ln k_\text{2nd}}{T}\right)_V=\frac{E_a}{RT^2}$$
- Then rewriting the _Eyring equation_:
$$\left(\pd{\ln k_\text{2nd}}{T}\right)_V=\frac{1}{T}+\left(\pd{\ln K^\ddagger}{T}\right)_V$$

- For the second term, use the [[#van't Hoff equation]]:
$$\frac{d\,\ln K}{dT}=-\frac{\Delta_rH^⦵}{RT^2}$$
- The usage of $K_c$ or $K_p$ depends on if the reaction is taking place in _solution_ or _gas_
	- In a _gas_, $K_c/K_p$ has a [[#van't Hoff equation|temperature dependence]]

- Combining the equations, one gets that in a _solution_:
$$E_a=\Delta_rH^{⦵,\ddagger}+RT\;\;\;\text{ in solution}$$
- Meanwhile, in a _gas_:
$$E_a=\Delta_rH^{⦵,\ddagger}+(1+\Delta\nu)RT\;\;\;\text{ in a gas}$$
- Hence, as expected, _activation energy_ and _enthalpy of activation_ have a strong correlation

- By _substituting_ the above into the Arrhenius equation, one can rewrite the _pre-exponential factor_ $A$
- For a _reaction in solution_:
$$k_\text{2nd}=\left[\frac{kT}{[]^⦵h}\exp\left(\frac{\Delta_r S^{⦵,\ddagger}}{R}+1\right)\right]\exp\left(-\frac{E_a}{RT}\right)$$

### Volume of activation
- Pressure of _gas phase reactions_ directly affects concentration and rate
- For a _reaction in solution_, at _sufficiently high pressures_, rate can be affected
	- The largest changes often involve _reactions with ions_
- From the Master equation:
$$\displaylines{dG=Vdp-S\,dT \\ d(\Delta_r G^\ddagger)=(\Delta_rV^\ddagger)\,dp-(\Delta_rS^\ddagger)\,dT \\ \left(\pd{\Delta_r G^\ddagger}{p}\right)_T=\Delta_r V^\ddagger}$$
- $\Delta_r V^\ddagger$ is known as the _volume of activation_ for the reaction, and can be interpreted as the _volume change_ in a reaction

- Using the Eyring equation:
$$\left(\pd{\ln k_\text{2nd}}{p}\right)_T=-\frac{\Delta_r V^\ddagger}{RT}$$
- Assuming that $\Delta_rV^\ddagger$ _does not change significantly_ with pressure, the right-hand side is constant

### Interpreting volume and entropies of activation
- Like the _enthalpy_ of activation, the _volume_ and _entropy_ of activation for a reaction is _dependent on the reaction mechanism_

- For a _bimolecular_ reaction $\ce{A +B->C}$, there is a _loss of translational degrees of freedom_ so there is a _negative_ $\Delta_r S^\ddagger$
- Similarly, a _dissociation_ results in a _positive_ $\Delta_r S^\ddagger$
- A _ring closing/opening_ reaction will also commonly result in a negative/positive $\Delta_r S^\ddagger$

- For _ions_ in a _polar solvent_, the _coordination_ of solvent molecules leads to a _low entropy_, this is known as _electrostriction_
	- Hence, the _association_ of ionic species to make a _neutral transition state_ will lead to a _positive_ $\Delta_rS^\ddagger$
	- This can also occur when the charge is more _spread out_, leading to less electrostriction

- A _charge dispersal/delocalisation_ will lead to a _positive_ $\Delta_r V^\ddagger$, while _charge separation_ in the transition state leads to a _negative_ $\Delta_r V^\ddagger$

- Consider a _substitution_ for transition metal complexes:
$$\ce{ML_5X + Y -> ML_5Y + X}$$
- The mechanism can be _associative_, _dissociative_, or _interchange_
	- Associative: $\Delta_rS^\ddagger, \Delta_rV^\ddagger<0$
	- Dissociative: $\Delta_rS^\ddagger, \Delta_rV^\ddagger>0$
