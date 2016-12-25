---
layout: project
title:  "TACTILE BRAILLE GLOVE FOR THE DEAFBLIND"
date:   2014-01-26 16:54:46
categories:
- project
img: haptic.jpg
carousel:
- glove.JPG
- solder.JPG
- team.JPG
website: https://github.com/tanay-bits/braille-glove
---
A Tactile Braille-based Mobile Communication and Translation Glove for the Deafblind
------------------------------

Team members: Tanay Choudhary, Saurabh Kulkarni, Pradyumna Reddy.   

Deafblind people are excluded from most forms of communication and information. This project, which was selected in the [Texas Instruments India Innovation Challenge 2014](https://e2e.ti.com/group/universityprogram/w/contests/2411.innovation-challenge-india), suggests a novel approach to support the communication and interaction of deafblind individuals, thus fostering their independence.

*   It includes a smart glove that translates the Braille alphabet, which is used almost universally by the literate deafblind population, into text and vice versa, and communicates the message via SMS to a remote contact. 
*   It enables user to convey simple messages by capacitive touch sensors as input sensors placed on the palmer side of the glove and converted to text by the PC/mobile phone. 
*   The wearer can perceive and interpret incoming messages by tactile feedback patterns of mini vibrational motors on the dorsal side of the glove. Since tactile sensitivity may vary from user to user, the system can be programmed to adjust the applied intensity via PWM to serve the individual user’s needs. 
*   We created a simple Android app for the system as well (shown at the end of the video below).  

The successful implementation of real-time duplex translation between English and Braille, and communication of the wearable device with a mobile phone/PC opens up new opportunities of information exchange which were hitherto unavailable to deafblind individuals, such as remote communication, as well as parallel one-to many broadcast. The glove also makes communicating with laypersons without knowledge of Braille possible. Perhaps most importantly, it can reduce dependence on trained interpreters (which is the most common but expensive option).  

We also presented a [paper at IEEE International Conference on Pervasive Computing 2015](http://dx.doi.org/10.1109/PERVASIVE.2015.7087033), the slides for which can be found [here](https://docs.google.com/presentation/d/1R4dQdzcAwUj9ac4KicE1NXhzODKzou9lrBKYr4DCpxQ/edit?usp=sharing). Click below to watch the demo video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/ONnZ_HP-dzM" frameborder="0" allowfullscreen></iframe> 

### System Overview:  

[![Input/Output Modes](http://i.imgur.com/wnVoP3r.png?1)](http://i.imgur.com/wnVoP3r.png?1 "Click to see full image")  

[![Prototype Hardware](http://i.imgur.com/bFXVYvd.jpg?1)](http://i.imgur.com/bFXVYvd.jpg?1 "Click to see full image")   

[![Algorithm](http://i.imgur.com/N8BBMIQ.png?1)](http://i.imgur.com/N8BBMIQ.png?1 "Click to see full image")   

[![Wireless](http://i.imgur.com/8kZsEx9.png?1)](http://i.imgur.com/8kZsEx9.png?1 "Click to see full image")  

<br />  

### Project Dependencies:

![Energia](https://www.ti.com/ww/en/launchpad/img/launchpad-energia-logo.png)&nbsp; &nbsp;
<img src="http://fizz.kiersmcfarlane.com/wp-content/uploads/2014/02/arduino_logo1.png" alt="Arduino" height="130" width="130">