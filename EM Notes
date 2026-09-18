# Graduate Electromagnetics — Foundations Study Guide

## From Basic Math → Fields → Maxwell's Equations → Waves

### Purpose

This guide is organized as a learning path rather than a collection of disconnected formulas.

The goal is to understand:

- what each mathematical operation means
- what each electromagnetic quantity represents
- what every symbol in an equation means
- why equations are structured the way they are
- how the major topics connect

The overall progression is:

> **Fields → How fields change → Maxwell's equations → Electromagnetic waves**

For every equation, ask:

1. What does every symbol mean?
2. What type of quantity is each side?
3. What physical question is the equation answering?

---

# 1. The Big Picture

Electromagnetics can initially look like hundreds of unrelated equations.

It isn't.

Most of electromagnetics can be organized around a few ideas:

> **Fields → How fields change → Maxwell's equations → Electromagnetic waves**

A **field** tells you what quantity exists at every location in space.

Examples:

- Temperature field → temperature everywhere
- Electric potential field → voltage everywhere
- Electric field → electric force direction and magnitude everywhere
- Magnetic field → magnetic effects everywhere

---

# 2. Scalars and Vectors

## Scalar

A scalar is a single number.

Examples:

- `5`
- `-10`
- `120 V`

A scalar has magnitude but no direction.

## Vector

A vector has:

- magnitude
- direction

For example:

$$
\mathbf A = 3\hat{x} + 4\hat{y}
$$

This means:

- 3 units in the x direction
- 4 units in the y direction

Its magnitude is:

$$
|\mathbf A| = \sqrt{3^2+4^2}=5
$$

### Remember

$$
\boxed{\text{Scalar}=\text{number}}
$$

$$
\boxed{\text{Vector}=\text{magnitude + direction}}
$$

---

# 3. Unit Vectors

A unit vector has a magnitude of exactly 1.

$$
|\hat{\mathbf A}|=1
$$

The hat means **unit vector**.

For a vector $\mathbf A$:

$$
\boxed{\hat{\mathbf A}=\frac{\mathbf A}{|\mathbf A|}}
$$

A unit vector tells you **direction**, not magnitude.

Examples:

$$
\hat{x},\quad\hat{y},\quad\hat{z}
$$

These point in the x, y, and z directions.

---

# 4. Coordinate Systems

The simplest coordinate system is Cartesian:

$$
x,\quad y,\quad z
$$

with unit vectors:

$$
\hat{x},\quad\hat{y},\quad\hat{z}
$$

A vector can therefore be written:

$$
\boxed{
\mathbf A=A_x\hat{x}+A_y\hat{y}+A_z\hat{z}
}
$$

where:

- $A_x$ = x component
- $A_y$ = y component
- $A_z$ = z component

Later in EM you will also encounter:

- cylindrical coordinates
- spherical coordinates

These are especially useful when the geometry is circular or spherical.

---

# 5. Dot Product

The dot product tells you:

> **How much does one vector point in the direction of another?**

The equation is:

$$
\boxed{
\mathbf A\cdot\mathbf B
=
|\mathbf A||\mathbf B|\cos\theta
}
$$

where:

- $\mathbf A$ = first vector
- $\mathbf B$ = second vector
- $|\mathbf A|$ = magnitude of $\mathbf A$
- $|\mathbf B|$ = magnitude of $\mathbf B$
- $\theta$ = angle between them

The result is a **scalar**.

### Important cases

Same direction:

$$
\theta=0^\circ
$$

Maximum positive result.

Perpendicular:

$$
\theta=90^\circ
$$

$$
\mathbf A\cdot\mathbf B=0
$$

Opposite direction:

$$
\theta=180^\circ
$$

Negative result.

### Why EM cares

The dot product appears whenever we care about a component **through** something.

That is why it appears in flux.

---

# 6. Cross Product

The cross product creates a new vector perpendicular to the two original vectors.

$$
\boxed{
\mathbf A\times\mathbf B
=
|\mathbf A||\mathbf B|\sin\theta\,\hat{\mathbf n}
}
$$

where:

- $\hat{\mathbf n}$ = perpendicular unit vector
- $\theta$ = angle between the vectors

The direction is determined using the right-hand rule.

### Important cases

Parallel:

$$
\theta=0^\circ
$$

$$
\mathbf A\times\mathbf B=0
$$

Perpendicular:

$$
\theta=90^\circ
$$

Maximum magnitude.

### Why EM cares

Magnetic force:

$$
\boxed{
\mathbf F=q(\mathbf v\times\mathbf B)
}
$$

Electromagnetic energy flow:

$$
\boxed{
\mathbf S=\mathbf E\times\mathbf H
}
$$

