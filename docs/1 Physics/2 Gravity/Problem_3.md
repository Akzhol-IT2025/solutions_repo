# Problem 3
Here’s a complete Markdown-style explanation for Problem 3 – Trajectories of a Freely Released Payload Near Earth, ready to be inserted into your Python code or Jupyter notebook (before or after adding the simulations).

⸻

🛰️ Problem 3 – Trajectories of a Freely Released Payload Near Earth

⸻

🚀 Overview & Motivation

When a payload is released from a moving rocket near Earth, its trajectory is determined by its initial velocity, altitude, and direction. These trajectories can vary widely, resulting in:
	•	Elliptical orbits (if the velocity is below escape speed),
	•	Parabolic paths (if velocity equals escape velocity),
	•	Hyperbolic trajectories (if the object escapes Earth’s gravity),
	•	Reentry paths (if it’s directed back toward Earth).

Understanding these paths is crucial for:
	•	Satellite deployment,
	•	Space mission planning,
	•	Escape trajectory design,
	•	Reentry capsule control.

⸻

📘 1 – Physics Background

The motion of the payload is governed by Newton’s Law of Universal Gravitation:

\vec{F} = -\frac{GMm}{r^2} \hat{r}

Which leads to the equation of motion:

\vec{a} = -\frac{GM}{r^2} \hat{r}

Where:
	•	G is the gravitational constant,
	•	M is the mass of Earth,
	•	m is the mass of the payload,
	•	r is the distance from the center of Earth.

⸻

📐 2 – Types of Trajectories

Depending on the initial speed v_0 and angle, the payload follows one of the conic sections:

Trajectory Type	Speed Condition	Shape
Suborbital / Reentry	v_0 < v_{\text{circular}}	Elliptical arc
Circular Orbit	v_0 = v_{\text{circular}}	Circle
Elliptical Orbit	v_{\text{circular}} < v_0 < v_{\text{escape}}	Ellipse
Parabolic Escape	v_0 = v_{\text{escape}}	Parabola
Hyperbolic Escape	v_0 > v_{\text{escape}}	Hyperbola

Where:
	•	v_{\text{circular}} = \sqrt{\frac{GM}{r}}
	•	v_{\text{escape}} = \sqrt{\frac{2GM}{r}}

⸻

🔢 3 – Numerical Simulation

We solve the equations of motion numerically using methods like Euler or Runge-Kutta (RK4).

The simulation tracks:
	•	Position: \vec{r}(t)
	•	Velocity: \vec{v}(t)

⸻

🛠️ 4 – Example Parameters

# Constants
G = 6.67430e-11       # Gravitational constant [m^3/kg/s^2]
M = 5.972e24          # Mass of Earth [kg]
R_earth = 6.371e6     # Radius of Earth [m]

# Initial conditions
altitude = 400e3                    # 400 km altitude
r0 = np.array([R_earth + altitude, 0])  # Initial position
v0 = np.array([0, 7500])           # Initial velocity (e.g., 7500 m/s tangential)


⸻

🖼️ 5 – Visualization & Outputs

Example of vehicle trajectory representation on the Cartesian coordinates and the curvilinear coordinates. 
![Payload Trajectories](images/payload_trajectories.png)


![Payload Trajectories](images/.trajectory.png)
Here is the plot showing different trajectories of a payload released from 400 km above Earth, depending on its initial speed:
	•	7000 m/s: suborbital or elliptical orbit (falls back).
	•	7670 m/s: circular orbit (stable).
	•	8000 m/s: elliptical orbit (longer, higher apogee).
	•	11200 m/s: escape trajectory (hyperbolic path).

This simulation visually confirms how initial velocity influences the motion type. 

⸻

🌍 6 – Real-World Relevance

These trajectory types are critical in:
	•	Space missions (e.g., Apollo landings, satellite deployments),
	•	International Space Station orbits,
	•	Interplanetary missions (using escape trajectories).

⸻

📌 Summary

Concept	Formula
Gravitational Force	F = \frac{GMm}{r^2}
Circular Velocity	v_c = \sqrt{\frac{GM}{r}}
Escape Velocity	v_e = \sqrt{\frac{2GM}{r}}

By adjusting the initial velocity vector, you simulate a range of orbital behaviors. This connects classical mechanics with modern astronautical engineering.