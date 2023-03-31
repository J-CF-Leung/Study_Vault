>[!info] Notation
>__This note__- Internal energy $=U$, work $=W$, Gibbs Free Energy $=G$, enthalpy $=H$
>
>SI units
>
>path-dependent infinitesimal change denoted by $\dbar$
>
>__Goodstein/Landau__- Internal energy $=E$, work $=R$, Gibbs potential $=\Phi$, enthalpy $=W$
>
>Gaussian units
>
>path-dependent infinitesimal change denoted by $\delta$

>[!quote]
>"Thermodynamics is the only physical theory of universal content  
which, within the framework of the applicability of its basic concepts, I  
am convinced will never be overthrown."
>-Albert Einstein

>[!quote]
>“Thermodynamics is a funny subject. The first time you go through it, you  
don’t understand it at all. The second time you go through it, you think  
you understand it, except for one or two small points. The third time you  
go through it, you know you don’t understand it, but by that time you are  
used to it, so it doesn’t bother you any more.”
>-Arnold Sommerfeld

>[!quote]
>"The development of ideas in thermodynamics has a formal elegance which is exceedingly satisfying aesthetically"
>"It has not perhaps quite the rigour of a perfect mathematical proof, but it approaches nearer that ideal than almost any other branch of natural science."
>"For this reason alone it may be regarded as an important part of the education of a scientist."
>-Sir A. B. Pippard

- Classical thermodynamics is a _phenomenological_ study of the properties of matter
- It is a result of _observations_ and _generalisation_
- It makes _no attempt to explain the laws themselves_
- There are _four_ (phenomenological) laws which govern _all systems_

- The _simplest_ thermodynamic systems are _homogeneous fluids and gases_
	- A _deformation_ without change in volume _leaves thermal properties unchanged_

- _Justifying_ all of the laws given below is the job of [[Statistical thermodynamics]]

# Brief statistical justifications
- [[Fundamental principles of statistical mechanics]]

- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of _microstates_
	- The number is denoted $\Omega$
