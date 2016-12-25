---
layout: project
title:  "STAIR CLIMBING WITH LOWER-LIMB WEARABLE ROBOTS"
date:   2015-05-08 16:54:46
categories:
- project
img: portfolio_04.jpg
carousel:
- walk.gif
- anklebot.jpg
- stairs.jpg
- marker.jpg
website:
---
Gait Analysis and Control Design for Stair Ambulation with Lower-limb Powered Prostheses
-----------------

I spent my final undergraduate semester at the [Lauflabor Locomotion Lab](https://lauflabor.ifs-tud.de/doku.php), TU Darmstadt, Germany for my bachelor's thesis under the guidance of [Prof. André Seyfarth](https://lauflabor.ifs-tud.de/doku.php?id=lab_members:lab_members_andreseyfarth).   

### Overview:  

*  Human lower limb joints and segments were investigated during level walking, stair ascent, and stair descent to determine their biomechanics for use in the design of new and robust powered prosthetic systems which can efficiently negotiate stairs in addition to walking on flat ground.
*  A motion-capture experiment with an instrumented staircase setup was performed with a healthy subject.
*  This study contributed two new control insights for gait intent and gait percent detection in wearable lower-extremity robots which are not available in the existing literature.
*  Significant savings in motor peak power and energy requirements across all gaits were obtained by optimizing the spring stiffness of the Series Elastic Actuator (SEA) based powered ankle prosthesis, which allows motor and battery dimensions to be kept to a minimum – an essential requirement of wearable robots.
*  The results showed that current powered prostheses can extend their capability beyond level walking to successfully negotiate stairs, with only minor modifications and sensor additions to their existing systems.  

![Stair Ambulation](/assets/img/project/stairamb.jpg)   

### Hypothesis:   

The primary challenge in conceptualizing a simplified prosthetic control scheme encompassing both level-ground walking and stair walking is to first ascertain if the kinematic and kinetic patterns are to be considered as particular evolution of the level walking pattern. This knowledge can, for example, serve as a reference for the imitation of natural motor control strategies in intelligent prostheses applied to walking on different terrains. If we compare the kinematic and kinetic patterns and are able to find a continuous progression in the patterns from stair descent (SD) to level-ground (LG) to stair ascent (SA), it would validate the hypothesis and allow the design of a unified controller for the three gaits.   

If however, the hypothesis turns out to be false, and the three gaits are actually three separate motor control strategies, we have to resort to a finite-state
controller. The pressing challenge then would become the discovery of
kinematic or kinetic parameters which can robustly perform the following two
functions:  

1.  Classify the 3 gait modes (LG, SA, SD) and detect a transition from one mode to another (for high-level controller).
2.  Track the current position within the particular gait cycle, i.e. act as a gait ‘clock’ or phase invariant (for middle-level controller).   
 
<h5 style="color:black;">Proposed hierarchical control scheme:</h5>
![Control Scheme](/assets/img/project/highlevel.jpg)  
<br /> 

### Motion Capture Experiment:  

<h5 style="color:black;">Click below to view a MATLAB animation of the motion capture experiment:</h5>
[![Animation](https://img.youtube.com/vi/C5TJHx1fBmA/0.jpg)](https://www.youtube.com/watch?v=C5TJHx1fBmA "MATLAB animation of the motion capture experiment")   

A healthy subject was asked to walk across a level walkway and up and down six steps. Motion-capture marker and force plate data were recorded and processed on MATLAB using low-pass Butterworth filter to estimate kinematic and kinetic patterns of motion for the three gait modes - Stair Ascent (SA), Stair Descent (SD), and Level Gait (LG).  

![Model](/assets/img/project/angles.png)
<h5 style="color:black;">Key joints, segments and angles. The cyan dotted line is the virtual leg (its angle is approximately the average of thigh and shank angles)</h5>  

### Key Results:  

![Ankle Work](/assets/img/project/AnkleWork.jpg)  
<br /> 
The results from a motion-capture experiment concluded that stair ambulation is not a particular evolution of
level-ground walking. Hence, a single graded control signal is not a viable solution. The ability to distinguish between the three gaits and choose appropriate control signal for each is necessary.


The Walk-Run Ankle from [SpringActive](https://www.springactive.com/) used in the experiment has a Series Elastic Actuator (SEA), to incorporate some of the inherent elastic nature of the human muscular system. After optimizing the spring stiffness based on peak motor power as well as energy required per gait cycle, significant energy savings were obtained:  

![MotorER](/assets/img/project/motorER.jpg)
[![MotorPower](/assets/img/project/powerprofiles.png)](/assets/img/project/powerprofiles.png "Click to see full size image")  

Finally, the thesis contributed two new control insights for gait intent and gait percent detection which are not available in the existing literature.  

### Future Work:  

This preliminary study presented useful general results, but to actually
implement them in a particular lower-limb wearable robot, more
comprehensive and customized trials are required – ones which include trans-
tibial amputees in addition to healthy subjects. How an amputee adjusts her gait in response to wearing the prosthesis, and how it might alter the natural
reference trajectories is a crucial aspect that needs to be explored. Future trials
should also incorporate different walking speeds – the effects of which need to be
studied in order to ensure a robust enough gait phase control.  

The results of this study have contributed a better understanding of the
biomechanics of stair ambulation in humans. Its applications are thus not limited
to the specific field of prosthetics, but may also be useful in other applications
which encounter stairs, like augmentation or rehabilitation exoskeletons and
bipedal robotics. But the ultimate success of this study would be the translation
of these insights into functional lower-limb prosthetic systems that greatly
reduce the metabolic cost of amputee stair ambulation, overcoming their
mobility challenges and thus improving quality of life.  

### Project Dependencies:  

<img src="https://static.wixstatic.com/media/4df942_6fde61c674654349a5c652751a603193.png/v1/fill/w_143,h_143,al_c,usm_0.50_1.20_0.00/4df942_6fde61c674654349a5c652751a603193.png" alt="MATLAB" height="110" width="110"> &nbsp; &nbsp;
![Qualisys Track Manager](https://www.delsys.com/wp-content/uploads/2014/04/Qualisys_Logo.gif)


