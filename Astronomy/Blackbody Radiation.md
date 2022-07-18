## Planck Formula
[Intensity](Radiation.md) of thermal radiation,
$$
B_\nu(T) = \frac{2h\nu^3}{c^2}\frac{1}{e^{h\nu/kT}-1}
$$
$$
B_\lambda(T) = \frac{2hc^2}{\lambda^5}\frac{1}{e^{hc/\lambda kT}-1}
$$
In the form of [energy density](Radiation.md), $u_\nu(T)=\frac{4\pi}{c}B_\nu(T)$,
$$
u_\nu(T) = \frac{8\pi h\nu^3}{c^3}\frac{1}{e^{h\nu/kT}-1}
$$
$$
u_\lambda(T) = \frac{8\pi hc}{\lambda^5}\frac{1}{e^{hc/\lambda kT}-1}
$$

## Stefan-Boltzmann Law
$$
\begin{align}
B(T) &= \int_0^\infty B_\nu(T) d\nu\\
&= \frac{2\pi^5 k^4}{15c^2 h^3} T^4\\
&= \sigma T^4
\end{align}
$$
where $\sigma = 5.67\,Wm^{-2}K^{-4}$

## Einstein 跃迁概率系数
Einstein 引入这样的跃迁概率系数，用来解释Planck公式为什么是这样的形式。

**（受激）吸收概率系数**：在辐射强度为 $I_\nu$ 的辐射场的作用下，单位时间内一个原子在 $d\omega$ 立体角内吸收能量为 $h\nu_{ik}$ 的光子从较低的 $i$ 能级跃迁到较高的 $k$ 能级的概率为 $B_{ik}I_\nu \dfrac{d\omega}{4\pi}$；
**自发发射概率系数**：在没有外场的情况下，单位时间一个原子从高能级 $k$ 跃迁到低能级 $i$ 同时在 $d\omega$ 立体角内发射一个能量为 $h\nu_{ik}$ 光子的概率为 $A_{ki} I_{\nu} \dfrac{d\omega}{4\pi}$
**受激发射概率系数**：在辐射强度为 $I_\nu$ 的辐射场的作用下，单位时间一个原子从高能级 $k$ 跃迁到低能级 $i$ 同时在 $d\omega$ 立体角内发射一个能量为 $h\nu_{ik}$ 光子的概率为 $B_{ki} I_{\nu} \dfrac{d\omega}{4\pi}$

在热动平衡下存在着细致平衡原理，
$$
N_i B_{ik}I_\nu = N_k(A_{ki} + B_{ki} I_\nu)
$$
于是
$$
I_\nu = \frac{A_{ki}}{B{ki}}\frac{1}{\frac{N_i B_{ik}}{N_k {B_{ki}}} - 1}
$$
在热动平衡下带入 Boltzmann 公式，就能得到黑体辐射公式的基本形式。常数可以通过和原公式对比得到（而原公式和实验符合得很好，其实就是和实验对比得到待定系数）
$$
I_\nu = \frac{A_{ki}}{B{ki}}\frac{1}{\frac{g_i B_{ik}}{g_k {B_{ki}}}e^{-\frac{h\nu_{ik}}{kT}} - 1}
$$
对比和实验符合得很好的 Planck 公式就可以得到三个爱因斯坦系数之间满足的关系，对任意两个能级，知其一则知其三。
$$
\begin{align}
A_{ki} &= \frac{2h\nu^3}{c^2}B_{ki}\\
g_i B_{ik} &= g_k B_{ki}
\end{align}
$$
