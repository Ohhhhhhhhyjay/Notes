## The Differential Equation of Hydrostatic Equilibrium
From static equilibrium of a small volume, the difference of the pressure on the inside and outside of the volume is gravity on the small volume.
$$
(p(r+dr)-p(r))d\sigma = dpd\sigma = -\rho gdrd\sigma
$$
Or in the view of equilibrium, pressure from inside (pointing outward) = pressure from outside (pointing inward) + gravity (pointing inward). 
$$
p(r+dr)d\sigma + \rho g dr d\sigma = p(r)d\sigma
$$

Therefore we have the differential equation in Euler description,
$$
\frac{dp}{dr} = -\rho g,
$$
Or in Lagrangian description, multiplying [the mass distribution function](<Stellar Model>) on both sides, 
$$
\frac{dp}{dM_r} = -\frac{g}{4\pi r^2} = -\frac{GM_r}{4\pi r^4}.
$$
## Hydrostatic Equilibrium Timescale
For non-equilibrium cases,
$$
\rho\ddot{R}d\sigma dr = p(r)d\sigma - p(r+dr)d\sigma - \rho g dr d\sigma
$$
Therefore,
$$
\ddot R = -\frac{1}{\rho}\frac{dp}{dr}-g
$$
1. Gravity dominates
	$$
	\tau_h \sim (\frac{1}{G\rho_0})^{1/2}
	$$
	is of the same magnitude with [free fall scale](<Star Formation>)
2. Pressure gradient dominates
	$$
	\tau_h \sim R(\frac{\rho}{p})^{1/2} = \frac{R}{c_s}
	$$