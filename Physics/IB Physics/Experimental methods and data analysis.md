>[!quote]
>"Experimental and theoretical physics attract rather different personality types, with different temperaments and abilities. Sociologists should find here a ripe field for a fruitful study."
>-Anthony Zee, 徐一鴻

# The process of experimental physics
![[Experimental methods flowchart.png]]
- Goals: _Minimise junk_ and effects _from the transducer_

- Examples of transducers: Thermocouples, photodiodes

- A common method is to convert the original effect into _electrical signals_
- In almost all cases, the measurement tool used to measure signals is the _oscilloscope_

# Measurement circuits and oscilloscopes
- The transducer becomes a _voltage source_ in an electrical circuit
- _Thevenin's theorem_ states that _any linear electrical circuit_ can be replaced by an _equivalent circuit_, consisting of a _voltage source in series with an impedance_
- Let the corresponding _perfect voltage source_ be $V_1$

- The transducer's _output impedance_ is defined as $Z_\text{out}=V_1/i$
	- where $i$ is the current flowing when $V_1$ and the impedance are shorted

- An oscilloscope is modelled as an _input impedance_ in _parallel with an ideal voltmeter_
![[Transducer and scope.png]]
- From this, the p.d. detected by the oscilloscope is:
$$V_\text{in}=V_1\frac{Z_\text{in}}{Z_\text{in}+Z_\text{out}}$$
- For accurate measurements:
	- $Z_\text{in}$ must be _high_
	- $Z_\text{out}$ must be _low_

- In real oscilloscopes, $Z_\text{in}$ _has a capacitive component_
- This leads to _lower voltage measurement for high frequencies_

- To solve this problem, _oscilloscope probes_ are used
- Probes also contain a capacitive component to compensate

- For _current measurements_, a _low_ $Z_\text{in}$ is desired
- To _transfer maximum power_ to another system, the _impedances should match_

# Operational amplifiers
![[Op-amp.png]]
- This is what happens when you eat the silica gel packets

![[Op-amp symbol.png|]]

- $A$ is the _open loop gain_ of the amplifier, defined with:
$$V_\text{out}=A(V_+-V_-)$$

- When connected in a circuit with other components, the gain of the _entire circuit_ is known as the _closed-loop gain_

## Ideality, negative feedback, and the golden rules
- An ideal voltage amplifier has the following properties:
$$A=\infty \hspace{1cm}Z_\text{in}\equiv\pd{V_\text{in}}{i_\text{in}}=\infty \hspace{1cm} Z_\text{out}\equiv\pd{V_\text{out}}{i_\text{out}}=0$$
- Real op-amps: $A>>10^5$
- $Z_\text{in}=\infty$: The op-amp works, _even for infinitesimally small currents_
- $Z_\text{out}=0$: There is no limit to output current

- By itself, an ideal op-amp would give infinite $V_\text{out}$, or the maximum allowed by the power supply. causing _clipping_
- The _closed-loop gain_ of an op-amp circuit can be controlled with _negative feedback_
- The negative feedback eventually creates an equilibrium

- For circuits containing ideal op-amps, there are two _Golden Rules_:
1. Since $Z_\text{in}$ is infinite, _the inputs draw no current_
	- _Output current_ is derived from the power supply, and _unrelated to current input_
2. The voltages on the $+$ and $-$ inputs are _the same, unless output is saturated_
	- Negative feedback is required for this to be true
	- Due to large $A$, $V_+-V_-$ is usually negligible

### The inverting voltage amplifier
![[Inverting voltage amplifier.png]]
- From applying _Kirchoff's rules_ plus the _Golden Rules_, the overall _closed-loop gain_ is:
$$G\equiv\frac{V_\text{out}}{V_\text{in}}=-\frac{R_2}{R_1}$$
- The gain is _purely determined by the two resistors_
- The negative feedback applies for _all frequencies_
- This value of gain is true as long as _$V_\text{out}$ does not exceed the limit set by the power supply_

### The non-inverting voltage amplifier
![[Non-inverting amplifier.png]]
- The _closed-loop gain_ is:
$$G\equiv\frac{V_\text{out}}{V_\text{in}}=1+\frac{R_2}{R_1}$$
- The circuit can also be understood as a _potential divider_

### More on amplifiers
- The external components _do not have to be resistors_
- Adding _inductors and capacitors_ introduces _frequency dependence_
- Potential circuits include _integrators_, _differentiators_, and _filters_
![[Filter circuit with op-amp.png]]

