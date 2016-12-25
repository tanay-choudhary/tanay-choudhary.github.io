---
layout: project
title:  "DC MOTOR CONTROL"
date:   2016-03-01 11:54:46
categories:
- project
img: mechatronix.jpg
carousel:
website: https://github.com/tanay-bits/dcmotor-control
---
DC Motor Control with PIC32 and MATLAB
-----------------

Final project for [ME 333](http://www.mccormick.northwestern.edu/mechanical/courses/descriptions/333-introduction-to-mechatronics.html): Introduction to Mechatronics, winter 2016.

<iframe src="https://player.vimeo.com/video/159664527" width="500" height="281" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

The client, written in MATLAB, communicates with the PIC32 on the NU32 development board via serial port, sending control gains and desired setpoints and motion trajectories, and tracking results are sent back to the MATLAB client for plotting. The PIC32 manages a nested control loop system consisting of a PID outer motion control loop and a high-speed PI inner current (torque) control loop:

![control system](https://i.imgur.com/KWmw4yz.png)

With my chosen Kp and Ki, the current control performance was as below:

![current control](http://i.imgur.com/vBWJ8kG.png)

And the position control performance for arbitrary step and cubic trajectories was:

![step](http://i.imgur.com/bxHuNWf.png)
![cubic](http://i.imgur.com/qjho8r5.png)

The most important electronic components of the system and their interconnections are shown in the image below:

![schematic](http://i.imgur.com/uQvyMtY.png)


Project Dependencies
-----

<img src="https://static.wixstatic.com/media/4df942_6fde61c674654349a5c652751a603193.png/v1/fill/w_143,h_143,al_c,usm_0.50_1.20_0.00/4df942_6fde61c674654349a5c652751a603193.png" alt="MATLAB" height="110" width="110"> &nbsp; &nbsp;
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/The_C_Programming_Language_logo.svg/140px-The_C_Programming_Language_logo.svg.png" alt="C" height="110" width="110"> &nbsp; &nbsp;
![PIC32](http://www.mouser.com/images/microsites/Microchip-logo.gif)
