# Task 1

## Problem:

*O**M* = *s*<sub>*r*</sub>(*t*) = 6*π**t*<sup>2</sup>  
$\phi (t) = \frac{\pi t^3}{6}$  
(1) Simulate the mechanism  
(2) Find absolute, transport and relative velocities and accelerations
for *M*  
(3) Find *t*, when *M* reaches *O*  
(4) Put on simulation the previous statements

The universe is immense and it seems to be homogeneous, in a large
scale, everywhere we look at.

![image](images/vel_coord.png)

There’s a picture of a galaxy above

## Solution:

I denoted the center of *O**A* as *C*  
(1) and (4) The simulation is available by the  
Link <https://www.geogebra.org/m/hhxbcrb6>  
(2)
$$\begin{split}
    \omega = \dot \phi(t)\\\\
    \underline{\underline{
    V_M ^{tr} = \omega O_2A, V_M ^{tr} \perp O_2A
    }}\\\\
    \underline{\underline{
    V_M ^{rel} = \dot s_r(t) = 12\pi t, V_M ^{rel} \perp CM
    }}\\\\
        \underline{\underline{
    \overrightarrow{V_M} = \overrightarrow{V_M ^{tr}} + \overrightarrow{V_M ^{rel}}
    }}\\\\
\end{split}$$
The logic for accelerations is the same. There is no Coriolis
acceleration, because semicirlce *D* does not have angular velocity
($\overrightarrow{V_A} = \overrightarrow{V_O}$)  
$$\begin{split}
    \underline{\underline{
    a\_{tr} ^{n} = \omega ^2 O_2A,  \overrightarrow{a\_{tr} ^{n}} \|\| O_2A
    }}\\\\
    \epsilon = \ddot \phi = \pi t
    \\\\
    \underline{\underline{
    a\_{tr} ^{\tau} = \epsilon O_2A, \overrightarrow{a\_{tr} ^{\tau}} \|\| \overrightarrow{V\_{tr}}
    }}\\\\
    \overrightarrow{a_M ^{rel}} =\overrightarrow{a\_{rel} ^{n}} + \overrightarrow{a\_{rel} ^{\tau}}\\\\
    \underline{\underline{
    a\_{rel} ^{n} = \frac{V\_{rel}^2}{R},  \overrightarrow{a\_{rel} ^{n}} \|\| CM
    }}\\\\
    \underline{\underline{
    a\_{rel} ^{\tau} = \ddot s_r = 12\pi, \overrightarrow{a\_{rel} ^{\tau}} \|\| \overrightarrow{V\_{rel}}
    }}\\\\
    \underline{\underline{
     \overrightarrow{a_M ^{tr}} =\overrightarrow{a\_{tr} ^{n}} + \overrightarrow{a\_{tr} ^{\tau}}
    }}
\end{split}$$

\(3\) Here I just solved a simple equation:
$$\begin{split}
    s_r (t) = \phi (t) R\\\\
    6 \pi t^2 = \frac{\pi t^3}{6} R\\\\
    \underline{\underline{
    t = \sqrt{\frac{R}{6}}
    }}
\end{split}$$

# Task 2

## Problem:

*O**M* = *s*<sub>*r*</sub>(*t*) = 75*π*(0.1+0.3*t*<sup>2</sup>)  
*ϕ*(*t*) = 2*t* − 0.3*t*<sup>2</sup>  
(1) Simulate the mechanism  
(2) Find absolute, transport and relative velocities and accelerations
for *M*  
(3) Find *t*, when *M* reaches *O* second time  
(4) Put on simulation the previous statements

## Solution:

I denoted the center of the circle as *O*<sub>2</sub>  
(1) and (4) The simulation is available by the  
Link <https://www.geogebra.org/m/pzvphvd3>  
(2)
$$\begin{split}
    \omega = \dot \phi(t)\\\\
    \underline{\underline{
    V_M ^{tr} = \omega O_1M, V_M ^{tr} \perp O_1M
    }}\\\\
    \underline{\underline{
    V_M ^{rel} = \dot s_r(t) = 75\pi (0.1+0.6t), V_M ^{rel} \perp O_2M
    }}\\\\
        \underline{\underline{
    \overrightarrow{V_M} = \overrightarrow{V_M ^{tr}} + \overrightarrow{V_M ^{rel}}
    }}\\\\
\end{split}$$
The logic for accelerations is the same. There is Coriolis
acceleration  
$$\begin{split}
    \underline{\underline{
    a\_{tr} ^{n} = \omega ^2 O_1M,  \overrightarrow{a\_{tr} ^{n}} \|\| O_1M
    }}\\\\
    \epsilon = \ddot \phi = -0.6
    \\\\
    \underline{\underline{
    a\_{tr} ^{\tau} = \epsilon O_1M, \overrightarrow{a\_{tr} ^{\tau}} \|\| \overrightarrow{V\_{tr}}
    }}\\\\
    \overrightarrow{a_M ^{rel}} =\overrightarrow{a\_{rel} ^{n}} + \overrightarrow{a\_{rel} ^{\tau}}\\\\
    \underline{\underline{
    a\_{rel} ^{n} = \frac{V\_{rel}^2}{R},  \overrightarrow{a\_{rel} ^{n}} \|\| O_2M
    }}\\\\
    \underline{\underline{
    a\_{rel} ^{\tau} = \ddot s_r = 75\pi 0.6t, \overrightarrow{a\_{rel} ^{\tau}} \|\| \overrightarrow{V\_{rel}}
    }}\\\\
    \underline{\underline{
    \overrightarrow{a_M ^{cor}} = 2 \omega \times  \overrightarrow{V\_{rel}}
    }}
    \\\\
    \underline{\underline{
     \overrightarrow{a_M ^{tr}} =\overrightarrow{a\_{tr} ^{n}} + \overrightarrow{a\_{tr} ^{\tau}} + \overrightarrow{a\_{M} ^{cor}}
     }}
\end{split}$$

\(3\) Here I just solved a simple equation:
$$\begin{split}
    s_r (t) = \phi (t) R\\\\
    75 \pi (0.1 + 0.3t^2) = 2\pi R\\\\
    \underline{\underline{
    t = \frac{-15+\sqrt{225+720R}}{90} \approx 1.17704 s
    }}
\end{split}$$
