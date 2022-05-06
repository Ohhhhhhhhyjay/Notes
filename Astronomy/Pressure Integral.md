## Introduction
具有动量 $p$ 的单个粒子对容器壁的压力的贡献为,
$$
f = \frac{\Delta p}{\Delta t} = 2p_x \frac{v_x}{2\Delta x} = \frac{p_x v_x}{\Delta x} = \frac{1}{3}\frac{pv}{\Delta x}
$$
其中 $\Delta t$ 是粒子和容器壁的作用时间的一半, $\Delta x$ 是粒子和容器壁碰撞作用的半程距离（只是作用的距离，与容器的大小无关）
$$
\begin{align}
P &= F/\sigma\\
&= \int_0^\infty \frac{1}{\sigma} f_p N_p dp\\
&= \frac{1}{3}\int_0^\infty \frac{N_p}{\sigma\Delta x}pv dp\\
P&= \frac{1}{3}\int_0^\infty n_ppv dp
\end{align}
$$
其中 $N_p$ 为系统中动量大小处于区间 $p\sim p+dp$ 的粒子数，$n_p$ 为单位体积中动量大小处于区间 $p\sim p+dp$ 的粒子数。

这式子称作压强积分
$$
P = \frac{1}{3}\int_0^\infty n_ppv dp
$$

## Application
### Ideal gas
$$p = mv$$
$$dn = n_p dp = n_v dv$$
Using Maxwell-Boltzmann Distribution
$$n_v dv = n\left(\frac{m}{2\pi kT}\right)^{3/2}e^{-mv^2/2kT}4\pi v^2 dv$$
Finally
$$P = m\frac{1}{3}\int_0^\infty n_v v^2dv = nkT$$

### Blackbody Radiation

$$p = \frac{h\nu}{c}$$
$$dn = n_p dp = n_\nu d\nu$$
$$P_R = \frac{1}{3}\int_0^\infty n_\nu \frac{h\nu}{c} cd\nu = \frac{1}{3}\int_0^\infty u_\nu d\nu$$
$$P_R = \frac{1}{3}aT^4=\frac{4}{3c}\sigma T^4$$
Where $u_\nu$ is the [energy density of radiation](Radiation), using Planck formula ([[Blackbody Radiation]]),

$$u_\nu = \frac{8\pi h \nu^3}{c^3}\frac{1}{e^{h\nu/kT} - 1} = \frac{1}{c}\int_{4\pi}B_\nu(T)d\omega = \frac{4\pi}{c}B_\nu(T)$$

And $P$ here corresponds to the radiation pressure mentioned in [radiation](Radiation) in the following way

$$
\begin{align}
P_{R,\nu} = \frac{1}{c}\int_{4\pi}B_\nu(T)\cos^2\theta d\omega = \frac{1}{c}B_\nu(T)\int_{4\pi}\cos^2\theta d\omega
\end{align}
$$
Where
$$\int_{4\pi}\cos^2d\omega = \frac{4\pi}{3}$$
Therefore
$$P_{R,\nu} = \frac{4\pi}{3c}B_{\nu}(T) = \frac{1}{3}u_\nu$$

