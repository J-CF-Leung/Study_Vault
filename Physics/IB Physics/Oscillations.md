#IB_Natsci 

## The simple harmonic oscillator
- Applies for a quadratic potential:
$$V(x)=\frac{1}{2}m\omega^2x^2$$
- General equation of motion:
$$\ddot{x}=-\omega^2x$$
- Solution for $x(t)$:
$$x=A\cos(\omega t+\phi)$$
	- $A$ and $\phi$ _depend on initial conditions_

- Simplest example: mass $m$ on spring obeying Hooke's law with spring constant $k$
	- Equation of motion $m\ddot{x}=-kx$
	- $\omega^2=k/m$

## The driven and damped harmonic oscillator
$$\displaylines{m\ddot{x}=F(t)-b\dot{x}-kx \\ F(t)=m\ddot{x}+b\dot{x}+kx}$$
- Define the parameters $\omega_0$ and $\gamma$:
$$\omega_0=\sqrt{\frac{k}{m}}$$
$$\gamma=\frac{b}{m}$$
$$\ddot{x}+\gamma\dot{x}+\omega_0^2x=\frac{F(t)}{m}$$
- The dimensionless _quality factor_ $Q$:
$$Q=\frac{\omega_0}{\gamma}$$
- Represent oscillating quantities using _phasors_, taking the _physical quantity as the real part_
$$x=\mathbb{R}[x_0\exp i(\omega t+\phi)]$$
- $A$ and $\phi$ depend on boundary conditions
- Velocity is $\pi/2$ ahead, acceleration is $\pi$ ahead

### Free damped oscillations
$$\ddot{x}+\gamma\dot{x}+\omega_0^2x=0$$
$$x=A\exp(pt)$$
$$p=-\frac{\gamma}{2}\left(1+\pm\sqrt{1-4Q^2}\right)$$
- Cases:
	- Light damping: $\gamma<2\omega_0$, $Q>0.5$
	- Critical damping: $\gamma=2\omega_0$,  $Q=0.5$
	- Heavy damping: $\gamma>2\omega_0$,  $Q<0.5$

#### Light damping
$$p=-\frac{\gamma}{2}\pm i\omega_f$$
 $$x=e^{-\gamma t/2}\left[A\exp(i\omega_f t)+A^*\exp(-i\omega_f t)\right]$$
	-  $A$ is complex, encodes initial amplitude and phase
$$\omega_f=\omega_0\sqrt{1-\frac{1}{4Q^2}}$$
- For _larger $Q$_, $\omega_f\approx \omega_0$
- _Still oscillates_ for many cycles
- Time constant $\tau$ of amplitude: $2/\gamma=2Q/\omega_0$
- _Energy $U$ decays twice as fast_ with time constant $1/\gamma=Q/\omega_0$
- $Q$ is the _number of radians elapsed_ when a lightly damped oscillation has its energy _decrease to $1/e$ of the initial value_
	- $=$ number of radians for _amplitude_ to decrease to $1/\sqrt{e}$ of original value

#### Critical damping
- $Q=0.5$, $\omega_0=\gamma/2$
$$x(t)=(C_1+C_2t)\exp(-\omega_0 t)$$
- _Most rapid_ approach to equilibrium _without overshooting_


#### Heavy damping
$$\mu_{1,2}=\frac{1}{2}\left(\gamma \pm\sqrt{\gamma^2-4\omega_0^2}\right)$$
$$x(t)=C_1\exp(i\mu_1t)+C_2\exp(i\mu_2t)$$
- No oscillations, slowly approaches equilibrium without overshooting


### Driven and damped oscillations
$$F(t)=m\ddot{x}+b\dot{x}+kx$$
- Any force can be represented as a sum of sinusoidal components
- Therefore, assume a sinusoidal force, one can find the _steady-state response_:
$$F=\Re\left[F_0\exp(i\omega t)\right]\hspace{1.5cm}x(t)=\Re\left[x_0\exp(i\omega t)\right]$$
$$x_0=\frac{F_0}{m}\frac{1}{(\omega_0^2-\omega^2)+i\gamma\omega}$$

