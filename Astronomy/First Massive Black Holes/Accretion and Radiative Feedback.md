## Growing BHs by Accretion: Is There an Eddington Limit?
**Theoretical possibilities of super/hyper-Eddington accretion**

Suppose a BH forms at the beginning of the universe and accretes at the Eddington limit accretion rate. The timescale for growth to $M_\bullet$ can be estimated by
$$
\dot M_{\bullet} = (1-\epsilon)f_\text{duty} \dot M_\text{Edd} = (1-\epsilon)f_\text{duty}\frac{L_\text{Edd}}{\epsilon c^2} = (1-\epsilon)f_\text{duty}\frac{4\pi cG}{\epsilon \kappa_\text{es}}M_\bullet
$$
Solving the equation, with initial condition $t=0, M_\bullet = M_\text{seed}$

$$
t_\text{grow} = \frac{\kappa_\text{es}}{4\pi cG}\frac{\epsilon}{(1-\epsilon)f_\text{duty}}\ln\left(\frac{M}{M_\text{seed}}\right) \approx 0.81 Gyr \rightarrow z \sim 6
$$
Adopting the fiducial values  $\epsilon = 0.1, f_\text{duty}=1, M_\text{seed}=100M_\odot, M_\bullet = 10^9 M_\odot$.

*The question with accretion comes in 2 ways. How matter gets into the event horizon, and how matter gets into the accretion disk.*

It's like for a race car in a long distance competition, it needs to burn it's fuel efficiently in the engine as well as to have continuous fuel supply at the tank. BHs are in a comic age long race like this.


### Photon trapping on small scales near the BH
$$
R_\text{tr} = \frac{\kappa_\text{es}}{4\pi c}\dot M_\bullet
$$
Photon trapped in optically-thick ([[Radiation]]) accreting matter could limit the luminosity at the same accretion rate, at the same time making it possible to accrete super fast under the same luminosity. In fact the luminosity could be fixed around $L_\text{Edd}$, **independent of the accretion rate.** This way the efficiency by which energy of accreted matter transfer into radiation could be as low as 1% (in some cases). Not only accretion rate is higher, but also the proportion of matter finally adds up to black hole rest mass $M_\bullet$ is larger.

![[Pasted image 20220516121059.png]]

> Is it true that the higher the accretion rate, the lower the efficiency, the more mass (in percentage) gets to add to the rest mass of the BH?

Discussion
- Rotating BHs have produce radiation more efficiently at lower accretion rates.
- A large amount of radiation emerges with $1 \lesssim L/L_\odot \lesssim 20$ toward the polar conical regions

> Could we have black hole pulsars in this case? And if so could we be able to verify this model by comparing the peak and valley luminosity?

- Highest accretion rates $\dot m \approx 5\times 10^3$: fast rotation + strong magnetic field -> so-called **magnetically arrested disk (MAD)** state, where luminosity rockets high $\sim 100 L_\text{Edd}$ and radiative efficiency remains $\epsilon < 1\%$ . 

Limitations and problems
- Instability of the flow under non-spherical symmetric scenario
- Efficiency of photon trapping is significantly reduced due to non-inflowing gas motion caused by **radiation pressure** and **magnetic buoyancy**, which is not considered in the analytical models. (red and orange lines from above)
- For long time and large scale (which the simulations did not cover) outside a small steady accretion disk with radius $R_\text{disk} \sim 20-100 R_\text{Sch}$ , "the mass-loss rate dominates significantly  over the BH feeding rate"
- *Valid only if a sufficient amount of gas supply is avaliable $\dot M \gg \dot M_\text{Edd}$ and not impeded by the strong radiation feedback.*

### Inflow from large scales
1. Baryons accrete into a DM halo along cold filamentary streams connected with the large-scale cosmic web (such large-scale inflows are expected to be triggered by major mergers of 2 galaxies.)
	$$
	\dot M \approx f_\text{b}\frac{V_\text{circ}^3}{G} \approx 0.3 M_\odot yr^{-1}\left(\frac{V_\text{circ}}{20\text{km\,s}^{-1}}\right)^3
	$$
2. Rapidly accreted pristine gas settles into a compact circum-nuclear disk and breaks up into smaller clumps because of gravitation instability.
	$$
	\dot M \approx \frac{M_\text{J}}{t_\text{ff}}\approx \frac{c_\text{s}^3}{G} \approx 4\times 10^{-3}M_\odot yr^{-1}T_3^{3/2}
	$$
3. Finally on smaller scale, gas is captured by BH and begins to accrete from Bondi radius. **Bondi radius is the radius where escaping velocity equals the sound speed.** It represents the boundary between subsonic and supersonic infall.

	Bondi rate
	$$
	\dot M_B = \pi e^{3/2}\rho \frac{G^2M_\bullet^2}{c_\text{s}^3} \approx 4.5\times 10^{-3} M_\odot yr^{-1} n_{H,6} T^{-3/2}_3\left(\frac{M_\bullet}{100 M_\odot}\right)^2
	$$
	- Bondi rate as an upper limit of BH accretion rate

### Photoionization and heating
Photoionization and heating at Bondi radius where matter is only marginally bound by the central BH can suppress gas inflow from large scales.

> What is the main difference between high z quasars and their low z counterparts, such as AGNs?

### Mechanical Feedback
BHs accreting at super-Eddington rates can exert negative feedback via winds and jets.

## Stellar-mass Black Hole Remnants of the First Stars
Because of
1. radiation and mechanical feedback blows the gas out of minihalos because their
potential is not deep enough.
2. Supernova explosions
3. Gravitational wave recoil kicks from mergers

Pop III remnant BHs likely has to wait until they end up in a more massive DM halos with potential deep enough to bind a sufficient amount of gas and recoiled BHs.

## Rapid Growth of Seed BHs in High-Redshift Protogalaxies
This section talks about how super/hyper Eddington accretion could actually happened and what role might they have played.

The natural place where such rapid BH growth may occur is in the atomic cooling halos (ACHs).

ACH: DM halos whose virial temperature is just above the atomic-cooling threshold ($T_{vir} \approx 8000K$). More common at lower z but are more likely to be polluted by metals. A sweet spot for metal-free/metal-poor ACHs is at $z=12-15$. This redshift is still sufficiently high to allow subsequent growth to $10^9 M_\odot$ at $z\sim 6-7$ at "the more leisurely Eddington rate".
