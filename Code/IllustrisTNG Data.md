https://www.tng-project.org/data/docs/specifications/

The data in Appalachia in stored in “/appalachia/d5/DISK/from_pleiades/snapshots”

Here are my explorations around IllustrisTNG-like data. It have similar structures and ran on same suite of codes, but they are not exactly the IllustrisTNG runs.

The IllustrisTNG snapshots:
PartType0 (Gas)
PartType1 (DM)
PartType3 (Tracers)
PartType4 (Stars)
PartType5 (BHs)

```Python
('Config', <HDF5 group "/Config" (0 members)>)
('Header', <HDF5 group "/Header" (0 members)>)
('Parameters', <HDF5 group "/Parameters" (0 members)>)
('PartType0', <HDF5 group "/PartType0" (16 members)>)
('PartType2', <HDF5 group "/PartType2" (4 members)>)
('PartType3', <HDF5 group "/PartType3" (4 members)>)
('PartType4', <HDF5 group "/PartType4" (10 members)>)
```

Gas

```python
>>> for n in f['PartType0'].items():
...     print(n)
... 
('Coordinates', <HDF5 dataset "Coordinates": shape (150185, 3), type "<f8">)
('Density', <HDF5 dataset "Density": shape (150185,), type "<f8">)
('DensityGradient', <HDF5 dataset "DensityGradient": shape (150185, 3), type "<f8">)
('ElectronAbundance', <HDF5 dataset "ElectronAbundance": shape (150185,), type "<f8">)
('GFM_CoolingRate', <HDF5 dataset "GFM_CoolingRate": shape (150185,), type "<f8">)
('GFM_Metallicity', <HDF5 dataset "GFM_Metallicity": shape (150185,), type "<f8">)
('GFM_Metals', <HDF5 dataset "GFM_Metals": shape (150185, 10), type "<f8">)
('InternalEnergy', <HDF5 dataset "InternalEnergy": shape (150185,), type "<f8">)
('Masses', <HDF5 dataset "Masses": shape (150185,), type "<f8">)
('NeutralHydrogenAbundance', <HDF5 dataset "NeutralHydrogenAbundance": shape (150185,), type "<f8">)
('ParticleIDs', <HDF5 dataset "ParticleIDs": shape (150185,), type "<u4">)
('Potential', <HDF5 dataset "Potential": shape (150185,), type "<f8">)
('Velocities', <HDF5 dataset "Velocities": shape (150185, 3), type "<f8">)
('VelocityCurl', <HDF5 dataset "VelocityCurl": shape (150185,), type "<f8">)
('VelocityDivergence', <HDF5 dataset "VelocityDivergence": shape (150185,), type "<f8">)
('Vorticity', <HDF5 dataset "Vorticity": shape (150185, 3), type "<f8">)
```

Dark Matter

```Python
In [4]: for n in f['PartType2'].items():
   ...:     print(n)
   ...: 
('Coordinates', <HDF5 dataset "Coordinates": shape (12481, 3), type "<f8">)
('ParticleIDs', <HDF5 dataset "ParticleIDs": shape (12481,), type "<u4">)
('Potential', <HDF5 dataset "Potential": shape (12481,), type "<f8">)
('Velocities', <HDF5 dataset "Velocities": shape (12481, 3), type "<f8">)
```



```Python
In [5]: for n in f['PartType3'].items():
   ...:     print(n)
   ...: 
('Coordinates', <HDF5 dataset "Coordinates": shape (137, 3), type "<f8">)
('ParticleIDs', <HDF5 dataset "ParticleIDs": shape (137,), type "<u4">)
('Potential', <HDF5 dataset "Potential": shape (137,), type "<f8">)
('Velocities', <HDF5 dataset "Velocities": shape (137, 3), type "<f8">)
```

Stars

```Python
In [6]: for n in f['PartType4'].items():
   ...:     print(n)
   ...: 
('Coordinates', <HDF5 dataset "Coordinates": shape (1687, 3), type "<f8">)
('GFM_InitialMass', <HDF5 dataset "GFM_InitialMass": shape (1687,), type "<f8">)
('GFM_Metallicity', <HDF5 dataset "GFM_Metallicity": shape (1687,), type "<f8">)
('GFM_Metals', <HDF5 dataset "GFM_Metals": shape (1687, 10), type "<f8">)
('GFM_StellarFormationTime', <HDF5 dataset "GFM_StellarFormationTime": shape (1687,), type "<f8">)
('Masses', <HDF5 dataset "Masses": shape (1687,), type "<f8">)
('MassiveStarMass', <HDF5 dataset "MassiveStarMass": shape (1687,), type "<f8">)
('ParticleIDs', <HDF5 dataset "ParticleIDs": shape (1687,), type "<u4">)
('Potential', <HDF5 dataset "Potential": shape (1687,), type "<f8">)
('Velocities', <HDF5 dataset "Velocities": shape (1687, 3), type "<f8">)
```

An overview of the magnitude of the data in PartType0 (Gas)