## Non-ideal performance
- Typical op-amps:
	- $10^4\lesssim A\lesssim10^6$, function of frequency
	- High but non-infnite $Z_\text{in}$
	- Low but non-zero $Z_\text{out}$
	- Finite _slew rate_, $dV_\text{out}/dt$

- _Bias current_: the op-amp draws a small current $(10^{-12}-10^{-7})\text{A}$
	- Sets a _limit on external resistance_ as there is a voltage _drop near the input pins_
	- There must be a path allowing the bias currents to _flow to ground_

- _Offset voltage_: Output voltage _independent of_ $(V_+-V_-)$, causing a _differential offset_ of $10^{-3}-10^{-2}\text{V}$, must be balanced with an _external potentiometer_

### Revisiting the non-inverting amplifier
- What a non-inverting amplifier actually looks like:
![[Non-ideal non-inverting amplifier.png]]

- The circuit can be treated as a _system_ with _open-loop gain_ $A'$ and _output impedance_ $Z_\text{out}$:
$$V_\text{out}=A'V_\text{in}-Z_\text{out}i_\text{out}$$
- As usual, for accuracy, _overall_ $Z_\text{in}=V_\text{in}/i_\text{in}$ should be high and $Z_\text{out}$ should be low
![[Op-amp circuit systems approach.png]]

- Taking _$A$ and $r_\text{in}$ to be very large_, $V_\text{out}/V_\text{in}$ is equal to $1+R_2/R_1$, _same as the ideal case_
- Taking the same limit, and low $R_\text{out}$, the impedances approach:
$$Z_\text{out}\approx\frac{R_\text{out}}{A}\left(1+\frac{R_2}{R_1}\right) \hspace{1cm}Z_\text{in}\approx\frac{r_\text{in}A}{1+R_2/R_1}$$
- The circuit has a _higher $Z_\text{in}$_, and _lower_ $Z_\text{out}$ than $r_\text{in}$ and $R_\text{out}$ _of the op-amp_ respectively

- Therefore, the limits _required for close to ideal behaviour_ are:
	- Large $A$
	- High $r_\text{in}$
	- Low $R_\text{out}$

- A useful case of the non-inverting amplifier is the _buffer/follower circuit_
- The buffer circuit has $R_2/R_1=0$
![[Buffer circuit.png]]
- Its characteristics are:
$$V_\text{out}=V_\text{in} \hspace{1cm} Z_\text{in}=Ar_\text{in} \hspace{1cm} Z_\text{out}=\frac{R_\text{out}}{A}$$
- This is very useful for connecting circuits

### Revisiting the inverting amplifier
- Taking the same limits as before, the characteristics of the circuit are:
$$\frac{V_\text{out}}{V_\text{in}}=-\frac{R_2}{R_1} \hspace{1cm} Z_\text{out}=\frac{R_\text{out}}{A}f\left(\frac{R_2}{R_1}\right) \hspace{1cm} Z_\text{in}=R_1+f\left(\frac{R_1}{A},\frac{R_2}{A},\frac{r_\text{in}}{A}\right)$$
- Here, $Z_\text{in}$ becomes _dependent on external components_
- For high $Z_\text{in}$, it is better to use a _non-inverting amplifier_

## Frequency-dependent behaviour
- Overall, the gain of the circuit is _frequency dependent_
- For _high frequencies_, due to capacitive components in $R$, _a phase shift is introduced_
- At a phase shift of $\pi$, _feedback becomes positive_, causing saturation and oscillation

- Practically, _all signals have some high frequency components_
- Therefore, op-amps are designed to _lower gain at high frequencies_
- Typically, after some threshold: 
$$A\propto 1/f$$

- _Decoupling capacitors_ are also connected between the op-amp and the power supply
- They _stop spontaneous oscillations_

# Feedback in systems
- In general, systems with feedback built in can be represented as:
![[System with feedback.png]]
- The input and output are related by:
$$\text{Output}=A(\text{Input}+\beta\times\text{Output})$$
- Here, $\beta$ is the fraction of the output fed back
- For _negative feedback_, $\beta<0$

- For the _non-inverting amplifier_, $\beta=-R_1/(R_1+R_2)$
- For the _inverting amplifier_, $\beta=(1+|-Z_2/Z_1|)^{-1}$

