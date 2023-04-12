- Rigorous discussion w/ _derivations_: [[Classical Thermodynamics]]

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

## Application of the Boltzmann distribution

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
- In terms of the _wave function_ and _energies_:
$$\displaylines{\psi=\psi_\text{trans}\psi_\text{rot}\psi_\text{vib}\psi_\text{elec}\\ \varepsilon_\text{tot}=\varepsilon_\text{trans}+\varepsilon_\text{rot}+\varepsilon_\text{vib}+\varepsilon_\text{elec}}$$
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
- Molecules also have [[Descriptions of bonding#Molecular term symbols|term symbols]]:
$$^{2S+1}\Lambda_{g/u}^{\pm}$$
- Most molecules have _closed-shell configurations_, giving a degeneracy of 1
- However, there are exceptions, such as oxygen:
$$^3\Sigma_g^-$$
- It is _triply degenerate_

# Internal energy and heat capacity

## Classical behaviour

## Translational contribution

## Rotational contribution

## Vibrational contribution

## Electronic contribution

## Total

# Entropy

## Different contributions

### Translational entropy

### Rotational entropy

### Vibrational entropy

### Electronic entropy

## Calorimetry

## Behaviour at low temperatures

# Nuclear spin statistics

## Nuclear spin wave functions

## Swapping nuclei

## Ortho- and para-hydrogen

## Raman spectra

## Zero spin

## Rotational partition function

# Chemical equilibrium

## Chemical potential and equilibrium

## Equilibrium constants

### In terms of concentration

### In terms of pressure

### Example: Ionisation of atoms

## Adsorption of a gas and the Langmuir isotherm


# Kinetics

## Potential energy surfaces

## Transition state theory

## Steric factors

## Kinetic isotope effect

## A thermodynamic formulation

### Relation to the Arrhenius equation

### Volume of activation