---

# 7. Scalar Fields and Vector Fields

This distinction is extremely important.

## Scalar field

A scalar field gives one number at every point.

Example:

$$
V(x,y,z)
$$

Electric potential is a scalar field.

## Vector field

A vector field gives a vector at every point.

Example:

$$
\mathbf E(x,y,z)
$$

Electric field is a vector field.

### Memorize

$$
\boxed{V=\text{scalar field}}
$$

$$
\boxed{\mathbf E=\text{vector field}}
$$

---

# 8. Partial Derivatives

A derivative tells you how something changes.

For example:

$$
\frac{dV}{dx}
$$

means:

> How quickly does $V$ change as $x$ changes?

With several variables we use partial derivatives:

$$
\frac{\partial V}{\partial x}
$$

This means:

> How does $V$ change with respect to $x$?

The other variables are treated as constant while taking this derivative.

---

# 9. The Nabla Operator

The symbol

$$
\boxed{\nabla}
$$

is called **nabla**.

In Cartesian coordinates:

$$
\boxed{
\nabla=
\hat{x}\frac{\partial}{\partial x}
+
\hat{y}\frac{\partial}{\partial y}
+
\hat{z}\frac{\partial}{\partial z}
}
$$

It is an **operator**.

What it does depends on what you put after it.

For example:

$$
\nabla V
$$

does something different from:

$$
\nabla\cdot\mathbf A
$$

and:

$$
\nabla\times\mathbf A
$$

---

# 10. Gradient

The gradient takes a scalar field and produces a vector field.

$$
\boxed{
\nabla V=
\frac{\partial V}{\partial x}\hat{x}
+
\frac{\partial V}{\partial y}\hat{y}
+
\frac{\partial V}{\partial z}\hat{z}
}
$$

The gradient points in the direction where the scalar increases fastest.

### Type

$$
\boxed{
\text{scalar}\rightarrow\text{vector}
}
$$

### Example

If $V$ represents temperature, then:

$$
\nabla V
$$

points toward the direction in which temperature increases most rapidly.

---

# 11. Divergence

Divergence asks:

> **Is the vector field spreading outward or converging inward at this point?**

For:

$$
\mathbf A=A_x\hat{x}+A_y\hat{y}+A_z\hat{z}
$$

the divergence is:

$$
\boxed{
\nabla\cdot\mathbf A
=
\frac{\partial A_x}{\partial x}
+
\frac{\partial A_y}{\partial y}
+
\frac{\partial A_z}{\partial z}
}
$$

The result is a **scalar**.

### Type

$$
\boxed{
\text{vector}\rightarrow\text{scalar}
}
$$

### Intuition

Imagine a tiny balloon.

If the field pushes more stuff out of the balloon than into it:

> positive divergence

If more stuff enters than leaves:

> negative divergence

If the amount entering and leaving balances:

> zero divergence

In electromagnetics, divergence is closely related to **sources and sinks** of fields.

---

# 12. Curl

Curl asks:

> **Is the vector field circulating around this point?**

Written:

$$
\boxed{\nabla\times\mathbf A}
$$

The result is a vector.

### Type

$$
\boxed{
\text{vector}\rightarrow\text{vector}
}
$$

Curl is extremely important in Maxwell's equations.

### Intuition

Imagine placing a tiny paddle wheel in a flowing fluid.

- If the fluid tends to make the paddle wheel rotate → nonzero curl
- If it does not → zero curl

This is only an analogy, but it is useful for building intuition.

---

# 13. Laplacian

The Laplacian is:

$$
\boxed{
\nabla^2V=\nabla\cdot(\nabla V)
}
$$

Follow the types:

$$
V
\rightarrow
\nabla V
\rightarrow
\nabla\cdot\nabla V
$$

Therefore:

$$
\boxed{
\text{scalar}\rightarrow\text{vector}\rightarrow\text{scalar}
}
$$

In Cartesian coordinates:

$$
\boxed{
\nabla^2V=
\frac{\partial^2V}{\partial x^2}
+
\frac{\partial^2V}{\partial y^2}
+
\frac{\partial^2V}{\partial z^2}
}
$$

The Laplacian is closely related to the **spatial curvature** of a quantity.

---

# 14. Integrals

An integral is essentially:

> **Add up lots of tiny pieces.**

For example:

$$
Q=\int_V\rho\,dv
$$

means:

> Add up the charge contained in every tiny volume element.

where:

- $Q$ = total charge
- $\rho$ = volume charge density
- $dv$ = tiny volume element

---

# 15. $d\mathbf l$ and $d\mathbf S$

## $d\mathbf l$

A tiny vector displacement along a path.

