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

There is the vector potential $$\mathbf A$$, which has only azimuthal value. To find $$\mathbf A$$, we can use Ampére's Law:

$$\oint_c \mathbf A \cdot d\vec \ell = \int_S \nabla \times \mathbf A \cdot d \vec a = \Phi$$

For outside the solenoid, the magnetic flux $$\Phi$$ is constant $$\Phi = \pi a^2 B$$.

Therefore, $$\mathbf A = \frac{\Phi}{2\pi r}\hat \phi$$ for outside the solenoid.$$

We can calculate vector potential $$\mathbf A$$ similar way. Actually this is not the point where I want to explain in this post. I just wanted to show there is $$\mathbf A$$ outside the solenoid, despite there is no magnetic field $$\mathbf B$$. We can graph azimutal component of $$\mathbf A$$(other direction, zero).
{% include figure.html image="https://cka09191.github.io/assets/SolenoidVectorPotentialGraph.png" alt="Figure of a graph of vector potential of phi direction of solenoid" %}

We can proceed to apply the Schrödinger equation:

$$i\hbar \frac{\partial\Psi}{\partial t} =\mathcal{H}\Psi$$

And using $$\mathbf A$$, we can calculate $$\mathcal{H}$$:

$$\begin{aligned}\mathcal{H}&=\frac{1}{2m} (\mathbf{p}-q \mathbf{A})^{2}+V
\\&=\frac{1}{2m} \left[-\hbar^2\nabla^2+q^2 A^2+2i\hbar q\mathbf A \cdot\nabla\right]
\\&=\frac{1}{2m} \left[-\frac{\hbar^2}{b^2}\frac{\partial^2}{\partial \phi}+\left(\frac{q^2 \Phi^2}{2\pi b}\right)^2+i\frac{\hbar q \Phi}{\pi b^2}\frac{\partial}{\partial \phi} \right]\end{aligned}$$

By substituting it to Schrödinger equation and rearranging:

$$\frac{\partial^2 \psi}{\partial \phi^2}-2i\beta\frac{d\psi}{d\phi}+\epsilon\psi=0$$

where $$\beta=\frac{q\Phi}{2\pi\hbar}$$ and $$\epsilon=\frac{2mE}{\hbar^2}-\beta^2$$

Let $$\phi = Ae^{i\lambda \phi}$$, then:

$$-\lambda^2 + 2\lambda \beta + \epsilon = 0$$

Therefore:

$$\lambda = \beta \pm \sqrt{\beta^2 +\epsilon} = \beta \pm \frac{b}{\hbar}\sqrt{2mE}$$

And using boundary condition:

$$\psi(\phi) = \psi(\phi + 2\pi)$$

Then

$$\lambda = n \quad(0,\pm 1,\pm 2, \dots)$$

And arrange the equation about $$E$$:

$$E_n = \frac{\hbar^2}{2m}\left(n-\frac{q\Phi}{2\pi\hbar}\right)$$


It quite took a time for calculating. But what's the important?

Let's return to the story we have talking : Aharonov-Bohm Effect.

Potential itself has meaning. In calculation of classical mechanics, the potential has no effect on [gauge transformation](https://cka09191.github.io/Fundamental-Concepts-in-Electromagnetics/). And we want to know this is same, in quantum mechanics.

With gauge transformation:

$$\mathbf A \rightarrow \mathbf A' = \mathbf A + \nabla + \Lambda$$

Let $$\psi'$$:

$$\psi \rightarrow \psi' = e^{iq\Lambda/\hbar}\psi$$

which maybe same: $$\Lambda = 0$$

By ?? Transformation:
$$\psi = e^{ig}\psi'$$ with $$g(\mathbf r) =\frac{q}{\hbar}\int^{\mathbf r}_0 \mathbf A (\mathbf r') \cdot d\mathbf r'$$

