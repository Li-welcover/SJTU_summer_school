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
actually, M-R relation is a curve that the radius firstly(when m is low) prompts to $M^{1/3}$, and then turn to $R \propto M^{-1/3}$ when M is high

slowly adding mass to a WD, what happens when its mass exceeds the Chandrasekhar Limit?
#### Neutron star
when M exceed the Ch limit, the electroforce won't be against the gravity, so the neuclears will touch each other
first question is that why neutron exist, why not $n\to p+e+\nu$?
when put many particles in small volume, electron will keep impacting(according to uncertain principle, electrons keep moving) proton and they will combine to neutron