$$
\boxed{
d\mathbf l=dx\hat{x}+dy\hat{y}+dz\hat{z}
}
$$

Think:

> Take a tiny step in this direction.

## $d\mathbf S$

A tiny vector area element.

Its direction is normally perpendicular to the surface.

Think:

> A tiny piece of surface, including which way the surface faces.

The direction of $d\mathbf S$ matters because of the dot product.

---

# 16. Closed Integrals

Normal integral:

$$
\int
$$

Closed integral:

$$
\boxed{\oint}
$$

The circle means the path or surface is closed.

For example:

$$
\oint_C\mathbf E\cdot d\mathbf l
$$

means:

> Integrate around a closed loop.

For a closed surface, you may see:

$$
\oiint_S
$$

---

# 17. Flux

Flux is one of the most important concepts to understand intuitively.

Flux means:

> **How much of a vector field passes through a surface.**

It is a mathematical measure. It is **not** literally a fluid flowing through the surface.

For a uniform field crossing a flat surface:

$$
\boxed{
\Phi=EA\cos\theta
}
$$

where:

- $\Phi$ = flux
- $E$ = field magnitude
- $A$ = surface area
- $\theta$ = angle between the field and the surface normal

The general form is:

$$
\boxed{
\Phi_E=\int_S\mathbf E\cdot d\mathbf S
}
$$

The dot product is important because we only care about the component going **through** the surface.

### Important distinction

Flux is **not** the same thing as reflection or refraction.

However, the material properties of a medium, especially its permittivity, affect how electromagnetic waves behave at boundaries. That can lead to reflection and refraction.

---

# 18. Charge

Electric charge is represented by:

$$
q
$$

or:

$$
Q
$$

depending on the author's notation.

Units:

$$
\boxed{\text{Coulombs (C)}}
$$

Often:

- $q$ = individual charge
- $Q$ = total charge

But this is a convention, not a universal rule.

---

# 19. Charge Density

Instead of asking:

> How much charge exists?

we can ask:

> How much charge exists per unit volume?

That's charge density.

The symbol is:

$$
\boxed{\rho}
$$

Greek letter **rho**.

## Volume charge density

$$
\boxed{
\rho=\frac{dQ}{dv}
}
$$

Units:

$$
\boxed{\text{C/m}^3}
$$

## Surface charge density

$$
\boxed{
\sigma=\frac{dQ}{dA}
}
$$

Units:

$$
\boxed{\text{C/m}^2}
$$

## Line charge density

$$
\boxed{
\lambda=\frac{dQ}{dl}
}
$$

Units:

$$
\boxed{\text{C/m}}
$$

### Important

Some symbols are reused in electromagnetics.

For example:

- $\sigma$ can mean surface charge density
- $\sigma$ can also mean electrical conductivity

Likewise:

- $\lambda$ can mean line charge density
- $\lambda$ can also mean wavelength

**Always use context.**

---

# 20. Electric Potential $V$

Electric potential is essentially **voltage at a location**.

It is a scalar field:

$$
\boxed{V(x,y,z)}
$$

It has no direction.

Units:

$$
\boxed{\text{volts (V)}}
$$

---

# 21. Electric Field $\mathbf E$

Electric field is a vector field.

It tells you the force that a positive test charge would experience per unit charge.

The fundamental relationship with potential is:

$$
\boxed{
\mathbf E=-\nabla V
}
$$

This means:

> Electric field points toward decreasing electric potential.

### Why the negative sign?

The electric field points in the direction that potential decreases most rapidly.

---

# 22. Permittivity $\epsilon$

The symbol:

$$
\boxed{\epsilon}
$$

is Greek **epsilon**.

Permittivity describes how a material responds electrically to an electric field.

For a simple linear material:

$$
\boxed{
\mathbf D=\epsilon\mathbf E
}
$$

where:

- $\mathbf D$ = electric flux density
- $\epsilon$ = permittivity
- $\mathbf E$ = electric field

A material with greater permittivity generally becomes more electrically polarized in response to an applied electric field.

---

# 23. Dielectrics

A dielectric is an electrically insulating material that can become polarized by an electric field.

Examples:

- glass
- plastic
- ceramic
- air

The electric field slightly shifts positive and negative charge distributions within the material.

This is called:

$$
\boxed{\text{polarization}}
$$

Material properties such as permittivity also affect electromagnetic wave behavior at boundaries, including reflection and refraction.

Again:

> **Flux itself is not reflection or refraction.**

---

# 24. Electric Flux Density $\mathbf D$

Electric flux density is represented by:

$$
\boxed{\mathbf D}
$$

It can be thought of roughly as:

> **Electric flux per unit area.**

Its units are:

$$
\boxed{\text{C/m}^2}
$$