- The _closed-loop gain_ in the general case is:
$$G\equiv\frac{\text{Output}}{\text{Input}}=\frac{A}{1-A\beta}$$
- If $A\beta=1$, the output "explodes"
- For _large $A$_, the gain becomes _independent of $A$_:
$$G\approx-\frac{1}{\beta}$$
- In most systems, $A$ _depends on external conditions_, will _fluctuate_, be _frequency-dependent_, and in some cases, _non-linear_
	- Examples: Biological buffers, stellar burning
- Hence, $|A\beta|>>1$ will be advantageous, especially for signal measurement

## Negative feedback
- In general, negative feedback _stanilises a system against perturbations_
- For a perturbation to the output $\delta$, after one cycle, the increase in output is $\delta/(1-A\beta)$

- In the context of circuits, like the _non-inverting amplifier_:
$$Z_\text{in}=r_\text{in}(1+|A\beta|)\hspace{1cm} Z_\text{out}=R_\text{out}/(1+|A\beta|)$$
- This is desirable for accurate measurement
- Does not apply for the inverting amplifier

## Positive feedback
- Positive feedback often causes _saturation or oscillation_
- If $\beta$ is _frequency dependent_, $A\beta$ can be $\approx 1$ for _only a specific frequency_
- This generates _spontaneous oscillations_ at that frequency

- For example, a circuit can be made to have a _$\pi$ phase shift_ at a specific $\omega_0$
- This acts as both an _oscillator_ and a _filter_ at $\omega_0$
	- Other components may be fed back but _not reinforced_ as much as $\omega_0$

# Errors
- Errors are _always_ given alongside experimental results
- _Random error_ is _unbiased_
	- a.k.a. _average_ error is 0
	- Found by _combining multiple measurements_
- _Systematic errors_ are _constant in time_
	- No amount of repeated measurements can eliminate it
	- Function of _experimental design_
	- Making measurements using _different methods_ can give some idea

- Measurement instruments (e.g. _rulers_) are always _quantised_
- Becomes significant when _magnitude of error is similar to quantisation interval_

- Special case: _electrical resistors_
- The _tolerance_ gives the _full range_ in which resistance can lie

- General case: there is a _Gaussian distribution in error_
- The quoted value is the _standard deviation_

## Statistical treatment for a single variable
- Let there be $N$ _measurements made in the same way_ for some quantity $x$
- The result of measurement $i$ is $x_i$
- The _best estimate_ of the true value is the _mean_:
$$\mean{x}=\frac{1}{N}\sum_ix_i$$
- The _variance_ is used to characterise the _spread_ of $x_i$
$$\displaylines{\text{Var}(x)=\frac{1}{N}\sum_i(x_i-\mean{x})^2}\equiv\mean{(x-\mean{x})^2}\equiv\braket{(x-\Braket{x})^2}$$
- The square root of the variance is the _standard deviation_:
$$\sigma_x=\sqrt{\frac{1}{N}\sum_i(x_i-\mean{x})^2}$$
- However, to estimate the random error in a _single datum_, the expression is:
$$\sigma=\sqrt{\frac{1}{N-1}\sum_i(x_i-\mean{x})^2}$$

- Each measurement is _inependent_, hence the _variances can simply be added_
- The _uncertainty of the mean_ is:
$$\sigma_m=\frac{\sigma}{\sqrt{N}}$$
#### Covariance and independent variables
- Let there be two variables $y$ and $z$, which _both have a mean of 0_
- The _covariance_ between them is defined as:
$$\text{CoVar}(y,z)=\mean{(y-\mean{y})(z-\mean{z})}=\mean{yz}-\mean{y}\mean{z}$$

- The variance of the _sum_ is:
$$\text{Var}(y+z)=\mean{(y-\mean{y}+z-\mean{z})^2}=\mean{(y+z)^2}=\mean{y^2}+\mean{z^2}+2\mean{yz}$$
- If they are _independent of each other_, $\mean{yz}=\mean{y}\mean{z}=0$
- Hence, _the variances add_

- Therefore, _the variances of independent measurements just add_

