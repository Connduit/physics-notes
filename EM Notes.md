# Graduate Electromagnetics — Foundations Study Guide

## From Basic Math → Fields → Maxwell's Equations → Electromagnetic Waves

> **Markdown compatibility note:** This version intentionally avoids `\boxed{}`. Equations use standard LaTeX math delimiters (`$...$` and `$$...$$`) and consistent vector notation such as `\mathbf{E}` and `\hat{\mathbf{x}}`.

---

# 1. The Big Picture

Electromagnetics becomes much easier when you understand the hierarchy:

```text
Math
 ↓
Vectors and calculus
 ↓
Fields
 ↓
Electric and magnetic quantities
 ↓
Maxwell's equations
 ↓
Electromagnetic waves
 ↓
Transmission, radiation, antennas, propagation, etc.
```

The central idea is:

> **Electric and magnetic fields exist in space and time, and Maxwell's equations describe how they are related to charge, current, and each other.**

A lot of graduate electromagnetics is learning different mathematical ways of asking:

* Where is charge?
* Where does a field point?
* How much field passes through a surface?
* Is a field spreading out?
* Is a field circulating?
* How do electric and magnetic fields change with time?
* How do fields propagate through space?

---

# 2. Scalars and Vectors

## Scalar

A **scalar** has magnitude only.

Examples:

* Temperature
* Mass
* Time
* Electric potential
* Charge density
* Frequency

Example:

$$
V = 5\text{ V}
$$

Here, $V$ is a scalar.

---

## Vector

A **vector** has:

1. Magnitude
2. Direction

Example:

$$
\mathbf{A}
$$

A vector in Cartesian coordinates can be written:

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

Where:

* $\mathbf{A}$ = vector
* $A_x$ = x-component
* $A_y$ = y-component
* $A_z$ = z-component
* $\hat{\mathbf{x}}$ = unit vector in the x-direction
* $\hat{\mathbf{y}}$ = unit vector in the y-direction
* $\hat{\mathbf{z}}$ = unit vector in the z-direction

The components $A_x$, $A_y$, and $A_z$ are scalars.

---

# 3. Unit Vectors

A **unit vector** has magnitude 1.

The Cartesian unit vectors are:

$$
\hat{\mathbf{x}},\qquad
\hat{\mathbf{y}},\qquad
\hat{\mathbf{z}}
$$

They point in the x, y, and z directions.

For any vector $\mathbf{A}$:

$$
\hat{\mathbf{A}}
=
\frac{\mathbf{A}}{|\mathbf{A}|}
$$

Where:

* $\hat{\mathbf{A}}$ = unit vector pointing in the direction of $\mathbf{A}$
* $\mathbf{A}$ = original vector
* $|\mathbf{A}|$ = magnitude of $\mathbf{A}$

---

# 4. Vector Magnitude

For:

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

the magnitude is:

$$
|\mathbf{A}|
=
\sqrt{
A_x^2+
A_y^2+
A_z^2
}
$$

This is just the 3D version of the Pythagorean theorem.

---

# 5. Dot Product

The dot product produces a **scalar**.

$$
\mathbf{A}\cdot\mathbf{B}
=
|\mathbf{A}|
|\mathbf{B}|
\cos\theta
$$

Where:

* $\mathbf{A}$ = first vector
* $\mathbf{B}$ = second vector
* $|\mathbf{A}|$ = magnitude of $\mathbf{A}$
* $|\mathbf{B}|$ = magnitude of $\mathbf{B}$
* $\theta$ = angle between the vectors
* $\cos\theta$ = determines how much the vectors point in the same direction

### Intuition

The dot product asks:

> **How much of one vector points in the direction of the other?**

If the vectors are parallel:

$$
\theta=0^\circ
$$

so:

$$
\cos(0^\circ)=1
$$

and the dot product is maximum.

If they are perpendicular:

$$
\theta=90^\circ
$$

so:

$$
\cos(90^\circ)=0
$$

and:

$$
\mathbf{A}\cdot\mathbf{B}=0
$$

---

# 6. Cross Product

The cross product produces a **vector**.

$$
\mathbf{A}\times\mathbf{B}
=
|\mathbf{A}|
|\mathbf{B}|
\sin\theta
\hat{\mathbf{n}}
$$

Where:

* $\mathbf{A}$ = first vector
* $\mathbf{B}$ = second vector
* $\theta$ = angle between the vectors
* $\hat{\mathbf{n}}$ = unit vector perpendicular to both $\mathbf{A}$ and $\mathbf{B}$

### Intuition

The cross product asks:

> **How strongly are these two vectors oriented perpendicular to each other, and what direction does that perpendicular point?**

Maximum occurs when:

$$
\theta=90^\circ
$$

because:

$$
\sin(90^\circ)=1
$$

Zero occurs when the vectors are parallel:

$$
\sin(0^\circ)=0
$$

---

# 7. Scalar Fields and Vector Fields

A **scalar field** assigns a scalar value to every point in space.

Example:

$$
V(x,y,z)
$$

Electric potential can vary from one location to another.

A **vector field** assigns a vector to every point in space.

Example:

$$
\mathbf{E}(x,y,z)
$$

The electric field can have a different magnitude and direction at every point.

Think of a field as:

> **A value attached to every location in space.**

---