For a simple linear material:

$$
\boxed{
\mathbf D=\epsilon\mathbf E
}
$$

Gauss's law can be written:

$$
\boxed{
\oint_S\mathbf D\cdot d\mathbf S
=
Q_{\text{free,enclosed}}
}
$$

This says:

> The total electric flux through a closed surface is related to the free charge enclosed by that surface.

---

# 25. $B$ vs $H$

These are the magnetic counterparts of $D$ and $E$.

## Magnetic flux density

$$
\boxed{\mathbf B}
$$

Units:

$$
\boxed{\text{tesla (T)}}
$$

## Magnetic field intensity

$$
\boxed{\mathbf H}
$$

Units:

$$
\boxed{\text{A/m}}
$$

They are related by:

$$
\boxed{
\mathbf B=\mu\mathbf H
}
$$

where:

$$
\mu=\text{permeability}
$$

### Useful analogy

Electric:

$$
\boxed{D=\epsilon E}
$$

Magnetic:

$$
\boxed{B=\mu H}
$$

---

# 26. Current Density

Current density is:

$$
\boxed{\mathbf J}
$$

Units:

$$
\boxed{\text{A/m}^2}
$$

It describes how much electric current flows through an area.

For a simple conductor:

$$
\boxed{
\mathbf J=\sigma\mathbf E
}
$$

where:

$$
\sigma=\text{electrical conductivity}
$$

### Important symbol warning

Here $\sigma$ means **conductivity**.

Earlier, $\sigma$ could mean **surface charge density**.

Context determines which meaning applies.

---

# 27. The Three Constitutive Relations

These are extremely important:

$$
\boxed{\mathbf D=\epsilon\mathbf E}
$$

$$
\boxed{\mathbf B=\mu\mathbf H}
$$

$$
\boxed{\mathbf J=\sigma\mathbf E}
$$

Think:

| Quantity | Relationship |
|---|---|
| Electric | $D=\epsilon E$ |
| Magnetic | $B=\mu H$ |
| Conduction | $J=\sigma E$ |

These equations describe how electromagnetic quantities relate to the properties of a material.

---

# 28. Maxwell's Four Equations

These are the foundation of classical electromagnetics.

## 1. Gauss's Law — Electric

$$
\boxed{
\nabla\cdot\mathbf D=\rho
}
$$

Meaning:

> **Electric charge produces electric flux.**

The left side asks how much $\mathbf D$ is spreading outward locally.

The right side tells us the charge density producing that behavior.

---

## 2. Gauss's Law — Magnetic

$$
\boxed{
\nabla\cdot\mathbf B=0
}
$$

Meaning:

> **There are no isolated magnetic monopoles in classical electromagnetism.**

Magnetic field lines do not begin or end at an isolated magnetic charge.

---

## 3. Faraday's Law

$$
\boxed{
\nabla\times\mathbf E
=
-\frac{\partial\mathbf B}{\partial t}
}
$$

Meaning:

> **A changing magnetic field produces a circulating electric field.**

Symbols:

- $\nabla\times$ = curl
- $\mathbf E$ = electric field
- $\mathbf B$ = magnetic flux density
- $t$ = time
- $\partial\mathbf B/\partial t$ = rate at which magnetic field changes with time

---

## 4. Ampère-Maxwell Law

$$
\boxed{
\nabla\times\mathbf H
=
\mathbf J+
\frac{\partial\mathbf D}{\partial t}
}
$$

Meaning:

> **Current and changing electric fields produce circulating magnetic fields.**

The two terms on the right are:

$$
\mathbf J
$$

= conduction current density

and:

$$
\frac{\partial\mathbf D}{\partial t}
$$

= displacement-current density.

---

# 29. Poisson's Equation

Starting with:

$$
\mathbf E=-\nabla V
$$

and:

$$
\nabla\cdot\mathbf D=\rho
$$

with:

$$
\mathbf D=\epsilon\mathbf E
$$

we eventually get:

$$
\boxed{
\nabla^2V=-\frac{\rho}{\epsilon}
}
$$

This is **Poisson's equation**.

It relates:

- electric potential $V$
- charge density $\rho$
- permittivity $\epsilon$

---

# 30. Laplace's Equation

If the region contains no charge:

$$
\rho=0
$$

then Poisson's equation becomes:

$$
\boxed{
\nabla^2V=0
}
$$

This is **Laplace's equation**.

### Remember

Poisson:

$$
\boxed{
\nabla^2V=-\frac{\rho}{\epsilon}
}
$$

No charge:

$$
\rho=0
$$

Therefore:

$$
\boxed{
\nabla^2V=0
}
$$

---

# 31. Boundary Conditions