```python
/PartType0/Coordinates
[[308.17532102 297.09485281 299.69017669]
 [308.17883959 297.09656353 299.69076377]
 [308.1764337  297.09936524 299.6861383 ]
 ...
 [307.60595019 296.56785915 300.13979892]
 [307.60762108 296.57178671 300.13709098]
 [307.60344509 296.57167086 300.13357429]]
 
/PartType0/Density
[0.00169523 0.00188494 0.00187443 ... 0.00132014 0.00124536 0.00131396]
 
/PartType0/DensityGradient
[[ 0.03854979  0.02613487 -0.00229575]
 [ 0.03970846  0.02801181 -0.00286574]
 [ 0.04392883  0.02665477 -0.00663974]
 ...
 [-0.01407933 -0.02121968 -0.00083435]
 [-0.01125934 -0.0160908  -0.00118392]
 [-0.01306992 -0.02263002 -0.00406674]]
 
/PartType0/ElectronAbundance
[0.42347422 0.40620271 0.40673839 ... 0.46674766 0.47685041 0.46795691]
 
/PartType0/GFM_CoolingRate
[9.19663278e-26 7.77308918e-26 9.35909641e-26 ... 8.58655613e-26
 1.01053710e-25 6.60967077e-26]
 
/PartType0/GFM_Metallicity
[0.01269999 0.01269999 0.01269999 ... 0.01269999 0.01269999 0.01269999]
 
/PartType0/GFM_Metals
[[7.38800017e-01 2.48499993e-01 2.39999803e-03 ... 6.99999425e-04
  1.29999893e-03 1.53656062e-58]
 [7.38800017e-01 2.48499993e-01 2.39999803e-03 ... 6.99999425e-04
  1.29999893e-03 2.16838691e-58]
 [7.38800017e-01 2.48499993e-01 2.39999803e-03 ... 6.99999426e-04
  1.29999893e-03 4.12962363e-58]
 ...
 [7.38800020e-01 2.48499992e-01 2.39999769e-03 ... 6.99999327e-04
  1.29999875e-03 2.32945228e-93]
 [7.38800020e-01 2.48499992e-01 2.39999769e-03 ... 6.99999327e-04
  1.29999875e-03 5.79687511e-92]
 [7.38800021e-01 2.48499992e-01 2.39999766e-03 ... 6.99999316e-04
  1.29999873e-03 1.30713397e-91]]
 
/PartType0/InternalEnergy
[128.55523285 126.52275448 126.19200816 ... 134.59026314 135.67859101
 135.14972159]
 
/PartType0/Masses
[1.23741853e-10 8.30739041e-11 8.72157486e-11 ... 1.39224412e-10
 1.40366702e-10 1.20729006e-10]
 
/PartType0/NeutralHydrogenAbundance
[0.60204814 0.61813872 0.61764436 ... 0.56178393 0.55240108 0.56065502]
 
/PartType0/ParticleIDs
[384387895 358723855 429278151 ... 331721653 338532987 306370113]
 
/PartType0/Potential
[-25775.88829887 -25768.94977425 -25773.71904182 ... -26871.28895819
 -26872.17314447 -26884.56067495]
 
/PartType0/Velocities
[[ 76.01476335 191.55455545   3.39030855]
 [ 76.31803012 191.60964434   3.18490357]
 [ 75.56297887 192.15523235   2.64160674]
 ...
 [136.07448281 219.6945109   -0.98514621]
 [136.73348102 219.77713872  -1.04982891]
 [136.39908259 219.99457654  -1.58093519]]
 
/PartType0/VelocityCurl
[ 78.61893466  74.26779305 150.01838115 ... 198.94338575 245.05217941
 169.65353436]
 
/PartType0/VelocityDivergence
[ 6842.07410011   447.8211983   1381.63078881 ... -3956.15120421
  8609.22809212 12808.45467304]
 
/PartType0/Vorticity
[[  -4.26308315   47.38853465   62.58665826]
 [  16.37198279   55.50431968   46.55033578]
 [ -49.87097302  125.59646865   65.14543571]
 ...
 [ -22.24071166 -197.4264912   -10.32482687]
 [  23.18003317 -243.49227874  -14.99222772]
 [  -4.69045727 -169.39275028    8.14969218]]

```


### Gas Temperature
https://www.tng-project.org/data/docs/faq/#gen5

The gas temperature must be derived from the internal energy $u$ and the electron abundance $x_e (=n_e/n_H)$ which are `PartType0` snapshot fields `InternalEnergy` and `ElectronAbundance`, respectively. First, the mean molecular weight can be calculated as

$$μ=\frac{4}{1+3X_H+4X_Hx_e}*m_p.$$

Then, the temperature in Kelvin is given by

$$T=(γ−1)∗u/k_B∗\frac{\text{UnitEnergy}}{\text{UnitMass}}∗μ.$$

Here, $γ=5/3$ is the adiabatic index, $k_B$ is the Boltzmann constant in CGS units, and $X_H=0.76$ is the hydrogen mass fraction. Finally, `UnitMass` and `UnitEnergy` are those code units in CGS units. Specifically, `UnitEnergy = UnitMass * UnitLength^2 / UnitTime^2` (UnitLength is 1 kpc, UnitTime is 1 Gyr), so their ratio is $10^{10}$.

