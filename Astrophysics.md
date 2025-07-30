## goals
- compact objects including white dwarfs neutron stars and BHs
- Exoplanets

Luminosity formula :
$$
L=4\pi R^{2}\sigma T_{s}^{4}
$$
where $T_{s}$ is temperature, sun's is 5800K
> [!exercise] Why MS mass range is 0.8~100 sun mass?
> you can find it directly from the HR diagram

HR=Hertzsprung-Russel, which means the diagram is describing star's scale and temperature
MS stars means Main Sequence stars, their $T_c=const.\approx 2\times 10^{7}$K

image that the mass is M and the radio is R, estimate the pressure in the center of star:
$$
\frac{dP}{dr}=-\rho g=-\frac{\rho Gm(r)}{r^{2}}\tag{1}
$$
integrate, we get: Pc~$\frac{GM^{2}}{R^{4}}$
according to black-body theory, if $$P_{c}=\frac{1}{3}aT_{c}^{4}$$, we can denote that $R\propto \sqrt{ M }$, which satisifies supermassive stars(usually more than 50 sun mass)

### mass scale for MS stars
we should calculate a star against gravity, so we should compute total pressure:
$$
P_{c}=P_{gas}+P_{rad}
$$
for ideal gas:
$$
P_{gas}=\frac{\rho_{c}kT_{c}}{\mu m_{p}}:=\beta_{c}P_{c}
$$
where $\beta$ describes how much ideal gas are there, for example, **lower mass star have more ideal gas**
$$
P_{rad}=\frac{1}{3}aT_{c}^{4}
$$
after Pc is known, use (1) can we denote M
 $$
M=10 \frac{(1-\beta)^{1/2}}{} ()(M_{\star})
$$

### stellar evolution
$H\to He$ is MS stage, while the whole procession is from H to Fe
two stage:
- core: neuclear burning, but change fuel after contraction
- Envelope: expansion or ejection

three types of remnants；
- white dwarf
- neutron star
- BH $R=\frac{2GM}{c^{2}}=3\text{km}\left( \frac{M}{M_{\odot}} \right)$
the escape velocity of BH: $\frac{v}{c}= \frac{2GM}{Rc^{2}}^{1/2}$