A boundary condition tells you what happens at the edge of a problem.

For example:

$$
V(0)=0
$$

means:

> At $x=0$, the potential is zero.

Boundary conditions are crucial because differential equations generally have many possible solutions.

The physical boundaries tell us which solution applies.

---

# 32. Electromagnetic Waves

A simple sinusoidal wave can look like:

$$
\boxed{
\cos(\omega t-kz)
}
$$

where:

- $t$ = time
- $\omega$ = angular frequency
- $k$ = wavenumber
- $z$ = position

The wave changes in both time and space.

The expression:

$$
\omega t-kz
$$

is the **phase**.

---

# 33. Frequency, Wavelength, and Wavenumber

## Frequency

$$
\boxed{f}
$$

Frequency tells you how many cycles occur per second.

Units:

$$
\boxed{\text{Hz}}
$$

## Period

$$
\boxed{
T=\frac1f
}
$$

where:

- $T$ = period
- $f$ = frequency

## Angular frequency

$$
\boxed{
\omega=2\pi f
}
$$

where:

- $\omega$ = angular frequency
- $f$ = frequency

Units:

$$
\boxed{\text{rad/s}}
$$

## Wavelength

$$
\boxed{\lambda}
$$

Wavelength is the spatial distance corresponding to one cycle.

Units:

$$
\boxed{\text{m}}
$$

## Wavenumber

$$
\boxed{
k=\frac{2\pi}{\lambda}
}
$$

where:

- $k$ = wavenumber
- $\lambda$ = wavelength

Units:

$$
\boxed{\text{rad/m}}
$$

## Wave velocity

$$
\boxed{
v=f\lambda
}
$$

and:

$$
\boxed{
v=\frac{\omega}{k}
}
$$

---

# 34. Plane Waves

A plane wave is an electromagnetic wave whose fields are uniform across planes perpendicular to the propagation direction.

Example:

$$
\boxed{
\mathbf E
=
\hat{x}E_0\cos(\omega t-kz)
}
$$

This means:

- $\mathbf E$ points in the x direction
- $E_0$ is the electric-field amplitude
- the wave varies with $z$
- the wave propagates in the z direction
- the field oscillates with time

For a simple plane EM wave:

$$
\boxed{
\mathbf E\perp\mathbf H
}
$$

and both are perpendicular to the propagation direction.

Thus:

$$
\boxed{
\mathbf E\perp\mathbf H\perp\text{propagation direction}
}
$$

---

# 35. Wave Velocity

For a simple homogeneous material:

$$
\boxed{
v=\frac1{\sqrt{\mu\epsilon}}
}
$$

where:

- $v$ = wave velocity
- $\mu$ = permeability
- $\epsilon$ = permittivity

In free space:

$$
\boxed{
c=\frac1{\sqrt{\mu_0\epsilon_0}}
}
$$

where:

- $c$ = speed of light
- $\mu_0$ = permeability of free space
- $\epsilon_0$ = permittivity of free space

This is one of the fundamental connections between electromagnetism and light:

> **Light is an electromagnetic wave.**

---

# 36. Intrinsic Impedance

Intrinsic impedance is:

$$
\boxed{
\eta=\sqrt{\frac{\mu}{\epsilon}}
}
$$

For a simple plane wave:

$$
\boxed{
\frac{E}{H}=\eta
}
$$

where:

- $E$ = electric-field amplitude
- $H$ = magnetic-field amplitude
- $\eta$ = intrinsic impedance

Units:

$$
\boxed{\Omega}
$$

---

# 37. Poynting Vector

The Poynting vector describes electromagnetic energy flow:

$$
\boxed{
\mathbf S=\mathbf E\times\mathbf H
}
$$

where:

- $\mathbf S$ = Poynting vector
- $\mathbf E$ = electric field
- $\mathbf H$ = magnetic field intensity

Because it is a cross product, its direction is perpendicular to both $\mathbf E$ and $\mathbf H$.

For a plane wave:

$$
\boxed{\mathbf S}
$$

points in the direction the electromagnetic energy travels.

Units:

$$
\boxed{\text{W/m}^2}
$$

---

# 38. Complex Numbers

Electrical engineering uses:

$$
\boxed{
j=\sqrt{-1}
}
$$

instead of $i$, because $i$ is commonly used for current.

The important identity is Euler's formula:

$$
\boxed{
e^{j\theta}
=
\cos\theta+j\sin\theta
}
$$

Complex numbers provide a convenient mathematical way to represent oscillations.

The physical electromagnetic field is still real.

---

# 39. Phasors

A phasor is a complex representation of a sinusoidal quantity.

Suppose:

$$
E(t)=E_0\cos(\omega t+\phi)
$$

