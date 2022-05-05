## Jeans Criterion
根据[位力定理](<Virial Theorem>)，自引力束缚的平衡系统有
$$
2K + U = 0
$$
其中 $K > 0$, $U < 0$. 考虑一个自引力束缚的分子云，若 $2K + U > 0$ 则动能主导，分子云膨胀。若$2K + U<0$ 则引力势能主导，分子云坍缩。由此可以导出分子云坍缩的金斯判据。

对一个忽略旋转，湍动，磁场，密度均匀($\rho=\text{const.}$)的球对称单原子分子云，其[自引力势能](<Gravitation Law>)为
$$
U = -\frac{3}{5}\frac{GM^2}{R}
$$
根据[能量均分定理](<Equipartition Theorem>)，分子云的热运动动能为
$$
K = \frac{3}{2}NkT = \frac{3}{2}\frac{M}{\mu m_H}kT
$$
由$2K+U<0$判据即可得金斯判据
$$
\begin{align}
3\frac{M}{\mu m_H}kT -\frac{3}{5}\frac{GM^2}{R} < 0\\
\\
M > \left(\frac{5kT}{G\mu m_H}\right)^{3/2}\left(\frac{3}{4\pi \rho}\right)^{1/2}:= M_J \propto T^{3/2}\rho^{-1/2}\\
R > \left(\frac{15kT}{4\pi G\mu m_H\rho}\right)^{1/2} := R_J
\end{align}
$$
其中$M_J, R_J$分别称金斯质量，金斯半径。上二式称恒星形成的金斯判据。


## Free Fall
解运动方程得到的分子云坍缩自由下落时标为
$$
t_\text{ff} = \frac{\pi}{2\chi} = \left(\frac{3\pi}{32}\frac{1}{G\rho_0}\right)^{1/2}
$$
- 同调坍缩 Homogeneous collapse
- 由内而外坍缩 Inside-out collapse (初始密度不均匀，内部较致密的巨分子云)

### Derivation

下面由第一性原理出发推导上式，考虑一个初始半径 $r_0$，初始密度均匀为 $\rho_0$ 的分子云。初期气体自身压强忽略，光学薄，引力势能释放不受阻，等温坍缩。处于距离分子云中心 $r$ 处的质量元的牛顿运动方程为
$$
\frac{d^2r}{dt^2} = -G\frac{M_r}{r^2}
$$
其中
$$
M_r = \int_0^r4\pi r^2\rho(r)dr
$$

Solution
1. Multiply $dr/dt$ on both sides and integrate twice.
	$$
	\frac{dr}{dt}\frac{d^2r}{dt^2} = \frac{dr}{dt}\frac{d}{dt}\frac{dr}{dt} = \frac{1}{2}\frac{d}{dt}\left(\frac{dr}{dt}\right)^2 = -G\frac{M_r}{r^2}\frac{dr}{dt},
	$$
	Integrate over $t$, i.e., $\int_0^t(\cdots) dt$
	$$
	\frac{1}{2}d\left(\frac{dr}{dt}\right)^2 = -G\frac{M_r}{r^2}dr,
	$$
	Integrate again $\int_i^f(\cdots)$. Note that during the collapse $r$ retracts while $M_r$ stays the same. The matter inside a spherical shell of radius $r$ moves inward along with $r$ and stays inside the shell. 
	$$
	\frac{1}{2}\left(\frac{dr}{dt}\right)^2 = G\frac{M_r}{r} + C_1,
	$$
	
2. When $t=0,\, r=r_0, dr/dt=0$
	$$
	\frac{dr}{dt} = -\left(\frac{8}{3}\pi G \rho_0 r_0^2 (\frac{r_0}{r} - 1)\right)^{1/2},
	$$
3. Let $\theta := r/r_0$, $\chi := (8/3\pi G\rho_0)^{1/2}$
	$$
	\frac{d\theta}{dt} = -\chi\left(\frac{1}{\theta} - 1\right)^{1/2},
	$$
4. Let $\cos^2\xi:=\theta$ and integrate
	$$
	\cos^2\xi\frac{d\xi}{dt} = \frac{1}{2}\xi dt,
	$$
	Integration yields
	$$
	\frac{\xi}{2} + \frac{1}{4}\sin{2\xi} = \frac{\xi}{2}t + C_2,
	$$
5. When $t=0,\, r=r_0, \xi=0$
	$$
	\frac{\xi}{2} + \frac{1}{4}\sin{2\xi} = \frac{\xi}{2}t.
	$$

As $r$ goes from $r_0$ to $0$, $\xi$ goes from $0$ to $\pi/2$. Take $\xi=\pi/2$, the $t$ obtained is $t_\text{ff}$.