#### The response function
- Define the _response function_ $R(\omega)=x_0/F_0$, its magnitude and argument are:
$$|R(\omega)|=\frac{1}{m\sqrt{(\omega_0^2-\omega^2)^2+\gamma^2\omega^2}}$$
$$\text{arg}(R)=\arctan\left[-\frac{\gamma\omega}{(\omega_0^2-\omega^2)}\right]$$
#### Frequency regimes
- Low frequency: response is _almost in phase_, motion _controlled by spring constant_
	- $|R|\approx 1/k$
	- $\text{arg}(R)\approx 0$
- High frequency: response is in _anti-phase_, motion _controlled by inertia_
	- $|R|\approx 1/(m\omega^2)$
	- $\text{arg}(R)\approx\pi$
- Resonance: _maximum value_ of $|R|$, $\omega\approx\omega_0$
	$$\omega_\alpha=\omega_0\sqrt{1-\frac{1}{2Q^2}}$$
	- $|R|\approx Q/(m\omega_0^2)$
	- $\text{arg}(R)\approx\pi/2$

#### Velocity response
- Define the _velocity response function_ as:
$$\frac{v_0}{F_0}=\frac{i\omega x_0}{F_0}=\frac{1}{m[(\omega_0^2-\omega^2)/(i\omega)+\gamma]}$$
- The velocity resonance occurs for maximum $|v_0|$, at $\omega_0=\omega$, and $|v_0|=F_0/(\gamma m)$
$$\text{arg}(v_0/F_0)=\arctan\left[\frac{\omega_0^2-\omega^2}{\gamma\omega}\right]$$
#### Acceleration response
- Acceleration response is defined as:
$$\frac{a_0}{F_0}=-\frac{1}{m[(\omega_0^2-\omega^2)/\omega^2+i\gamma/\omega]}$$
- The acceleration resonance occurs at:
$$\omega_{acc}=\omega_0\left(1-\frac{1}{2Q^2}\right)^{-1/2}$$
- Acceleration resonance frequency is slightly above $\omega_0$

#### Power
- The power is $P=Fv$
- Multiplying the real parts of both, one gets:
$$P=\Re(F_0e^{i\omega t})\Re(v_0e^{i\omega t})=\frac{1}{2} \Re[F_0v_0e^{2i\omega t}+F_0v_0^*]$$
- The time average is:
 $$\braket{P}=\frac{1}{2}\Re[F_0v_0^*]=\frac{1}{2}|F_0||v_0|\cos(\phi_F-\phi_v)$$
	- Force and velocity are _not necessarily in phase_, dependeing on the system
	- The cosine is the _power factor_
	- In phase: $\braket{P}$ is at a maximum
	- _In quadrature_ ($\pi/2$ out of phase): $\braket{P}=0$
- The mean power _required to drive a damped oscillator_, substituting the velocity response function:
 $$\braket{P}=\frac{1}{2}b|v_0|^2$$
	- Power input = power dissipated by damping force
- _Power resonance_ occurs at the same frequency as _velocity resonance_, at $\omega=\omega_0$
- The width of the power resonance peak is characterised by the _half-power points_ $\omega_+$ and $\omega_-$, where $\braket{P}(\omega_\pm)=1/2$
- Using algebra, the _half-power bandwidth_ is:
$$\Delta\omega=\omega_+-\omega_-=\gamma$$
- This gives another definition of the quality factor:
 $$Q=\frac{\omega_0}{\Delta\omega}$$
	 - The better the oscillation, the _narrower the peak_

#### The transient response
- The motion of the _oscillator without driving force_ is the _complementary function_
	- Determined by _2 parameters depending on initial conditions_
- The motion due to the driving force is the _particular integral_

