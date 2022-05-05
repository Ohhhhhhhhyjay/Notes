## 辐射强度
- 辐射强度 $I_\nu$
$$
	dE_\nu = I_\nu d\sigma \cos{\theta} d\nu dt d\omega,
$$
- 辐射流 $\pi F_\nu$
$$
	\pi F_\nu = \int_{4\pi} I_\nu(\theta) \cos{\theta} d\omega,
$$
- 辐射流矢量 $\pi \vec F_\nu$
- 平均辐射强度 $J_\nu$
$$
	J_\nu = \dfrac{1}{4\pi} \int_{4\pi}I_\nu(\theta)d\omega,
$$
- 辐射密度 $U_\nu$
$$
	U_\nu = \dfrac{1}{c} \int_{4\pi} I_\nu d\omega,
$$
- 辐射压力 $P_{R,\nu}$
$$
	P_{R,\nu} = \frac{1}{c}\int_{4\pi}I_\nu(\theta)\cos^2\theta d\omega,
$$
- 辐射压力张量 $\vec P_{R,\nu}$

## 辐射转移方程
- 光学深度 $\tau_\nu$
$$
\tau_\nu = \int_0^s \chi_\nu\rho ds,\quad d\tau_\nu = \chi_\nu \rho ds,
$$
	$\tau_\nu \gg 1$ 称光学厚
	$\tau_\nu \ll 1$ 称光学薄
- 发射系数 $j_\nu$
$$
dE_\nu = j_\nu dm ds dt d\nu d\omega
$$
- 吸收系数 $\chi_\nu$
$$
dE_\nu = -\chi_\nu I_\nu dm dt d\nu d\omega
$$

则根据能量守恒可推导出辐射转移方程为
$$
\frac{dI_\nu}{ds} = -\chi_\nu I_\nu \rho + j_\nu\rho
$$
其中$ds$沿着光线传播的方向

## 参考资料
《恒星大气物理》汪珍如 曲钦岳