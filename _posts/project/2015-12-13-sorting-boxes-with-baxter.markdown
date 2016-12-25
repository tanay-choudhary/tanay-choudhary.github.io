---
layout: project
title:  "VISUAL SERVOING TO SORT OBJECTS WITH BAXTER USING ROS"
date:   2015-12-13 16:54:46
categories:
- project
img: baxter_builder.png
carousel:
website: https://github.com/opti545/baxter_builder
---
Visual Servoing to Sort Objects With Baxter Using ROS
-----------

### Overview:

*	Making the Baxter robot pick green and red blocks and place them in their respective boxes.
*	The Services framework of ROS was used for communicating between nodes, MoveIt! and TRAC-IK were used for motion planning, and OpenCV image processing was done on the left hand camera feed to detect objects.
*   Most of my contribution was using OpenCV to process the left-hand camera feed (thresholding, morphological operations, finding centroids of contours), and experimentally finding the camera calibration factor to convert pixel coordinates to Baxter's base frame coordinates.
*	This was the final project of the course [Embedded Systems in Robotics](https://www.mccormick.northwestern.edu/mechanical/courses/descriptions/495-embedded-systems-in-robotics.html), taught by [Dr. Jarvis Schultz](https://nxr.northwestern.edu/people/jarvis-schultz) at Northwestern University.
Team members: Jose Miranda, Sofya Akhmametyeva, Yves Nazon and Tanay Choudhary
*	For the complete documentation and code, head to the GitHub page [here](https://github.com/opti545/baxter_builder)

<iframe src="https://player.vimeo.com/video/149335007" width="500" height="275" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
<p><a href="https://vimeo.com/149335007">Baxter Sorting Objects by Color</a> from <a href="https://vimeo.com/user15691748">Tanay Choudhary</a> on <a href="https://vimeo.com">Vimeo</a>.</p>
<br />

### Project Dependencies:

<img src="https://static.wixstatic.com/media/4df942_bb8a7365e4874634aced781a6bc6ec95.png/v1/fill/w_161,h_43,al_c,usm_0.50_1.20_0.00/4df942_bb8a7365e4874634aced781a6bc6ec95.png" alt="ROS" height="80" width="100"> &nbsp; &nbsp;
<img src="https://static.wixstatic.com/media/4df942_9a744943a3304bd59d9b90bf954e43db.png/v1/fill/w_81,h_100,al_c,usm_0.50_1.20_0.00/4df942_9a744943a3304bd59d9b90bf954e43db.png" alt="OpenCV" height="40" width="40"> &nbsp; &nbsp;
![Python](https://static.wixstatic.com/media/4df942_8017c46cfbbd47a5b157b97f6764562c.png/v1/fill/w_156,h_46,al_c,usm_0.50_1.20_0.00/4df942_8017c46cfbbd47a5b157b97f6764562c.png)&nbsp; &nbsp;
<img src="https://gazebosim.org/assets/logos/gazebo_vert_pos-2db9e2180ddedd4245ffc709453c5ec0.png" alt="Gazebo" height="100" width="100">
<img src="https://i.imgur.com/jXlM9XN.png?1" alt="Baxter" height="80" width="150"> &nbsp; &nbsp;
<img src="https://sdk.rethinkrobotics.com/mediawiki-1.22.2/images/6/66/Moveit_logo.png" alt="MoveIt" height="80" width="150"> 