where:

- $E_0$ = amplitude
- $\omega$ = angular frequency
- $t$ = time
- $\phi$ = phase

Instead of repeatedly carrying the entire sinusoid, we can represent its amplitude and phase with:

$$
\boxed{
\tilde E=E_0e^{j\phi}
}
$$

The major advantage is that differentiation becomes:

$$
\boxed{
\frac{\partial}{\partial t}
\rightarrow
j\omega
}
$$

for sinusoidal steady-state analysis.

---

# 40. Fourier Transform

Fourier analysis asks:

> **What frequencies make up this signal?**

The Fourier transform is commonly written:

$$
\boxed{
X(f)
=
\int_{-\infty}^{\infty}
x(t)e^{-j2\pi ft}\,dt
}
$$

where:

- $x(t)$ = time-domain signal
- $X(f)$ = frequency-domain representation
- $f$ = frequency
- $t$ = time
- $j=\sqrt{-1}$

Conceptually:

$$
\boxed{
\text{Time domain}
\rightarrow
\text{Fourier transform}
\rightarrow
\text{Frequency domain}
}
$$

For SDR, this is the mathematical foundation behind looking at signals in the frequency domain.

---

# 41. DFT vs FFT

These are easy to confuse.

## DFT

**Discrete Fourier Transform**

A mathematical transformation operating on a finite set of discrete samples.

## FFT

**Fast Fourier Transform**

An efficient algorithm for calculating the DFT.

Therefore:

$$
\boxed{
\text{FFT is an algorithm for computing the DFT.}
}
$$

It isn't a completely different transform.

---

# 42. Sampling

If:

$$
f_s
$$

is the sampling frequency, the basic Nyquist condition is:

$$
\boxed{
f_s>2f_{\max}
}
$$

where:

- $f_s$ = sampling frequency
- $f_{\max}$ = highest frequency present

If you sample too slowly:

$$
\boxed{\text{aliasing occurs}}
$$

This is directly relevant to SDR.

### Intuition

Sampling converts a continuous-time signal into discrete measurements.

If there aren't enough measurements per cycle, different frequencies can become indistinguishable after sampling.

---

# 43. Convolution and Filters

A filter can be represented as:

$$
\boxed{
y(t)=x(t)*h(t)
}
$$

where:

- $x(t)$ = input signal
- $h(t)$ = impulse response
- $y(t)$ = output signal
- $*$ = convolution

In the frequency domain:

$$
\boxed{
Y(f)=X(f)H(f)
}
$$

where:

- $X(f)$ = input spectrum
- $H(f)$ = filter frequency response
- $Y(f)$ = output spectrum

This is why Fourier analysis is so useful for understanding filters.

---

# 44. Divergence Theorem

The divergence theorem connects local divergence to total flux through a closed surface.

$$
\boxed{
\iiint_V\nabla\cdot\mathbf A\,dv
=
\oiint_S\mathbf A\cdot d\mathbf S
}
$$

Intuitively:

> Add up all the sources inside a volume → get the total outward flux through its boundary.

This theorem is important because it allows us to move between:

- a **local differential description**
- a **global integral description**

---

# 45. Stokes' Theorem

Stokes' theorem connects curl over a surface to circulation around its boundary.

$$
\boxed{
\iint_S
(\nabla\times\mathbf A)\cdot d\mathbf S
=
\oint_C
\mathbf A\cdot d\mathbf l
}
$$

Intuitively:

> Add up the local circulation across a surface → get the circulation around the boundary.

Like the divergence theorem, Stokes' theorem connects differential and integral descriptions.

---

# 46. Differential Equations

EM uses differential equations constantly.

A first derivative:

$$
\frac{dV}{dx}
$$

describes how something changes.

A second derivative:

$$
\frac{d^2V}{dx^2}
$$

describes how the rate of change itself changes.

A partial derivative:

$$
\frac{\partial V}{\partial x}
$$

is used when a quantity depends on multiple variables.

EM uses differential equations because electromagnetic fields vary with:

- position
- time

---

# 47. Separation of Variables

You may encounter something like:

$$
V(x,y)=X(x)Y(y)
$$

The idea is to take a complicated multidimensional equation and separate it into simpler equations.

This is especially common when solving:

- Laplace's equation
- wave equations
- boundary-value problems

Later you'll encounter:

- eigenvalues
- eigenfunctions

These are part of the mathematical machinery used to solve many EM problems.

---

# 48. Master Equation Sheet

## Vector Mathematics

### Vector magnitude

$$
\boxed{
|\mathbf A|
=
\sqrt{A_x^2+A_y^2+A_z^2}
}
$$

### Unit vector