- The _general solution_ to the equation of motion for the _driven and damped_ harmonic oscillator is a _linear combination_ of the complementary function and particular integral

## LCR circuits
- Given a circuit with supplied voltage $V(t)$, resistance $R$, capacitance $C$, inductance $L$:
$$V(t)=\frac{1}{C}q+R\dot{q}+L\ddot{q}$$
- One gets:
$$\ddot{q}+\gamma \dot{q}+\omega_0^2q=\frac{V}{L}$$
$$\gamma=\frac{R}{L}\hspace{1.5cm}\omega_0^2=\frac{1}{\sqrt{LC}}$$
- The circuit _can be driven_, with $V=\Re[V_0\exp(i\omega t)]$, giving the current $I\equiv\dot{q}=\Re[I_0\exp(i\omega t)]$ 
- The quality factor of the oscillations in this circuit is:
$$Q=\frac{\omega_0}{\gamma}=\frac{1}{R}\sqrt{\frac{L}{C}}$$
- The _current response_ is:
$$\frac{|I|}{|V|}=\frac{1}{\sqrt{(\omega L-\frac{1}{\omega C})^2+R^2}}$$
- Peaks - 
	- Current: analagous to velocity, peaks at $\omega=\omega_0$
	- Voltage of capacitor $V_C$: analagous to displacement, peaks below $\omega_0$
	- Voltage of inductor $V_L$: analagous to acceleration, peaks above $\omega_0$
- The _impedance_ $Z$ is defined as:
	$$Z=\frac{V_0}{I_0}$$
	- The voltage amplitude needed to drive a circuit with current amplitude $I_0$
- The electrical impedance of an LCR circuit is given as:
$$Z=i\omega L+\frac{1}{i\omega C}+R=Z_L+Z_C+Z_R$$
- The power dissipated is given as:
$$\braket{P}=\frac{1}{2}\Re[V_0I_0^*]=\frac{1}{2}|I_0|^2\Re(Z)=\frac{1}{2}R|I_0|^2$$
### Mechanical impedance
- Impedance can also be defined for a mechanical system:
$$Z_{mech}=\frac{F_0}{v_0}$$
- For the mechanical system given above:
$$Z=m\left[\frac{\omega_0^2-\omega^2}{i\omega}+\gamma\right]$$
- The mean power dissipated becomes:
$$\braket{P}=\frac{1}{2}|v_0|^2\Re(Z)=\frac{1}{2}b|v_0|^2$$

## Atoms as oscillators
- An _electron cloud_ with Bohr radius $a$ can be driven by an _oscillating electric field_ $E_0\exp(i\omega t)$
- The nucleus displaced by $x$ feels a _linear restoring force_ 
	- Charge $\propto x^3$, force is inverse-square
- For hydrogen, the _undamped natural frequency_ is:
$$\omega_0^2=\frac{k}{m}=\frac{e^2}{4\pi\epsilon_0m_ea^3}$$
- Visible light has frequency $f$ orders of magnitude below $\omega_0$, hence amplitude is relatively unaffected by change in $\omega$

- Damping: Larmor radiation of accelerating electron cloud
- $P_{rad}\propto x_0^2$
- Since mean energy $W \propto x_0^2$, the oscillation energy decays exponentially
- The usual quality factor of an atom $\approx 10^6$

## Anharmonic oscillations
- Many potentials are _non-quadratic_
- Equations become non-linear, superposition is not possible

- Example: pendulum for large amplitudes, expanding $\sin\theta$ to $\theta^3$:
$$\ddot{\theta}+\frac{g}{L}\theta\left(1-\frac{\theta^2}{6}\right)=0$$

- Typical symmetric, anharmonic potential
$$V(x)=\frac{kx^2}{2}\left(1+\frac{\alpha}{2}x^2\right)$$
$$\ddot{x}+(1+\alpha x^2)\omega_0^2x=0$$
	- Positive $\alpha$: "Hard" potential, spring stiffens with extension

