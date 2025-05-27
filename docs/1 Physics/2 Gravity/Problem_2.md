# Problem 2

Excellent! Here’s a complete, clean write-up for Gravity – Problem 2: Escape Velocities and Cosmic Velocities, following the same style and clarity as the previous problems. You can paste this directly into your Python/Markdown file.

⸻

Problem 2

Escape Velocities and Cosmic Velocities

⸻

Motivation

To move from Earth into orbit, leave Earth’s gravity, or escape the Solar System entirely, spacecraft must reach specific speeds. These are known as the first, second, and third cosmic velocities. Understanding these speeds helps define the energy required for different types of space missions and is fundamental in orbital mechanics and interplanetary travel.

⸻

1 - Definitions and Physical Meaning

First Cosmic Velocity – Orbital Speed (Low Earth Orbit)
	•	The minimum horizontal speed needed to enter a stable circular orbit just above a planet’s surface.
	•	For Earth, it allows satellites to remain in orbit without propulsion.

$$
v_1 = \sqrt{\frac{G M}{R}}
$$

⸻

Second Cosmic Velocity – Escape Velocity
	•	The minimum speed needed to completely escape the gravitational pull of a planet, assuming no further propulsion.

$$
v_2 = \sqrt{2} \cdot v_1 = \sqrt{\frac{2 G M}{R}}
$$

⸻

Third Cosmic Velocity – Interstellar Escape
	•	The minimum speed needed to escape the Solar System from Earth orbit, overcoming the Sun’s gravity.
	•	Typically calculated from Earth’s orbital position around the Sun.

$$
v_3 = \sqrt{v_{\text{esc,Sun}}^2 + v_{\text{orb,Earth}}^2}
$$
Where:
	•	v_{\text{esc,Sun}} = \sqrt{\frac{2 G M_{\text{Sun}}}{r}}
	•	v_{\text{orb,Earth}} \approx 29.78 \, \text{km/s}

⸻

2 - Parameters and Derivations

All velocities depend on:
	•	G: gravitational constant \approx 6.674 \times 10^{-11} \, \text{m}^3/\text{kg}/\text{s}^2
	•	M: mass of the celestial body
	•	R: radius from the center of the body (e.g., planetary radius)

⸻

3 - Python Calculation and Visualization

import numpy as np
import matplotlib.pyplot as plt

# Constants
G = 6.67430e-11  # m^3 kg^-1 s^-2

# Celestial bodies: Earth, Mars, Jupiter
bodies = {
    "Earth": {"mass": 5.972e24, "radius": 6.371e6},
    "Mars": {"mass": 6.417e23, "radius": 3.389e6},
    "Jupiter": {"mass": 1.898e27, "radius": 6.9911e7},
}

# Calculate velocities
results = {}
for name, data in bodies.items():
    M = data["mass"]
    R = data["radius"]
    v1 = np.sqrt(G * M / R)
    v2 = np.sqrt(2) * v1
    results[name] = {"v1": v1, "v2": v2}

# Display results
for body, values in results.items():
    print(f"{body}:")
    print(f"  First Cosmic Velocity (v1): {values['v1'] / 1000:.2f} km/s")
    print(f"  Second Cosmic Velocity (v2): {values['v2'] / 1000:.2f} km/s")
    print()

# Plotting
labels = list(results.keys())
v1_vals = [results[body]["v1"] / 1000 for body in labels]
v2_vals = [results[body]["v2"] / 1000 for body in labels]

x = np.arange(len(labels))
width = 0.35

fig, ax = plt.subplots()
ax.bar(x - width/2, v1_vals, width, label='v1 (Orbital Speed)')
ax.bar(x + width/2, v2_vals, width, label='v2 (Escape Velocity)')
ax.set_ylabel('Velocity (km/s)')
ax.set_title('Cosmic Velocities for Various Planets')
ax.set_xticks(x)
ax.set_xticklabels(labels)
ax.legend()
plt.grid(True)
plt.show()


⸻

4 - Importance in Space Exploration
	•	v1: Used for launching satellites, space stations, and spacecraft into orbit.
	•	v2: Required for missions leaving Earth (e.g., to the Moon, Mars).
	•	v3: Necessary for missions aiming to exit the Solar System (e.g., Voyager, interstellar probes).

⸻

Summary

Cosmic Velocity	Meaning	Formula
v₁	Orbital Speed	\sqrt{\frac{G M}{R}}
v₂	Escape Velocity	\sqrt{2} \cdot v_1
v₃	Interstellar Escape from Sun	\sqrt{v_{\text{esc,Sun}}^2 + v_{\text{orb,Earth}}^2}

These velocities provide the foundation for orbital mechanics and are central to any space mission’s launch strategy and trajectory planning.

⸻

![Graph](./media/velocities_graph.png) 