# Problem 1

Orbital Period and Orbital Radius

Orbital motion around a central body (like a planet or star) is governed by gravity. A central concept in celestial mechanics is Kepler’s Third Law, which relates the square of the orbital period to the cube of the orbital radius for circular orbits. This relationship enables astronomers to calculate distances, periods, and masses of celestial bodies.

⸻

1 – Newton’s Law of Universal Gravitation and Centripetal Force

For an object of mass m in circular orbit of radius r around a much larger mass M (e.g., planet orbiting the Sun), the gravitational force provides the necessary centripetal force:

$$
\frac{G M m}{r^2} = \frac{m v^2}{r}
$$

Solving for orbital speed v:

$$
v = \sqrt{\frac{G M}{r}}
$$

⸻

2 – Orbital Period T

The orbital period is the time it takes to complete one full orbit:

$$
T = \frac{2\pi r}{v}
$$

Substitute v from above:

$$
T = \frac{2\pi r}{\sqrt{\frac{G M}{r}}} = 2\pi \sqrt{\frac{r^3}{G M}}
$$

⸻

3 – Kepler’s Third Law

The square of the orbital period is proportional to the cube of the orbital radius:

$$
T^2 \propto r^3
$$

Or more precisely:

$$
T^2 = \frac{4\pi^2}{G M} \cdot r^3
$$

This is Kepler’s Third Law for circular orbits.

⸻

4 – Real-World Applications
	•	Earth’s Moon: Using the Moon’s known orbital radius r \approx 3.84 \times 10^8 \, \text{m} and T = 27.3 \, \text{days}, the relation holds.
	•	Satellite Orbits: Helps engineers determine correct orbital altitude and timing.
	•	Solar System: Used to compare periods and distances of planets.

⸻

5 – Computational Model (Python Concept)

Kepler’s Law using Python:
import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # gravitational constant
M = 5.972e24     # mass of Earth (kg)
radii = np.linspace(6.7e6, 4.2e7, 100)  # orbital radii in meters
T_squared = (4 * np.pi**2 * radii**3) / (G * M)

plt.plot(radii, T_squared)
plt.title('Kepler\'s Third Law: $T^2$ vs $r^3$')
plt.xlabel('Orbital Radius r (m)')
plt.ylabel('Orbital Period Squared $T^2$ (s$^2$)')
plt.grid(True)
plt.show()


⸻

Summary
	•	Gravitational force provides the centripetal force in circular orbits.
	•	Orbital velocity depends on \sqrt{GM/r}.
	•	Kepler’s Third Law: T^2 \propto r^3
	•	This law is used in satellite placement, planetary motion analysis, and astronomy.
	•	Python simulations can validate the T^2 vs r^3 relationship graphically.

⸻

Visualization

![Kepler Law](Keplers_3rdlaw.png)