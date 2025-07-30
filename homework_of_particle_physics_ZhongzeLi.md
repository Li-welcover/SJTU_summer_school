 姓名：李忠泽
## first homework
[[2025-07-08]]
> [!exercise] what is the minimum electron energy ?
> 考虑非相对论极限，电子能量可以表示为：
> $$
E=h\nu=\frac{2\pi \hbar c}{\lambda}$$
> 由图可知德布罗意波长为：$0.2\text{nm}$
> 代入解得：$E\approx{1}\text{keV}$

> [!exercise] Can estimate the range of interaction vs. mass of virtual particle?
>we start from mass-energy equation:$$E\sim mc^{2}$$
> according to uncertainty principle we get$$\Delta t \approx \frac{\hbar}{2\Delta E}=\frac{\hbar}{2mc^{2}}$$
> so $$R\sim c\times\Delta t\sim \frac{\hbar}{2mc}\sim \frac{\hbar}{mc}$$
>luckily we motivate **Yukawa range formula**:
>$$
R\sim\frac{\hbar c}{m}$$
>we can easily calculate :$$R=\frac{200MeV \cdot fm}{140MeV}\approx 1.4\text{fm}$$


> [!exercise] which energy scale correspond to $10^{-18}$ m?
> notice that in natural units we can regard E as m, so according to Yukawa range formula:
> $$M\sim E\sim \hbar \frac{c}{R}$$
> which denote that $E\sim \frac{200\text{MeV}\cdot \text{fm}}{10^{-3}fm}\sim200\text{GeV}$ 
> 
 
## second homework
[[2025-07-09]]
> [!exercise] estimate the temperature needed to create a 100 GeV particles
> *kinetic theory applies to photon gas as well*
> kinetic theory of ideal gas:$$\frac{3}{2}k_{B}T= <KE>\text{of}\,\text{molecule}$$
> so $T=\frac{2}{3k_{B}}E\sim\frac{100 \times 10^9 \, \text{eV}}{8.617 \times 10^{-5} \, \text{eV/K}} \approx 1.16 \times 10^{15} \, \text{K}$

> [!exercise] estimate at which temperature would proton stop turning into neutron
> $$n\to p+e+\bar{\nu}_{e}$$
$$\bar{\nu}_{e}+p\to n+e^{+}$$
$M_{n}=939.57$MeV, $M_{p}=938.28$MeV
> we should consider mass difference as energy change:$$
\Delta m = M_n - M_p = 939.57 - 938.28 = 1.29 \, \text{MeV}$$
> So when $k_B T \lesssim \Delta m$, there’s **not enough thermal energy** to produce neutrons from protons.
> at this time $$T_{\text{freeze}} \sim \frac{\Delta m}{k_B} = \frac{1.29 \, \text{MeV}}{k_B}\sim 10^{10}\text{K}$$


> [!exercise] Can deuteron make beta decay? And why?
> No
> The reason is that the mass of deuteron is less than the sum of its parts after beta decay. First we know that a deuteron is made of n+p, and it's 2.2MeV lighter than total mass of n&p.
> Beta decay makes n into p+e+$\nu$, and the mass difference is the anti number of last question: $\Delta m=-1.29$MeV, so even the sum of the left parts' mass reduce, it's still heavier than deuteron.
> In other word, at least although there many deuterons in our drinking water, but we are save from the radiation.

> [!exercise] If neutrino mass is 1 eV, estimate the relic neutrino's speed
> from the materials saying that the neutrinos are also cold, about 2K, so we can assume that $T_{\nu}=2$K
> to estimate speed we should know the momentum because: $v\sim \frac{p}{m}$
> The average momentum is approximately$$\langle p_\nu \rangle \approx 3.15 \, k_B T \approx 3.15 \times 8.617 \times 10^{-5} \times 2 \approx 5.43 \times 10^{-4} \, \text{eV}$$
> so $v\sim \frac{5.43\times10^{-4}\text{eV}}{1\text{eV}}\sim5.43\times 10^{-4}c$

