# Simple Pendulum: Numerical vs Analytical Solution

## Description
This project investigates the motion of a simple pendulum by numerical solution of the non-linear equation. This solution obtained using Runge-Kutta 4th order method then compared with analytical solution which obtained by small angle approximation.

## Objectives
- to implement the fourth-order of Runge-Kutta method
- to compare the numerical solution with the analytical small-angle approximation solution
- to investigate the effect of the initial angular displacement on the motion

## Physics
Consider a pendulum of mass m and length L of string fixed to the ceiling, deflected with an initial angle $\theta$ and allowed to swing under the influence of gravity.

From Newton 2nd law of rotational motion:

$$
\tau = I\alpha
$$

the gravitational 
for a point mass:

$$
I = mL^2
$$

and,

$$
\alpha = \frac{d^2\theta}{dt^2}
$$

Therefore