$$
\boxed{
\hat{\mathbf A}
=
\frac{\mathbf A}{|\mathbf A|}
}
$$

### Dot product

$$
\boxed{
\mathbf A\cdot\mathbf B
=
|\mathbf A||\mathbf B|\cos\theta
}
$$

### Cross product magnitude

$$
\boxed{
|\mathbf A\times\mathbf B|
=
|\mathbf A||\mathbf B|\sin\theta
}
$$

---

## Vector Calculus

### Gradient

$$
\boxed{
\nabla V
=
\frac{\partial V}{\partial x}\hat{x}
+
\frac{\partial V}{\partial y}\hat{y}
+
\frac{\partial V}{\partial z}\hat{z}
}
$$

### Divergence

$$
\boxed{
\nabla\cdot\mathbf A
=
\frac{\partial A_x}{\partial x}
+
\frac{\partial A_y}{\partial y}
+
\frac{\partial A_z}{\partial z}
}
$$

### Curl

$$
\boxed{
\nabla\times\mathbf A
}
$$

### Laplacian

$$
\boxed{
\nabla^2V
=
\nabla\cdot\nabla V
}
$$

$$
\boxed{
\nabla^2V
=
\frac{\partial^2V}{\partial x^2}
+
\frac{\partial^2V}{\partial y^2}
+
\frac{\partial^2V}{\partial z^2}
}
$$

---

## Electrostatics

$$
\boxed{
\mathbf E=-\nabla V
}
$$

$$
\boxed{
\mathbf D=\epsilon\mathbf E
}
$$

$$
\boxed{
\nabla\cdot\mathbf D=\rho
}
$$

$$
\boxed{
\nabla^2V=-\frac{\rho}{\epsilon}
}
$$

$$
\boxed{
\nabla^2V=0
\qquad(\rho=0)
}
$$

---

## Materials

$$
\boxed{
\mathbf D=\epsilon\mathbf E
}
$$

$$
\boxed{
\mathbf B=\mu\mathbf H
}
$$

$$
\boxed{
\mathbf J=\sigma\mathbf E
}
$$

---

## Maxwell's Equations

$$
\boxed{
\nabla\cdot\mathbf D=\rho
}
$$

$$
\boxed{
\nabla\cdot\mathbf B=0
}
$$

$$
\boxed{
\nabla\times\mathbf E
=
-\frac{\partial\mathbf B}{\partial t}
}
$$

$$
\boxed{
\nabla\times\mathbf H
=
\mathbf J+
\frac{\partial\mathbf D}{\partial t}
}
$$

---

## Waves

$$
\boxed{
\omega=2\pi f
}
$$

$$
\boxed{
k=\frac{2\pi}{\lambda}
}
$$

$$
\boxed{
v=f\lambda
}
$$

$$
\boxed{
v=\frac{\omega}{k}
}
$$

$$
\boxed{
v=\frac1{\sqrt{\mu\epsilon}}
}
$$

$$
\boxed{
\eta=\sqrt{\frac{\mu}{\epsilon}}
}
$$

$$
\boxed{
\mathbf S=\mathbf E\times\mathbf H
}
$$

---

## Complex Numbers

$$
\boxed{
j=\sqrt{-1}
}
$$

$$
\boxed{
e^{j\theta}
=
\cos\theta+j\sin\theta
}
$$

$$
\boxed{
\frac{\partial}{\partial t}
\rightarrow
j\omega
}
$$

---

## Signal Processing

$$
\boxed{
X(f)
=
\int x(t)e^{-j2\pi ft}\,dt
}
$$

$$
\boxed{
f_s>2f_{\max}
}
$$

$$
\boxed{
y(t)=x(t)*h(t)
}
$$

$$
\boxed{
Y(f)=X(f)H(f)
}
$$

---

# 49. Symbol Reference

| Symbol | Meaning | Type / Units |
|---|---|---|
| $V$ | Electric potential | Scalar, V |
| $\mathbf E$ | Electric field | Vector, V/m |
| $\mathbf D$ | Electric flux density | Vector, C/m² |
| $\mathbf B$ | Magnetic flux density | Vector, T |
| $\mathbf H$ | Magnetic field intensity | Vector, A/m |
| $\rho$ | Volume charge density | Scalar, C/m³ |
| $\sigma$ | Surface charge density or conductivity | Context-dependent |
| $\lambda$ | Line charge density or wavelength | Context-dependent |
| $\mathbf J$ | Current density | Vector, A/m² |
| $Q,q$ | Electric charge | Scalar, C |
| $\epsilon$ | Permittivity | Material property |
| $\mu$ | Permeability | Material property |
| $\Phi$ | Flux | Scalar |
| $d\mathbf l$ | Differential displacement | Vector |
| $d\mathbf S$ | Differential surface area | Vector |
| $\nabla$ | Nabla operator | Differential operator |
| $f$ | Frequency | Hz |
| $T$ | Period | s |
| $\omega$ | Angular frequency | rad/s |
| $\lambda$ | Wavelength | m |
| $k$ | Wavenumber | rad/m |
| $\eta$ | Intrinsic impedance | Ω |
| $j$ | Imaginary unit | $\sqrt{-1}$ |
| $\mathbf S$ | Poynting vector | W/m² |

