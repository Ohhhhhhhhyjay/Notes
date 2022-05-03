# Synthetic Stream
## Pal 5-like Synthetic Streams
Original: [Detecting Thin Stellar Streams in External Galaxies: Resolved Stars and Integrated Light](https://iopscience.iop.org/article/10.3847/1538-4357/ab3e06/pdf)
Followed: [The Hough Stream Spotter: A New Method for Detecting Linear Structure in Resolved Stars and Application to the Stellar Halo of M31](https://arxiv.org/pdf/2107.00017.pdf)

>In particular, we inject mock streams to data from the PAndAS M31 Survey and produce simulated M31 backgrounds mimicking what WFIRST will observe in M31.

### Assumptions
- The fact that the stream should be wider toward its endpoints should is not considered.
- Assume the same age $t$ of the stream in all cases.

### How to generate [Pal 5](Pal%205.md 5>)-like synthetic streams
1. Download [isochrones](Stellar%20Isochrone.md Isochrones.md>) for a Pal 5-like cluster from PARSEC evolutionary tracks
	- $\text{Age} = 11.5 \,\text{Gyr}$
	- [Metallicity](<Stellar Streams.md#Metallicity>) $\text{[Fe/H]}=-1.3$
	- Shift the isochrones to $d = 23.5\,kpc, d_\text{mod} = 16.86$ (Pal 5's current distance in the Milky Way) (?)
2. Compute a luminosity function ($N(m)\rightarrow g_0 \sim m\rightarrow N(g_0)$)
	- Sample masses $m = 0.01-120M_\odot$ from a power-law initial mass function $dN/dm \propto m^{0.5}$.
	- Use the [isochrone table](http://stev.oapd.inaf.it/cgi-bin/cmd) to infer the stars' magnitudes 
3. Determine how many stars we can observe in a Pal 5-like stream at a given limiting magnitude
	1. Normalize the luminosity function from CFHT such that there are 3000 stars with $20<g_0<23$ (?)
	2. Compute the cumulative number of stars at a given limiting magnitude
4. Set mass and galactocentric radii
	1. $m = m_\text{Pal5}, 5 m_\text{Pal5}, 10m_\text{Pal5}$
	2. $R_\text{GC}=15, 35, 55 kpc$
5. Width $$
	w = R_\text{GC}\left(\dfrac{m}{M(R_\text{GC})}\right)^{1/3} = R_\text{GC}\left(\dfrac{mG}{v_c^2 R_\text{GC}}\right)^{1/3} \propto R_\text{GC}^{2/3}\dfrac{m^{1/3}}{v_c^{2/3}}
	$$
	$M$ is the enclosed mass of the host within the stream's orbit;
	$v_c$ is the circular velocity at radius $R_\text{GC}$;
	$m$ is the mass of the cluster;
	$M(R_\text{GC})$ is the enclosed mass of the host within the stream's orbit.
	
	Update/Scale the width based on circular velocity $v_c$ at $R_{GC}$, galactocentric radii $R_{GC}$,  mass of the stream $m$.
	$$
	w = \left(\dfrac{m}{m_\text{Pal5}}\right)^{1/3}\left(\dfrac{R_\text{GC}}{R_\text{GC, Pal5}}\right)^{2/3} \left(\dfrac{v_{c}}{v_{c,\text{Pal5}}}\right)^{-2/3} w_{\text{Pal5}}
	$$
6. Length $$
	\begin{align}
	\Psi &= 4\left(\dfrac{m}{M(R_\text{GC})}\right)^{1/3} \dfrac{2\pi t}{T_\psi} \propto \left(\dfrac{m}{M(R_\text{GC})}\right)^{1/3} \dfrac{t}{T_\psi}\\
	&\propto \left(\dfrac{m}{v_c^2R_\text{GC}}\right)^{1/3}\dfrac{v_c t}{R_\text{GC}} = \dfrac{m^{1/3}}{R_\text{GC}^{4/3}}v_c^{1/3}t
	\end{align}
	$$
	$t$ is the dynamical age of the stream;
	$T_\psi$ is the azimuthal period of the cluster around its host galaxy.
	$$
	L \propto R_\text{GC}\Psi \propto \dfrac{m^{1/3}}{R_\text{GC}^{1/3}}v_c^{1/3}t
	$$
	Updata/Scale the length based on $m, R_\text{GC}, v_c$
7. Sample the stream stars from a normal distribution, with a dispersion (width) $w$ calculated using equation above.

	![](Pasted%20image%2020220422032748.png)

$$
\begin{align}
	n &= n_0\exp\{-\dfrac{1}{2}x^T\Sigma^{-1} x\}\\
	\Sigma &= \begin{pmatrix}
	l^2 & 0\\
	0 & w^2
	\end{pmatrix} 
\end{align}
$$

### Notes
PARSEC evolutionary tracks: Padova-Trieste evolutionary tracks.