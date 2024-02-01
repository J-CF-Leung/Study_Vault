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

- _Justifying_ all of the laws given below is the job of [[Foundations of statistical thermodynamics]]

# Brief statistical justifications
- [[Principles of statistical mechanics]]

- For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of _microstates_
	- The number is denoted $\Omega$
- In _classical mechanics_, this _specifies position and velocity of every constituent particle_
- In _quantum mechanics_, it is the _multi-particle wave function_

- For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the _initial conditions become irrelevant_ as particles redistribute energy and momentum until equilibrium is reached
2. For a system _in equilibrium_, all possible microstates are equally likely 
	- [[Principles of statistical mechanics#The equal probabilities postulate]]

- A *macrostate* is defined by the _bulk properties_ of the system, and _incorporates many microstates_
		- The probability of a particular microstate, _given a macrostate_ is governed by the [[Principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
- Macrostates are described by _thermodynamic variables_ such as $U, N, V, S, T, p, \mu$
- Macrostates with energy more or less _equally shared_ among particles become way more likely (way _more available mcirostates_)
	- Consequence of equal probabilities

- _Microstates_ can evolve _reversibly and deterministically with timet_
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

## Describing a state
- Overall, one will need _at least two_ variables to describe a system
- This comprises of an _extensive_ and _intensive_ variable

- An _extensive_ variable _does not scale with system size_
	- Example: Pressure, temperature (in an 
- An _intensive_ variable _scales with system size_
	- Example: Volume, mass, energy

- For an ideal gas, _only_ volume $V$ and pressure $p$ are required to fully determine the state of a system

- Intensive and extensive variables come in _conjugate pairs_, coming from the _mathematical description of energy_ ([[#State variables|here]])

## Empirical temperature, the zeroth law, and equations of state
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
>[!info] Zeroth Law of Thermodynamics
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

# The first law, internal energy, and heat
- The _molecular origin_ of internal energy will be ignored in a phenomenological study
	- In an _ideal gas_, it would be the _kinetic energy_ of the molecules
	- For many systems, it also depends on _external fields_ (gravitational, magnetic, etc.)

## Work, heat, and the first law
- From experiments (mostly performed by Joule), it was found that _performing work on a system changes its stored energy_
	- Rotating a paddle in water contained in an _adiabatic vessel_
- It was also found that _the manner in which work is performed_ does not matter

- If the _heat_ transferred to a system, then _stored energy also increases_
- Heat _accounts for energy not supplied by work_
- An _adiabatic system_ will _not allow transfer of heat_ into the system

- This led to the _First Law of Thermodynamics_:
>[!info] First Law of Thermodynamics
>Energy is conserved, and both heat and work are forms of energy
>Put mathematically: $$\Delta U=Q+W$$
- $U$ is the _internal energy_ of the system
- $Q$ is the _heat supplied_ to the system
- $W$ is the _work done on_ the system

- This applies to the _beginning and end_ of _any process_, no matter the time elapsed

## Functions of state and the differential form
- From observations, energy is a _function of state_:
$$U=U(P,V)\hspace{0.2cm}\text{ or }\hspace{0.2cm} U=U(P,T)\hspace{0.2cm} \text{ or }\hspace{0.2cm}U=U(V,T)$$
- It may have an _additive constant_, but it is still a _function of state variables_
- The differential of $U$ is said to be _exact_

- The _manner_ in which work or heat is delivered, or the _current state_ of the system _does not matter_, as long as the _same amount_ of work/heat is supplied, the _change in energy_ $\Delta U$ does not change

- Because of this, $Q$ and $W$ are _not functions of state_
- They are more adequately described as _processes_

- Because of this, the _differential form_ of the first law is written as:
$$dU=\dbar Q+\dbar W$$
- The symbol $\dbar$ indicates that $Q$ and $W$ are _path-dependent_, instead of state dependent

## Heat, temperature, and heat capacities
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


# Quasi-static changes, reversibility and cyclic processes
- Often, one would want to express $\dbar W$ in terms of _state variables_
- However, the _state variables are only defined during equilibrium_

- Therefore, this is only possible for _quasi-static processes_, where the system is _always in equilibrium_
- In practice, this is easily _approximated_, as the _relaxation time_ of a fluid is low

## Reversibility
- In thermodynamics, a _reversible_ process is one that _may be exactly reversed by an infinitesimal change in external conditions_
	- It is a _special case_ of quasi-static processes
- Example: If a gas is being _compressed by a piston_, as long as it is _quasi-static_, and there is _no friction_, the gas can instead be _expanded_ by an _infinitesimal reduction in external pressure_

## Work done on a gas
- Let there be a _piston_ pushing on a gas with _pressure_ $p'$
- As long as there is no _friction_ between the container walls and the piston, for _equilibrium_, $p'$ must be _equal to gas pressure_, hence $p=p'$

- If a _change in volume_ is done slowly enough to _keep the gas in equilibrium_, then infinitesimal work done can be written as:
$$\dbar W=-p\,dV$$
- This indicates that _compression of a gas does work on it_

- For a _finite process_, the _total work done on the gas_ can be written as:
$$W=-\int p\,dV$$
- This integral is _still path-dependent_, as _depending on the nature of the surroundings_, other state variables such as $T$ can still change

### First law, energy, and heat capacities for gases
- In the case of a _quasistatic change_, the [[#The first law, internal energy, and heat|first law]] can be rewritten as:
$$\dbar Q=dU+p\,dV$$
- For gases, the energy is a function of _volume_ and _temperature_:
$$\displaylines{U=U(T,V) \\ dU=\left(\pd{U}{T}\right)_V\,dT+\left(\pd{U}{V}\right)_T\,dV}$$

- This allows the [[#Heat, temperature, and heat capacities|heat capacity]] at _constant volume_ to be written as:
$$C_V=\left(\pd{Q}{T}\right)_V=\left(\pd{U}{T}\right)_V$$
- Similarly, the heat capacity at _constant pressure_ becomes:
$$C_p=\left(\pd{Q}{T}\right)_p=\left(\pd{U}{T}\right)_V+\left[\left(\pd{U}{V}\right)_T+p\right] \left(\pd{V}{T}\right)_p$$
- Their _difference_ is:
$$C_p-C_V=\left[\left(\pd{U}{V}\right)_T+p\right] \left(\pd{V}{T}\right)_p$$

## Cyclic processes, refrigerators and engines
- Due to this path dependence, one can do a _cyclic process_, and _convert work done on the gas into heat_, which is then _extracted from the gas_:
$$Q_\text{net, extracted}=W=-\oint p\,dV$$
- Since the gas goes through a _cycle_, $\Delta U=0$
- At _some points_ during the process, heat will be _input into the gas_, hence it is _not perfect_
- This type of _cyclic process_ is known as _refrigeration_, as heat is taken _out of the gas_

- Similarly, one can run this cycle in a _reverse direction_, converting _heat supplied to the gas_, in order to _extract work done by the gas_:
$$W_\text{done}=\oint p\,dV$$
- This is known as an _engine_
- Like the refrigerator, _some heat will be expelled_, preventing perfect efficiency
- This is repeated in [[#Multiple formulations|Kelvin's statement of the second law]]

![[Cycle types.png]]


## Work done for non-gaseous systems
- For many systems _in equilibrium_, the work can be written as:
$$\dbar W=X\,dx$$
- $X$ is some _generalised force_, which is always _intensive_
- $x$ is some _generalised displacement_, which is always _extensive_

- This _pair_ of variables are known as _conjugates_

- Example: _Elastic rod_
$$\dbar W=f\,dl$$
- $f=$ restoring foce
- $l=$ length
- Valid in the absece of _hysteresis_ and plastic deformation

- Example: _Surface of a fluid_:
$$\dbar W=\gamma\,dA$$
- $\gamma=$ surface tension
- $A=$ area

# The second law and entropy
>[!quote]
>"Réﬂexions sur la puissance motrice du feu et sur les machines propres à développer cette puissance"
>(Reflections on the Motive Power of Fire and on Machines Fitted to Develop that Power)
>-Sadi Carnot

- In most cases, one can observe that _changes in nature occur irreversibly_
	- In fact, _reversible_ processes are more of an _idealised case_
- An _isolated_ system will always _irreversibly tend to equilibrium_
- Example: _Heat_ flows from a _hotter_ to a _colder_ body

- The _irreversibility_ of a process is alluded to in the _Second Law of Thermodynamics_

## Multiple formulations
- Over the years, there have been _many equivalent statements_ of the Second Law
- Ultimately, they all lead to the establishment of the _function of state_ known as _Entropy_

- The formulations of Clausius and Kelvin lead to _Carnot's Theorem_, which then leads to the _Clausius inequality_, establishing that for any _reversible change_, $\dbar Q=T\,dS$, where $T$ is a function of _empirical temperature_, and $S$ is a _function of state_
- This can all also be proven _purely from Carathéodory's statement_

### Clausius and Kelvin
- There are two _formulations_, given by Clausius and Kelvin, based on _empirical observations_
>[!info] Clausius' statement
>It is impossible to devise an engine which, working in a cycle, shall produce no effect other than the transfer of heat from a colder to a hotter body
- It is possible to do so with a _non-cyclic process_, but _never with a cycle_

>[!info] Kelvin's statement
>It is impossible to devise an engine which, working in a cycle, shall produce no effect other than the extraction of heat from a reservoir, and the performance of an equal amount of mechanical work
- In other words, _one cannot build an engine that does not produce waste heat_

### Carathéodory
- There is also a more _mathematical_ statement given by Carathéodory:
>[!info] Carathéodory's statement
>Adiabatic surfaces exist.
>In other words, in the neighbourhood of any equilibrium state of a system, there are always states which are inaccessible by an adiabatic process
- This asserts that for _any system_, there is a _family of unique surfaces_ that can be reached by adiabatic changes
	- The second statement implies that the inaccessible states are always _infinitesimally close_, which then leads to the first

- For _two independent variables_, the _first law_ is sufficient to make this true
	- Using the first law, one finds that $dp/dV$ for $\dbar Q=0$ is _always unique_
- For _three or more independent variables_, this statement is necessary as the _first law is insufficient_ to constrain the variables to make this possible

- On each adiabatic surface, there is some _function of state_ $S$ which is _constant_

### Equivalence
- All of these three statements are _equivalent_
- A violation of Clausius' law _leads to_ a violation of Kelvin's law, and _vice versa_
	- Combining a Kelvin violator and a [[#Cyclic processes|refrigerator]] makes it a Clausius violator, and vice versa
- Carathéodory's statement can be _derived from_ Kelvin's law
	- [[#Alternative derivations: Adiabatic surfaces|Proof]]

## The Carnot engine
- Let there be a _four-stage heat engine_, with _two isothermal_ and _two adiabatic_ processes:
![[Carnot.png]]
- Dotted lines: adiabats, solid lines: isotherms
- It operates between two _reservoirs_ of different temperatures

- On the _higher temperature isotherm_ $AB$, the gas _absorbs heat_ $Q_h$ at temperature $T_h$
- On the _lower temperature isotherm_ $CD$, the gas _expels heat_ $Q_l$ at temperature $T_l$
	- From Kelvin's statement, $Q_l>0$

- From the conservation of energy, the _work done by the gas_, and the _efficiency_ is:
$$\displaylines{W=Q_h-Q_l \\ \eta \equiv\frac{W}{Q_h}=1-\frac{Q_l}{Q_h}<1}$$
- The efficiency can be thought of as _how much work can be extracted for a given amount of heat input_

>[!info] Carnot's Theorem
>All heat engines operating between $T_l$ and $T_h$ have an efficiency lower than or equal to the Carnot Engine also operating at $T_l$ and $T_h$
>
>Corollary: Any reversible engine operates at the same efficiency as the Carnot engine
- Proof: _Assume_ there is some engine $E$ with a higher efficiency
	![[Carnot proof.png|400]]
	- Run the Carnot engine in _reverse_
	- Since $E$ is more efficient, $Q_h'<Q_h$
	- From the first law, $Q_h-Q_h'=Q_l-Q_l'$ and both sides are _positive_
	- Hence, the _sole action_ of the combined device is to _deposit heat from a cold reservoir to a hot one_, hence this _violates Clausius' statement_
- Hence, Carnot's Theorem is _equivalent to the second law_
- Proof of corollary: _Assume_ there is some _reversible_ engine $R$ with a _lower_ efficiency:
	![[Carnot corollary proof.png]]
	- Run $R$ in _reverse_
	- With a similar process to the proof above, this _violates Clausius' statement_

## Carnot efficiency and thermodynamic temperature
- From the arguments above, the efficiency of the Carnot engine, $\eta_\text{Carnot}$ _must be a function of the two temperatures_:
$$\eta_\text{Carnot}(T_l,T_h)=1-f(T_l,T_h)$$
- Consider _two Carnot engines_, one running at $(\theta_1,\theta_2)$, the other at $(\theta_2,\theta_3)$, with $\theta_1<\theta_2<\theta_3$
- By considering the _individual and overall efficiencies_, one gets:
$$\displaylines{f(\theta_1,\theta_3)=f(\theta_1,\theta_2)f(\theta_2,\theta_3)}$$
- From this, _define_ $T$ such that:
$$\eta_\text{Carnot}=1-\frac{T_l}{T_h}$$
- This _defines_ the thermodynamic temperature scale
- From [[#Ideal gases|computing efficiency for ideal gases]], it can be shown that _this is the same temperature as the_ [[#Ideal gases|ideal gas temperature scale]]

## Clausius' inequality and entropy
- From the definition above, for a Carnot cycle:
	$$\sum_\text{Carnot}\frac{Q}{T}=0$$
	- Sign convention: any heat _supplied_ is positive, heat _expelled_ is negative

>[!info] Clausius' Theorem
>For any cyclic process, with $\dbar Q>0$ for heat supplied to the system:
>$$\oint \frac{\dbar Q}{T}\leq 0$$
>The equality holds for reversible processes
- Proof: Consider some engine $E$ with the Carnot engine running in _reverse_
	$$\displaylines{W=Q_h-Q_l=Q_h'-Q_l' \\ Q_h'>Q_h \\ \frac{Q_h'}{T_h}-\frac{Q_l'}{T_l}=(Q_h'-Q_h)\left(\frac{1}{T_h}-\frac{1}{T_l}\right)\leq0}$$
	- Any _continuous_ cycle can be _cut_ into discrete "bits"
	- Equality for reversible cycles: the inequality holds in both directions

- This implies that for _reversible paths_, one can define some function $S$ such that:
$$S(B)-S(A)=\int_A^B \frac{\dbar Q}{T} \hspace{1cm}\text{ for any reversible path AB}$$
- This function is _entropy_, which is a _state function_:
$$dS=\frac{dQ_\text{rev}}{T}$$
- Like energy, it is _extensive_, and defined _up to a constant_ (Later given by the Third Law)

- One can then visualise the _Carnot cycle_ on the $T-S$ plane:
![[Carnot in T-S.png]]

## Law of increase of entropy
- Consider two paths, one reversible, one irreversible, from $A$ to $B$:
![[Two paths.png]]
- From Clausius' Theorem:
$$\displaylines{\int_A^B\frac{\dbar Q}{T}+\int_B^A\frac{dQ_\text{rev}}{T}\leq0 \\ dS=\frac{dQ_\text{rev}}{T}\geq\frac{\dbar Q}{T}}$$
- For a _thermally isolated system_:
$$dS\geq 0$$
>[!info] Second Law of Thermodynamics
>For a thermally isolated system, entropy cannot decrease
- As a consequence, if any _irreversible process_ occurs in the system, entropy _must increase_
- If a change is _adiabatic_, it is also inherently reversible and _isentropic_

- For the _universe_ as a whole, $U$ remains constant while $S$ increases
- This gives rise to the _arrow of time_
>[!quote] The Moving Finger
>بر لوح نشان بودنی‌ها بوده‌است
>پیوسته قلم ز نیک و بد فرسوده‌است
>در روز ازل هر آنچه بایست بداد
>غم خوردن و کوشیدن ما بیهوده‌است
>
>The Moving Finger writes; and having writ,
>Moves on: nor all your Piety nor Wit
>Shall lure it back to cancel half a Line,
>Nor all your Tears wash out a Word of it.
>
>By عمر خیّام (Omar Khayyam), translated from Persian by Edward Fitzgerald

## Alternative derivations: Adiabatic surfaces
- For any adiabatic change of any system:
$$\displaylines{\dbar Q=dU-\sum_i X_i\,dx_i=0 \\ \sum_i Y_i\,dy_i=0}$$
- Where $y_i$ iterates over _all state variables_, and $Y_i$ encompasses $X_i$ plus any necessary _partial derivatives of $U$_

- For any _two-variable_ system, such as a gas, an _adiabatic line_ obeys:
$$\displaylines{dU-p\,dV=0 \\ \frac{dp}{dV}=-\frac{(\partial U/\partial V)_p+p}{(\partial U/\partial p)_V}}$$
- This gives a _unique_ gradient, giving rise to a _family of adiabatic lines_
- Only the _first law_ can already _guarantee_ the uniqueness of these adiabats
- Example: For an ideal gas, the adiabats and isotherms
![[Isotherms and adiabats.png]]

- However, for _more than two variables_, the _adiabatic surfaces are not guaranteed to be unique_
- Example: For three variables, $Z_1\,dz_1+Z_2\,dz_2+Z_3\,dz_3=0$ _can encompass all space_, and is _constrained to a surface iff_:
$$Z_1\left(\pd{Z_2}{z_3}-\pd{Z_3}{z_2}\right)+Z_2\left(\pd{Z_3}{Z_1}-\pd{Z_1}{z_3}\right)+Z_3\left(\pd{Z_1}{z_2}-\pd{Z_2}{z_1}\right)=0$$

- Instead, the _existence of adiabatic surfaces_ must be derived from _Kelvin's statement_
	![[Caratheodory from Kelvin.png]]
	- Let $X$ be a third state variable
	- Suppose _both $AB$ and $AC$ were adiabats_
	- On $AB$, since $Q=0$ and $\Delta U<0$, _work is done by the system_
	- On $BC$, since no work is done and $\Delta U>0$, _heat $Q$ is absorbed by the system_
	- On $CA$, _work is done on the system without it expelling heat_
	- Hence, this cycle _violates Kelvin's statement of the Second Law_
	- Hence, for any point, _there are points inaccessible adiabatically_
- This proves _Carathéodory's statement is another form of the Second Law_

- Having proven that unique adiabatic surfaces exist, one can prove that for _any reversible change_, there exists a _function of empirical temperature_ $T(\theta)$ and _function of state_ $S$, such that $dQ_\text{rev}=T\,dS$ (warning: Long proof)
	- Let there be a system with $n$ _independent parameters_ $\{y_i\}$
	- Introduce a _new function of state_ $\phi(y_i)$ which is _constant for an adiabatic change_:
	$$\sum_i Y_i\,dy_i=0 \hspace{1cm} \sum_i\pd{\phi}{y_i}\,dy_i=0$$
	- Hence, for any changes _on the adiabatic surface_, and _any function of state_ $\lambda$:
	$$\sum_i\left(Y_i-\lambda\pd{\phi}{y_i}\right)\,dy_i=0$$
	- On the surface, there are only $n-1$ independent variables 
	- _Choosing_ $\lambda$ such that for the _dependent_ variable $y_1$:
	$$Y_1=\lambda\pd{\phi}{y_1}$$
	- Hence, if the equations above have to be _true in general_, then _on the surface_:
	$$Y_i=\lambda\pd{\phi}{y_i}\,\,\,\,\,\forall i$$
	- Therefore, for a _reversible, non-adiabatic change_:
	$$\dbar Q=\sum_i Y_i\,dy_i=\sum_i\lambda\pd{\phi}{y_i}\,dy_i=\lambda\,d\phi$$
	- Now, one must prove that $\lambda$ is _purely a function of $\theta$ and $\phi$_
	- Introduce a second system described by $m$ _independent variables_ $\{z_i\}$, in _thermal equilibrium_ with the first, at empirical temperature $\theta$
	- Introduce $\lambda'$ and $\phi'$ asuch that
	$$\dbar Q=\lambda\,d\phi \hspace{1cm} \dbar Q'=\lambda'\,d\phi'$$
	- Then, introduce functions $\Phi(y_i,z_i)$ and $\Lambda(y_i,z_i)$ such that:
	$$\displaylines{\Lambda\,d\Phi=\dbar Q+\dbar Q'=\lambda\,d\phi+\lambda'\,d\phi' \\ d\Phi=\frac{\lambda}{\Lambda}\,d\phi+\frac{\lambda'}{\Lambda'}\,d\phi'}$$
	- Perform a change of variable to replace $(y_1,y_2)$ with $(\theta,\phi)$, and $(z_1,z_2)$ with $(\theta,\phi')$
	- From the _total differential_ of $\Phi$, it is _purely a function of $\phi$ and $\phi'$_, and this extends to its _partial derivatives_, $\lambda/\Lambda$ and $\lambda/\Lambda$, hence:
	$$\displaylines{\Lambda=\Lambda(\phi,\phi',\theta) \hspace{1cm} \lambda=\lambda(\phi,\theta)\hspace{1cm}\lambda'=\lambda'(\phi',\theta)\\ \pd{}{\theta}\left(\frac{\lambda}{\Lambda}\right)=\pd{}{\theta}\left(\frac{\lambda'}{\Lambda}\right)=0 \\ \pd{\ln\lambda}{\theta}=\pd{\ln\lambda'}{\theta}=\pd{\ln\Lambda}{\theta}}$$
	- From the last line, one infers that _all terms are a function of $\theta$_
	- Hence:
	$$\lambda=F(\phi)\exp\left[\int\,g(\theta)\,d\theta\right]$$
	- The form of $F(\phi)$ is _determined by the way in which the surfaces are labelled_
	- Then, define:
	$$\displaylines{T(\theta)\equiv C\exp\left[\int g(\theta)\,d\theta\right]\\ S(\phi)=\frac{1}{C}\int\,F(\phi)\,d\phi}$$
	- Hence, for _any reversible process_:
	$$dQ_\text{rev}=T\,dS$$
	- where $T$ is a function of _empirical temperature only_, and $S$ is a _function of state_

# State variables
- So far, to descibe a _gas_ (assuming constant $N$), one can deploy the variables:
	- Intensive - _Absolute temperature_ $T$, _pressure_ $p$
	- Extensive - _Internal energy_ $U$, _volume_ $V$, _entropy_ $S$

## The first master equation
- Note that for a _reversible process_, as $dQ_\text{rev}=T\,dS$ and $\dbar W=-p\,dV$:
$$dU=T\,dS-p\,dV$$
- In this equation, _only state variables are used_
- Hence, this is _applicable for all processes, no matter if it is reversible_
- This is known as a _Master Equation_

- For _irreversible processes_:
$$\displaylines{dU=\dbar Q+\dbar W=T\,dS-p\,dV \\ \dbar Q_\text{irrev.}<T\,dS \\ \dbar W_\text{irrev.}>-p\,dV}$$
	- Example: Due to _friction_, the _applied pressure_ $p'>p$, and _more work is done_

- The Master Equation also implies that $U$ is a _function of_ $S$ and $V$:$$U=U(S,V)$$
- From the Master Equation, one can write:
$$T=\left(\pd{U}{S}\right)_V\hspace{1cm}p=-\left(\pd{U}{V}\right)_S$$
- It can also be _inverted_ to give _entropy as a function of $U$ and $V$_:
$$\displaylines{S=S(U,V) \\ dS=\frac{1}{T}\,dU+\frac{p}{T}\,dV}$$
- Hence, for the _internal energy_ of the system to be known, $S$ and $V$ must be known
- They are known as the "natural variables" for $U$, as knowing $U(S,V)$ then gives _complete thermodynamic information_ for the system
	- If $U$ is known as a function of $T$ and $V$, then there are still _unknowns_ for the system (in this case, $S$ and $p$ are unknown)
	- To find these unknowns, one would need _equations of state_ so one can state $U$ in terms of the _proper variables_

## Thermodynamic potentials
- For an _isolated_ system, _entropy_ must _never decrease_
- However, many systems are often kept in contact with a _reservoir_ at constant temperature
- In these cases, one must maximise _total entropy_ of both the system and the reservoir
- Hence, one can consider _thermodynamic potentials_ that must be _extremised_ in these cases

- They are also useful for describing the system using _variables other than_ $S$ and $V$, as the former can be _hard to measure_

- To derive them, one must perform _Legendre transforms_

- The _enthalpy_ $H$ is defined as:
$$\displaylines{H=U+pV \\ dH=T\,dS+V\,dp}$$
- The _Helmholtz Free Energy_ $F$ is defined as:
$$\displaylines{F=U-TS \\ dF=-S\,dT-p\,dV}$$
- The _Gibbs Free Energy_ is defined as:
$$\displaylines{G=H-TS=U+pV-TS \\ dG=-S\,dT+V\,dp}$$


- For example, if $G(p,T)$ were known, then _complete thermodynamic information_ can be obtained for the system

## Gibbs-Helmholtz relations
- In some cases. [[#The Free Energies]] are more useful to measure and evaluate
- Hence, one can express $U$ and $H$ in terms of the _derivatives_ of these quantities
- Using the definitions of entropy as:
$$S=-\left(\pd{F}{T}\right)_V=-\left(\pd{G}{T}\right)_p$$
- Then using the definitions of $F$ and $G$:
$$\displaylines{U=F+TS=F-T\left(\pd{F}{T}\right)_V=-T^2\left(\pd{(F/T)}{T}\right)_V \\ H=G+TS=G-T\left(\pd{G}{T}\right)_p=-T^2\left(\pd{(G/T)}{T}\right)_p}$$
- These are the _Gibbs-Helmholtz relations_

## Maxwell relations
- There are _special relationships_ between thermodynamic variables, using the fact that if $f$ is a _single-valued_, _differentiable_ function everywhere, then $df$ is an _exact differential_:
$$\displaylines{f=f(x,y) \longrightarrow df=\left(\pd{f}{x}\right)\,dx+\left(\pd{f}{y}\right)\,dy \\ \pd{^2f}{x\partial y}=\pd{^2f}{y\partial x}}$$

- By considering the _partial derivatives of each thermodynamic potential_:
$$\left(\pd{}{S}\right)_V\left(\pd{U}{V}\right)_S=\left(\pd{}{V}\right)_S\left(\pd{U}{S}\right)_V \longrightarrow -\left(\pd{p}{S}\right)_V=\left(\pd{T}{V}\right)_S$$
- Similarly, the collection of four _Maxwell's relations_ is:
$$\begin{aligned}\left(\pd{T}{V}\right)_S &=-\left(\pd{p}{S}\right)_V \\ \left(\pd{T}{p}\right)_S &=\;\;\;\left(\pd{V}{S}\right)_p \\ \left(\pd{S}{V}\right)_T &=\;\;\;\left(\pd{p}{T}\right)_V \\ \left(\pd{S}{p}\right)_
T &= -\left(\pd{V}{T}\right)_p\end{aligned}$$
### An alternative derivation
- Consider a _cyclic process_, where since $U$ Is a state function and _does not change_:
$$\displaylines{\oint p\,dV=\oint T\,dS \\ \int\int\,dp\,dV=\int\int\,dT\,dS}$$
- The _work done by the gas_ (area in the $p-V$ plane), is the same as the _heat absorbed by the gas_ (area in the $T-S$ plane)
- Hence:
$$\pd{(T,S)}{(p,V)}=1$$
- This is the [[Vector calculus in 3-dimensions#The Jacobian matrix|Jacobian]] of the transformation from the $p-V$ plane to the $T-S$ plane is 1
- Hence:
$$\pd{(T,S)}{(x,y)}=\pd{(p,V)}{(x,y)}$$
- Here, $(x,y)$ are each _pair of independent variables_ used in describing the system

### Useful theorems
- When considering partial derivatives, there are some useful relationships
- For some function $x$:
$$x=x(y,z) \hspace{1.5cm}dx=\left(\pd{x}{y}\right)_z\,dy+\left(\pd{x}{z}\right)_y\,dz$$
- The _reciprocal theorem_:
$$\left(\pd{x}{y}\right)_z=\frac{1}{(\partial y/\partial x)_z}$$
- The _reciprocity theorem_:
$$\left(\pd{x}{y}\right)_z\left(\pd{y}{z}\right)_x\left(\pd{z}{x}\right)_y=-1$$
- This can be combined to give:
$$\left(\pd{x}{y}\right)_z=-\left(\pd{x}{z}\right)_y\left(\pd{z}{y}\right)_x$$

## Number of particles and the chemical potential
- All extensive variables scale with the _size_ of the system
- This size is often determined by the _number of particles_
- In many systems, this number can _change_
	- Example: Chemical _reactions_

- Terminology:
	- An _isolated system_ can exchange _neither particles or energy_ with surroundings
	- A _closed system_ can exchange _energy, but not particles_ with surroundings
	- An _open system_ can exchange _energy and particles_ with surroundings

- In systems where the number of particles $N$ can change:
$$dU=T\,dS-p\,dV+\mu\,dN$$
- Here, $\mu$ is known as the _chemical potential_
- It is the _energy change when adding 1 particle while keeping $S$ and $V$ constant_:
$$\mu=\left(\pd{U}{N}\right)_{S,V}$$
- It is often _negative_, as keeping $S$ and $V$ constant _while adding particles_ will require a _reduction in energy_

- When considering other themodynamic potentials:
$$\displaylines{dH=T\,dS+V\,dp+\mu\,dN \\ dF=-S\,dT-p\,dV+\mu\,dN \\ dG=-S\,dT+V\,dp+\mu\,dN\\\mu=\left(\pd{U}{N}\right)_{S,V}=\left(\pd{H}{N}\right)_{S,p}=\left(\pd{F}{N}\right)_{T,V}=\left(\pd{G}{N}\right)_{T,p}}$$
- Similarly, $dS$ can be rewritten:
$$dS=\frac{dU}{T}+\frac{p}{T}\,dV-\frac{\mu}{T}\,dN$$

### Multiple types of particles
- If there are _many types of particles_, each with number $N_i$, then the Master Equations must be rewritten as:
$$\displaylines{dU=T\,dS-p\,dV+\sum_i \mu_i\,dN_i \\ dH=T\,dS+p\,dV+\sum_i \mu_i\,dN_i \\ dF=-S\,dT-p\,dV+\sum_i \mu_i\,dN_i \\ dG=V\,dp-S\,dT+\sum_i \mu_i\,dN_i}$$
- Each type of particle has _its own chemical potential_:
	$$\mu_i=\left(\pd{U}{N_i}\right)_{S,V,N_j}$$
	- The amount of particles for _other components_ $j\neq i$ must not change
- This is required when considering [[Chemical thermodynamics#Chemical equilibrium|chemical equilibrium]]

# Interpreting thermodynamic functions
- Aside from _mathematical convenience_, each thermodynamic function has some _physical meaning_
- For this section, consider a $p-V$ system, ignoring _other types of work_, or _external fields_

## Entropy and types of equilibria

$$\displaylines{dS=\frac{dU}{T}+\frac{p}{T}\,dV-\frac{\mu}{T}\,dN \\ \left(\pd{S}{U}\right)_{V,N}=\frac{1}{T} \hspace{1cm} \left(\pd{S}{V}\right)_{U,N}=\frac{p}{T} \hspace{1cm} \left(\pd{S}{U}\right)_{U,V}=-\frac{\mu}{T}}$$
- For an _isolated system_, entropy can _never decrease_
- When it is at a _maximum_, the system has reached an _equilibrium_

- For the case of _thermal equilibrium_, consider _two systems_, with constant $V$ and $N$, at _different temperatures_, able to _exchange energy_:
![[Thermal equilibrium.png]]
- Since the two systems are _isolated_:
$$dU_1+dU_2=0$$
- The _total entropy change_ is:
$$dS=\frac{dU_1}{T_1}+\frac{dU_2}{T_2}=\left(\frac{1}{T_1}-\frac{1}{T_2}\right)dU_1\geq0$$
- Hence, if $T_1\neq T_2$, then _energy flows from the system with higher temperature_
- This occurs until $T_1=T_2$, where the systems are in _thermal equilibrium_

- Similarly, for two systems _with fixed $U$_ and $N$, sharing a _fixed total volume_, with a _frictionless, movable partition_ between them:
$$dS=\left(\frac{p_1}{T_1}-\frac{p_2}{T_2}\right)dV_1\geq0$$
- Hence, if $T_1=T_2$, the _partition moves towards the system with lower pressure_, until $p_1=p_2$, where _mechanical equilibrium is reached_

- Similarly, for two systems _with fixed_ $U$ and $V$, sharing a _fixed total number of particles_, able to _exchange particles_ between them:
$$dS=\left(\frac{\mu_2}{T_2}-\frac{\mu_1}{T_1}\right)dN_1\geq0$$
- Hence, if $T_1=T_2$, _particles go towards the system with lower chemical potential_, until $\mu_1=\mu_2$, where _chemical equilibrium is reached_

## Changes in heat
- Many process involving heat exchange are done with _constraints_ on the system, such as _constant volume or pressure_

- If heat is _emitted by_ a system $(\dbar Q<0)$, the process is said to be _exothermic_
- If heat is _absorbed by_ a system $(\dbar Q>0)$, the process is said to be _endothermic_

### Constant volume
- The change in internal energy $U$ for any process:
$$dU=T\,dS+p\,dV=\dbar Q+\dbar W$$
- Consider a _reversible, isochoric_ $(dV=0)$ process:
$$dU)_V=T\,dS=\dbar Q_\text{rev})_V$$
- Any _reversible heat change_, at _constant volume_, is always equal to the _change in internal energy_
- Hence, for this type of process:
$$\displaylines{dU=C_V\,dT \\ \Delta U=\int_{T_1}^{T_2}C_V\,dT}$$

### Constant pressure
- The change in enthalpy $H$ for any process:
$$\displaylines{H=U+pV \\ dH=dU+pdV+Vdp=TdS+Vdp}$$
- Consider a _reversible, isobaric_ $(p=0)$ process:
$$dH)_p=T\,dS=\dbar Q_\text{rev})_p$$
- Any _reversible heat change_, at _constant pressure_, is always equal to the _change in internal energy_
- Hence, for this type of process:
$$\displaylines{dH=C_p\,dT \\ \Delta H=\int_{T_1}^{T_2}C_p\,dT}$$

## Availability and variational principles
- Often times, given the _constraints_ on a system (e.g. a _reservoir_), one may want to know:
	- The maximum amount of _work_ that can be _extracted_ from the system
	- The quantity to _extremise_ in order to _maximise entropy of the universe_

- Consider a system, in contact with infinitely large _surroundings_, at _fixed_ temperature $T_0$ and pressure $p_0$: ![[System with surroundings.png|300]]
- The system is _free to exchange heat with and do work on_ the surroundings

- If heat $\dbar Q$ _enters_ the system, then the entropy change _of the system_ $dS\geq \dbar Q/T_0$ 
- The first law is then:
$$\dbar Q=dU-(\dbar W-p_0\,dV)$$
- $\dbar W$ is _work done on the system_, specifically _excluding the surroundings_
- Hence:
$$\dbar W\geq dU+p_0\,dV-T_0\,dS$$
- Define the _availability_ of the system as:
$$A=U+p_0V-T_0S$$
- Hence, _work done on the system by an external agent can increase its availability_:
$$\dbar W\geq dA$$
- If the process is _reversible_, then $\dbar W=dA$
- In other words, $dA$ is the _maximum amount of work that can be done by the system_

- $dA$ can also be written as:
$$dA=(T-T_0)\,dS-(p-p_0)\,dV$$
- If the system is at _the same condition as the surroundings_, then it can _do no work_

- If a system _cannot do work on other systems_:
$$dA\leq0$$
- This means the system will _tend towards an equilibrium where $A$ is minimum_

- For an _isolated_ system with _fixed volume_, $dS\geq0$ 
- For a system with _constant volume_, fixed at $T_0$, $F$ must be _minimised_
- For a system at _constant pressure_, fixed at $T_0$, $G$ must be _minimised_

- For specific situations, it is useful to derive inequalities considering $dS$ of both the system _and the reservoir_, where the _total must never decrease_
	- For the _reservoir_, all heat exchange is _reversible_, hence $\dbar Q_\text{res}=T_0dS_\text{res}$

## The Free Energies
- The term _free energy_ indicates the _work that can be extracted by the system_

### Helmholtz Free Energy
- At _constant temperature_ $T_0$, the _total_ work done _on the system_ (including surroundings at $p_0$, plus any external sources), is $\dbar W-p_0\,dV$
	- Where $\dbar W$ is defined as above (not including surroundings)
- Then, using the _inequality for availability_ above:
$$\dbar W_\text{tot}=\dbar W-p_0\,dV\geq dA)_{T=T_0}-p_0dV=dF)_{T=T_0}$$
- This can also be derived by considering considering the _entropy change of the universe_, when the system is connected to a _reservoir_ at $T_0$

- Hence, at $T_0$, $-dF)_{T=T_0}$ is the _maximum work obtainable from the system_:
$$\dbar W_\text{by})_{T=T_0}\leq dF)_{T=T_0}$$
- At _constant $T$ and $V$_, the system will _continue to do non-expansion work_ until the system is _at equilibrium_, where $dF=0$
	- More "useful" for physicists

### Gibbs Free Energy
- Consider a system at _constant temperature $T_0$ and pressure $p_0$_
- The system is _not entirely $p-V$_, meaning there are _other system variables_ $x_i$, with _conjugate variables_ $X_i$
	- Example: a mixture of _reacting chemical species_
- Let the work _done by the system_ consist of a $p-V$ work term, as well as a _non-expansion work_ term:
$$\dbar W_\text{by}=p_0\,dV+\sum_i X_i\,dx_i$$
- Then, by either considering _availability_ or _total entropy change_, one gets:
$$\sum_i X_i\,dx_i\leq -dG)_{T,p}$$
- Hence, at $T_0$ and $p_0$, $-dG)_{T,p}$ is the _maximum non$-pV$ work obtainable from the system_

- At _constant $T$ and $p$_, the system will _continue to do non-expansion work_ until it is _at equilibrium_, where $dG=0$
	- Especially useful for studying systems in chemistry
	- Example: [[Chemical thermodynamics#Reactions and equilibrium|Equilibrium in chemistry]]

## Scaling the system
- Let there be a system with _one type of particle_
- Then, consider _scaling the system_, causing all _extensive_ variables to _increase_, while _keeping intensive variables constant_:
$$dU=TdS-pdV+\mu dN$$
- One can come to the conclusion that:
$$U=TS-pV+\mu N$$
- Or, by rearranging terms:
$$G=\mu N$$
- Hence, the _chemical potential_ $\mu$ can be considered _Gibbs Energy per particle_

## Gibbs-Duhem relation
- From the formula for $U$, one gets:
$$S\,dT-V\,dp+N\,d\mu=0$$
- Defining the _entropy density_ $s$ and _number density_ $n$:
$$dp=s\,dT+m\,d\mu$$
- This is the _Gibbs-Duhem relation_

## Thermodynamic derivatives
- Heat capacity

- Isothermal _compressibility_

# Thermodynamic systems
- The above discussion is _general_, applying to _all systems_
- However, they can be _applied in specific scenarios_, given an _equation of state_ which connects all state variables

## Ideal gases
- An ideal gas assumes _no molecular interactions_, and _no molecular size_

### Equation of state
- A series of observations on the _ideal gas_:
	- _Boyles' Law_ states that at _constant temperature_, $pV$ is a _constant_
	- _Charles' Law_ states that at _constant pressure_, $V/T$ is a _constant_
- This leads to a _reference-independent, absolute temperature scale_, where temperature is commonly labelled $T$
	- This coincides with the absolute temperature scale from consideration of [[#The Carnot engine]]
- At _zero temperature_, $pV=0$

- _Avogadro's Law_ then states that for _equal volumes_ of gas at _the same pressure and temperature_ must contain _equal numbers of molecules_

- Combining the previous gas laws, one gets the _ideal gas law_:
$$pV=nRT=NkT$$
	- $n$, $N$: Number of molecules (in moles or pure number)
	- $R$, $k$: _universal_ constants

- This is the _equation of state_ for an ideal gas

### Internal energy from kinetic theory
- The expression for internal energy relies on _kinetic theory_
- By considering the movement of $N$ particles in a _cuboid_ box:
$$p=\frac{Nm}{V}\mean{v_x^2}=\frac{1}{3}\frac{Nm}{V}\mean{v^2}$$
- Hence:
$$U=\frac{1}{2}Nm\mean{v^2}=\frac{3}{2}NkT$$
- The energy is _completely temperature-dependent_

### Heat capacities
- Recall the expressions for [[#First law, energy, and heat capacities for gases|heat capacities of a gas]] $$\displaylines{C_V=\left(\pd{U}{T}\right)_V \\ C_p=\left(\pd{U}{T}\right)_V+\left[\left(\pd{U}{V}\right)_T+p\right] \left(\pd{V}{T}\right)_p}$$
- Since $U=U(T)$, using the _ideal gas equation of state_:
$$\left(\pd{U}{V}\right)_T=0 \hspace{1cm} p\left(\pd{V}{T}\right)_p=Nk$$
- Hence, the _heat capacities for one mole of gas_ are:
$$\displaylines{C_V=\frac{3}{2}R \hspace{1cm} C_p=\frac{5}{2}R \\ C_p-C_V=R \hspace{1cm} \gamma=\frac{C_p}{C_V}=\frac{5}{3}}$$
- Using the _adiabatic ratio_ $\gamma$, $C_p$ and $C_V$ can be rewritten as:
$$C_V=\frac{1}{\gamma-1}R\hspace{1cm} C_p=\frac{\gamma}{\gamma-1}R$$

### Entropy
- Using the expression for an _infinitesimal change_ in entropy, for $n$ _moles_ of gas:
$$dS=\frac{\dbar Q_\text{rev}}{T}=\frac{dU}{T}+\frac{p}{T}\,dV=\frac{nC_V}{T}\,dT+\frac{nR}{V}\,dV$$
- Then using the ideal gas equation of state and _integrating along any path_:
$$S=nC_V\ln T+nR\ln V+S_0(n)$$
- $S_0(n)$ is an _integration constant_ dependent on $n$, which has to be derived from [[Foundations of statistical thermodynamics|statistical mechanics]]
- Since $n\ln V$ is not extensive, $S_0(n)$ has to be manipulated to _make entropy extensive_:
$$S(n)=nC_V\ln T+nR\ln\frac{V}{n}+nS_0'$$
- The _first term_ accounts for the effects of _heat input_
- The _second term_ accounts for the effects of _particle configuration_ in the container

### Isothermal and Joule expansion
- If a gas expands _isothermally_, then there is _no change in internal energy_:
$$\Delta U=\Delta Q+\Delta W=0$$
- As the gas must do _work_ to its surroundings, it has to _absorb heat_ in order to do so
- If the expansion is done _reversibly_ (i.e. with a piston that can _match the gas pressure_), then the heat absorbed is:
$$\Delta Q=-\Delta W=\int_{V_1}^{V_2} p\,dV=\int_{V_1}^{V_2}\frac{nRT}{V}\,dV=nRT\ln\frac{V_2}{V_1}$$
- The _entropy change_ associated with the process is:
$$\Delta S=nR\ln(V_2/V_1)$$
- This agrees with the expression given [[#Entropy|above]]
- This _reversible change_ results in _no change in entropy of the universe_, as the _reservoir_ used to maintain temperature will _lose heat_

- If instead, the gas were to expand _suddenly_, in a _thermally isolated_ container previously filled with _vacuum_:
$$\Delta U=\Delta Q=\Delta W=0$$
- This is termed _Joule expansion_
- However, since entropy is a _state function_, the entropy change is _still_ given by the expression above
- In this case, there is an _entropy gain for the universe_

### Adiabatic expansion
- If the gas is _thermally isolated_, any _work done_ by it costs its internal energy:
$$dU=\dbar W$$
- If done _reversibly_:
$$C_V\,dT=p\,dV$$
- By integrating appropriately, one can get:
$$pV^\gamma=\text{const.}$$
- By using the ideal gas equation of state, one can also get:
$$TV^{\gamma-1}=\text{const.}$$
- This expression can also be obtained from the fact that the [[#Entropy|entropy of the ideal gas]] remains _constant_

### Mixing and the Gibbs Paradox
- Recall that for the _Joule expansion for $n$ moles of one type of gas_:
$$\Delta S=nR\ln\left(\frac{V_2}{V_1}\right)$$
- Now consider _two distinguishable, non-interacting gases_, separated by a _partition_:
![[Gibbs Paradox setup.png]]
- If the partition is _removed_, since the gases _do not interact_, the entropy is simply _additive_:
	$$\Delta S_\text{tot}=n_1R\ln\left(1+\frac{V_2}{V_1}\right) + n_2R\ln\left(1+\frac{V_1}{V_2}\right)$$
	- The corresponding _reversible process_ used in this case requires _separate isothermal expansions_ of each gas, using _partitions only permeable to one gas_
- However, if the two gases are made the _same_, then $\Delta S$ _vanishes_ despite the same action of removing the partition

- This leads to the fact that the _statistical mechanics of indistinguishable particles is completely different_
- If the two gases are the same, then _effectively nothing happens_, so $\Delta S=0$

## Engines
- In general, an engine is a [[#Cyclic processes, refrigerators and engines|cyclic process]] which involves _inputting heat $Q_h$ into a gas_, converting it into _work $W$ done by the gas on another system_
- The heat input is usually done via a _high-temperature reservoir_

- The _second law_ (specifically, [[#Carnot efficiency and thermodynamic temperature|Carnot's Theorem]] and [[#Clausius and Kelvin|Kelvin's statement]]) state that there are _no perfectly efficient engines_
- The heat $Q_l$ which is _not converted to work_ is then _expelled_, typically into a _low temperature reservoir_:
![[General engine.png|300]]
- As the gas has to _do net positive work_, the cycle appears _clockwise_ on a $p-V$ diagram:
![[Engine work done.png|350]]
$$W=\oint p\,dV$$

- The _efficiency_ of the engine is then defined similarly to the Carnot engine:
$$\eta=\frac{W}{Q_h}=1-\frac{Q_l}{Q_h}$$
- From Carnot's Theorem, for any engine consisting of only _reversible processes_, its efficiency is the _same as the Carnot engine_:
$$\eta_\text{rev}=\eta_\text{Carnot}=1-\frac{T_l}{T_h}$$
- For any engine with _irreversible_ processes:
$$\eta_\text{irrev}<\eta_\text{rev}$$
- _Real_ heat engines are often _irreversible_
	- Friction and heat conduction cause _heat loss_
	- Ideal processes often require high _speed_ and temperature/pressure _gradients_
	- Hence, diagrams of engine cycles are _idealised_

- Example: the _Otto_ and _Diesel_ cycles
	- The _Otto_ cycle imitates an _internal combustion engine_
	- It _takes in_ fuel and air _before_ performing the cycle $1\to2\to3\to4$, with the _isochoric heating_ performed by an _combustion_, and _isochoric cooling_ performed by an exhaust valve, plus _adiabatic expansion and compression_ in between
	- _After_ the cycle, the gas is _expelled_ before more fuel and air is taken _in_
	![[Otto_cycle-transformed.png|375]]
	- The _efficiency_ of the cycle is given by: $$\eta_\text{Otto}=1-r^{1-\gamma}\equiv 1-\left(\frac{V_1}{V_2}\right)^{1-\gamma}$$
	- $r$ is known as the _compression ratio_
	- Typically, the _ideal_ efficiency that can be achieved is $\approx 0.6$, but only _half_ that is achieved
		- When $r$ is _too high_, it can cause _shock waves_ that damage the engine
	- It can be improved with the _Diesel cycle_: ![[fig5DieselIdeal_web-transformed.jpeg]]
	- The combustion is instead at constant _pressure_, with the fuel being _injected_ during the process
	- While having a _lower ideal efficiency than the Otto cycle_, it is easier to _achieve_:
	$$\displaylines{\eta_\text{D}=1-r^{1-\gamma}\left(\frac{\alpha^\gamma-1}{\gamma(\alpha-1)}\right) \\ \alpha=\frac{V_3}{V_2}}$$
	- The Otto and Diesel engines are _internal combustion engines_, where everything is done in _one container_

- Example: the _Stirling_ engine
	- It is an _external_ combustion engine
	- Gas is expanded in a _hot cylinder_, moved to the _cold cylinder_ where it is then _compressed_, before being transferred _back into the hot cylinder_
	![[Stirling cycle.png]]
	- It is often done via two pistons in _quadrature_ ($90^o$ out of phase):
	![[Stirling engine operation.png|600]]
	- The wire _between cylinders_ acts as a "regenerator" to _store heat_, so the process is _not too irreversible_

## Refrigerators and heat pumps
- If an engine runs _backwards_, converting _work $W$ done on the system_, along with _heat $Q_l$ extracted_ from a low-temperature reservoir, into heat $Q_h$, which is then _expelled from the gas_, into a _high-temperature reservoir_:
![[Refrigerator schematic.png|300]]
- This is a _refrigerator_, aimed at _keeping the low temperature reservoir cool_

![[Refrigerator work done.png|350]]

- The _efficiency_ of the refrigerator is defined as:
$$\eta=\frac{Q_l}{W}$$
- It is the _heat extracted per unit of work_, and can be _larger than $1$_

- The _ideal refrigerator_ is the _Carnot cycle run in reverse_, which still follows:
$$\frac{Q_l}{T_l}=\frac{Q_h}{T_h}$$
- The _ideal efficiency_ is then:
$$\eta_\text{Carnot}=\frac{T_l}{T_h-T_l}$$

- The same setup can also be utilised as a _heat pump_, which aims to _maintain the temperature of the hot reservoir_
- In this case, the efficiency is:
$$\eta=\frac{Q_h}{W}>1$$
- The ideal efficiency is:
$$\eta_\text{Carnot}=\frac{T_h}{T_h-T_l}$$
- Hence, it is _more efficient than direct heating_

## Non-gaseous systems



# The third law and absolute zero
- Originated from _electrochemical measurements_ at low temperatures:
>[!info] Nernst's statement
>Near absolute zero, all reactions in a system in internal equilibrium take place with no change in entropy

- Further _postulate_:
>[!info] Planck's statement 
>The entropy of all systems in _internal equilibrium_ at absolute zero may be _taken at zero_

- _Experimentally_, even at temperatures _close_ to absolute zero, systems may have some "frozen-in" disorder, or be in a _non-equilibrium_ state that requires energy to settle into _internal equilibrium_

- _Quantum mechanically_, from the [[Foundations of statistical thermodynamics#Statistical view of temperature|statistical definition of entropy]], this means that there is _no degeneracy_ at the _ground state_
	- For _large systems_, perturbations will ensure there is _splitting_, even at the ground level
	- Components of _large systems_ will also still be able to _exchange energy_ before reaching _internal equilibrium_

## Determining entropy
- Experimentally, _heat capacity_ gives information on entropy:
$$\displaylines{dS=\frac{\dbar Q_\text{rev}}{T} \\ C_p=T\left(\pd{S}{T}\right)_p}$$
- By mapping $C_p$ as a function of _temperature_:
$$S(T)=S(T_0)+\int_{T_0}^T \frac{C_p}{T}\,dT$$
- The Third Law allows $S(T=0)$ to be set at _zero_, such that entropy has a _definite value_ at any temperature

## Consequences
- Consider the _heat capacity_ when holding variable $x$ constant:
$$C_x=T\left(\pd{S}{T}\right)_x$$
- A phase of a system goes to zero entropy _smoothly_
- Hence, _heat capacities go to zero_ at absolute zero
- This leads to the fact that _classical models_ which predict _constant heat capacities_ ([[Foundations of statistical thermodynamics#The classical limit: equipartition|equipartition of energy]]) are _false_, and only good approximations at _high temperatures_

- Similarly, from the _Maxwell relations_, other derivatives such as _expansivity_ vanish:
$$\frac{1}{V}\left(\pd{V}{T}\right)_p=\frac{1}{V}\left(\pd{S}{p}\right)_T\to0$$

## Unattainability of absolute zero
- Consider using a _Carnot cycle_ to cool a system

- It can be shown that a consequence of the third law is that _absolute zero can never be obtained in finite steps_
![[Third law cooling.png]]

>[!info] An alternative form of the Third Law 
>It is impossible by any procedure, no matter how idealized, to reduce the temperature of
>any system to zero temperature in a finite number of finite operations



# Phase equilibrium and transitions
- The _van der Waals gas_:
$$\left( p+a \frac{N^{2}}{V^{2}} \right)(V-Nb)=Nk_{B}T$$