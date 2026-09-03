# Simple Pendulum: Numerical vs Analytical Solution

## Description
This project investigates the motion of a simple pendulum by numerical solution of the non-linear equation. This solution obtained using Runge-Kutta 4th order method then compared with analytical solution which obtained by small angle approximation.

## Objectives
- to implement the fourth-order of Runge-Kutta method
- to compare the numerical solution with the analytical small-angle approximation solution
- to investigate the effect of the initial angular displacement on the motion

## Physics
A simple pendulum consisting of a point mass $m$ attached to a string of length $L$ to the ceiling. The pendulum is displaced from equilibrium by angular displacement $\theta$ and released under the influence of gravity.

The equation of motion is obtained from the rotational form of Newton's second law,

$$
\tau = I\alpha.
$$

The gravitational torque is,

$$
\tau = -mgL\sin\theta,
$$

where the negative sign indicates that the torque acts toward the equilibrium position. For a point mass,

$$
I = mL^2,
$$

and

$$
\alpha = \frac{d^2\theta}{dt^2}.
$$

Substituting these relations, gives the nonlinear equation of motion,

$$
\boxed{
\frac{d^2\theta}{dt^2} = -\frac{g}{L}\sin\theta
}
$$

### First-Order Form

For numerical integration using the fourth order Runge-Kutta (RK4) method, the second-order equation is expressed as a first-order equations. Defining the angular velocity as

$$
\omega = \frac{d\theta}{dt},
$$

thus

$$
\frac{d\theta}{dt} = \omega,
$$

$$
\frac{d\omega}{dt} = -\frac{g}{L}\sin\theta.
$$

The corresponding state vector is

$$
\mathbf{y} =
\begin{bmatrix}
\theta \\ \omega
\end{bmatrix}.
$$

## Analytical Solution

For small angular displacements, the $\sin\theta$ term can be approximated by

$$
\sin\theta \approx \theta.
$$

Thus

$$
\frac{d^2\theta}{dt^2} = - \frac{g}{L}\theta
$$

$$
\frac{d^2\theta}{dt^2} + \frac{g}{L}\theta = 0.
$$

This is the equation of a simple harmonic oscillator. For the initial conditions

$$
\theta(0)=\theta_0,
\qquad
\omega(0)=0,
$$

the analytical solution is

$$
\boxed{
\theta(t) = \theta_0 \cos\left(\sqrt{\frac{g}{L}}\,t\right)
}.
$$

This analytical solution is valid for small-angle approximation (can be proved by Taylor series). Therefore, its agreement with the numerical solution is expected to decrease as the initial angular displacement increases.

## Numerical Method

This nonlinear equation is solved using the classical fourth-order Runge-Kutta
(RK4) method, implemented from scratch in Python.
