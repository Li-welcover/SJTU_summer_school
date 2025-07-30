The quantum Hall effect inspires researches. What is KUDI electron gas in other two directions?
When the outer magnet field is near to zero, the relationship between $\rho_{xx}$ and B is linear by the Lorentz force, but when B is larger than about 2Tesla, the phenomenon becomes quantumized. 
How can these precises be so high? —— **Topological phases of the electron**!

---
the electron states are different plat holes which can be described by topological phases.
the Hofstadter butterfly is 2D bloch band in a magnetic field. the band is splid into q sub-bands, if the magnetic flux per unit cell is a fraction of $\frac{h}{e}$(flux quantum). the y axis is energy, and the x axis is magnetic flux.
the band is described by Kubo formula for the Hall conductance.
### Adiabatic quantum pump
one dimentional question
### quantum hall conductance as a topological invariant
instead of Landau energy belt theory. almost all the time we don't care phase except time-dependent occations. The additional phase produced by geometric is Berry phase: 
$$
\gamma_{n}=\oint_{C}d\lambda \bra{\psi_{n}}i \frac{\partial}{\partial \lambda}\ket{\psi_{n}}  
$$
according to Stokes integrate theorem:
$$
\gamma_{n}= \iint d \lambda_{1}d \lambda_{2}\Omega
$$
which derives Berry curvature $\Omega$
in analogies with classical electric dynamics, 
- Berry curvature $\Omega(\vec{r})$ - magnetic field $B(\vec{r})$
- Berry connection $\bra{\psi_{n}}i \frac{\partial}{\partial \lambda}\ket{\psi_{n}}$ - vector potential $A(\vec{r})$
- Geometric phase - Aharonov-Bohm phase
- Chern number $\oint d^{2}\lambda \Omega(\vec{\lambda})=integer$ - Monopole $\oint d^{2}rB(\vec{r})=\Phi=integer\, \frac{h}{e}$

---
the time-depent eigen eq:
$$
\hat{H}(t)\psi_{n}(t)=E_{n}(t)\psi(t)
$$

the solution can be written as series of eigen vectors:$$
\psi(t)=\sum c_{n}\psi_{n}\implies \sum c_{n}(t)\psi_{n}(t)
$$
take them back to Schrodinger eq:$i\partial_{t}\psi=H\psi$
$$
\int i\sum_{n}\partial_{t}c_{n}(t)\cdot \psi_{n}(t)+c_{n}(t)\partial_{t}\psi_{n}(t)=\hat{H}\psi=\sum_{n}E_{n}\psi_{n}
$$
with left times with $\psi^\star$, we can finally get $c_{n}\sim e^{i\phi_{B}}e^{i\phi_{d}}$

### Dirac Model 1
for a spin 1/2 system, the Hamilton can be written as:
$$
H=vk_{X}\sigma_{X}+vk_{Y}\sigma_{Y}+vk_{Z}\sigma_{Z}
$$
eigen eq:
$$
E=\pm v|k|
$$
so put eigen vector into it, we can solve the matrix eq to get two eigen vectors $\psi_{\pm}$

### Dirac Model 2
in sopherical coordination:
$$
\psi_{+}^{(1)}=\begin{pmatrix}
\cos \frac{\theta}{2}e^{-i\varphi} \\
\sin \frac{\theta}{2} 
\end{pmatrix}
$$
$k_{x}=k\sin \theta \cos \varphi\,\dots$
fix $\theta=\theta_{0}$(for simple, we can set $\theta=0$), the Berry phase will become:
$$
\Phi_{B}=\int dk\bra{\psi}i\partial_{k}\ket{\psi}
$$
$$\Phi^{(1)}=2\pi \cos ^{2} \frac{\theta}{2},\,\Phi^{(2)}=-2\pi \sin ^{2} \frac{\theta}{2}$$

### Dirac Model 3
for example, we set $A=\bra{\psi}i\partial_{k}\ket{\psi}$ as the Berry connection.
if we set: $\ket{\psi}\to e^{i\varphi}\ket{\psi}$, then $A\to A-\partial \varphi$(the Berry connection changes), and $\Phi_{B}\to \Phi_{B}+\Delta \Phi=\Phi_{B}+2n\pi$
However, the Berry curvature doesn't change: 
$$
\Omega\equiv \nabla \times A
$$
---
### Hofstadter Butterfly
any number can be splitted: Spectral splitting:
$$
\phi=\frac{1}{f_{1}+\frac{1}{f_{2}+\frac{1}{\dots}}}
$$
---
what is condensed matter physics?
the definitions can be: structure and transport, by the old PRL division
the aims are: To develop useful models for experimental systems, to reveal mechanisms for observed phenomena, to develop accurate methods to predict properties