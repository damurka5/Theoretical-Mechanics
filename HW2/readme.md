# Task 1

## Problem:

\(1\) Simulate the mechanism;  
(2) Find velocities for A, B, C, D, E, F and their angular velocities;  
(3) Find acc. for A and B;  
(4) Plot

## Solution:

\(1\) To simulate the system I find positions of all points.  
For A it was easy, for the rest I solved the system of equations:  
Let me denote *ω*<sub>*O*<sub>1</sub>*A*</sub> as *ω*, and
*O*<sub>1</sub> as origin:
$$\begin{cases}
    x_A = O_1A \cos(\omega t)\\\\
    y_A = O_1A \sin(\omega t)\\\\
    (x_A-x_B)^2 + (y_A-y_B)^2 = AB^2\\\\
    (x_A-x_C)^2 + (y_A-y_C)^2 = AC^2\\\\
    (x_C-x_B)^2 + (y_C-y_B)^2 = BC^2\\\\
    (x_B-56)^2 + (y_B+26)^2 = O_2B^2\\\\
    (x_D-x_C)^2 + (y_D-y_C)^2 = CD^2\\\\
    (x_E-x_C)^2 + (y_E-y_C)^2 = CE^2\\\\
    (x_E-x_D)^2 + (y_E-y_D)^2 = ED^2\\\\
    (x_F-66)^2 + (y_F-41)^2 = O_3F^2\\\\
    (x_F-x_E)^2 + (y_F-y_E)^2 = EF^2\\\\
    y_D = 16
    \end{cases}$$
Then I found the angle when the system can exist:  
The first extreme position is when *A*, *B*, *O*<sub>2</sub> lie on one
line  
$$\begin{cases}
    (x)^2 + (y)^2 = O_1A^2\\\\
    (x-56)^2 + (y+26)^2 = (AB+O_2B)^2
    \end{cases}$$
$$\begin{split}
    \tan{\phi_1} = \frac{y}{x}\\\\
    \phi_1 \approx 122.7 \degree
\end{split}$$
The second extreme position is when *A*, *O*<sub>1</sub> and *B* on the
same line:  
$$\begin{cases}
    \frac{x_A}{x_B} = \frac{y_A}{y_B}\\\\
    x_A ^2 + y_A ^2 = 21^2\\\\\\
    (x_B-56)^2 + (y_B +26)^2=25^2\\\\
    (x_A-x_B)^2 + (y_A - y_B)^2=54^2
    \end{cases}$$
$$\begin{split}
    \tan{\phi_2} = \frac{y_A}{x_A}\\\\
    \phi_2 \approx -6.98 \degree
\end{split}$$

Animation is available here:  
Link
<https://drive.google.com/file/d/1v227ElpF-51pBqSWI8nVU-dY8Y-i3eIo/view?usp=sharing>  
Colab is here:  
Link
<https://drive.google.com/file/d/1QeVTCAL9XqE9UZaO5M8qW2dMAtRZ969h/view?usp=sharing>  
(2) To find velocities I took derivatives of coordinates of each
point:  
$$\underline{\underline{
\begin{split}
    V\_{Ax} = -\omega \* O1A \* \sin{(\phi + \omega\*t)}\\\\
    V\_{Ay} = \omega \* O1A \* \cos{(\phi + \omega\*t)}\\\\
    V\_{Bx} = \dot x_B\\\\
    V\_{By} = \dot y_B\\\\
    V\_{Cx} = \dot x_C\\\\
    V\_{Cy} = \dot y_C\\\\
    V\_{Dx} = \dot x_D\\\\
    V\_{Dx} = \dot y_D\\\\
    V\_{Ex} = \dot x_E\\\\
    V\_{Ex} = \dot y_E\\\\
    V\_{Fx} = \dot x_F\\\\
    V\_{Fx} = \dot y_F\\\\
\end{split}
}}$$

# Task 2

## Problem:

Find:  
(1) angular velocity and angular acceleration of A;  
(2) vel. and acc. for M point;  
(3) draw plots for previous statements;  

## Solution:

\(1\) Lets define the distance from *O* to the center of a small circle
(*O*<sub>*A*</sub>) as *l* and the radius of the circle as *r*  
$$\begin{split}
r = 20\sqrt{2-\sqrt{3}} \\\\
  l = 20\sqrt{2+\sqrt{3}}
\end{split}$$
The angle between *l* and *z*-axis is *π*/4  
The angular velocity can be expressed as
*ω* = *ω*<sub>1</sub> + *ϵ*<sub>1</sub>*t*  
So, the angular velocity of A can be found knowing the velocity of the
center of A and the distance from *z*-axis to *O*<sub>*A*</sub>:  
$$\begin{split}
    V\_{OA} = \omega l \frac{\sqrt{2}}{2}\\\\
    a\_{OA} = \epsilon_1 l \frac{\sqrt{2}}{2}\\\\
    \underline{\underline{
        \omega_A = - \frac{V\_{OA}}{r}
    }}\\\\
    \underline{\underline{
        \epsilon_A = \frac{a\_{OA}}{r}
    }}
\end{split}$$
(2) The velocity of M is:  
$$\underline{\underline{
        V_M =  \omega_A (2r-M_0 M)
    }}$$
To plot it I used rotation matrices, but before I described the motion
of M with respect to *O*<sub>*A*</sub>. I put the small cone to
*x*-axis, then rotated around *z*-axis by *ω**t* and rotated around new
*y*-axis by *π*/4. I got for V:
$$\begin{split}
\underline{\underline{
    V\_{Mx} = \frac{\sqrt{2}}{2} l \cos{(\omega t)}-\sin{(\omega t)} d \cos{(\omega\_{a} t)}-\frac{\sqrt{2}}{2} d \cos{(\omega t)} \sin{(\omega\_{a} t)} 
    }}\\\\
    \underline{\underline{
     V\_{My} = \frac{\sqrt{2}}{2} l \sin{(\omega t)}-\sin{(\omega t)} d \cos{(\omega\_{a} t)}-\frac{\sqrt{2}}{2} d \sin{(\omega t)} \sin{(\omega\_{a} t)} 
     }}\\\\
     \underline{\underline{
     V\_{Mz} = \frac{\sqrt{2}}{2} l+\frac{\sqrt{2}}{2} d \sin(\omega\_{a} t)}}
\end{split}$$
To find accelerations I differentiated components of *V*<sub>*M*</sub>
over time (slava Bogu, geogebra umeet eto delat’):

$$\begin{split}
\underline{\underline{
    a\_{Mx} = \dot V\_{Mx}
    }}\\\\
    \underline{\underline{
     a\_{My} = \dot V\_{My}
     }}\\\\
     \underline{\underline{
      a\_{Mz} = \dot V\_{Mz}
      }}
\end{split}$$

To get $\overrightarrow{a_n}$ and $\overrightarrow{a\_\tau}$ I should
find their lengths and, knowing that they are perpendicular to each
other, I can find them
$$\underline{\underline{
    a\_{\tau M} = \frac{\overrightarrow{a_M} \cdot \overrightarrow{V_M}}{\|\overrightarrow{V_M}\|} 
    }}$$

$$\underline{\underline{
    a\_{nM} = \frac{\overrightarrow{a_M} \times \overrightarrow{V_M}}{\|\overrightarrow{V_M}\|}
    }}$$

\(3\) Graph is available here  
Link : <https://www.geogebra.org/m/mxt7m7rn>
