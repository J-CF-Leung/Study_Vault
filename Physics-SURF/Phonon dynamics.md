- Hamiltonian of the system:
$$\displaylines{H=H_{e}+H_{p}+H_{e-p}+H_{p-p} \\ H_{e}=\sum_{k,n}\epsilon_{kn}c_{kn}^{\dagger}c_{kn} \\ H_{p}=\sum_{q,\eta}\hbar\omega_{q\eta}b_{q\eta}^{\dagger}b_{q\eta} \\ H_{e-p}=\sum_{k,q,\eta,n}M_{\eta}(q)c_{k+q,n}^{\dagger}c_{k,n}(b_{q\eta}+b_{-q\eta}^{\dagger})\\ H_{p-p}=\sum_{q,q',q''}\sum_{\eta,\eta',\eta''}(b_{q\eta}+b_{-q\eta}^{\dagger})(b_{q'\eta'}+b_{-q'\eta'}^{\dagger})(b_{q''\eta''}+b_{-q''\eta''}^{\dagger})}$$

- (Anti-)commutation relations:
$$\displaylines{\{c_{i},c_{j}^{\dagger}\}=\delta_{ij}\hspace{1cm}\{c_{i},c_{j}\}=\{c_{i}^{\dagger},c_{j}^{\dagger}\}=0 \\ [b_{i},b_{j}^{\dagger}]=\delta_{ij}\hspace{1cm}[b_{i},b_{j}]=[b_{i}^{\dagger},b_{j}^{\dagger}]=0}$$

- Heisenberg picture:
$$\frac{dA}{dt}=\frac{i}{\hbar}[H,A]$$
- One-phonon density matrix:
$$\rho=\pmatrix{\langle b_{q+k,\eta_{2}}^{\dagger}b_{q+k,\eta_{2}} \rangle & \langle b_{q+k,\eta_{2}}^{\dagger}b_{q,\eta_{1}} \rangle \\ \langle b_{q,\eta_{1}}^{\dagger}b_{q+k,\eta_{2}} \rangle & \langle b_{q,\eta_{1}}^{\dagger}b_{q,\eta_{1}} \rangle  }$$
- Define the _phonon-assisted polarisation operator_:
$$s^{q,\eta}_{q+k,k}=\langle b_{q,\eta}c_{q+k}^{\dagger}c_{k} \rangle $$

- Dynamics of the density matrix elements:
$$\displaylines{\begin{align}
\frac{d}{dt}(\langle b_{q+k,\eta_{2}}^{\dagger}b_{q,\eta_{1}} \rangle )&=\frac{i}{\hbar}\sum_{k',n'}[M_{\eta_{2}}(q+k)s^{q,\eta_{1}}_{k'+q+k,k'}-M_{\eta_{1}}(-q)(s^{q+k,\eta_{2}}_{k',k'-q})^{*}] \\ &-i(\omega_{q,\eta_{1}}-\omega_{q+k,\eta_{2}})\langle b_{q+k,\eta_{2}}^{\dagger}b_{q,\eta_{1}} \rangle 
\end{align} \\ \frac{d}{dt}(\langle b_{q\eta_{1}}^{\dagger}b_{q\eta_{1}} \rangle ) =\frac{i}{\hbar }\sum_{k'n'}[M_{\eta_{1}}(q)s^{q,\eta_{1}}_{k'+q,k'}-M_{\eta_{1}}(-q)(s_{k',k'-q}^{q,\eta_{1}})^{*}]}$$