## Combination of random errors
- Consider a _multi-variable function_ $f(x,y,\dots)$
- Given _standard deviation of each variable_ $\sigma_x,\sigma_y,\dots$
- Assuming _all errors are Gaussian_, $f$ will _also have a Gaussian spread_, with $\sigma_f$:
$$\sigma_f^2=\left(\pd{f}{x}\right)^2\sigma_x^2+\left(\pd{f}{y}\right)^2\sigma_y^2+\dots$$
- Special cases:
$$\displaylines{f=x\pm y\hspace{1cm} \sigma_f^2=\sigma_x^2+\sigma_y^2 \\ f=x^n \hspace{1cm} \frac{\sigma_f}{f}=n\frac{\sigma_x}{x} \\ f=xy \hspace{1cm} \left(\frac{\sigma_f}{f}\right)^2=\left(\frac{\sigma_x}{x}\right)^2+\left(\frac{\sigma_y}{y}\right)^2}$$
## Reducing systematic errors
- Always _calibrate_ instruments

- Measuring voltages: _Reverse connections to voltmeter_ to find systematic error

- Try _different methods_ to find the same quantity

- Impedance measurements: using a _null method_ that uses balance, such as a _bridge_
	- Advantage: Bridge _does not need to be linear or well-calibrated_

- Keep track of _changes with time_

- Use _differential measurements_ and compare with _standards_

- Keep _selection biases and effects_ in mind

# Digital sampling
- Transducers often output _continuous_ signals
- However, due to many difficulties such as maintaining precision or information volume, the data is _sampled digitally_ into a _finite list of values_

- _Instantaneous_ values are taken at _regular intervals_
- Variables include _interval, accuracy, and sampling duration_

- To _digitise_ a signal, one first needs to _sample_ the signal, then _quantise_ it

## Fourier transforms
- Much more detail: [[Fourier series and transforms]]
- For an _aperiodic_ function $f(t)$, the _amplitudes and phases of constituent signals_ is given by the _Fourier transform_ $g(\omega)$:
$$\displaylines{f(t)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty g(\omega)e^{i\omega t}\,d\omega \\ g(\omega)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty f(t)e^{-i\omega t}\,dt}$$

- The _convolution_ of two functions $f$ and $g$ is: 
$$(f*g)(x)=\int_{-\infty}^\infty f(y)g(x-y)\,dy$$
- The relation between _convolutions and multiplications_ in $x-$space and $k-$space are:
$$\displaylines{\mathcal{F}[(f*g)(x)]=\sqrt{2\pi}\mathcal{F}[f]\mathcal{F}[g] \\ \mathcal{F}[f(x)g(x)]=\frac{1}{\sqrt{2\pi}}\mathcal{F}[f]*\mathcal{F}[g]}$$

- For experiments, the common convention is to use _frequency_ $\nu=\omega/2\pi$ 

