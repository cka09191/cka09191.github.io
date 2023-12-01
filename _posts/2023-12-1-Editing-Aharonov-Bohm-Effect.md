---
title: Aharonov-Bohm Effect(Editing)
categories:
  - Quantum Mechanics
feature_text: |
  The Aharonov-Bohm effect reveals that in quantum mechanics, potential itselves has real effect on charged particles, even in regions where there are no electromagnetic fields or forces acting. This stands in contrast to classical physics, which does not attribute any physical significance to potentials in the absence of fields.
excerpt: |
  The Aharonov-Bohm effect reveals that in quantum mechanics, potential itselves has a real effect on charged particles, even in regions where there are no electromagnetic fields or forces acting. This stands in contrast to classical physics, which does not attribute any physical significance to potentials in the absence of fields.
---


Think of an "ideal" solenoid:
{% include figure.html image="https://cka09191.github.io/assets/SolenoidVectorPotential.png" alt="Figure of A Solenoid and Vector Potential arrows" %}

There's a constant magnetic field in the direction of $$\widehat z$$(red arrows). Around the solenoid, there exists a [vector potential](https://cka09191.github.io/Fundamental-Concepts-in-Electromagnetics) in the direction of $$\widehat\phi$$(blue arrows). But it have no effect on charge because magnetic field is zero outside the solenoid. In other words, if you put a charge outside the solenoid, it is not affected no matter how the magnetic field is strong.

But, this explanation induced in classical electromagnetics. How it would charge does in quantum world?

Considering the [Hamiltonian that includes the Lorentz force](https://cka09191.github.io/Fundamental-Concepts-in-Electromagnetics) within the solenoid:

$$\mathcal{H}=\frac{1}{2m} (\mathbf{p}-q \mathbf{A})^{2}+V$$

There is the vector potential $$\vec A$$, which has only azimuthal value. To find $$\vec A$$, we can use Ampére's Law:

$$\oint_c \vec A \cdot d\vec \ell = \int_S \nabla \times \vec A \cdot d \vec a = \Phi$$

For outside the solenoid, the magnetic flux $$\Phi$$ is constant $$\Phi = \pi a^2 B$$.

Therefore, $$\vec A = \frac{\Phi}{2\pi r}\hat \phi$$ for outside the solenoid.$$

We can calculate vector potential $$\vec A$$ similar way. Actually this is not the point where I want to explain in this post. I just wanted to show there is $$\vec A$$ outside the solenoid, despite there is no magnetic field $$\mathbf B$$. We can graph azimutal component of $$\vec A$$(other direction, zero).
{% include figure.html image="https://cka09191.github.io/assets/SolenoidVectorPotentialGraph.png" alt="Figure of a graph of vector potential of phi direction of solenoid" %}

we can proceed to apply the Schrödinger equation:

$$i\hbar \frac{\partial\Psi}{\partial t} =\left[\frac{1}{2m}\left(\frac{k}{i}\nabla - q\vec A \right)^2+V\right]\Psi$$

