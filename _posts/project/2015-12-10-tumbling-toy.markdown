---
layout: project
title:  "NONLINEAR DYNAMICS OF THE TUMBLING TOY AND MORE"
date:   2015-12-10 16:54:46
categories:
- project
img: vyk05.gif
carousel:
- tumble2.png
- tumble.jpg
website: https://github.com/tanay-bits/tumbling-toy
---
Nonlinear Dynamics of the Tumbling Toy   
-----------------

### Overview:

This was my final project for [Prof. Todd Murphey](http://www.mccormick.northwestern.edu/research-faculty/directory/profiles/murphey-todd.html)'s class, [Theory of Machines - Dynamics](http://www.mccormick.northwestern.edu/mechanical/courses/descriptions/314-theory-of-machines-dynamics.html). It involved modeling and simulating (on Mathematica) the impact-driven nonlinear dynamics of the tumbling toy, which consists of   

+	a hollow wooden case with a pivot on each side, 
+	a metal ball which can roll along the long axis of the case,
+	an inclined saw-toothed rail on which the pivots step down.   

Click below to see a video of the toy in action (credits - Bruce Yeany):
<iframe width="560" height="315" src="https://www.youtube.com/embed/CfCqWEdos2A" frameborder="0" allowfullscreen></iframe> 

This multibody system has been of special interest to researchers due to its complex dynamical behaviour. The tumbling motion is characterized by the alternating rotation of the case around one of the two pivots with the rolling of the ball from end to end of the case. The system has 4 degrees of freedom, which are the configuration variables of the simulation: q = [xRC,  yRC,  θ,  xCB]<sup>T</sup> , where xRC and yRC are the tangential and normal displacement of the CoM of the case relative to the rail, and θ is the rotation of the of the case with respect to the rail. xCB is the displacement of the ball within the body. Below are short animations of the simulation from two different sets of initial conditions:   

![Animation](/assets/img/project/tumblanim.gif)

![Animation2](/assets/img/project/tumblarbitinit.gif)


Following impacts govern the motion of the system:   

*   Impacts of the ball with the ends of the case
*   Elastic impacts of the pivots on the rail    

The modeling assumptions are:   

+   Friction between the pivots and the rail in negligible, hence it is ignored
+   The ball is considered a point mass moving without friction within the case
+   All impacts are elastic
+   Pivots are triangular prisms, instead of cylinders (to make impacts less cumbersome to handle)


### Coordinate Frames of the Modeled System:
![Frames](http://i.imgur.com/qZo6kcu.png?1)   
![Transformations](/assets/img/project/tfs.png)   

### Problem Set-Up and Simulation:   
The inertial and geometric parameters were sourced from [this paper](http://www.inm.uni-stuttgart.de/mitarbeiter/leine/papers/journal_publications/Leine_x_van_Campen_x_Glocker_-_Nonlinear_Dynamics_and_Modeling_of_Various_Wooden_Toys_with_Impact_and_Friction.pdf) by Leine, Campen, and Glocker, which used the Newton-Euler approach to solve this system. I instead used the Variational Principle (Lagrangian Dynamics) to get the equations of motion.   

The kinetic energy of the case and the ball were written in terms of their body velocities. The potential energy of each was found using homogeneous transformations to represent height in world frame. With the Lagrangian now available, 4 Euler-Lagrange equations (one corresponding to each state variable) were written. The RHS of each eq. was 0, since the only constraint (ball’s translation confined to the case) is embedded within the transformation matrix from the case to the ball, and there are no external forces.   

Mathematica's *NDSolve* is used to numerically integrate the Euler-Lagrange equations, with arbitrarily chosen initial conditions. However, this integration is done piecewise, since it is stopped whenever an impact is detected (using *WhenEvent*). 8 impact conditions were checked at every instant (6 from the vertices of the two triangular pivots, and 2 from the ball hitting the case’s ends). After every impact, new initial conditions for integration are found by solving the impact laws of momentum change and Hamiltonian conservation (giving 5 eqs.). It is assumed that at any instant only one impact condition from the 8 is true.  


Some Other Dynamic Systems Simulated Using the Variational Principle During the Course
-----------------

### Modeling the Splits:
![splits](/assets/img/project/splits.gif)

### Triple Pendulum and Impact:
![tripend](/assets/img/project/tripend.gif)
![tripendhit](/assets/img/project/tripendhit.gif)

### Constrained Triple Pendulum:
![conpend](/assets/img/project/conpend.gif)


### Project Dependencies:

<img src="https://static.wixstatic.com/media/4df942_0d7bfd5e9ccf41a0a8f064c179ec22ec.png/v1/fill/w_301,h_224,al_c,usm_0.50_1.20_0.00/4df942_0d7bfd5e9ccf41a0a8f064c179ec22ec.png" alt="Mathematica" height="140" width="140">