## The Nyquist criterion and aliasing
>[!Nyquist's Theorem]
>For a _band-limited_ function, one needs to sample at a _minimum_ rate of _twice the highest frequency component_ present in the signal
>If the sampling is _noiseless_, then the signal can be recovered _perfectly_

![[Fourier transform.ipynb]]
- If the signal's maximum frequency is _too high_, then _aliasing_ occurs:
![[Aliasing.png]]

- If the _true frequency_ is $f$ and the _sampling frequency_ is $f_s$, then the _aliased signal_ may be detected at $|kf_s\pm f|$
	- Minus sign: real sinusoidal wave contains components at both $f$ and $-f$
- Therefore, the maximum frequency $f$ must be smaller than $f_s-f$, hence $f_s>2f$

## Signal processing
- The sampled signal $s(t)$ can be understood as a _product_ of the _original signal_ $x(t)$ and a _Dirac comb_ $c(t)$, with spacing $T$
- Then, in _frequency space_, the sampled signal $\tilde{S}(\nu)$ will be a _convolution_ of $\tilde{X}(\nu)$, and another _comb function_ $C(\nu)$, with spacing $1/T$
$$s(t)=x(t)c(t) \iff \tilde{S}(\nu)=\frac{1}{\sqrt{2\pi}}\tilde{X}(\nu)*C(\nu)$$
- This creates _convolution images_ of the original signal:
![[Signal processing.png]]
- Nyquist's criterion corresponds to the fact that _the convolution images must not overlap_

- To recover the original signal, the convolution image can be _multiplied with a top hat_, then _inverse Fourier transformed_ 
- This corresponds to _convolving_ $s(t)$ _with a $\sinc$ function_ to get the original function

- However, if a signal is over a range of frequencies that _does not include $0 \text{Hz}$_, but still has a finite _bandwidth_ $B$, then the convolution images do not overlap as long as $f_s>2B$
- To sample a bit slower, one can _shift the signal down to a lower frequency band_

## Quantisation
- For all values, one should hopefully have a _quantisation level close to the actual value_
- If the signal is _noisy_, there is no point sampling so finely

- If there are $2^N$ quantising bins, it is known as _N-bit sampling_
- If one _oversamples_ with a frequency _factor of $N$ above Nyquist rate_, this allows _averaging_ to improve the _resolution_ by $\sqrt{N}$

- Overall, a sampling of $N$ times the normal rate will _reduce the signal-to-noise ratio_ by $\sqrt{N}$

## Sampling duration
- The Nyquist criterion requires _two samples per cycle_ for the _highest frequency_
- Therefore, _long period variations_ require a _long sampling time_

- The _spectral resolution_ $\Delta f$ is _equals_ $1/T_\text{max}$

# Strategies to eliminate unwanted influences

## Summary
- _Filtering_ to remove _noise_
- _Differential measurement_ to get rid of a _systematic error_
- _Shielding_ for _electromagnetic fields_ or _heat_
- _Eliminate at source_

## Noise
- If the noise and the signal have _non-overlapping spectra_, it is very easy to filter via a _step function_ (or an approximation to one)

- The more complicated case is if the noise is _wide-spectrum_:
![[Physics/Images/Phase sensitive detection.png]]
- This sort of filtering is known as _phase-sensitive detection_
- This requires a filter with _small $\Delta\nu$_, ideally _similar to intrinsic width of the signal_

- Typically in experiments, one can _encode_ a measurement with a _given frequency_, transmit then using a _frequency-specific filter_

- To choose the encoding frequency, one must consider the behaviour of the noise:
	- At _low frequencies_, noise is often _inversely proportional to $f$_
	- At _high frequencies_, noise is often _white_ (not frequency dependent)
		- Examples: [[#Shot noise]], [[#Johnson/Thermal noise]]
- Hence, _DC signals are often heavily affected by noise_

- Example: Noise in LIGO
![[LIGO noise.png]]

## Phase-sensitive detection
![[Phase sensitive detection 1.png]]
- Original: Small _DC voltage_ $V_s$ is transmitted _from transducer to amplifier_, very susceptible to noise
- Let the ampliier have _open-loop gain_ $G$

- Circuit _with phase-sensitive detection_:
- _Modulators multiply their input_ with a _periodic signal_, with angular frequency at $\omega_r$ determined by the _reference oscillator_
- Let the _phase difference_ from 1 to 2 be $\phi$
- The _reference oscillator_ makes the _modulators_ produce _periodic_ signals with frequency $\omega_r$

- The _first modulator_ uses a _sine wave_ to modulate the original signal:
$$V_1=V_sG\sin(\omega_rt+\phi)$$
- The _second modulator_ multiplies $V_1$ with a _square wave_

- After the _cycle average_, the detected signal is:
$$\begin{align}\mean{V_\text{out}}&=\frac{G}{T}\left[\int_0^{\pi/\omega_r}V_s\sin(\omega_rt+\phi)\,dt+\int_{\pi/\omega_r}^{2\pi/\omega_r}-V_s\sin(\omega_rt+\phi)\,dt\right] \\ &=\frac{2V_s}{\pi}G\cos\phi\end{align}$$
- The $\cos\phi$ term is the "phase-sensitivity"
- By _shifting the phase_ by $\pi/2$, one can solve the equations for $V_s$ and $\phi$
	- The shifted signal is the _quadrature component_

- Any noise added _after the first modulator_ will be _randomised_ by the second, and _average to zero_
	- Also works for _constant systematic offsets_
- For this to work, the two modulator waveforms must have _identical frequencies and fixed phase difference_
	- Achieved using reference oscillator

- There may be noise added _before first modulation_ (or, _off-carrier noise_) at a frequency _close to $\omega_r$_, (i.e. $\omega_r+\Delta\omega$)
- The output _oscillates at_ $\Delta\omega$, therefore the _time-average_ must be done _for a longer time_
	- Therefore, the system can be said to have an _effective bandwidth_
- Therefore the _reference oscillator_ must be _phase-stable_ for the considered time-scale

# Probability distributions
- Let there be a _probability distribution_ $P(x)$
- $P(x)dx$ is the _probability that $x$ lies in the range_ from $x$ to $x+dx$
- The function must be _normalised_:
$$\int_{-\infty}^\infty P(x)\,dx=1$$
- Then the _expected value_ of a function $f(x)$ is:
$$\mean{f(x)}=\int_{-\infty}^\infty f(x)P(x)\,dx$$

- In experiments, the probability distribution is deduced from _relative frequencies of events in the limit of a large number of trials_

## The binomial distribution
- Let there be _two possible outcomes_ to a measurement
- Let the probability of a "success" be $p$, then the other probabilit is $1-p$
- Consider $N$ _independent trials_, with $r$ successes and $N-r$ failures

- Since _permutation does not matter_, the probability is:
$$\text{Prob}(r|p, N)=\binom{N}{r}p^r(1-p)^{N-r}=\frac{N!}{r!(N-r)!}p^r(1-p)^{N-r}$$
- This distribution is _automatically normalised_
	- The sum from $r=0$ to $N$ is simply $1^N=1$

- The _expected number of successes_ is:
$$\mean{r}=Np$$
- The _variance_ is:
$$\text{Var}(r)=Np(1-p)$$
	- Always _less than the mean_

- General behaviour of the distribution:
	- _Peak_ around $\mean{r}$
	- As $N$ increases, the peak _narrows with respect to $N$_
	- The peak is _widest_ when $p=0.5$, and the graph is also _symmetrical_
	- Obviously, if $p\neq0.5$, the graph is _skewed_

## The Poisson distribution
- Sometimes, the "failure" case _cannot be detected_
- Instead of the probability of one event, the occurence is characterised by a _mean rate_
	- The mean rate would be the _actual rate measured over a long time_ i.e. $N\to\infty$
- The event is still _random_, just with a _known mean rate_, with each occurence _independent of the last_

- The limit is to have $p\to0$ and $N\to\infty$, but have $\mean{r}=Np$ _stay finite_
- Let there be _$\lambda$ events per unit interval_, where $\lambda=Np$
- Using the limits, the distribution becomes:
$$\text{Prob}(r|\lambda)=\frac{\lambda^r}{r!}e^{-\lambda}$$
- Like the binomial distribution, the distribution is _already normalised_
	- The sum from $r=0$ to $\infty$ is $e^{-\lambda}e^\lambda=1$

- Both the _mean and variance are equal to $\lambda$_
$$\displaylines{\mean{r}=\lambda \\ \text{Var}(r)=\lambda}$$

- General behaviour of the distribution:
	- The Poisson distribution is _broader_ than the binomial distribution
	- There is a _characteristic long upper tail_
	- The number of events observed _can greatly exceed the mean rate_

- Example of event modelled by Poisson distribution:
	- Radiation

### Shot noise
- Another event modelled by the Poisson distribution is _shot noise_, which consists of _discrete charges arriving at random times_

- Since each pulse is short, the _frequency spectrum is approximately flat_ (white)
- If $N$ electrons arrive in random during $\Delta t$, there is a _current fluctuation_ $\sqrt{N}e/\Delta t$
- The _average current_ is $Ne/\Delta t$
- If there is a range of frequencies $\Delta\nu=1/\Delta t$, then:
$$\mean{\Delta I^2}\approx 2I_\text{av}e\Delta\nu$$

## The Gaussian distribution
- The distribution is:
$$\text{Prob}(x|\mu,\sigma)=\frac{1}{\sqrt{2\pi\sigma^2}}\exp\left[-\left(\frac{x-\mu}{2\sigma^2}\right)^2\right]$$
- The shift is _always a bell curve_, with a _shift and scaling_
- $\mu$ is the _mean_
- $\sigma$ is the _standard deviation_

- The Gaussian distribution can be considered _the limit of a Poisson distribution_ with _large $\lambda$_
- Also the _limit of a binomial distribution_ for _large $N$_

>[!The Central Limit Theorem]
>If many independent variables are summed up, their sum tends towards the Gaussian distribution, no matter the distribution of each variable

### Johnson/Thermal noise
- Johnson noise is _electrical noise generated by thermal agitation_
- From the equipartition theorem, for each degree of freedom, there is _average thermal energy_ $kT/2$
- Example: A _capacitive_ circuit with _no power supply_ will produce _small voltage fluctuations_
- When _a limited bandwidth is considered_, the _amplitude distribution is nearly Gaussian_
	- Example, in an $RC$ circuit, the bandwidth is $\Delta\nu=1/\tau=1/RC$, where $\tau$ is the _decay time constant_
	- The power from Johnson noise is given by:
	$$\mean{V^2}/R=4kT\Delta\nu$$

# Inference

- Given some _hypothesis_ of how data behaves, plus the _data points_, one must be able to _infer_ if the hypothesised model is a _good fit_

## The likelihood function
- Let the _observable_ in question be $X$, it is measured $n$ times to yield _data set_ $\{x_i\}$
- Let there be a _theoretical model_, which states for some interval $[x,x+dx]$, the _probability that $X$ is in the range_, given some _parameters_ $\bm{a}$, is given by $p(x|\bm{a})\,dx$

- Then, assuming _all $n$ measurements are independent_, the _probability_ of measuring $\{x_i\}$ within intervals $[x_i+dx_i]$ _given values of parameters_ $\bm{a}$ is:
$$p(x_1|\bm{a})\,dx_1\times p(x_2|\bm{a})\,dx_2 \times\dots p(x_n|\bm{a})\,dx_n=\prod_{i=1}^n p(x_i|\bm{a})\,dx_i$$
- Define the _likelihood function_:
$$L(\bm{x}|\bm{a})=\prod_{i=1}^np(x_i|\bm{a})$$

- If $f$ is a _good model of the data_, the _likelihood_ will end up high
- Hence, to find good values of $\bm{a}$, one needs to _maximise_ $L$

## Bayesian considerations
- Technically, $L(\bm{x}|\bm{a})$ is the likelihood that $\bm{x}$ is the data measured _given fixed values_ of $\bm{a}$
- Usually, one wishes to find the _values of $\bm{a}$ given fixed data points $\bm{x}$_ 

- From Bayes' Theorem, they are related by:
$$\text{Prob}(\bm{a}|\bm{x})=\text{Prob}(\bm{x}|\bm{a})\times\frac{\text{Prob}(\bm{a})}{\text{Prob}(\bm{x})}$$
- $\text{Prob}(\bm{x})$ is simply a normalising factor

- $\text{Prob}(\bm{a})$ is the _prior probability_, while $\text{Prob}(\bm{a}|\bm{x})$ is the _posterior probability_

- Normally, there is an _assumption_ that the _prior is constant over some range of $\bm{a}$_
	- If the _magnitude) of $\bm{a}$ is _completely unknown_, one would use a prior _constant in log space_, or $p(a)\propto 1/a$
- Given this, the two likelihoods are _proportional_, and one would still want to _maximise_ $L(\bm{x}|\bm{a})$

## Flat priors, Gaussian errors
- Let there be _data values_ $\{y_i\}$
- For each value, there is a _corresponding independent variable_ $\{x_i\}$, controlled by the experimenter, assumed to have _no error_
- There is also a corresponding _error_ $\sigma_i$
- There is also a _theoretical value_ $f(x_i|\bm{a})$

- _Assume_ the errors are _Gaussian_
	- Could be an _intrinsic property_ of the system
	- Could be controlled by _many variables_, in which case the [[#The Gaussian distribution|Central Limit Theorem]] states the total error will be Gaussian

- Under these conditions (Flat prior, Gaussian error):
$$p(y_i|\bm{a})=\frac{1}{\sqrt{2\pi\sigma_i^2}}\exp\left(-\frac{[y_i-f(x_i|\bm{a})]^2}{2\sigma_i^2}\right)$$
- In this case, $L$ will be a _product of Gaussians_, so it is easier to _maximise_ $\ln L$:
$$\ln L=-\frac{1}{2}\sum_i\left[\frac{y_i-f(x_i|a)}{\sigma_i}\right]^2-\frac{1}{2}\sum_i\ln(2\pi\sigma_i^2)$$

- Define $\chi^2$, which must be _minimised_ to maximise $L$:
$$\displaylines{\chi^2\equiv\sum_i\left[\frac{y_i-f(x_i|a)}{\sigma_i}\right]^2 \\ \pd{\chi^2}{a_j}=0}$$

- The square means the _sign of deviation_ from theoretical value is _unimportant_
- Also, _comparitively larger_ deviations will contribute a lot to $\chi^2$
- The deviations are _weighted_ inversely to the _expected deviation_

## Straight line fitting
- Often, the theoretical model is of a _straight line_:
$$y_i=\hat{m}x_i+\hat{c}$$
- The hats indicate _best estimates_ for gradient and intercept

### Constant error
- Assume _all errors_ are equal to $\sigma$, then:
$$\displaylines{\chi^2=\frac{1}{\sigma^2}\sum_i\left[y_i-(\hat{m}x_i+\hat{c})\right]^2 \\ \pd{\chi^2}{m}=\pd{\chi^2}{c}=0}$$
- By dividing the derivatives by $N$, the _number of data_, then solving, one obtains:
$$\displaylines{\hat{m}=\frac{\mean{xy}-\mean{x}\mean{y}}{\mean{x^2}-\mean{x}^2}\equiv\frac{\text{CoVar}(x,y)}{\text{Var}(x)} \\ \hat{c}=\frac{\mean{x^2}\mean{y}-\mean{x}\mean{xy}}{\mean{x^2}-\mean{x}^2}\equiv\mean{y}-\hat{m}\mean{x}}$$
- The best fit line is said to go through the _centre of gravity_ of points

- From [[#Combination of random errors|Error propagation]], the errors in these quantities are given by:
$$\displaylines{\sigma_m^2=\sum_i\left(\pd{\hat{m}}{y_i}\right)^2\hat{\sigma}^2 \\ \hat{\sigma}^2=\frac{1}{N-2}\sum_i[y_i-(\hat{m}x_i+\hat{c})]^2}$$
- $\hat{\sigma}^2$ quantifies the _deviation of data from the best-fit model_
- The $N-2$ is the _number of degrees of freedom_ in the model, as there are two parameters

- Using the above expressions:
$$\displaylines{\sigma_m^2=\frac{\hat{\sigma}^2}{N\left(\mean{x^2}-\mean{x}^2\right)} \\ \sigma_c^2=\frac{\hat{\sigma}^2\mean{x^2}}{N\left(\mean{x^2}-\mean{x}^2\right)}}$$

### Varying error
- If the errors $\{\sigma_i\}$ are _not identical_:
$$\chi^2=\sum_i\left[\frac{y_i-\hat{m}x_i-\hat{c}}{\sigma_i}\right]^2$$
- This implies _the same equations as before_, but with _differently weighted means_:
$$\mean{y}=\left(\sum_i\frac{1}{\sigma_i^2}\right)^{-1}\sum_i\frac{y_i}{\sigma_i^2}$$
- This means _data with larger deviation are weighted less_

- All of the formulas above _still apply_, but with modified means
- _Except_, the standard deviation $\hat{\sigma}^2$ is now:
$$\hat{\sigma}^2=\frac{1}{N-2}\left(\sum_i\frac{1}{\sigma_i^2}\right)^{-1} \sum_i\left(\frac{y_i-\hat{m}x_i-\hat{c}}{\sigma_i}\right)^2$$

## Hypothesis testing
- Given the _best estimate_ of the parameters for the hypothesised model, one must check the _match_ between the data and the model

### The chi-squared test
- Like the $\chi^2-$optimisation, this _assumes_:
	- Error is _Gaussian_
	- _Flat prior_
	- _Independent measurements_

- If $f(x_i|\bm{a})$ _exactly models_ the data, the _deviation should approximately match the errors_, hence:
$$\chi^2\approx N_\text{data}$$
- If $\chi^2>>N_\text{data}$, then the model is _likely to be wrong_
- If $\chi^2<<N_\text{data}$, then the _estimates for $\sigma$ may be too large_

- Gievn that $y_i$ has _Gaussian fluctuations_, then it can be proved that $\chi^2$ _fluctuates according to the $\chi^2-$distribution_:
$$p\left(\chi^2|n\right)=\frac{1}{2^{n/2}\Gamma(n/2)}\chi^{n/2}\exp(-\chi^2/2)$$
- Here, $n$ is the _number of degrees of freedom_ in the model, equal to the _number of data points minus the number of parameters_:
$$n=N_\text{data}-N_a$$

- The _probability_ $\alpha$ that the $\chi^2$ observed is _larger than some value_ $\chi_0^2$ is:
$$\alpha\left(\chi_0^2\right)=\int_{\chi_0^2}^\infty p\left(\chi^2|n\right)\,d(\chi^2)$$
- This is known as the _confidence level_
- If the $\chi^2$ observed gives a value of $\alpha$ _above some threshold_, then that theory is _likely to be correct_
\sum_i\frac{1}{\sigma_i^2}\right)^{-1}
### Non-parametric tests
- If the _underlying probability distribution_ is unknown, then one needs _non-parametric statistics_

- One may need tests for:
	- _Randomness_ and _independence_ of the measurements
	- Whether or not two variables _have the same probability distribution_