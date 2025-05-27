# Problem 1

Problem 1

Orbital Period and Orbital Radius

⸻

Motivation

Kepler’s Third Law reveals a deep connection between time and space in celestial mechanics. It states that the square of a planet’s orbital period is proportional to the cube of its average orbital radius. This principle helps astronomers and engineers determine orbits, planetary masses, and understand large-scale gravitational systems.

⸻

1 - Derivation of Kepler’s Third Law (Circular Orbits)

From Newton’s law of gravitation and circular motion:
	•	Gravitational force:
$$
F_g = \frac{G M m}{r^2}
$$
	•	Centripetal force:
$$
F_c = \frac{m v^2}{r}
$$
Set F_g = F_c:
$$
\frac{G M m}{r^2} = \frac{m v^2}{r} \Rightarrow v^2 = \frac{G M}{r}
$$

Orbital velocity:
$$
v = \frac{2\pi r}{T}
$$
Substitute:
$$
\left( \frac{2\pi r}{T} \right)^2 = \frac{G M}{r}
$$

Solve for T^2:
$$
T^2 = \frac{4\pi^2 r^3}{G M}
$$

⸻

2 - Interpretation
	•	T^2 \propto r^3 for all small orbiting bodies (mass m) around a large mass M
	•	Applies to planets, moons, satellites, and more
	•	The constant of proportionality depends on the central mass M

⸻

3 - Real-World Examples

The Moon
	•	r \approx 3.84 \times 10^8\, \text{m}
	•	T \approx 27.3\, \text{days}
	•	Used to compute Earth’s mass using Kepler’s law

Planets
	•	Earth: r = 1\, \text{AU}, T = 1\, \text{year}
	•	Mars: r = 1.52\, \text{AU}, T = 1.88\, \text{years}
	•	Verify: \frac{T^2}{r^3} \approx \text{constant}

⸻

4 - Python Simulation

import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11      # Gravitational constant [m^3 kg^-1 s^-2]
M = 1.989e30         # Mass of the Sun [kg]

# Orbital radii [m]
radii = np.linspace(5e10, 3e11, 100)
T_squared = (4 * np.pi**2 * radii**3) / (G * M)

# Plot T^2 vs r^3
plt.plot(radii**3, T_squared, label='T² vs r³')
plt.xlabel("Orbital Radius Cubed (r³) [m³]")
plt.ylabel("Orbital Period Squared (T²) [s²]")
plt.title("Kepler's Third Law - Verification")
plt.grid(True)
plt.legend()
plt.show()


⸻

5 - Extensions to Elliptical Orbits
	•	Replace r with semi-major axis a:
$$
T^2 = \frac{4\pi^2 a^3}{G M}
$$
	•	Applies to all elliptical orbits, not just circular ones
	•	In binary systems: use M + m for the total mass

⸻

Summary
	•	Kepler’s 3rd Law: T^2 \propto r^3
	•	Fundamental in predicting and analyzing orbital motion
	•	Simulations confirm the proportionality
	•	Widely used in astrophysics, aerospace, and planetary science

    
![Kepler's Law](images/kepler_third_law.png)