---
title: Fundamental Concepts in Electromagnetics
categories:
- Physics
---
This post introduces fundamental concepts in electromagnetics, including electromagnetic fields and potentials, Maxwell's Equations, the Lorentz force, Gauge transformation.

<!-- more -->

# Maxwell's Equations
Maxwell's Equations consist of four fundamental laws that govern the behaviors of electric fields ($$\mathbf E$$) and magnetic fields ($$\mathbf B$$).


### Gauss's Law
$$\nabla \cdot \mathbf E = \frac{\rho}{\epsilon_0}\quad \left(\equiv\quad \nabla \cdot \mathbf D=\rho_f\right)$$

This law describes how the electric field ($$\mathbf E$$) diverges from electric charges. It relates to the concept of electric monopoles, namely electric charges.

### Gauss's Law For Magnetism
$$\nabla \cdot \mathbf B = 0$$

This states that magnetic monopoles do not exist, unlike electric monopoles (electric charges). Although we can theoretically conceptualize magnetic monopoles (or magnetic charges), this law indicates that such entities cannot exist in reality.

### Maxwell-Faraday Equation
$$\nabla \times \mathbf E = -\frac{\partial \mathbf B}{\partial t}$$

This equation explains the principle behind motors and generators. In motors, moving a magnet (changing $$\mathbf B$$) induces an electric field ($$\nabla \times \mathbf E$$).
Conversely, in generators, moving a magnet(changing $$\mathbf B$$) generates a current in an electric circuit($$\nabla \times \mathbf E$$).

### Ampère's Circuital Law
$$\nabla \times \mathbf B = \mu_0\left(\mathbf J + \epsilon_0 \frac{\partial \mathbf E}{\partial t}\right)\quad\left(\equiv\quad \nabla \times \mathbf H =\frac{1}{c}\left(4\pi\mathbf J_f + \frac{\partial \mathbf D}{\partial t}\right)\right)$$

This law states that electric currents (either free current $$\mathbf J$$ or displacement current $$\frac{\partial \mathbf E}{\partial t}$$) generate a magnetic field($$\mathbf B$$).

# Electromagnetic Potentials
Electromagnetic fields can be expressed in terms of potentials:

$$\mathbf E = -\nabla \Phi - \frac{\partial \mathbf A}{\partial t}$$

$$\mathbf B = \nabla \times \mathbf A$$

Here, $$\Phi$$ is called scalar potential (aka electric potential), and $$\mathbf A$$ is the vector potential (aka magnetic potential)

# Lorentz Force
$$\mathbf F = q\left(\mathbf E + \mathbf v \times \mathbf B\right)$$

A charge in an electromagnetic field experiences the Lorentz force.

The Lorentz force can also be described using electromagnetic potentials:

$$\mathcal{H}=\frac{1}{2m} (\mathbf{p}-q \mathbf{A})^{2}+q \Phi$$

This representation integrates the effects of the scalar and vector potentials on a charged particle.

# Gauge transformation
In gauge transformation, we change the electromagnetic potentials like this:

$$\Phi' = \Phi-\frac{\partial \Lambda}{\partial t}\quad and\quad \mathbf A' = \mathbf A+\nabla \Lambda$$

Even with these changes, the behavior of charges remains unaffected. This means we can choose any potential that satisfies these equations. As a result, electromagnetic potentials in these scenarios are often considered 'not really physical'—their specific values don't alter the actual physical phenomena occurring. This principle, where different potentials lead to the same physical outcomes, is what we refer to as gauge symmetry.
