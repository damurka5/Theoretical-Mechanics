# Task 1

## Problem:

You should find
$y(x), \overrightarrow{v}, \overrightarrow{a}, \overrightarrow{a_n},\overrightarrow{a\_\tau}, \kappa$
(Osculating circle) for  
*t* ∈ \[−5,5\].
$$\begin{cases}
        x = 3t
        \\\\
        y = 4t^2 + 1
\end{cases}$$
Plot them

## Solution:

\(1\) Let me derive the *y*(*x*). I just express *t* through *x* and
substitute it to *y* = 4*t*<sup>2</sup> + 1  
I obtain:  
$$\underline{\underline{y(x) = \frac{4}{9} x^2 +1}}$$
  
(2) To get *v⃗* I should take derivatives of *x*(*t*) and *y*(*t*) with
respect to *t*:
*v*<sub>*x*</sub> = *ẋ* = 3
*v*<sub>*y*</sub> = *ẏ* = 8*t*

$$\underline{\underline{
\overrightarrow{v}=
    \begin{pmatrix}
    3\\\\
    8t
    \end{pmatrix}
}}$$
$$v = \sqrt{9+64t^2}$$

\(3\) To get *a⃗* I should take derivatives of *v*<sub>*x*</sub>(*t*) and
*v*<sub>*y*</sub>(*t*) with respect to *t*:
$$a_x = \dot{v_x} = 0$$
$$a_y = \dot{v_y} = 8$$

$$\underline{\underline{
\overrightarrow{a}=
    \begin{pmatrix}
    0\\\\
    8
    \end{pmatrix}
}}$$

\(4\) To get $\overrightarrow{a_n}$ and $\overrightarrow{a\_\tau}$ I
should find their lengths and, knowing that they are perpendicular to
each other and $\overrightarrow{a\_\tau}$ is tangent to
$y(x) = \frac{4}{9} x^2 +1$, I can find and plot them:

$$a\_\tau = \frac{\overrightarrow{a} \cdot \overrightarrow{v}}{\|\overrightarrow{v}\|} = \frac{64t}{\sqrt{9+64t^2}}$$

$$a_n = \frac{\overrightarrow{a} \times \overrightarrow{v}}{\|\overrightarrow{v}\|} = \frac{24}{\sqrt{9+64t^2}}$$
*a*<sub>*n*</sub> directed to the center of curvature  
To calculate coordinates of $\overrightarrow{a_n}$ I found
$y'(x) = \frac{8}{9}x$ – it is a slope and tangent line has the same
slope. Knowing slope and the length of $\overrightarrow{a_n}$, it is
easy to find its coordinates.
$$\begin{cases}
        \sqrt{x^2\_{a_n} + y^2\_{a_n}} = a_n
        \\\\
        \frac{y\_{a_n}}{x\_{a_n}} = y'(x)
\end{cases}$$
Solving the equation I get:

$$\underline{\underline{
    \overrightarrow{a_n} = 
    \begin{pmatrix}
        \frac{64t}{\frac{64}{3}t^2 +3}
        \\\\
        \frac{8}{3}t \frac{64t}{\frac{64}{3}t^2 +3}
    \end{pmatrix}
}}$$

$$\overrightarrow{a\_\tau} = \overrightarrow{a} - \overrightarrow{a_n} = 
    \underline{\underline{
        \begin{pmatrix}
            -\frac{64t}{\frac{64}{3}t^2 +3}
            \\\\
            8-\frac{8}{3}t \frac{64t}{\frac{64}{3}t^2 +3}
        \end{pmatrix}
    }}$$

\(5\) The osculating circle *κ* is tangent to *y*(*x*) and its radius is
equal to:
$$\underline{\underline{
    \rho = \frac{v^2}{a_n} = \frac{(9+64t^2)^{1.5}}{24}
}}$$
  

## Plotting:

Link : <https://www.geogebra.org/m/wuss3jqt>

# Task 2

## Problem:

