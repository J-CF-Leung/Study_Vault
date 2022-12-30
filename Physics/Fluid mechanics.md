## Basic characteristics of fluid flow
- Fluid: continuous medium
	- Any 'infinitely' small volume element still contains a large number of molecules
- Mathematical quantities:
	- Flow velocity $\bm{v}(x,y,z,t)$
	- Pressure $p(x,y,z,t)$
	- Density $\rho(x,y,z,t)$
### Continuity
- $\bm{j}=\rho\bm{v}$: mass flux density
- Decrease in mass of fluid inside specified volume:
$$-\int\pd{\rho}{t}\, dV$$
- Flow out of closed volume:
$$\oint \bm{j}\cdot \,d\bm{S}=\oint \nabla\cdot(\rho\bm{v})\,dV$$
- Continuity equation:
$$\pd{\rho}{t}+\nabla\cdot(\rho\bm{v})=0$$