# 8. Partial Derivatives

A partial derivative measures how something changes with respect to one variable while treating the others as constant.

Example:

$$
\frac{\partial V}{\partial x}
$$

means:

> How quickly does $V$ change as I move in the x-direction?

Similarly:

$$
\frac{\partial V}{\partial y}
$$

asks how $V$ changes moving in the y-direction.

And:

$$
\frac{\partial V}{\partial z}
$$

asks how $V$ changes moving in the z-direction.

---

# 9. The Nabla Operator

The symbol:

$$
\nabla
$$

is called **nabla** or **del**.

In Cartesian coordinates:

$$
\nabla
=
\hat{\mathbf{x}}\frac{\partial}{\partial x}
+
\hat{\mathbf{y}}\frac{\partial}{\partial y}
+
\hat{\mathbf{z}}\frac{\partial}{\partial z}
$$

It is an operator.

It is not itself a normal scalar or vector quantity.

It performs spatial derivatives.

Depending on how it is used, it gives us:

* Gradient
* Divergence
* Curl
* Laplacian

---

# 10. Gradient

The gradient operates on a scalar field and produces a vector.

For electric potential $V$:

$$
\nabla V
=
\frac{\partial V}{\partial x}\hat{\mathbf{x}}
+
\frac{\partial V}{\partial y}\hat{\mathbf{y}}
+
\frac{\partial V}{\partial z}\hat{\mathbf{z}}
$$

Where:

* $V$ = scalar field
* $\nabla V$ = gradient of $V$
* $\frac{\partial V}{\partial x}$ = rate of change of $V$ in x
* $\frac{\partial V}{\partial y}$ = rate of change of $V$ in y
* $\frac{\partial V}{\partial z}$ = rate of change of $V$ in z

### Intuition

The gradient tells you:

> **Which direction does the scalar field increase most rapidly, and how rapidly does it increase?**

The gradient points toward increasing values.

---

# 11. Divergence

Divergence operates on a vector field and produces a scalar.

For:

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

the divergence is:

$$
\nabla\cdot\mathbf{A}
=
\frac{\partial A_x}{\partial x}
+
\frac{\partial A_y}{\partial y}
+
\frac{\partial A_z}{\partial z}
$$

Where:

* $\mathbf{A}$ = vector field
* $A_x,A_y,A_z$ = components of $\mathbf{A}$
* $\nabla\cdot\mathbf{A}$ = divergence of $\mathbf{A}$

### Intuition

Divergence asks:

> **Is this vector field spreading out from this point or flowing into this point?**

Positive divergence:

```text
      ↑
      |
←-----•-----→
      |
      ↓
```

The point behaves like a source.

Negative divergence:

```text
      ↓
      |
→-----•-----←
      |
      ↑
```

The point behaves like a sink.

---

# 12. Curl

Curl operates on a vector field and produces a vector.

$$
\nabla\times\mathbf{A}
$$

### Intuition

Curl asks:

> **Does this vector field locally circulate around this point?**

Imagine putting a tiny paddle wheel into the field.

If the paddle wheel rotates, the field has curl.

In Cartesian coordinates:

$$
\nabla\times\mathbf{A}
=
\begin{vmatrix}
\hat{\mathbf{x}} & \hat{\mathbf{y}} & \hat{\mathbf{z}}\\
\frac{\partial}{\partial x} &
\frac{\partial}{\partial y} &
\frac{\partial}{\partial z}\\
A_x&A_y&A_z
\end{vmatrix}
$$

which gives:

$$
\nabla\times\mathbf{A}
=
\left(
\frac{\partial A_z}{\partial y}
-
\frac{\partial A_y}{\partial z}
\right)\hat{\mathbf{x}}
$$

$$
+
\left(
\frac{\partial A_x}{\partial z}
-
\frac{\partial A_z}{\partial x}
\right)\hat{\mathbf{y}}
$$

$$
+
\left(
\frac{\partial A_y}{\partial x}
-
\frac{\partial A_x}{\partial y}
\right)\hat{\mathbf{z}}
$$

---

# 13. Laplacian

The Laplacian of a scalar field is:

$$
\nabla^2V
=
\nabla\cdot(\nabla V)
$$

In Cartesian coordinates:

$$
\nabla^2V
=
\frac{\partial^2V}{\partial x^2}
+
\frac{\partial^2V}{\partial y^2}
+
\frac{\partial^2V}{\partial z^2}
$$

The Laplacian tells you about the local curvature of a scalar field.

---

# 14. Integrals

An integral essentially means:

> **Add up infinitely many tiny pieces.**

For example:

$$
Q=\int_V\rho\,dv
$$

means:

> Add up all the tiny pieces of charge inside a volume.

---

# 15. Differential Displacement

A tiny displacement in Cartesian coordinates is:

$$
d\mathbf{l}
=
dx\hat{\mathbf{x}}
+
dy\hat{\mathbf{y}}
+
dz\hat{\mathbf{z}}
$$

Where:

* $d\mathbf{l}$ = tiny vector displacement
* $dx$ = tiny displacement in x
* $dy$ = tiny displacement in y
* $dz$ = tiny displacement in z

---

# 16. Differential Surface Area

A tiny surface element can be represented as:

$$
d\mathbf{S}
=
\hat{\mathbf{n}}\,dS
$$