#### white dwarf
an example is Sirius B, whose T=6000K, $L<\approx 0.003L_{\odot}$
to understand such star we need QM
To support against gravity we need enough pressure:
$$
P-\frac{GM}{R}\rho_{c}\implies \langle v^{2} \rangle-\frac{GM}{R}\implies \epsilon- \frac{GMm_{p}}{R} 
$$
where $\epsilon$ is averaged particle kinetic energy inside the star, and the *numerical density* is
$$
n_{e}=\frac{Z\rho}{Am_{p}}\sim \frac{\#}{\text{cm}^{3}}
$$
so, $\Delta x\sim \frac{1}{n_{e}^{3}}$
from $\Delta p=\frac{h}{\Delta x},E=\frac{p^{2}}{2m}$ we can easily get
$$
R\sim \frac{h^{2}}{Gm_{e}m_{p}^{5/3}}M^{-1/3}
$$
which implicates that when M up, R down, then velocity of particles:
$$
v_{zp}=\frac{p_{zp}}{m_{e}}\sim \frac{hn_{e}^{-1/3}}{m_{e}}\leq c
$$
which leads M to Ch limit(钱德赛拉卡极限)

**$M_{ch}$ is High-M limit, but what's the low-M limit?**
actually, M-R relation is a curve that the radius firstly(when m is low) prompts to $M^{1/3}$, and then turn to $R \propto M^{-1/3}$ when M is high, just like an inverse parabola

slowly adding mass to a WD, what happens when its mass exceeds the Chandrasekhar Limit?
#### Neutron star
when M exceed the Ch limit, the electroforce won't be against the gravity, so the neuclears will touch each other
first question is that why neutron exist, why not $n\to p+e+\nu$?
Slowly adding mass to a white dwarf, what happens when the mass exceeds Ch limit?
when put many particles in small volume, electron will keep impacting(according to uncertain principle, electrons keep moving) proton and they will combine to neutron
[[2025-07-14]]

Neutron stare maximum mass( regardless of stiff EOS)
Force balance in star is Pressure balances gravity, should be modified by GR that is different from Newtonian form.The pressure balances gravity will be described by **TOV Equation**:
$$
\frac{dP}{dr}=-\frac{Gm\rho}{r^{2}}\left[  \frac{\left( 1+\frac{P}{\rho c^{2}} \right)\left( 1+\frac{4\pi r^{2}P}{mc^{2}} \right)}{1-\frac{2Gm}{rc^{2}}} \right]
$$
and the Maximum mass is **TOV limit**

#### Black Hole
What happens when Neutron star's mass exceeds the TOV mass?
Radium of BH is: $$
R=\frac{2GM}{c^{2}}\sim 3\text{km}=3\text{km}\left( \frac{M}{1M_{\odot}} \right)
$$
the escape velocity eq is:$$
v=\sqrt{ \frac{2GM}{R}}
$$so when $v=c$, we calculate the radium of the dark star.
However, although the answer is correct, but the derivation of Newtown, the particle description of light, is wrong.

---
the first exact solution to Einstein equation describing non-rotating BH is Schwarzchild solution: The horizon radius is:$$
R_{s}=\frac{2GM}{c^{2}}
$$
and Kerr find the solution of spinning BHs.

---
### Two key ideas of GR
1. Geometric Interpretation of gravity
Newton's is mass produces a force field:$$
\nabla^{2}\Phi(r)=4\pi G\rho(r)
$$
GR: gravity is not a force but warpage of spacetime mass-energy distorts spacetime around it:$$
G_{\mu \nu}=8\pi T_{\mu \nu}
$$
2. How does a mass respond to gravity?
Newton's 2nd law:$$
\vec{F}=m\vec{a}
$$
GR: a test mass mobes along geodesics which is modified by spacetime warpage(curvature)
So it's demand for us to find an interpretation or description of gravity
#### Metric
in SR we know that interval between two nearby events is:$$
ds^{2}=(cdt)^{2}-dx^{2}-dy^{2}-dz^{2}
$$
which is Lorentz invariant that is an intrinsic property of spacetime.
So we can define **spacetime metric**:$$
ds^{2}=g_{\mu \nu}dx^{\mu}dx^{\nu}
$$
for example, the simplest st is flat st described by Minkowski metric:
$$
ds^{2}=ds^{2}=(cdt)^{2}-dx^{2}-dy^{2}-dz^{2}
$$
another example is Schwarzschild metric describing space around a big mass M:
$$
ds^{2}=\left( 1-\frac{R_{s}}{r} \right)c^{2}dt^{2}- \frac{dr^{2}}{1-\frac{R_{s}}{r}}-r^{2}(d\theta^{2}+\sin ^{2}\theta d\varphi^{2})
$$
while $R_{s}=\frac{2GM}{c^{2}}$ is Sch radius.
Now we research the property of Sch metric.

#### property of Sch BH
1. when $r\gg R_{s}$, (far away from the BH), $ds^{2}\implies$flat. At the same time, $$
d\tau_{\infty}=\frac{ds}{c}_{d\vec{r}=0}=dt
$$
while sitting at r=infinite, proper time will be:
$$
d\tau(r)=dt\left( 1-\frac{R_{s}}{r} \right)^{1/2}
$$
we call that **Gravitational time dilution**, it will cause effect if a stationary atom at r emits with $\nu_{em}$, the observed frequency at infinity is
$$
\nu_{\infty}=\nu_{em}\left( 1-\frac{R_{s}}{r} \right)^{1/2}
$$the effect is called **Gravitational redshift**
when $r=R_{s}\implies \nu_{\infty}=0$, we call the radius is **Horizon radius**.
2. r=0 is a singularity, enclosed by the horizon.

> [!exercise] Calculate Kepler problem in GR——the motion of test mass around a Sch-BH
> suppose the test particle's proper time is $\tau$, the path of the particle is: $(t(\tau),r(\tau),\theta(\tau),\varphi(\tau))$, for simple we can set $\theta=\frac{\pi}{2}$.
> for $\tau_{1}\to \tau_{2}$, the spacetime interval (the action) is
> $$\begin{equation}\begin{aligned} S_{12}&=\int \sqrt{ ds^{2} }d\tau\\&=\int \mathscr{L}(x^{\alpha},\dot{x}^{\alpha})d\tau
\end{aligned}\end{equation}$$
> using the smallest action principle the particle's trajectory is determined by:$\delta S_{12}$
> to simplify Eular-Lagrange Eq, we get geodesic Eq. 

 Eliminate t&phi, we have:
 $$
\frac{1}{2}\dot{r}^{2}+\frac{1}{2}\left( 1-\frac{2M}{r} \right)\left( 1+\frac{l^{2}}{r^{2}} \right)=\frac{1}{2}\epsilon^{2}$$
the second item is Effective Potential:
$$
V_{eff}=\frac{1}{2}\left( 1-\frac{2M}{r} \right)\left( 1+\frac{l^{2}}{r^{2}} \right)=\frac{1}{2}-\frac{M}{r}+\frac{l^{2}}{2r^{2}}-\frac{Ml^{2}}{r^{2}}
$$
to find a single $l$ that makes $V_{eff}$ minimum:$$
\frac{{\partial V_{eff}}}{\partial r}=0\implies r_{0}(l)
$$
$$
l_{crit}=\sqrt{ 12 }M,\,r_{0,crit}=6M
$$is ISCO condition: Inner-most stable circular orbit
Energy of particle (unit mass) in circular orbit:$$
E_{cir}(r=r_{0})=\frac{r-2M}{\sqrt{ r(r-3M) }}
$$
when the particle is far enough from the BH, r is much much larger than 2M, doing Taylor expansion we get the first item is 1, which is $mc^{2}$ indeed.
$$
E=1-\frac{M}{2r}=mc^{2}-\frac{GMm}{2r}
$$shapes same as Newtonian form.
$$
E_{cir}(r_{ISCO})=\sqrt{ \frac{8}{9} }c^{2},\,E(\infty)-E_{cir}(r_{ISCO})=c^{2}-\sqrt{ \frac{8}{9} }c^{2}=5.72\% ^58f6e7
$$
---
shock wave cause rebounding shock, if the shock is energetic enough and succeeds spreading in the star, it  leads to core-collapse supernova explosion.Then the protoneutron star comes into being.
the proto-NS is hot, the energy comes out as neutrinos over ~10s. Some neutrinos are absorbed by fluid behind the shock, shock can be revived. If the explosion succeeds, NS forms; If explosion fails or significant mass fallback, BH forms.

[[2025-07-15]]
Latest News from LIGO 2025.7.14: a gravitational-wave signal from the most massive binary black hole observed to date
not just the objects themselves, but also the interaction we curios to.
 
### white dwarf in binaries (pairs)
there're two kinds of binaries: WD+non-degenerate stars; WD+WD
A challenge problem is that *what will happen when the two stars meet each other?*
the answer is may lead to different outcomes(depending on mass and composition)
- AIC (accretion-induced collapse to neutron star)
- Thermonuclear supernova = SN Ia
SN Ia is thermonuclear runaway explosion of C/O white dwarf
so what is supernovae?

How do we know the distance?
By the observation of the flux:$$
f_{obs}=\frac{L}{4\pi D^{2}}
$$
where D is the distance. L is luminous that we can calculate from the Temperature and travel time $\Delta t$.

Isolated Neutron Stars including Radio Pulsars and Magnetic stars

#### Radio Pulsars 
Rotating magnetic Neutron Stars, what happens undergo its rotation?
拉莫尔进动: $$
\frac{d}{dt}\left( \frac{1}{2}I\Omega^{2} \right)=-\frac{2}{3c^{3}} |\frac{d^{2}\mu}{dt^{2}}|^{2}=-\frac{2(\mu \sin \alpha)}{3c^{3}}\Omega^{4}
$$
by measuring $P,\,\dot{P}\implies B_{\text{dipole}}$, radiation at all wavelenths.
#### Magnetars
Neutron stars powered by superstrong magnetic fields(B>$10^{14}$G=$10^{10}$T)
the star quake can product magnetic field dissipation, but where such strong magnetic field comes from?
it's because electricurve. We know earth is charge neutron. 
before core collapse, the star is big enough to allow the magnetic curve distribute deseperately. but after what it will be much tighter than before, so the strength of the magnetic field become much larger.
the other reason is that Dynamo (field generation) in proto-neutron star

photon's energy-momentum release:$E=p$, but the momentum consevation was broken in the strong magnetic field because some of which was absorbed by the field.
#### Exotic QED processes in superstrong B fields
One photon pair production:$\gamma\to e^{+}+e^{-}$
photon splitting: $\gamma\to \gamma+\gamma$
Vacuum polarization in strong B (propegate in B field)
another conclusion is: At least some of FRBs are created by Magnetars!

Isolated BHs are boring because they cannot be observed. but recently we know that BHs can radio.
instead, there is a kind of BHs named Accreting Black Holes.
Stellar-mass BHs in binaries is a good example. is X-ray Ninaries which can be detected.
Accreting gas has angular momentum that product Accreting disk(吸积盘).

the accretion power of BH can be calculated.
- Penrose Process: Extracting spin energy from BH.
- Blandford-Znajek Process: Interaction of BH with magnetized plasma

---
TDE
### GW
$$
g_{\mu \nu}=\eta_{\mu \nu}+h_{\mu \nu}
$$
GW propagating along z-axis:
$$
ds^{2}=-dt^{2}+(1+h_{+})dx^{2}+(1-h_{-})dy^{2}+2h_{\times}dxdy+dz^{2}
$$
the two masses' reaction to GW is $h_{+}L=\Delta L$ on x,y-axis. always h is very small $h<~10^{-21}$ so:
$$
\Delta L=hL\leq h\times 4\text{km}
$$
#### GW's Generation
in Electromagnetism, dipole's momentum:$$
P=\frac{2}{3c^{3}}|\ddot{\vec{d}}|^{2},\,\vec{d}=\int \rho(\vec{r})\vec{r}\,\text{d}^{3}x
$$
quadrupole's momentum:$$
P_{Q}\sim \frac{|\dddot{Q}|^{2}}{c^{5}}
$$
but in Gracitational radiation,
$$
\int \rho \vec{r}d^{3}x=M_{tot}\vec{R}\implies \dot{\vec{d}}=M_{tot}\vec{V}\implies \vec{P}_{tot}
$$
the total momentum is conserved, so the double class of derivative of mass dipole is 0. **There's no dipole gravitation radiation.**

For a binary$(m_{1},m_{2})$ in a circular orbit (a):
$$
P_{Q}=\frac{32}{5} \frac{G(\mu a^{3}\Omega^{3})}{c^{5}}\sim \frac{G(\mu a^{3}\Omega^{3})}{c^{5}},\,\mu=\frac{m_{1}m_{2}}{m_{1}+m_{2}},\,\Omega=\sqrt{ \frac{G(m_{1}+m_{2})}{a^{3}} }
$$

#### GW from Binary Inspiral
$$
h\sim \frac{G}{c^{4}D}\ddot{Q}\sim \frac{G}{c^{4}D}\mu a^{2}\Omega^{2}
$$
frequency:
$$
f=\frac{2\Omega}{2\pi}
$$
as the two stars becoming nearer, the frequency and amplitude will be higher.
the rate is:
$$
\frac{\dot{f}}{f}=\frac{96}{5}M_{c}^{5/3}(\pi f)^{8/3},\,M_{c}\equiv \mu^{3/5}(m_{1}+{m_{2}}^{2/5})
$$
where $M_{C}$ is Chirp mass.

the frequency is$$
\Omega=\sqrt{ \frac{GM}{a^{3}} }
$$by the third law of Kepler.
the Schwartzchild radium of BH: $r_{\text{sch}}=\frac{2GM}{c^{2}}$
so we can estimate that:$$
\Omega\sim \sqrt{ \frac{GM}{\left( \frac{2GM}{c^{2}} \right)^{3}} }\propto \frac{1}{M}
$$70=