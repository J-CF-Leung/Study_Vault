- Soft matter is matter that is often _deformed_ by _thermal fluctuations and mechanical stresses_

- The tendency to deform is determined by $E$, the _elastic modulus_
- Given _pressure_ $p=F/A$ and _strain_ $\delta L/L$:
$$E=\frac{p}{\delta L/L}$$
- Deformation under _atomospheric pressure_ $10^{5}\,\text{Pa}$
	- _Diamond_ has $E=1.2\times 10^{11}\,\text{Pa}$, which gives _strain_ $8\times 10^{-7}$
	- _Rubber_ has $E\sim 10^{7}\,\text{Pa}$, which gives strain $1\times 10^{-2}$
	- _Gelatin_ has $E\sim 10^{3}\text{Pa}$, which gives strain $100$
		- The strain is _no longer small_, hence the _elastic regime breaks down_

- The elastic modulus can be thought of _characteristic energy per characteristic volume_
- The characteristic energy is the _binding energy per atom_
- The characteristic volume is the _volume per atom_

- Given _thermal fluctuations_ $\sim k_{B}T$, the relevant _length scale_ $(k_{B}T/E)^{1/3}$ is typically _much larger than atomic spacing_
- Hence, _quantum effects are irrelevant_, and _all fluctuations are thermal_

- The _scaling behaviour_ of polymers are typically _independent of atomic composition_
- They also have both _viscous_ and _elastic_ properties
- They can also _self-assemble_ into structures

# Fluids
- A _fluid_ is a collection of _particles_ each with their own mass $m_{i}$, position $\boldsymbol{r}_{i}$ and velocity $\boldsymbol{v}_{i}$
- In some _continuum desciption_, one can take a _small region of space_ and _average over_ the number of particles to obtain the _coarse-grained quantities_ $\rho(\boldsymbol{r})$, $\boldsymbol{v}(\boldsymbol{r})$, etc.

- The fluid obeys _conservation laws_

## Conservation laws
- The _total mass_ within some volume $V$:
$$M_{V}(t)=\int_{V} \, d^{3}\boldsymbol{r} \,\rho(\boldsymbol{r},t) $$
- The _total momentum_ within the volume:
$$\boldsymbol{P}_{V}(t)=\int_{V} \, d^{3}\boldsymbol{r}\,\rho(\boldsymbol{r},t)\boldsymbol{v}(\boldsymbol{r},t) $$
- $\rho \boldsymbol{v}$ is the _momentum density_

### Conservation of mass
- Any _change in mass_ must correspond to some _change in density_, as well as some _in/outflow_:
$$\frac{dM_{V}}{dt}=\int _{V} \, d^{3}\boldsymbol{r}\left( \frac{\partial \rho}{\partial t}\right)=-\int _{S}\rho \boldsymbol{v}\cdot \, d\boldsymbol{S}  $$
- Using the _divergence theorem_, and using the fact that this must be true for _arbitrary volumes_:
$$\frac{\partial \rho}{\partial t}+\nabla\cdot (\rho \boldsymbol{v})=0$$
- For an _incompressible_ fluid where $\rho(\boldsymbol{r},t)=\rho_{0}$:
$$\nabla\cdot \boldsymbol{v}=0$$

### Conservation of momentum
- The _change in momentum_ in the volume:
$$\frac{\partial P_{i}}{\partial t}=\int \, d^3 \boldsymbol{r}\left[ \frac{\partial}{\partial t}(\rho v_{i})+\partial_{j}(\rho v_{i}v_{j})\right]$$
- The second term accounts for _flow in the_ $i-$_direction_, across a _surface_ normal to $j$

- For an _incompressible fluid_:
$$\frac{\partial P_{i}}{\partial t}=\int  \, d^3 \boldsymbol{r}\left[ \frac{\partial}{\partial t}(\rho v_{i})+\rho(\boldsymbol{v}\cdot \nabla)v_{i} \right] $$
- Define the _material derivative_:
$$D_{t}=\partial_{t}+\boldsymbol{v}\cdot \nabla$$
- This is a derivative _following a fluid element_
- This gives:
$$\frac{\partial P_{i}}{\partial t}=\rho D_{t}\boldsymbol{v}$$

- Define a _momentum flux density tensor_:
$$\Pi_{ij}=\rho v_{i}v_{j}$$
- The _momentum outflow_:
$$\int  \, d^3\boldsymbol{r}\partial_{j}(\rho v_{i}v_{j})=\int _{S} \, dx  $$
- _Pressure_ from the fluid is _isotropic_:
$$F^{\text{p}}_{i}=$$
- The _viscous stress_ arising from _velocity gradients_ of the fluid:
$$F_{i}^{\text{visc}}=$$
- The _Newtonian viscous stress tensor_:
	- Equilibrium demands that the stress tensor be _symmetric_
	- One term _vanishes_ in the integral as the fluid is _incompressible_
$$\sigma_{ij}^{\text{v}}=\eta(\partial_{i}v_{j}+\partial_{j}v_{i})$$
- There are also _body forces_ $f_{i}$ such as _gravity_ or _electrostatic_ forces

- This gives the _Navier-Stokes equation_:
$$\rho \frac{D\boldsymbol{v}}{Dt}=-\nabla p+\eta \nabla ^{2}\boldsymbol{v}+\boldsymbol{f}$$

- For a _conservative force_ (such as gravity):
$$\boldsymbol{f}=\nabla V$$

## Reynolds number
- Given a _characteristic length scale_ $L$, _velocity_ $u$
- One can define _time scale_ $L/u$, and _pressure_ $\eta u/L$

- Define the _Reynolds number_, which is _dimensionless_
$$\text{Re}=\frac{\rho uL}{\eta}$$
- _Rescale_ the Navier Stokes equation:
$$\text{Re}()$$
- Flows of the _same Reynolds number_ will _behave similarly_