Where:

* $d\mathbf{S}$ = vector differential surface area
* $\hat{\mathbf{n}}$ = unit vector normal to the surface
* $dS$ = scalar differential area

The direction of $d\mathbf{S}$ is perpendicular to the surface.

---

# 17. Closed Integrals

A line integral around a closed path is written:

$$
\oint_C
$$

The circle on the integral means:

> The path is closed.

A surface integral over a closed surface is written:

$$
\oiint_S
$$

---

# 18. Flux

Flux is a measure of:

> **How much of a field passes through a surface.**

For a uniform field:

$$
\Phi
=
EA\cos\theta
$$

Where:

* $\Phi$ = flux
* $E$ = magnitude of the field
* $A$ = surface area
* $\theta$ = angle between the field and the surface normal

The general electric-field flux is:

$$
\Phi_E
=
\int_S
\mathbf{E}\cdot d\mathbf{S}
$$

The dot product is important.

It means only the component of $\mathbf{E}$ perpendicular to the surface contributes to flux.

---

# 19. Charge

Electric charge is measured in coulombs.

Symbol:

$$
Q
$$

A tiny amount of charge is:

$$
dQ
$$

Total charge can be found by integrating charge density:

$$
Q
=
\int_V\rho\,dv
$$

---

# 20. Charge Density

Charge can be distributed through space.

### Volume charge density

$$
\rho
=
\frac{dQ}{dv}
$$

Units:

$$
\text{C/m}^3
$$

### Surface charge density

$$
\sigma
=
\frac{dQ}{dS}
$$

Units:

$$
\text{C/m}^2
$$

### Line charge density

$$
\lambda
=
\frac{dQ}{dl}
$$

Units:

$$
\text{C/m}
$$

Be careful:

$\lambda$ can also represent wavelength, depending on context.

---

# 21. Electric Potential

Electric potential is represented by:

$$
V
$$

and measured in volts.

It is a scalar.

A useful intuition is:

> **Electric potential is like electrical potential energy per unit charge.**

Electric field is related to potential by:

$$
\mathbf{E}
=
-\nabla V
$$

The negative sign means:

> The electric field points toward decreasing electric potential.

---

# 22. Electric Field

The electric field is:

$$
\mathbf{E}
$$

Units:

$$
\text{V/m}
$$

or equivalently:

$$
\text{N/C}
$$

Electric field is a vector.

It tells you:

> **What force would a positive test charge experience per unit charge?**

The fundamental relationship is:

$$
\mathbf{E}
=
\frac{\mathbf{F}}{q}
$$

Where:

* $\mathbf{E}$ = electric field
* $\mathbf{F}$ = electric force
* $q$ = test charge

---

# 23. Permittivity

Permittivity is represented by:

$$
\epsilon
$$

It describes how a material responds to an electric field.

The fundamental relationship is:

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

Where:

* $\mathbf{D}$ = electric flux density
* $\epsilon$ = permittivity
* $\mathbf{E}$ = electric field

For a linear isotropic material:

$$
\epsilon
=
\epsilon_r\epsilon_0
$$

Where:

* $\epsilon$ = material permittivity
* $\epsilon_r$ = relative permittivity
* $\epsilon_0$ = permittivity of free space

---

# 24. Dielectrics

A dielectric is an electrically insulating material that can become polarized by an electric field.

Examples:

* Glass
* Plastic
* Ceramic
* Air

The electric field can cause positive and negative charges inside atoms or molecules to shift slightly.

This creates polarization.

The material response is represented through permittivity.

---

# 25. Electric Flux Density

Electric flux density is:

$$
\mathbf{D}
$$

with units:

$$
\text{C/m}^2
$$

For a linear isotropic material:

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

Think of the distinction as:

```text
E → electric field
D → electric flux density
```

They are related, but they are not the same quantity.

---

# 26. Magnetic Flux Density vs Magnetic Field Intensity

There are two important magnetic quantities:

$$
\mathbf{B}
$$

and

$$
\mathbf{H}
$$

They are related by:

$$
\mathbf{B}
=
\mu\mathbf{H}
$$

Where:

* $\mathbf{B}$ = magnetic flux density
* $\mathbf{H}$ = magnetic field intensity
* $\mu$ = permeability

Units:

$$
\mathbf{B}: \text{tesla}
$$

$$
\mathbf{H}: \text{A/m}
$$

For a linear material:

$$
\mu
=
\mu_r\mu_0
$$

---

# 27. Current Density

Current density is:

$$
\mathbf{J}
$$

Units:

$$
\text{A/m}^2
$$

It tells you how much electric current is flowing through a given area.

For a simple conductor:

$$
\mathbf{J}
=
\sigma\mathbf{E}
$$

Where:

* $\mathbf{J}$ = current density
* $\sigma$ = electrical conductivity
* $\mathbf{E}$ = electric field

---

# 28. The Three Important Constitutive Relations

These three relationships connect fields to material properties:

### Electric

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

### Magnetic

$$
\mathbf{B}
=
\mu\mathbf{H}
$$

### Conductive current

$$
\mathbf{J}
=
\sigma\mathbf{E}
$$

Memorize these.

They are fundamental.

---

# 29. Maxwell's Four Equations

These are the core equations of classical electromagnetics.

## Gauss's Law for Electricity

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

