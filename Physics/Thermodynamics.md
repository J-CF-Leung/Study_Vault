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

## Fundamentals
For a system with an enormous number of particles, and thus, degrees of freedom, there is an immeasurable number of *microstates*

For thermodynamics to work, 2 fundamental suppositions must be made:
1. After a sufficiently long time, the initial conditions become irrelevant as particles redistribute energy and momentum until equilibrium is reached
2. For a system in equilibrium, all possible microstates are equally likely 
	-[[Fundamental principles of statistical mechanics#The equal probabilities postulate]]

- A *macrostate* is defined by the bulk properties of the system, and incorporates many microstates 
		- The probability of a particular microstate, given a macrostate is governed by the [[Fundamental principles of statistical mechanics#The statistical distribution function|statistical distribution function]]
- Macrostates are described by thermodynamic variables such as $U, N, V, S, T, p, \mu$
- Macrostates with energy more or less equally shared among particles become way more likely

### Energy and entropy
- The entropy of a system is defined as:
$$S=k_B\ln\Omega$$
	-$k_B=$ Boltzmann's constant
	- $\Omega=$ Number of microstates
- At equilibrium, entropy can be expressed as a function of 3 variables:
$$S=S(U,N,V)$$
	- $U=$ internal energy, $N=$ number of particles, $V=$ volume
	- $S, U, N, V$ are extensive variables, as they scale with system size
- The function can be inverted:
$$U=U(S, V, N)$$
- For infinitesimal changes in the system, the differential of internal energy is:
$$dU=\left(\pd{U}{S}\right)_{N, V}dS+\left(\pd{U}{V}\right)_{N, S}dV + \left(\pd{U}{N}\right)_{S, V}dN$$
- This expression defines 3 thermodynamic quantities:
$$T=\left(\pd{U}{S}\right)_{N, V}\hspace{25pt}P=-\left(\pd{U}{V}\right)_{N, S}\hspace{25pt}\mu=\left(\pd{U}{N}\right)_{S, V}$$
	- $T=$ temperature, $p=$ pressure, $\mu=$ chemical potential 
	- $T, p, \mu$ are intensive variables, which do not scale with system size
- This changes the expression to:
$$dU=T\,dS-P\,dV+\mu\,dN$$
### Thermal equilibrium and temperature
- When two bodies are in thermal equilibrium, they must have the same temperature
- Zeroth law: if $A$  is in thermal equilibrium with $B$ and $C$, $B$ and $C$ are in thermal equilibrium with each other
	- i.e. The thermodynamic concept of temperature "makes sense"
- To understand definition of temperature, let there be 2 bodies in thermal contact with small fluctuations
	- Can exchange $U$, but $N$ and $V$ remain fixed
	- Total microstates = $\Omega_1\Omega_2$, total entropy = $S_1+S_2$
	- The most probable macrostate maximises $S$
	- Energy conservation: $\delta U_1+\delta U_2=0$
	- Maximum entropy: $\delta S_1+\delta S_2=0$
	- Using above definition of temperature, $T_1=T_2$

### The first law
$$dU = \dbar Q + \dbar W$$
	- $Q=$ heat transferred from a source outside the system
	- $W=$ work done on the system
- When there is an external pressure $p$ upon the system, with no change in $N$, $\dbar W=-p\,dV$ 
- For equilibrium changes and fixed $N$, $dU=T\,dS+\dbar W$
- Work: mechanical ($-p\,dV$), electrical, spring, magnetic

### The second and third laws
- Second law: Entropy never decreases
	- As time goes on, the number of microstates available to a system never decreases
	- At equilibrium, maximum entropy is reached
- Third law: At absolute zero, the entropy of any body is zero
	- A body cannot be brought to absolute zero by any finite series of operations

## Thermodynamic potentials
- The descriptors of a system come in pairs of intensive and extensive variables
	- $T$ and $S$, $p$ and $V$ for a system with a fixed $N$ 
- For energy, $S$ and $V$ are the _proper independent variables_, as an expression for $U(S,V)$ is all the necessary information to derive all other quantities ($T$, $p$) 
- Other thermodynamic potentials defined as functions of another pair of proper independent variables
	- One variable from $S$ or $T$, another from $p$ or $V$
	- Formulas derived from Legendre transforms
- For a system at equilibrium with fixed $N$, two non-conjugate variables are sufficient to determine the state of the system
### Enthalpy/heat function
- Enthalpy $H$ (or $W$ if you use $R$ for work like Goodstein)
$$\begin{aligned} H(S,P)&=U+PV \\ dH &= T\,dS+V\,dP \end{aligned}$$
- For equilibrium changes at constant pressure, $dH)_P = \dbar Q$

### Helmholtz Free Energy
- Helmholtz Free Energy $F$ (or $A$):
$$\begin{aligned}F(T,V) &= U-TS \\ dF &= -S\,dT-P\,dV\end{aligned}$$
- For equilibrium changes at constant temperature, $dF)_T = \dbar W$
	- Analagous to $dU)_S = \dbar W$
### Gibbs Free Energy
- Gibbs Free Energy $G$ (or $\Phi$):
$$\begin{aligned}G(P,T)&=F+PV=H-TS \\ dG &= -S\,dT+V\,dP \end{aligned}$$

### Maxwell's relations
- Due to the symmetry of mixed derivatives, using the definitions of the potentials:
$$\begin{aligned}\left(\pd{P}{T}\right)_V&=\left(\pd{S}{V}\right)_T \\ \left(\pd{T}{V}\right)_S&=-\left(\pd{P}{S}\right)_V \\ \left(\pd{V}{S}\right)_P&=\left(\pd{T}{P}\right)_S \\ \left(\pd{S}{P}\right)_T&=-\left(\pd{V}{T}\right)_P    \end{aligned}$$
- Holds for any system
- Demonstrates that two non-conjugate variables can determine the behaviour of a system

## Changing number of particles and the chemical potential
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

- Chemical potential is an intensive variable like $P$ and $T$
- Consider a system with one type of particle, scaled up by $\lambda$, and $d(\lambda U)$, one gets:
$$U=TS-PV+\mu N$$
- By considering the differential, $\mu$ is shown to be a function of $P$ and $T$:
 $$d\mu = \frac{V}{N}dP-\frac{S}{N}dT$$
 - The same Legendre transforms apply, allowing $\mu$ to be redefined:
$$G(P,T,N)=\mu N$$

- The chemical potential is not necessarily positive
	- To keep $S$ and $V$ constant while adding a particle, $U$ may have to decrease
	- For strong repulsions, $U$ may increase

### The Landau potential
- With the new pair of conjugate variables, new thermodynamic potentials are available
- The _Landau potential_ is defined as:
$$\displaylines{\Omega(T,V,\mu)=F-\mu N=-PV \\ d\Omega=-S\,dT-P\,dV-N\,d\mu}$$
- With this, differentials of the potentials are related by:
$$(\dbar\Omega)_{T,V,\mu}=(\dbar U)_{S,V,N}=(\dbar F)_{T,V,N}=(\dbar G)_{T,P,N}=(\dbar H)_{S,P,N}$$

## Variational principles

## Magnetic variables



## Gases