- Small anharmonicity ($|\alpha|<<1$):
$$x(t)=A(\cos\omega_ft+\epsilon\cos{3\omega_ft}\,+\,...)$$
	- For small $|\alpha|$, $\omega_f\approx \omega_0$, $\epsilon <<1$
	- Approximating $x\approx \cos\omega t$, $\cos^3$ term gives $\cos 3\omega t$

- Keeping first-order terms in $\epsilon$ and $\alpha A^2$, one gets:
$$\omega_f\approx\omega_0\left(1+\frac{3}{8}\alpha A^2\right)$$
$$\epsilon\approx\frac{1}{32}\alpha A^2$$

- As expected, anharmonic correction increases with $A$
- Period becomes amplitude-dependent
	- Soft potential: longer period as amplitude increases

- For asymmetric potentials, the expansion would include even harmonics


## Linear system with multiple frequencies
- The equation of motion is linear, therefore the responses can be added _as if the individual forces acted separately_
$$F(t)=F_1(t)+F_2(t)\iff x(t)=x_1(t)+x_2(t)$$
$$\displaylines{F(t)=F_1\cos(\omega_1t+\alpha_1)+F_2\cos(\omega_2t+\alpha_2) \\ x(t)=A_1\cos(\omega_1t+\alpha_1+\phi)+A_2\cos(\omega_2t+\alpha_2+\phi)}$$
	- $A_i=F_i|R|$, $\phi=\text{arg}(R)$

### Coherence
- If $\omega_1=\omega_2$, the amplitude depends on the _relative phase_:
$$A^2=A_1^2+A_2^2+2A_1A_2\cos(\alpha_2-\alpha_1)$$
- For $F_1=F_2$:
	- In-phase leads to double amplitude and quadruple power
	- Anti-phase leads to no response

- In practice, the relative phase is likely to drift over time and average to zero
- In that case, the forces are _incoherent_
- For coherency, the forces will need to come from a _common source_

### Different driving frequencies
- If $\omega_1\neq\omega_2$, the response shows _beating_
	- Does not necessarily have to be the same amplitude

- For equal amplitudes, the motion can be written as:
$$x(t)=A'\cos\left(\frac{\omega_1+\omega_2}{2}\,t+\phi'_f\right)\cos\left (\frac{\omega_1-\omega_2}{2}\,t+\phi'_s\right)$$
- There is a fast oscillation at $(\omega_1+\omega_2)/2$, modulated by an envelope of $(\omega_1-\omega_2)/2$

## Superposition
- The equation of motion for the driven and damped harmonic oscillator is _linear_
- If a force is the _sum of different driving forces_ with different frequencies, the solution is _a linear combination of individual responses at each frequency_ 

- _Any_ driving force $F(t)$ can be [[Fourier series and transforms|Fourier transformed]] to give the "weight" of each frequency $g(\omega)$
- For some [[#The response function|response function]] $R(\omega)$, the actual response is a _superposition of responses_:
$$x(t)=\frac{1}{\sqrt{2\pi}}\int g(\omega)R(\omega)\exp[i\omega t]\,d\omega=\mathcal{F}^{-1}\left[R(\omega)\mathcal{F}\{F(t)\}\right]$$

- Suppose a system is struck with a _sharp impulse_ $F(t)=\delta(t)$
- The response is the _impulse response function_ $R'(t)$
- For damped oscillators, $R'$ is the transient after there is some _initial velocity_
- Using the above formula, the relation between the two responses are:
$$R'(t)=\frac{1}{\sqrt{2\pi}}\mathcal{F}^{-1}[R(\omega)]$$
- Any force can be written as a _convolution_ of some function $F(t')$ with $\delta(t-t')$
- From this, the response _can also be written as a convolution_:
$$x(t)=\int F(t')R'(t-t')\,dt'$$