Where:

* $\nabla$ = spatial derivative operator
* $\mathbf{D}$ = electric flux density
* $\rho$ = volume charge density

### Meaning

> Electric charge acts as a source or sink of electric flux.

---

## Gauss's Law for Magnetism

$$
\nabla\cdot\mathbf{B}
=
0
$$

Where:

* $\mathbf{B}$ = magnetic flux density

### Meaning

There are no isolated magnetic monopoles in classical electromagnetics.

Magnetic field lines form closed loops.

---

## Faraday's Law

$$
\nabla\times\mathbf{E}
=
-\frac{\partial\mathbf{B}}{\partial t}
$$

Where:

* $\mathbf{E}$ = electric field
* $\mathbf{B}$ = magnetic flux density
* $t$ = time
* $\nabla\times$ = curl

### Meaning

> A changing magnetic field produces a circulating electric field.

This is the principle behind electromagnetic induction.

---

## Ampère-Maxwell Law

$$
\nabla\times\mathbf{H}
=
\mathbf{J}
+
\frac{\partial\mathbf{D}}{\partial t}
$$

Where:

* $\mathbf{H}$ = magnetic field intensity
* $\mathbf{J}$ = conduction current density
* $\mathbf{D}$ = electric flux density
* $t$ = time

The two terms on the right are important:

$$
\mathbf{J}
$$

and

$$
\frac{\partial\mathbf{D}}{\partial t}
$$

The first is ordinary conduction current.

The second is the **displacement current density**.

### Meaning

> Electric current and changing electric fields produce circulating magnetic fields.

---

# 30. Maxwell's Equations — Physical Picture

You can remember them conceptually:

```text
Charge
  ↓
Electric field divergence

No magnetic monopoles
  ↓
Magnetic field has zero divergence

Changing magnetic field
  ↓
Electric field curl

Current + changing electric field
  ↓
Magnetic field curl
```

The last two equations are especially important for electromagnetic waves.

---

# 31. Poisson's Equation

Start with:

$$
\mathbf{E}
=
-\nabla V
$$

and:

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

Therefore:

$$
\mathbf{D}
=
-\epsilon\nabla V
$$

Gauss's law says:

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

Substitute:

$$
\nabla\cdot(-\epsilon\nabla V)
=
\rho
$$

For constant $\epsilon$:

$$
-\epsilon\nabla^2V
=
\rho
$$

Therefore:

$$
\nabla^2V
=
-\frac{\rho}{\epsilon}
$$

This is **Poisson's equation**.

---

# 32. Laplace's Equation

If there is no charge in the region:

$$
\rho=0
$$

Poisson's equation becomes:

$$
\nabla^2V
=
0
$$

This is **Laplace's equation**.

So:

```text
Charge present
    ↓
Poisson's equation

No charge
    ↓
Laplace's equation
```

---

# 33. Boundary Conditions

Electromagnetic problems often involve different materials meeting at a boundary.

For example:

```text
Material 1
----------------
       boundary
----------------
Material 2
```

The fields must satisfy specific boundary conditions.

For the normal component of $\mathbf{D}$:

$$
\hat{\mathbf{n}}
\cdot
(\mathbf{D}_2-\mathbf{D}_1)
=
\rho_s
$$

Where:

* $\hat{\mathbf{n}}$ = unit normal vector pointing from region 1 to region 2
* $\mathbf{D}_1$ = electric flux density on side 1
* $\mathbf{D}_2$ = electric flux density on side 2
* $\rho_s$ = surface charge density

For tangential electric field:

$$
\hat{\mathbf{n}}
\times
(\mathbf{E}_2-\mathbf{E}_1)
=
0
$$

These become very important when solving interfaces between materials.

---

# 34. Electromagnetic Waves

An electromagnetic wave consists of coupled electric and magnetic fields.

For a simple plane wave traveling in the +z direction:

$$
\mathbf{E}
=
\hat{\mathbf{x}}
E_0
\cos(\omega t-kz)
$$

Where:

* $\mathbf{E}$ = electric field
* $\hat{\mathbf{x}}$ = unit vector in x-direction
* $E_0$ = electric-field amplitude
* $\omega$ = angular frequency
* $t$ = time
* $k$ = wavenumber
* $z$ = position in the propagation direction

The electric field points in x.

The wave travels in z.

The magnetic field therefore points in y.

Conceptually:

```text
        E
        ↑ x
        |
        |
--------+--------→ z
       wave
        |
        |
        B → y
```

The three directions are mutually perpendicular.

---

# 35. Frequency, Period, and Angular Frequency

Frequency:

$$
f
$$

Units:

$$
\text{Hz}
$$

Frequency means cycles per second.

Period:

$$
T
=
\frac{1}{f}
$$

Where:

* $T$ = period in seconds
* $f$ = frequency in hertz

Angular frequency:

$$
\omega
=
2\pi f
$$

Where:

* $\omega$ = angular frequency in rad/s
* $f$ = frequency in Hz

---

# 36. Wavelength and Wavenumber

Wavelength:

$$
\lambda
$$

is the physical distance corresponding to one complete cycle.

Wavenumber:

$$
k
=
\frac{2\pi}{\lambda}
$$

Where:

* $k$ = wavenumber in rad/m
* $\lambda$ = wavelength in meters