- In _classical mechanics_, this _specifies position and velocity of every constituent particle_
- In _quantum mechanics_, it is the _multi-particle wave function_

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_ as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely 
	- [[Fundamental principles of statistical mechanics#The equal probabilities postulate]]

- A *macrostate* is defined by the _bulk properties_ of the system, and _incorporates many microstates_
		- The probability of a particular microstate, _given a macrostate_ is governed by the [[Fundamental principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
- Macrostates are described by _thermodynamic variables_ such as $U, N, V, S, T, p, \mu$
- Macrostates with energy more or less _equally shared_ among particles become way more likely (way _more available mcirostates_)
	- Consequence of equal probabilities

- _Microstates_ can evolve _reversibly and deterministically with time_
- As time goes on, a _macrostate irreversibly tends to its mean_, which defines _statistical equilibrium_
	- This will later be characterised by the state variable of _entropy_
- The _final_ macrostate will tend to be one with _the most number of microstates_
	- Consequence of equal probabilities (the system spends the most time in the macrostate)

# The zeroth law and equations of state

## Containers and equilibrium
- When discussing the behaviour of _contained physical systems_, one needs to specify the nature of the _container_
- In most cases, a container _does not allow exchange of particles with the outside_

- If the substance within is _completely unaffected by any outside influence_, then the walls are _adiabatic_, and the substance is _isolated_, or _insulated_
- If the wall is not adiabatic, then it is _diathermal_
- Two systems _separated by a diathermal wall_ are said to be in _thermal contact_, and are able to _exchange energy_
- If an _isolated system_ is left alone for long enough, it is said to have reached _equilibrium_

- Types of equilibria: mostly _analagous to mechanical systems_
	- _Stable_: bottom of a well, resistant to perturbations, pure gas at rest
	- _Unstable_: top of a hill, _no thermodynamic analogues_
	- _Neutral_: flat, unchanged after perturbation
	- _Metastable_
	- 
	- 
	- : stable w.r.t. small displacements, unstable w.r.t. large ones, examples include supercooled vapour
- The equilibrium is _macroscopic_, ignoring _fluctuations_ which occur over a _very short period of time_
- It is also _dynamic_, as there are still _microscopic changes_, but _macroscopic measurements  yield a constant result_
- The process _leading to equilibrium_ is known as _thermalisation_

## Temperature, the zeroth law, and equations of state
- _Without electric or magnetic fields_, for a _given mass in equilibrium_, the _properties_ of a gas are observed to be _fully determined_ by the _volume_ $V$ and _pressure_ $p$
- In other words, _any physical quantity_ can be expressed as some _function_ of $p$ and $V$

- Let there be _two fluids independently in equilibrium_, with _state variables_ $(p_1,V_1),(p_2,V_2)$
	- They can take _arbitrary values_
- If they are placed in _thermal contact_, after some time, they will be _in equilibrium with each other_
- This is termed _thermal equilibrium_
- In thermal equilibrium, _three of the variables can be chosen arbitrarily_
- In mathematical terms, when the two bodies are in thermal equilibrium:
$$F(p_1,V_1,p_2,V_2)=0$$
- The _form_ of $F$ will depend on the _specific type of fluid_

- At this point, one requires the _zeroth law of thermodynamics_:
>[!Zeroth Law of Thermodynamics]
>Consider three bodies, $A$. $B$, and $C$
>If $A$ is in thermal equilibrium with $B$, and if $A$ is separately in thermal equilibrium with $C$, then $B$ and $C$ will also be in thermal equilibrium with each other
- From this, one can derive the fact that if two bodies are in _thermal equilibrium_, there exists two functions $A$ and $B$ such that:
$$\theta_A(p_1,V_1)=\theta_B(p_2,V_2)$$
- Proof:
	- Let the three (arbitrary) bodies $A,B,C$ be described by variables $(p_1,V_1,),(p_2,V_2),(p_3,V_3)$
	- The constraint for the thermal equilibrium of $A$ and $C$ can be written, then _inverted_
	- The same can be done for $B$ and $C$:
	$$\displaylines{F_{AC}(p_1,V_1,p_3,V_3)=0 \hspace{1cm} V_3=f_{AC}(p_1,V_1,p_3) \\ F_{BC}(p_2,V_2,p_3,V_3)=0 \hspace{1cm} V_3=f_{BC}(p_2,V_2,p_3)}$$
	- This implies the constraint for the equilibrium of $A$ and $B$ can be written in _two different ways_:
	$$\displaylines{f_{AC}(p_1,V_1,p_3)=f_{BC}(p_2,V_2,p_3) \\ F_{AB}(p_1,V_1,p_2,V_2)=0}$$
	- The latter _does not depend on $p_3$_, hence it must appear in the upper expression in a way where it can be _cancelled on both sides_
	- After the cancellation, one obtains:
	$$\theta_A(p_1,V_1)=\theta_B(p_2,V_2)$$

- The value $\theta$ is known as the _temperature_ of the system
- At this point, it is worth noting that this definition is _empirical_, with a value depending on a choice of _thermometric body_ (Body $C$ in this case, e.g. mercury thermometer)

- The _equation of state_ for a type of fluid is an equation in the form:
$$\theta=f(p,V)$$
- For a _given value_ of $\theta$, one can use this relationship to plot a curve on a _$p-V$ diagram_, known as an _isotherm_

- For systems more complex than fluids (e.g. solids), _more variables_ will be needed to write the equation of state

## The ideal gas equation of state
- A series of observations on the _ideal gas_:
	- _Boyles' Law_ states that at _constant temperature_, $pV$ is a _constant_
	- _Charles' Law_ states that at _constant pressure_, $V/T$ is a _constant_
- This leads to a _reference-independent, absolute temperature scale_, where temperature is commonly labelled $T$
- At _zero temperature_, $pV=0$

- _Avogadro's Law_ then states that for _equal volumes_ of gas at _the same pressure and temperature_ must contain _equal numbers of molecules_

- Combining the previous gas laws, one gets the _ideal gas law_:
$$pV=nRT=NkT$$
	- $n$, $N$: Number of molecules (in moles or pure number)
	- $R$, $k$: _universal_ constants

- This is the _equation of state_ for an ideal gas

- Historical note: an actual absolute/thermodynamic temperature scale first came from [[#Engines and entropy|consideration of the Carnot engine]]

# The first law, internal energy, and heat
- The _molecular origin_ of internal energy will be ignored in a phenomenological study

## Work, heat, and the first law
- From experiments (mostly performed by Joule), it was found that _performing work on a system changes its stored energy_
	- Rotating a paddle in water contained in an _adiabatic vessel_
- It was also found that _the manner in which work is performed_ does not matter

- If the _heat_ transferred to a system, then _stored energy also increases_
- Heat _accounts for energy not supplied by work_
- An _adiabatic system_ will _not allow transfer of heat_ into the system

- This led to the _First Law of Thermodynamics_:
>[!First Law of Thermodynamics]
>Energy is conserved, and both heat and work are forms of energy
>Put mathematically: $$\Delta U=Q+W$$
- $U$ is the _internal energy_ of the system
- $Q$ is the _heat supplied_ to the system
- $W$ is the _work done on_ the system

## Functions of state and the differential form
- From observations, energy is a _function of state_:
$$U=U(P,V)\hspace{0.2cm}\text{ or }\hspace{0.2cm} U=U(P,T)\hspace{0.2cm} \text{ or }\hspace{0.2cm}U=U(V,T)$$
- It may have an _additive constant_, but it is still a _function of state variables_
- The _manner_ in which work or heat is delivered, or the _current state_ of the system _does not matter_, as long as the _same amount_ of work/heat is supplied, the _change in energy_ $\Delta U$ does not change

- Because of this, $Q$ and $W$ are _not functions of state_
- They are more adequately described as _processes_

- Because of this, the _differential form_ of the first law is written as:
$$dU=\dbar Q+\dbar W$$
- The symbol $\dbar$ indicates that $Q$ and $W$ are _path-dependent_, instead of state dependent

## Heat and temperature
- If two bodies with _different temperatures_ are placed in _thermal contact_:
	- Their _individual energies_ will change without any work done
	- The _heat supplied_ by one body is equal to the _heat gained_ by the other
	- The _total energy_ stays the same
	- The body with the _higher temperature_ supplies energy to the other

- Then, it is concluded that _heat transfer arises from differences in temperature_
- This links temperature to the concept of "hotness"

- It can also be concluded that _a body supplied with heat will always rise in temperature_
- So, one can define the _heat capacity_:
$$C=\frac{\dbar Q}{dT}$$
- Heat capacity _depends on the manner in which heat is supplied_
- So, depending on the process, for a _given temperature rise_, the amount of heat needed can vary

- The common variants of heat capacity are _under constant volume_ and _under constant pressure_:
$$C_V=\left(\pd{Q}{T}\right)_V\hspace{1cm}C_p=\left(\pd{Q}{T}\right)_V$$

- For reasons seen later, it is useful to define the _adiabatic index_ $\gamma$ as a _ratio of heat capacities_:
$$\gamma=\frac{C_p}{C_V}$$

## Forms of work
- Depending on the system, work can _be done in different ways_

### Gases



# Reversibility and quasi-static changes

# Entropy and the second law

# State variables

# Thermodynamic systems

# Variational principles

# Phase equilibrium and transitions

# OLD

## The state variables
- At equilibrium, _entropy can be expressed as a function_ of 3 variables:
$$S=S(U,N,V)$$
	- $U=$ internal energy, $N=$ number of particles, $V=$ volume
	- $S, U, N, V$ are _extensive variables, as they scale with system size_
- The function can be inverted:
$$U=U(S, V, N)$$
- For infinitesimal changes in the system, the differential of internal energy is:
$$dU=\left(\pd{U}{S}\right)_{N, V}dS+\left(\pd{U}{V}\right)_{N, S}dV + \left(\pd{U}{N}\right)_{S, V}dN$$
- This expression defines 3 thermodynamic quantities:
$$T=\left(\pd{U}{S}\right)_{N, V}\hspace{25pt}P=-\left(\pd{U}{V}\right)_{N, S}\hspace{25pt}\mu=\left(\pd{U}{N}\right)_{S, V}$$
	- $T=$ temperature, $p=$ pressure, $\mu=$ chemical potential 
	- $T, p, \mu$ are _intensive variables, which do not scale with system size_
- This changes the expression to:
$$dU=T\,dS-P\,dV+\mu\,dN$$
- The intensive variables give rise to concepts of _thermal, mechanical, and chemical equilibrium_

## The first law
$$dU = \dbar Q + \dbar W$$
	- $Q=$ _heat transferred_ from a source _outside the system_
	- $W=$ _work done_ on the system
- When there is an external pressure $p$ upon the system, with no change in $N$, $\dbar W=-p\,dV$ 
- For equilibrium changes and fixed $N$, $dU=T\,dS+\dbar W$
- Work: mechanical ($-p\,dV$), electrical, spring, magnetic

## The second and third laws
- Second law: Entropy never decreases
	- As time goes on, the number of microstates available to a system never decreases
	- At equilibrium, maximum entropy is reached
- Third law: At absolute zero, the entropy of any body is zero
	- A body cannot be brought to absolute zero by any finite series of operations

# Engines and entropy
>[!quote]
>"Reflections on the Motive Power of Fire and on Machines Fitted to Develop that Power"
>-Sadi Carnot


# Thermodynamic potentials
- The descriptors of a system come in _pairs of intensive and extensive variables_
	- $T$ and $S$, $p$ and $V$ for a system with a fixed $N$ 
- For energy, $S$ and $V$ are the _proper independent variables_, as an expression for $U(S,V)$ is all the necessary information to derive all other quantities ($T$, $p$) 
- Other thermodynamic potentials defined as functions of another pair of proper independent variables
	- One variable from $S$ or $T$, another from $p$ or $V$
	- Formulas derived from _Legendre transforms_
- For a system _at equilibrium_ with fixed $N$, _two non-conjugate variables_ are sufficient to determine the state of the system
## Enthalpy/heat function
- Enthalpy $H$ (or $W$ if you use $R$ for work like Goodstein)
$$\begin{aligned} H(S,P)&=U+PV \\ dH &= T\,dS+V\,dP \end{aligned}$$
- For equilibrium changes at _constant pressure_, $dH)_P = \dbar Q$

## Helmholtz Free Energy
- Helmholtz Free Energy $F$ (or $A$):
$$\begin{aligned}F(T,V) &= U-TS \\ dF &= -S\,dT-P\,dV\end{aligned}$$
- For equilibrium changes at _constant temperature_, $dF)_T = \dbar W$
	- Analagous to $dU)_S = \dbar W$

## Gibbs Free Energy
- Gibbs Free Energy $G$ (or $\Phi$):
$$\begin{aligned}G(P,T)&=F+PV=H-TS \\ dG &= -S\,dT+V\,dP \end{aligned}$$

## Maxwell's relations
- Due to the _symmetry of mixed derivatives_, using the definitions of the potentials:
$$\begin{aligned}\left(\pd{P}{T}\right)_V&=\left(\pd{S}{V}\right)_T \\ \left(\pd{T}{V}\right)_S&=-\left(\pd{P}{S}\right)_V \\ \left(\pd{V}{S}\right)_P&=\left(\pd{T}{P}\right)_S \\ \left(\pd{S}{P}\right)_T&=-\left(\pd{V}{T}\right)_P    \end{aligned}$$
- Holds for _any system_
- Demonstrates that two non-conjugate variables can determine the behaviour of a system

# Number of particles and the chemical potential
- Differentials with $dN$:
	$$\begin{aligned}dU&=T\,dS-P\,dV+\mu\,dN \\ 
dH &= T\,dS+V\,dP+\mu \,dN \\ dF &= -S\,dT-P\,dV +\mu\,dN \\
dG &= -S\,dT+V\,dP+\mu\,dN\end{aligned}$$
	- All definitions and transforms above still apply, with $N$ as an extra variable
- Definition of chemical potential $\mu$:
$$\mu = \left(\pd{U}{N}\right)_{S, V} = \left(\pd{H}{N}\right)_{S, P} = \left(\pd{F}{N}\right)_{T, V} = \left(\pd{G}{N}\right)_{T, P}$$
- Infinitesimal changes with proper independent variables fixed:
$$\mu\,\dbar N = (\dbar U)_{S,V} = (\dbar H)_{S,P} = (\dbar F)_{T,V} = (\dbar \Phi)_{T,P}$$
- Last 3 equalities applicable to any change (not necessarily $N$)

- Chemical potential is an _intensive variable_ like $P$ and $T$
- Consider a system with one type of particle, scaled up by $\lambda$, and $d(\lambda U)$, one gets:
$$U=TS-PV+\mu N$$
- By considering the differential, $\mu$ is shown to be a function of $P$ and $T$:
 $$d\mu = \frac{V}{N}dP-\frac{S}{N}dT$$
 - The same Legendre transforms apply, allowing $\mu$ to be redefined:
$$G(P,T,N)=\mu N$$

- The chemical potential is _not necessarily positive_
	- To _keep $S$ and $V$ constant_ while adding a particle, $U$ may have to decrease
	- For strong repulsions, $U$ may increase
- One now needs _three non-conjugate variables_ in order to completely determine a system

## The Landau potential
- With the new pair of conjugate variables, new thermodynamic potentials are available
- The _Landau potential_ is defined as:
$$\displaylines{\Omega(T,V,\mu)=F-\mu N=-PV \\ d\Omega=-S\,dT-P\,dV-N\,d\mu}$$
- With this, differentials of the potentials are related by:
$$(\dbar\Omega)_{T,V,\mu}=(\dbar U)_{S,V,N}=(\dbar F)_{T,V,N}=(\dbar G)_{T,P,N}=(\dbar H)_{S,P,N}$$

# Variational principles
- There is often some _constraint_ in the processes occuring in a system
	- e.g. constant $T$, constant $p$
- Then, one may want to know the _maximum amount of work_ that can be extracted, i.e. the _free energy_

# Non-gaseous systems