*ω*<sub>*O**A*</sub> = 1*r**a**d*/*s*, *ϵ*<sub>*O**A*</sub> = 0,
*O**A* = *O**P* = 25, *A**B* = 80, *A**C* = 20  
(1) Simulate the mechanism  
(2) Find velocities for points B, C  
(3) Find accelerations for points B, C  
(4) Plot

## Solution:

(1)To simulate the model I found coordinates of points A, B, C with
respect to *t*:  
$$A:
\underline{\underline{
    \begin{cases}
        x_A = OAcos(\omega\_{OA}t)
        \\\\
        y_A = OAsin(\omega\_{OA}t)
\end{cases}
}}$$
It is much harder to find B, but I did.  
$$B:
    \begin{cases}
        (x_B-x_A)^2 + (y_B-y_A)^2 = AB^2
        \\\\
        y_B = \frac{x_B}{\sqrt{3}} + 25
\end{cases}\\\\$$

$$\frac{4}{3}x_B+x_B(\frac{50\sqrt{3}-2\sqrt{3}y_A}{3} - 2x_A) - 50y_A - 5150 = 0$$
$$D = (\frac{50\sqrt{3}-2\sqrt{3}y_A}{3} - 2x_A)^2 + \frac{16}{3}(50y_A + 5150)$$

$$\underline{\underline{
        x_B= \frac{2x_A - \frac{50\sqrt{3}-2\sqrt{3}y_A}{3} - \sqrt{D}}{8/3}
        }}$$

$$\underline{\underline{
        y_B= \frac{x_B}{\sqrt{3}}+25
        }}$$
  
C point was found with vectors:
$$\overrightarrow{OC} = \overrightarrow{OB}+\frac{BC}{\|\overrightarrow{BA}\|}\overrightarrow{BA} = \begin{pmatrix}
            \frac{1}{4}x_B + \frac{3}{4}x_A
            \\\\
            \frac{1}{4}y_B + \frac{3}{4}y_A
    \end{pmatrix}$$
  
$$\underline{\underline{
    x_C = \frac{1}{4}x_B + \frac{3}{4}x_A
    }}$$
  
$$\underline{\underline{
    y_C = \frac{1}{4}y_B + \frac{3}{4}y_A
    }}$$
  
The simulation is available by link :
<https://www.geogebra.org/m/z833xxxj>  
  
(2) The velocities are just time-derivatives, so:
*v*<sub>*B**x*</sub> = *ẋ*<sub>*B*</sub>=
$$\underline{\underline{
     =\frac{-75sin(t)+25\sqrt{3}cos(t)}{4} - \frac{5625cos(t)-1875sin(2t)+1875\sqrt{3}sin(t)+1875\sqrt{3}cos(2t)}{2\sqrt{262200+45000sin(t)-15000\sqrt{3}cos(t)+7500\sqrt{3}sin(2t)+15000cos^2(t)}}
     }}\\\\$$
$$\underline{\underline{
    v\_{By} = \dot y_B = \frac{\dot x_B}{\sqrt{3}}
}}$$
  
For point C they are:
$$\underline{\underline{
    v\_{Cx} = \dot x_C = \frac{1}{4}(v\_{Bx}-75sin(t))
    }}$$
$$\underline{\underline{
    v\_{Cy} = \dot y_C = \frac{1}{4}(v\_{By}+75cos(t))
    }}$$
  
(3) The same algorithm as above – just (ha-ha, da-da, prosto kak dva
pal’ca ob asfal’t) find time-derivatives:  
First, let me denote
$(5625cos(t)-1875sin(2t)+1875\sqrt{3}sin(t)+1875\sqrt{3}cos(2t))$ as
*f*, and
$(2\sqrt{262200+45000sin(t)-15000\sqrt{3}cos(t)+7500\sqrt{3}sin(2t)+15000cos^2(t)})$
as *l*, their derivatives
$(-5625sin(t)-3750cos(2t)+1875\sqrt{3}cos(t)-3750\sqrt{3}sin(2t))$ as
*f**p**r**i**m**e* and
$(\frac{-4500cos(t)+15000\sqrt{3}sin(t)+15000\sqrt{3}cos(2t)-15000sin(2t)}{\sqrt{262200-45000sin(t)-15000\sqrt{3}cos(t)+7500\sqrt{3}sin(2t)+15000cos^2(t)}})$
as *l**p**r**i**m**e* so:
$$\underline{\underline{
    a\_{Bx} = \dot v\_{Bx} = - \frac{75cos(t)+25\sqrt{3}sin(t)}{4}-\frac{l\*fprime-f\*lprime}{l^2}
}}$$
$$\underline{\underline{
        a\_{By} = \dot v\_{By} = \frac{\dot v\_{Bx}}{\sqrt{3}}
    }}$$
Accelerations of point C is easier, because I already calculated
neccessery derivatives:
$$\underline{\underline{
        a\_{Cx} = \dot v\_{Cx} = \frac{\dot v\_{Bx} - 75 cos(t)}{4}
    }}$$
$$\underline{\underline{
        a\_{Cy} = \dot v\_{Cy} = \frac{\dot v\_{By} - 75 sin(t)}{4}
    }}$$
To find $\overrightarrow{a\_{\tau}}$ I calculated its length:
$$\underline{\underline{
    a\_{\tau} = \frac{\overrightarrow{a}{\overrightarrow{V}}}{{\|\overrightarrow{V}\|}} = \frac{a\_{Cx}\*v\_{Cx} + a\_{Cy}\*v\_{Cy}}{\sqrt{v^2\_{Cx} + v^2\_{Cy}}} 
    }}$$
and it is parallel with *v*<sub>*C*</sub>.  
$\overrightarrow{a_n}$ is perpendicular to the
$\overrightarrow{a\_{\tau}}$ and can be found by:
$$\underline{\underline{
    \overrightarrow{a_n} = \overrightarrow{a} - \overrightarrow{a\_{\tau}}
    }}$$

# Task 3

## Problem:

The mechanism consists of stepped wheels 1, 2, 3, which are in contact
and connected by a belt drive, a rack 4 and a weight 5, tied to the end
of a thread, wound on one of the wheels.  
The radii of steps of wheels are equal accordingly: at wheel 1 -
*r*<sub>1</sub> = 2 cm, *R*<sub>1</sub> = 4 cm, at wheel 2 -
*r*<sub>2</sub> = 6 cm, *R*<sub>2</sub> = 8 cm, at wheel 3 -
*r*<sub>3</sub> = 12 cm, *R*<sub>3</sub> = 16 cm. Points A, B and C are
located on the rims of the wheels.  
The law of motion of the load is given:
*s*<sub>5</sub> = *t*<sup>3</sup> − 6*t* (cm).  
The positive direction is downward.  
Find (*t* = 2):  
1. velocities of A,C;  
2. angular acc of 3;  
3. acc of B and 4;  

## Solution:

(1)  
$$\begin{split}
            & V_C = \omega_3 \* R_3; \\\\
            & V\_{s_5} = \dot s_5  = \omega_3 \* r_3; \\\\
            &
            \underline{\underline{
             V_C = \dot s_5 \frac{R_3}{r_3} = (3t^2 - 6) \frac{16}{12} = 8;
            }}
    \end{split}$$
Same logic with A:
$$\begin{split}
            & V_B = V_C \frac{R_2}{r_2}; \\\\
            & 
            \underline{\underline{
            V_A = V_C \frac{R_2}{r_2} \frac{R_1}{r_1} = \frac{64}{3} 
            }}
    \end{split}$$
(2)
$$\underline{\underline{
    \epsilon_3 = \dot \omega_3 = \frac{\ddot s_5}{r_3} = \frac{6t}{12} = 1;
}}$$
(3) I consider the point B
$$\begin{split}
            & V_B = \dot s_5\frac{R_3}{r_3} \frac{R_2}{r_2}; \\\\
            & a_n = \frac{V^2_B}{R_2} = \frac{128}{9};\\\\
            & \epsilon_B = \dot \omega_B = \frac{V_B}{R_2} = \ddot s_5\frac{R_3}{r_2 r_3}; \\\\
            & a\_{\tau} = \epsilon_B R_2 = \ddot s_5\frac{R_2 R_3}{r_2 r_3} = \frac{64}{3};\\\\
            &
            \underline{\underline{
            a = \sqrt{a^2_n + a^2\_{\tau}} \approx 25.64;
            }}
    \end{split}$$
Here I consider 4:
$$\begin{split}
            & a_4 = \epsilon_A R_1;\\\\
            & \epsilon_A = \dot \omega_A = \frac{\dot V_B}{r_1} = \ddot s_5 \frac{R_3 R_2}{r_1 r_2 r_3};\\\\
            &
            \underline{\underline{
            a_4 = \ddot s_5 \frac{R_3 R_2 R_1}{r_1 r_2 r_3} \approx 42.67;
            }}
    \end{split}$$