---

# 37. Wave Velocity

Wave velocity is:

$$
v
=
f\lambda
$$

Using:

$$
\omega=2\pi f
$$

and:

$$
k=\frac{2\pi}{\lambda}
$$

we can also write:

$$
v
=
\frac{\omega}{k}
$$

---

# 38. Electromagnetic Wave Velocity

In a material:

$$
v
=
\frac{1}{\sqrt{\mu\epsilon}}
$$

Where:

* $v$ = electromagnetic wave velocity
* $\mu$ = permeability
* $\epsilon$ = permittivity

In free space:

$$
c
=
\frac{1}{\sqrt{\mu_0\epsilon_0}}
$$

Where:

* $c$ = speed of light
* $\mu_0$ = permeability of free space
* $\epsilon_0$ = permittivity of free space

Therefore:

> Light is an electromagnetic wave.

---

# 39. Intrinsic Impedance

The intrinsic impedance of a medium is:

$$
\eta
=
\sqrt{\frac{\mu}{\epsilon}}
$$

Where:

* $\eta$ = intrinsic impedance
* $\mu$ = permeability
* $\epsilon$ = permittivity

For a plane wave:

$$
\frac{E}{H}
=
\eta
$$

Where:

* $E$ = electric-field magnitude
* $H$ = magnetic-field magnitude

In free space:

$$
\eta_0
\approx
377\ \Omega
$$

---

# 40. Poynting Vector

The Poynting vector describes electromagnetic energy flow.

$$
\mathbf{S}
=
\mathbf{E}
\times
\mathbf{H}
$$

Where:

* $\mathbf{S}$ = Poynting vector
* $\mathbf{E}$ = electric field
* $\mathbf{H}$ = magnetic field intensity

Units:

$$
\text{W/m}^2
$$

The direction of $\mathbf{S}$ gives the direction electromagnetic energy is flowing.

For a plane wave:

```text
E × H → direction of propagation
```

---

# 41. Complex Numbers

Electrical engineering frequently uses:

$$
j=\sqrt{-1}
$$

where $j$ is the imaginary unit.

Euler's identity:

$$
e^{j\theta}
=
\cos\theta
+
j\sin\theta
$$

This lets us represent sinusoidal signals using complex exponentials.

---

# 42. Phasors

Suppose:

$$
E(t)
=
E_0\cos(\omega t+\phi)
$$

Where:

* $E(t)$ = time-domain electric field
* $E_0$ = amplitude
* $\omega$ = angular frequency
* $t$ = time
* $\phi$ = phase

We can represent the sinusoid with a phasor:

$$
\tilde{E}
=
E_0e^{j\phi}
$$

The time dependence $e^{j\omega t}$ is understood.

This makes differentiation much easier.

For example:

$$
\frac{\partial}{\partial t}
\rightarrow
j\omega
$$

So:

$$
\frac{\partial E}{\partial t}
\rightarrow
j\omega\tilde{E}
$$

This is one reason phasors are so useful.

---

# 43. Fourier Transform

The Fourier transform converts a signal from the time domain into the frequency domain.

The continuous Fourier transform is:

$$
X(f)
=
\int_{-\infty}^{\infty}
x(t)e^{-j2\pi ft}\,dt
$$

Where:

* $x(t)$ = time-domain signal
* $X(f)$ = frequency-domain representation
* $f$ = frequency
* $t$ = time
* $j$ = imaginary unit

Conceptually:

```text
Time domain
     |
     | Fourier Transform
     ↓
Frequency domain
```

Instead of asking:

> What is the signal doing over time?

you can ask:

> What frequencies make up the signal?

---

# 44. DFT vs FFT

The **DFT** is the mathematical operation.

For $N$ samples:

$$
X[k]
=
\sum_{n=0}^{N-1}
x[n]
e^{-j2\pi kn/N}
$$

Where:

* $x[n]$ = input sample number $n$
* $X[k]$ = frequency bin $k$
* $N$ = number of samples
* $n$ = time-domain sample index
* $k$ = frequency-bin index

The **FFT** is an efficient algorithm for computing the DFT.

Important:

> FFT is not a different transform from the DFT.

It is a faster way of calculating the DFT.

---

# 45. Sampling

When converting an analog signal into digital samples, the sampling frequency must be sufficiently high.

The Nyquist condition is:

$$
f_s
>
2f_{\max}
$$

Where:

* $f_s$ = sampling frequency
* $f_{\max}$ = highest frequency contained in the signal

If this condition is violated, **aliasing** can occur.

Conceptually:

```text
Analog signal
     ↓
Sampling
     ↓
Digital samples
```

If you sample too slowly, different frequencies can become indistinguishable.

---

# 46. Convolution

Convolution is fundamental to signal processing and filtering.

$$
y(t)
=
x(t)*h(t)
$$

Where:

* $x(t)$ = input signal
* $h(t)$ = impulse response of the system/filter
* $y(t)$ = output signal
* $*$ = convolution

In the frequency domain:

$$
Y(f)
=
X(f)H(f)
$$

This is extremely important:

> **Convolution in time corresponds to multiplication in frequency.**

This is why filters are often easier to understand in the frequency domain.

---

# 47. Divergence Theorem

The divergence theorem connects a volume integral with a closed-surface integral.

