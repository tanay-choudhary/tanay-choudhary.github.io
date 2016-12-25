---
layout: project
title:  "A PYTHON LIBRARY FOR ROBOTIC MANIPULATION"
date:   2015-12-09 16:54:46
categories:
- project
img: roblib.gif
carousel:
- ur5.png
- wam.png
- timescaling.png
website: https://github.com/tanay-bits/robo-lib
---
A Python Library for Robotic Manipulation
-----------------

As part of [Prof. Kevin Lynch](http://www.mccormick.northwestern.edu/research-faculty/directory/profiles/lynch-kevin.html)'s class, [Robotic Manipulation](http://www.mccormick.northwestern.edu/mechanical/courses/descriptions/449-robotic-manipulation.html), I wrote a Python library of functions to implement the concepts learned in class. The functions span from basic operations on SO(3) and SE(3) elements, screw axes, matrix exponentials, calculating Jacobians, to more advanced algorithmic procedures like numerical inverse kinematics and dynamics, polynomial time-scaling and optimum joint trajectory generation. Head to the repository [here](https://github.com/tanay-bits/robo-lib) for the commented code.   

Many of these functions were used to [simulate real robots](https://gist.github.com/sherifm/f76cab0e785943f9aadc) - the [UR5](http://www.universal-robots.com/products/ur5-robot/) (6DoF) and [WAM](http://www.barrett.com/DS_WAM.pdf) (7DoF) robotic arms - using their URDF files. Below are some simulations visualized in [RViz](http://wiki.ros.org/rviz) - the 3D visualization tool for ROS.

UR5 Robot Straight Line End-Effector Trajectory:
![ee](http://i.giphy.com/FvQo7RQFhoIaQ.gif)

UR5 Robot Straight Line Joint-Space Trajectory:
![js](http://i.giphy.com/eX0abp1dbLtKg.gif)

### Project Dependencies:

<br />  

![Python](https://static.wixstatic.com/media/4df942_8017c46cfbbd47a5b157b97f6764562c.png/v1/fill/w_156,h_46,al_c,usm_0.50_1.20_0.00/4df942_8017c46cfbbd47a5b157b97f6764562c.png)&nbsp; &nbsp;
<img src="https://raw.githubusercontent.com/ros-visualization/rviz/indigo-devel/images/splash.png" alt="RViz" height="200" width="130">