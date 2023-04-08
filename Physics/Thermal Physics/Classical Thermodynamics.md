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

- _Justifying_ all of the laws given below is the job of [[statistical thermodynamics]]

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

- Historical note: an actual absolute/thermodynamic temperature scale first came from [[#Carnot efficiency and thermodynamic temperature|consideration of the Carnot engine]]

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

## Cyclic processes
- Due to this path dependence, one can do a _cyclic process_, and _convert work done on the gas into heat_, which is then _extracted from the gas_:
$$Q_\text{net, extracted}=W=-\oint p\,dV$$
- Since the gas goes through a _cycle_, $\Delta U=0$
- At _some points_ during the process, heat will be _input into the gas_, hence it is _not perfectly efficient_
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
$$\displaylines{W=Q_h-Q_l \\ \eta \equiv\frac{W}{Q_h}=1-\frac{Q_l}{Q_h}}$$
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
- From [[#Ideal gases|computing efficiency for ideal gases]], it can be shown that _this is the same temperature as the_ [[#The ideal gas equation of state|ideal gas scale]]

## Clausius' inequality and entropy
- From the definition above, for a Carnot cycle:
	$$\sum_\text{Carnot}\frac{Q}{T}=0$$
	- Sign convention: any heat _supplied_ is positive, heat _expelled_ is negative

>[!info] Clausius' Theorem
>For any cyclic process, with $\dbar Q>0$ for heat supplied to the system:
>$$\oint \frac{\dbar Q}{T}\leq 0$$
>The equality holds for reversible processes
- Proof: Consider some engine $E$ with the Carnot engine running in reverse
	$$\displaylines{W=Q_h-Q_l=Q_h'-Q_l' \\ Q_h'>Q_h \\ \frac{Q_h'}{T_h}-\frac{Q_l'}{T_l}=(Q_h'-Q_h)\left(\frac{1}{T_h}-\frac{1}{T_l}\right)\leq0}$$
	- Any _continuous_ cycle can be _cut_ into discrete "bits"
	- Equality for reversible cycles: the inequality holds in both directions

- This implies that for _reversible paths_, one can define some function $S$ such that:
$$S(B)-S(A)=\int_A^B \frac{\dbar Q}{T} \hspace{1cm}\text{ for any reversible path AB}$$
- This function is _entropy_, which is a _state function_:
$$dS=\frac{dQ_\text{rev}}{T}$$
- Like energy, it is _extensive_, and defined _up to a constant_ (Later given by the Third Law)

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

- For the universe as a whole, $U$ remains constant while $S$ increases
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
- So far, to descibe a gas (assuming constant $N$), one can deploy the variables:
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

- From the Master Equation, one can write:
$$T=\left(\pd{U}{S}\right)_V\hspace{1cm}p=-\left(\pd{U}{V}\right)_S$$
- It can also be _inverted_ to give _entropy as a function of $U$ and $V$_:
$$\displaylines{dS=\frac{1}{T}\,dU+\frac{p}{T}\,dV}$$

## Thermodynamic potentials

## Maxwell relations

## Number of particles and the chemical potential

# Thermodynamic systems

## Ideal gases

## Engines

## Refrigerators

## Non-gaseous systems

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