$$
\iiint_V
\nabla\cdot\mathbf{A}\,dv
=
\oiint_S
\mathbf{A}\cdot d\mathbf{S}
$$

Where:

* $V$ = volume
* $S$ = closed surface surrounding the volume
* $\mathbf{A}$ = vector field
* $\nabla\cdot\mathbf{A}$ = divergence
* $dv$ = differential volume
* $d\mathbf{S}$ = differential surface-area vector

### Intuition

It says:

> Total amount of "source behavior" inside a volume equals total outward flux through its boundary.

This is directly connected to Gauss's law.

---

# 48. Stokes' Theorem

Stokes' theorem connects surface curl to circulation around the boundary.

$$
\iint_S
(\nabla\times\mathbf{A})
\cdot d\mathbf{S}
=
\oint_C
\mathbf{A}\cdot d\mathbf{l}
$$

Where:

* $S$ = surface
* $C$ = closed boundary of the surface
* $\mathbf{A}$ = vector field
* $\nabla\times\mathbf{A}$ = curl
* $d\mathbf{S}$ = differential surface vector
* $d\mathbf{l}$ = differential line vector

### Intuition

It says:

> Total curl through a surface equals the circulation around the boundary.

This is directly connected to Faraday's law and Ampère's law.

---

# 49. Differential Equations

A differential equation contains derivatives.

For example:

$$
\frac{dV}{dx}
=
2x
$$

The unknown is $V(x)$.

The equation tells us how $V$ changes.

Electromagnetics contains many differential equations because fields vary through space and time.

Maxwell's equations are differential equations.

---

# 50. Separation of Variables

A common technique for solving electromagnetic boundary-value problems is separation of variables.

Suppose:

$$
V=V(x,y)
$$

We might assume:

$$
V(x,y)
=
X(x)Y(y)
$$

Where:

* $V(x,y)$ = unknown scalar field
* $X(x)$ = function of x only
* $Y(y)$ = function of y only

This can turn one difficult partial differential equation into multiple simpler ordinary differential equations.

---

# 51. Master Equation Sheet

## Vector math

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

$$
|\mathbf{A}|
=
\sqrt{
A_x^2+A_y^2+A_z^2
}
$$

$$
\mathbf{A}\cdot\mathbf{B}
=
|\mathbf{A}||\mathbf{B}|\cos\theta
$$

$$
\mathbf{A}\times\mathbf{B}
=
|\mathbf{A}||\mathbf{B}|\sin\theta
\hat{\mathbf{n}}
$$

---

## Vector calculus

$$
\nabla
=
\hat{\mathbf{x}}\frac{\partial}{\partial x}
+
\hat{\mathbf{y}}\frac{\partial}{\partial y}
+
\hat{\mathbf{z}}\frac{\partial}{\partial z}
$$

$$
\nabla V
=
\frac{\partial V}{\partial x}\hat{\mathbf{x}}
+
\frac{\partial V}{\partial y}\hat{\mathbf{y}}
+
\frac{\partial V}{\partial z}\hat{\mathbf{z}}
$$

$$
\nabla\cdot\mathbf{A}
=
\frac{\partial A_x}{\partial x}
+
\frac{\partial A_y}{\partial y}
+
\frac{\partial A_z}{\partial z}
$$

$$
\nabla\times\mathbf{A}
$$

$$
\nabla^2V
=
\nabla\cdot(\nabla V)
$$

---

## Electromagnetics

$$
\mathbf{E}
=
-\nabla V
$$

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

$$
\mathbf{B}
=
\mu\mathbf{H}
$$

$$
\mathbf{J}
=
\sigma\mathbf{E}
$$

---

## Maxwell

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

$$
\nabla\cdot\mathbf{B}
=
0
$$

$$
\nabla\times\mathbf{E}
=
-\frac{\partial\mathbf{B}}{\partial t}
$$

$$
\nabla\times\mathbf{H}
=
\mathbf{J}
+
\frac{\partial\mathbf{D}}{\partial t}
$$

---

## Electrostatics

$$
\mathbf{E}
=
-\nabla V
$$

$$
\nabla^2V
=
-\frac{\rho}{\epsilon}
$$

$$
\nabla^2V
=
0
\qquad
(\rho=0)
$$

---

## Waves

$$
T
=
\frac{1}{f}
$$

$$
\omega
=
2\pi f
$$

$$
k
=
\frac{2\pi}{\lambda}
$$

$$
v
=
f\lambda
$$

$$
v
=
\frac{\omega}{k}
$$

$$
v
=
\frac{1}{\sqrt{\mu\epsilon}}
$$

$$
\eta
=
\sqrt{\frac{\mu}{\epsilon}}
$$

$$
\frac{E}{H}
=
\eta
$$

$$
\mathbf{S}
=
\mathbf{E}\times\mathbf{H}
$$

---

## Signals

$$
e^{j\theta}
=
\cos\theta+j\sin\theta
$$

$$
\frac{\partial}{\partial t}
\rightarrow
j\omega
$$

$$
X(f)
=
\int_{-\infty}^{\infty}
x(t)e^{-j2\pi ft}\,dt
$$

$$
f_s>2f_{\max}
$$

$$
y(t)=x(t)*h(t)
$$

$$
Y(f)=X(f)H(f)
$$

---

