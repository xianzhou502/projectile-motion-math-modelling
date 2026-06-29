# Projectile Motion with Air Resistance

## Overview

This is an undergraduate mathematical modelling project that studies the trajectory of a projectile under gravity and linear air resistance.

The project models an airgun pellet launched from an initial height with an initial speed and angle. Instead of using the ideal projectile model that ignores air resistance, this analysis introduces a drag force proportional to velocity, making the motion more realistic and mathematically richer.

Although this is a smaller project, it demonstrates several important modelling skills: translating a physical problem into differential equations, solving the equations symbolically, using numerical methods when closed-form solutions are difficult, and visualising how model behaviour changes with launch angle.

## Project Aim

The aim of this project is to model the flight path of a pellet and investigate:

* The projectile trajectory under linear air resistance
* The maximum horizontal range across launch angles
* The effective range before the pellet slows below a specified speed threshold
* How the trajectory changes as the launch angle varies

## Mathematical Model

The projectile is modelled using Newton’s second law.

Let:

* (m) be the mass of the pellet
* (r) be the air resistance coefficient
* (v_0) be the initial speed
* (\theta) be the launch angle
* (g) be the gravitational acceleration
* (x(t)) and (y(t)) be the horizontal and vertical positions at time (t)

The horizontal motion is affected by air resistance:

[
\ddot{x}(t) = -\frac{r}{m}\dot{x}(t)
]

The vertical motion is affected by both gravity and air resistance:

[
\ddot{y}(t) = -g - \frac{r}{m}\dot{y}(t)
]

The full trajectory is represented as the parametric curve:

[
(x(t), y(t))
]

## Methods

The project combines symbolic mathematics and numerical computation.

### 1. Symbolic Derivation

The differential equations for horizontal and vertical motion are solved symbolically to obtain expressions for (x(t)), (y(t)), and projectile speed.

### 2. Numerical Root-Finding

Because the landing time cannot always be solved cleanly in closed form, numerical root-finding is used to estimate the time when the projectile hits the ground.

### 3. Maximum Range Analysis

For each launch angle, the model estimates the time when the pellet reaches the ground and computes the horizontal range. This allows the maximum range to be studied as a function of the launch angle.

### 4. Effective Range Analysis

The project also defines an effective range based on the condition that the projectile remains above ground and maintains sufficient speed.

This adds a practical modelling layer: the projectile may continue flying, but its effective range is limited once its speed drops below the chosen threshold.

### 5. Animation and Visualisation

The notebook includes trajectory visualisations and an animation showing how the full trajectory and effective trajectory change with launch angle.

## Key Features

* Models projectile motion with air resistance
* Uses differential equations to describe physical motion
* Applies symbolic mathematics to derive motion equations
* Uses numerical methods to solve landing-time and speed-threshold problems
* Compares full range and effective range
* Visualises projectile trajectories across launch angles
* Includes an animation of changing launch trajectories

## Tools Used

* Python
* Jupyter Notebook
* SymPy
* SciPy
* NumPy
* Matplotlib

## Project Files

| File                                                  | Description                                                                                     |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `Math Modelling_The trajectory of a projectile.ipynb` | Main Jupyter Notebook containing the mathematical derivation, computation, plots, and animation |
| `Math Modelling_The trajectory of a projectile.html`  | HTML export of the notebook for easier viewing                                                  |

## Skills Demonstrated

* Mathematical modelling
* Differential equations
* Newtonian mechanics
* Symbolic computation
* Numerical root-finding
* Scientific programming
* Simulation
* Data visualisation
* Technical communication
* Python-based mathematical analysis

## Why This Project Matters

This project is a compact example of applied mathematics in action. It shows how a real-world physical problem can be converted into equations, solved using computational tools, and interpreted through visual output.

For a portfolio, this project helps demonstrate mathematical foundations behind modelling and simulation. It is especially useful as supporting evidence for quantitative problem-solving skills developed during undergraduate study.

## Limitations

This model uses linear air resistance, which is mathematically convenient but simplified. In real projectile motion, drag may be nonlinear and affected by factors such as pellet shape, air density, wind, spin, and changing environmental conditions.

The model should therefore be viewed as a mathematical modelling exercise rather than a fully realistic ballistic simulation.

## Conclusion

This project demonstrates how symbolic calculation and numerical methods can work together in mathematical modelling. By deriving the projectile equations, estimating maximum and effective range, and visualising trajectories across launch angles, the notebook provides a clear and practical example of computational mathematics applied to a physical system.
