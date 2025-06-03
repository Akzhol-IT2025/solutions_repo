#📘 Problem 2: Forced Damped Pendulum

Objective:
Understand the motion of a pendulum under the influence of damping and external periodic forcing, and analyze how its behavior transitions from regular oscillations to complex or chaotic dynamics.

---

##🧠 What is a Forced Damped Pendulum?

A forced damped pendulum is a pendulum that experiences:
	•	A restoring force due to gravity
	•	A damping force that resists motion
	•	An external driving force that pushes it periodically

This combination leads to nonlinear motion, which can display a variety of behaviors — from simple oscillations to unpredictable chaos — depending on the system’s parameters.

---

##1️⃣ Governing Equation

The motion is described by a second-order nonlinear differential equation:

$$
\frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \sin(\theta) = A \cos(\omega t)
$$

Where:
	•	\theta(t) – angular displacement (radians)
	•	b – damping coefficient
	•	g – gravitational acceleration (~9.8 m/s²)
	•	L – length of the pendulum (meters)
	•	A – amplitude of the driving force
	•	\omega – angular frequency of the driving force

---

##2️⃣ Small-Angle Approximation

For small angles (\theta \ll 1), we use the approximation:

$$
\sin(\theta) \approx \theta
$$

This simplifies the equation to a linear form:

$$
\frac{d^2\theta}{dt^2} + b \frac{d\theta}{dt} + \frac{g}{L} \theta = A \cos(\omega t)
$$

This form helps us study resonance and system stability under small oscillations.

---

##3️⃣ Types of Motion

Depending on the system’s parameters, the pendulum may exhibit:
	•	Periodic motion – predictable and repeating cycles
	•	Quasiperiodic motion – structured but non-repeating
	•	Chaotic motion – irregular, sensitive to initial conditions

These behaviors are typically studied using:
	•	Time-domain plots
	•	Phase space diagrams
	•	Poincaré sections
	•	Bifurcation diagrams

---

##4️⃣ Parameter Influence

Key parameters that affect the system:
	•	Damping coefficient (b): controls how quickly motion decays
	•	Driving amplitude (A): higher values can trigger chaotic behavior
	•	Driving frequency (ω): near-resonance increases oscillation amplitude

At resonance \omega \approx \sqrt{\frac{g}{L}}, the system experiences large amplitude oscillations if not heavily damped.

---

##✅ Summary of Key Variables

Symbol	Meaning
\theta	Angular displacement (radians)
b	Damping coefficient
g	Acceleration due to gravity (~9.8 m/s²)
L	Length of the pendulum (meters)
A	Driving force amplitude
\omega	Driving force frequency (rad/s)
t	Time (seconds)


---

##📌 Applications

Forced damped pendulum dynamics are applied in:
	•	Engineering (vibration damping, resonance analysis)
	•	Electrical circuits (driven RLC circuits)
	•	Biomechanics (human walking and posture)
	•	Energy harvesting systems
	•	Climate and atmospheric modeling

---



🖼️ Diagram

![alt text](<Screenshot 2025-06-03 at 16.15.21.png>)
![alt text](<Screenshot 2025-06-03 at 16.16.14.png>)

Figure: Angular Displacement Over Time

This plot shows the evolution of angular displacement $$\theta(t)$$over 30 seconds.
	•	The motion starts at $$\theta_0 = 0.2 \, \text{rad}$$
	•	The periodic external force (with amplitude A = 1.2) keeps the oscillation going
	•	Despite damping b = 0.5, the system reaches a steady-state oscillation

 Phase Space: 

$$\theta vs. \frac{d\theta}{dt}$$
This plot illustrates the phase space trajectory, showing how angle and angular velocity evolve:	
The path forms a nearly closed loop, indicating stable periodic motion	
A more complex trajectory or spiral would suggest quasiperiodic or chaotic behavior
Here, the motion remains regular due to moderate damping and forcing