> [!exercise] estimate the number of electron neutrino per second created from the sun
> $M_{\odot}=2\times 10^{30}\text{kg}$, energy is released via proton-proton fuse into He4 in the core, about 10% of the mass. the sun will burn for 10 billion years.
> the nuclear equation is:
> $$
p+p+p+p\implies He4=\alpha+e^{+}+e^{+}+\nu_{e}+\nu_{e}$$
> Mass of the fusion is $M=2\times 10^{29}\text{kg}$, mass of protons per reaction is $4m_p \approx 4 \times 1.67 \times 10^{-27} \, \text{kg} = 6.68 \times 10^{-27} \, \text{kg}$, so the number of the reactions is $$
N = \frac{M}{6.68 \times 10^{-27}} \approx \frac{2 \times 10^{29}}{6.68 \times 10^{-27}} \approx 3 \times 10^{55}$$
> according to the nuclear equation, each reaction gives 2 neutrinos, so its number is:$$
N_{\nu}=2N=6 \times 10^{55}$$
> We also know the burn time:$$t = 10^{10} \, \text{years} = 3.15 \times 10^{17} \, \text{s}$$
> so we get the rate of the neutrinos' radiation:
> $$
\frac{dN_{\nu}}{dt} = \frac{6 \times 10^{55}}{3.15 \times 10^{17}} \approx 1.9 \times 10^{38} \, \nu/\text{s}$$
 
## third homework
[[2025-07-11]]
[[particle detection]]
> [!exercise] design an optical far detector distance
> use the neutrinos oscillation to calculate the phase difference, according to the diagram, we know that $\sin ^{2}\left( \frac{1.27\Delta m^{2}L}{E} \right)=1$, using $\Delta m$ and $E_{\nu}$ we can get final solution
> $$\frac{1.27\Delta m^{2}L}{E}=\frac{\pi}{2}\implies L= \frac{\pi E}{2\times1.27 \Delta m^{2}}=$$

> [!exercise] Estimate the neutrino energy when the coherent nucleus interaction becomes important?
> If coherent scatter occurs, the scale of neutrino's wavelength should be large enough to match the scale of nuclears, which shows the infimum of $E_{\nu}$. While if the nuclear recoil could be detected, the impact energy should be large enough to satisify the condition.
> so we can estimate the range of the neutrinos.
> Infimum of energy can be calculated by Yukawa formula we mentioned before:
> $$E_\nu \lesssim \frac{\hbar c}{R} = \frac{\hbar c}{R_0 A^{1/3}} \approx \frac{164}{A^{1/3}} \, \text{MeV}$$
> Supremum of energy can be calculated by the empirical formula:
> $$\bar{E}A = \frac{2}{3A} \left( \frac{E\nu}{1 \, \text{MeV}} \right)^2 \, \text{keV}$$
> the resolution of detectors nowadays is about 1keV, so:
> $$\bar{E}_{A} = \frac{2}{3A} \left( \frac{E\nu}{1 \, \text{MeV}} \right)^2 \, \text{keV}\gtrsim 1 \, \text{keV}$$
> $$E_\nu \geq \sqrt{ \frac{3A}{2} } \, \text{MeV} $$

## fourth homework
 > [!exercise] compute the flux of 100 GeV DM
 > according to flux formula:
 > $$J = \left( \frac{\rho_{\text{DM}}}{M_x} \right) \cdot v$$
 > we plug in: 
 > $$J = \frac{0.3 \, \text{GeV}/\text{cm}^3}{100 \, \text{GeV}} \cdot 2.2 \times 10^7 \, \text{cm/s} = \left( 3 \times 10^{-3} \, \text{cm}^{-3} \right) \cdot 2.2 \times 10^7 \, \text{cm/s}$$
 > so
 >$$J \approx 6.6 \times 10^4 \, \text{particles} / \text{cm}^2 / \text{s}$$

 
 