---

# 50. What to Memorize First

**Do not attempt to memorize this entire document.**

Use this progression.

## Stage 1 — Math Vocabulary

Memorize:

- scalar
- vector
- unit vector
- dot product
- cross product

---

## Stage 2 — Vector Calculus

Understand:

$$
\nabla V
$$

$$
\nabla\cdot\mathbf A
$$

$$
\nabla\times\mathbf A
$$

$$
\nabla^2V
$$

Know:

- what each takes as input
- what it outputs
- what it means physically

| Operation | Input | Output | Intuition |
|---|---|---|---|
| Gradient | Scalar | Vector | Fastest increase |
| Divergence | Vector | Scalar | Spreading out |
| Curl | Vector | Vector | Circulation |
| Laplacian | Scalar | Scalar | Spatial curvature/change |

---

## Stage 3 — EM Quantities

Memorize these:

$$
\boxed{
V,\mathbf E,\mathbf D,\mathbf B,\mathbf H,\mathbf J,\rho
}
$$

Then understand what each physically represents.

---

## Stage 4 — Material Relationships

Memorize:

$$
\boxed{
D=\epsilon E
}
$$

$$
\boxed{
B=\mu H
}
$$

$$
\boxed{
J=\sigma E
}
$$

---

## Stage 5 — Maxwell

Memorize the four equations:

$$
\boxed{
\nabla\cdot D=\rho
}
$$

$$
\boxed{
\nabla\cdot B=0
}
$$

$$
\boxed{
\nabla\times E=-\frac{\partial B}{\partial t}
}
$$

$$
\boxed{
\nabla\times H
=
J+\frac{\partial D}{\partial t}
}
$$

But also memorize their **meaning**, not just their appearance.

---

## Stage 6 — Electrostatics

Understand this chain:

$$
\boxed{
V
\overset{-\nabla}{\longrightarrow}
E
\overset{\epsilon}{\longrightarrow}
D
\overset{\nabla\cdot}{\longrightarrow}
\rho
}
$$

Combining the relationships gives Poisson's equation:

$$
\boxed{
\nabla^2V=-\frac{\rho}{\epsilon}
}
$$

and, when $\rho=0$:

$$
\boxed{
\nabla^2V=0
}
$$

---

## Stage 7 — Waves

Memorize:

$$
\boxed{
\omega=2\pi f
}
$$

$$
\boxed{
k=\frac{2\pi}{\lambda}
}
$$

$$
\boxed{
v=f\lambda
}
$$

$$
\boxed{
v=\frac1{\sqrt{\mu\epsilon}}
}
$$

---

## Stage 8 — Phasors and Fourier

Then learn:

$$
\boxed{
j=\sqrt{-1}
}
$$

$$
\boxed{
e^{j\theta}=\cos\theta+j\sin\theta
}
$$

$$
\boxed{
\frac{\partial}{\partial t}\rightarrow j\omega
}
$$

and:

$$
\boxed{
\text{Fourier transform}
\rightarrow
\text{frequency-domain representation}
}
$$

---

# 51. The Most Important Mental Map

If you can understand this diagram, you're starting to understand the structure of EM:

```text
                       ELECTROMAGNETICS
                              │
             ┌────────────────┴────────────────┐
             │                                 │
            MATH                            PHYSICS
             │                                 │
      ┌──────┴──────┐                 ┌────────┴────────┐
      │             │                 │                 │
   Scalars       Vectors          Electric          Magnetic
      │             │                 │                 │
      V             E                 D               B / H
      │                               │                 │
      │                               │                 │
      └── gradient ────────────────→ E                 │
                                      │                 │
                                      D = εE            │
                                      │                 │
                                divergence              │
                                      │                 │
                                      ρ                 │
                                                        │
                                                   B = μH
                                                        │
                                                        │
                         ┌──────────────────────────────┘
                         │
                         ▼
                  Maxwell's Equations
                         │
                         ▼
                  Electromagnetic Waves
                         │
              ┌──────────┴──────────┐
              │                     │
             E-field             H-field
              │                     │
              └────── E × H ───────┘
                         │
                         ▼
                    Energy Flow