# 52. Symbol Reference

| Symbol             | Meaning                                | Type / Units          |
| ------------------ | -------------------------------------- | --------------------- |
| $V$                | Electric potential                     | Scalar, V             |
| $\mathbf{E}$       | Electric field                         | Vector, V/m           |
| $\mathbf{D}$       | Electric flux density                  | Vector, C/m²          |
| $\mathbf{B}$       | Magnetic flux density                  | Vector, T             |
| $\mathbf{H}$       | Magnetic field intensity               | Vector, A/m           |
| $\mathbf{J}$       | Current density                        | Vector, A/m²          |
| $\rho$             | Volume charge density                  | Scalar, C/m³          |
| $\sigma$           | Surface charge density or conductivity | Context-dependent     |
| $\lambda$          | Line charge density or wavelength      | Context-dependent     |
| $Q,q$              | Electric charge                        | Scalar, C             |
| $\epsilon$         | Permittivity                           | F/m                   |
| $\mu$              | Permeability                           | H/m                   |
| $\Phi$             | Flux                                   | Scalar                |
| $d\mathbf{l}$      | Differential displacement              | Vector                |
| $d\mathbf{S}$      | Differential surface area              | Vector                |
| $\nabla$           | Nabla/del operator                     | Differential operator |
| $f$                | Frequency                              | Hz                    |
| $T$                | Period                                 | s                     |
| $\omega$           | Angular frequency                      | rad/s                 |
| $\lambda$          | Wavelength                             | m                     |
| $k$                | Wavenumber                             | rad/m                 |
| $\eta$             | Intrinsic impedance                    | $\Omega$              |
| $j$                | Imaginary unit                         | $\sqrt{-1}$           |
| $\mathbf{S}$       | Poynting vector                        | W/m²                  |
| $\hat{\mathbf{x}}$ | x-direction unit vector                | Unit vector           |
| $\hat{\mathbf{y}}$ | y-direction unit vector                | Unit vector           |
| $\hat{\mathbf{z}}$ | z-direction unit vector                | Unit vector           |
| $\hat{\mathbf{n}}$ | Surface-normal unit vector             | Unit vector           |

---

# 53. What to Memorize First

Do **not** try to memorize everything at once.

Use this order.

## Level 1 — Vector fundamentals

Know:

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

Know:

* Scalar vs vector
* Magnitude
* Unit vector
* Dot product
* Cross product

---

## Level 2 — Vector calculus

Know what these mean intuitively:

$$
\nabla V
$$

$$
\nabla\cdot\mathbf{A}
$$

$$
\nabla\times\mathbf{A}
$$

$$
\nabla^2V
$$

Memorize the meanings:

```text
Gradient   → direction of greatest increase
Divergence → spreading out / sources
Curl       → circulation / rotation
Laplacian  → spatial curvature
```

---

## Level 3 — EM quantities

Know these cold:

```text
V  = electric potential
E  = electric field
D  = electric flux density
B  = magnetic flux density
H  = magnetic field intensity
J  = current density
rho = volume charge density
```

---

## Level 4 — Constitutive relations

Memorize:

$$
\mathbf{D}=\epsilon\mathbf{E}
$$

$$
\mathbf{B}=\mu\mathbf{H}
$$

$$
\mathbf{J}=\sigma\mathbf{E}
$$

---

## Level 5 — Maxwell's equations

Memorize these four:

$$
\nabla\cdot\mathbf{D}=\rho
$$

$$
\nabla\cdot\mathbf{B}=0
$$

$$
\nabla\times\mathbf{E}
=
-\frac{\partial\mathbf{B}}{\partial t}
$$

$$
\nabla\times\mathbf{H}
=
\mathbf{J}
+
\frac{\partial\mathbf{D}}{\partial t}
$$

But more importantly, understand what each one means.

---

# 54. The Most Important Mental Map

This is one of the most useful chains for electrostatics:

```text
Electric potential
       V
       ↓
    gradient
       ↓
Electric field
       E
       ↓
  multiply by ε
       ↓
Electric flux density
       D
       ↓
    divergence
       ↓
Charge density
       ρ
```

Mathematically:

$$
V
\rightarrow
-\nabla V
\rightarrow
\mathbf{E}
\rightarrow
\epsilon\mathbf{E}
\rightarrow
\mathbf{D}
\rightarrow
\nabla\cdot\mathbf{D}
\rightarrow
\rho
$$

This produces:

$$
\mathbf{E}
=
-\nabla V
$$

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

Combining them gives:

$$
\nabla^2V
=
-\frac{\rho}{\epsilon}
$$

which is Poisson's equation.

If:

$$
\rho=0
$$

then:

$$
\nabla^2V=0
$$

which is Laplace's equation.

---

# 55. The Four Maxwell Equations as a Mental Map

Think of Maxwell's equations like this:

```text
                    CHARGE
                      ↓
             ∇ · D = ρ
                      |
                      |
                      ↓
                 ELECTRIC
                   FIELD
                      ↑
                      |
      changing B -----+
          |
          ↓
      curl E

CURRENT + changing E
          |
          ↓
      curl H
          |
          ↓
      MAGNETIC
       FIELD
          |
          |
          ↓
       ∇ · B = 0
```

The most important conceptual relationship for waves is:

```text
Changing magnetic field
          ↓
     creates E-field
          ↓
Changing electric field
          ↓
     creates H-field
          ↓
Changing magnetic field
          ↓
         ...
```

This mutual coupling allows an electromagnetic wave to propagate through space.

---

# 56. Three Questions to Ask for Every Equation

Whenever you encounter an equation in your graduate class, ask these three questions.

## Question 1 — What does every symbol mean?

For example:

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

Identify:

* $\nabla$ = spatial derivative operator
* $\cdot$ = dot product
* $\mathbf{D}$ = electric flux density
* $\rho$ = volume charge density

---

## Question 2 — What type of thing is each side?

For:

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

$\mathbf{D}$ is a vector.

Divergence turns a vector into a scalar.

Therefore:

$$
\nabla\cdot\mathbf{D}
$$

is a scalar.

And $\rho$ is also a scalar.

So the equation makes mathematical sense.

---

## Question 3 — What physical question is the equation answering?

For:

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

the physical meaning is:

> **Electric charge is the source of electric flux.**

That is much more useful than simply memorizing the equation.

---

# 57. Final Study Strategy

When learning graduate electromagnetics, avoid trying to memorize every equation immediately.

Instead, build the hierarchy:

```text
1. Scalars and vectors
          ↓
2. Dot and cross products
          ↓
3. Partial derivatives
          ↓
4. Gradient / divergence / curl
          ↓
5. Integrals and flux
          ↓
6. Electric and magnetic quantities
          ↓
7. Constitutive relations
          ↓
8. Maxwell's equations
          ↓
9. Electrostatic equations
          ↓
10. Boundary conditions
          ↓
11. Electromagnetic waves
          ↓
12. Phasors
          ↓
13. Fourier analysis
```

The goal is not:

> "I have memorized 50 equations."

The goal is:

> "I can look at an equation and understand what every symbol means, what mathematical operation is happening, what kind of quantity comes out, and what physical phenomenon the equation describes."

Once that becomes natural, the graduate-level material becomes substantially easier to follow.

---

# Quick Reference — The Stuff You Should Eventually Know Cold

$$
\mathbf{A}
=
A_x\hat{\mathbf{x}}
+
A_y\hat{\mathbf{y}}
+
A_z\hat{\mathbf{z}}
$$

$$
\nabla
=
\hat{\mathbf{x}}\frac{\partial}{\partial x}
+
\hat{\mathbf{y}}\frac{\partial}{\partial y}
+
\hat{\mathbf{z}}\frac{\partial}{\partial z}
$$

$$
\mathbf{E}
=
-\nabla V
$$

$$
\mathbf{D}
=
\epsilon\mathbf{E}
$$

$$
\mathbf{B}
=
\mu\mathbf{H}
$$

$$
\mathbf{J}
=
\sigma\mathbf{E}
$$

$$
\nabla\cdot\mathbf{D}
=
\rho
$$

$$
\nabla\cdot\mathbf{B}
=
0
$$

$$
\nabla\times\mathbf{E}
=
-\frac{\partial\mathbf{B}}{\partial t}
$$

$$
\nabla\times\mathbf{H}
=
\mathbf{J}
+
\frac{\partial\mathbf{D}}{\partial t}
$$

$$
\nabla^2V
=
-\frac{\rho}{\epsilon}
$$

$$
v
=
\frac{1}{\sqrt{\mu\epsilon}}
$$

$$
\eta
=
\sqrt{\frac{\mu}{\epsilon}}
$$

$$
\mathbf{S}
=
\mathbf{E}\times\mathbf{H}
$$

$$
\omega=2\pi f
$$

$$
k=\frac{2\pi}{\lambda}
$$

$$
v=f\lambda
$$

$$
v=\frac{\omega}{k}
$$

---

# One-Sentence Intuition for the Major Operators

| Expression                    | Think                                         |
| ----------------------------- | --------------------------------------------- |
| $\nabla V$                    | "Which way does $V$ increase?"                |
| $\nabla\cdot\mathbf{E}$       | "Is the field spreading out here?"            |
| $\nabla\times\mathbf{E}$      | "Is the field circulating here?"              |
| $\nabla^2V$                   | "How is $V$ curving here?"                    |
| $\mathbf{E}\cdot d\mathbf{S}$ | "How much field passes through this surface?" |
| $\mathbf{E}\times\mathbf{H}$  | "Which way is EM energy flowing?"             |

---

# Core Mental Model

If you remember nothing else initially, remember this:

```text
                    ELECTROMAGNETICS

                         Fields
                           |
             +-------------+-------------+
             |                           |
        Electric                     Magnetic
             |                           |
             E                           H
             |                           |
          D = εE                     B = μH
             |                           |
             +-------------+-------------+
                           |
                     Maxwell's
                      Equations
                           |
                           ↓
                Electromagnetic Waves
                           |
                           ↓
                Propagation / Radiation
```

And the two most important coupling relationships are:

$$
\nabla\times\mathbf{E}
=
-\frac{\partial\mathbf{B}}{\partial t}
$$

and

$$
\nabla\times\mathbf{H}
=
\mathbf{J}
+
\frac{\partial\mathbf{D}}{\partial t}
$$

These tell you that **changing electric and magnetic fields are coupled to one another**, which is ultimately what allows electromagnetic waves to exist.
