---
layout: project
title:  "REAL-TIME FACE RECOGNITION (EIGENFACES AND FISHERFACES)"
date:   2016-02-22 16:54:46
categories:
- project
img: facerec.png
carousel:
website: http://github.com/tanay-bits/cvlib/tree/master/Face%20Recognition
---
Real-Time Face Detection and Recognition (Eigenfaces and Fisherfaces) Using OpenCV+Python
-----------------

This is a small Python program I wrote in collaboration with [Abhishek Patil](https://patilnabhi.github.io/portfolio/) as a final project for [EECS 332](http://www.mccormick.northwestern.edu/eecs/courses/descriptions/332.html): Introduction to Computer Vision, winter 2016. It performs [face detection using Haar cascades](http://docs.opencv.org/3.1.0/d7/d8b/tutorial_py_face_detection.html#gsc.tab=0) based on the [Viola-Jones framework](https://en.wikipedia.org/wiki/Viola%E2%80%93Jones_object_detection_framework), as well as face recognition with a choice of two of the most popular algorithms for this purpose - EigenFaces and FisherFaces. For a detailed introduction to these techniques, refer to [this tutorial](http://docs.opencv.org/2.4/modules/contrib/doc/facerec/facerec_tutorial.html).

<iframe width="560" height="315" src="https://www.youtube.com/embed/nvPzOo8tyUs" frameborder="0" allowfullscreen></iframe>

Program Interface
----------------------

![sec](https://raw.githubusercontent.com/tanay-bits/cvlib/master/Face%20Recognition/misc/flow_chart.png)

+  Save the Python scripts and XML files (from the GitHub repository) in a directory and create a subdirectory within it named "face_data".
+  Run the *gui_face.py* script to start up the program. Type in the user's name and hit *Train (FisherFaces)* or *Train (EigenFaces)*. Note that FisherFaces requires at least two users trained, for [LDA](https://en.wikipedia.org/wiki/Linear_discriminant_analysis) to work.

![sec](https://raw.githubusercontent.com/tanay-bits/cvlib/master/Face%20Recognition/misc/gui.png)

+  A webcam feed is opened from which photos of the user's face are detected and captured (stored in a folder corresponding to the user within the "face_data" folder) at regular intervals. The number of images captured to make the user's training dataset is set in *face_train_fisher.py* and *face_train_eigen.py* as the value of global variable *NUM_TRAINING* (currently 100). For the algorithms to work robustly, it is advisable to capture photos of the face at several distances, with different expressions, and different background lighting conditions. If there is someone else near you, make sure that during the capturing process, you (the intended user for whom the training set is being created) are in closest to the camera, to ensure only your face is captured. Once training images are captured, hit 'q' on your keyboard to close the webcam feed.

![sec](https://raw.githubusercontent.com/tanay-bits/cvlib/master/Face%20Recognition/misc/Capture.PNG)

+  Other users who wish to be recognized should take turns to enter their names in the GUI and use the desired training method, going through the same process as described above.
+  Once all users have finished making their training sets, press *Recognize (FisherFaces)* or *Recognize (EigenFaces)*, depending on the method that was used for training. A webcam feed pops up, which shows blue boxes around recognized faces (and shows their name and confidence value), and red boxes around unknown faces.
+ The lower the confidence value, the more accurate is the recognition.
+ Every time you train a face, the training data is updated instead of overwritten, which means you can add to a previous user's training data in different lighting/distance settings later on.

Results
---------

![sec](https://raw.githubusercontent.com/tanay-bits/cvlib/master/Face%20Recognition/misc/Results.png)

+ There is a clear difference between the confidence values reported by the two algorithms - FisherFaces results in much lower confidence values (=> more accurate) than EigenFaces.
+ Having more pictures in each user's dataset, both in number and in diversity of setting (expression, lighting, distance, etc.) produces more reliable recognition compared to small datasets in the same location. But in any case, Fisherfaces is more robust against external sources of variation like illumnination, since it also takes into account the training images' label when doing classification.
+ Because of higher confidence values and hand-picked threshold for the same, the number of misclassifications was generally higher when using Eigenfaces as compared to Fisherfaces. Hence, Fisherfaces was decided as our preferred face recognition method.

Conclusion
-----------

Face detection using the Viola-Jones framework is very fast and accurate, at least for frontal face images. But it can be also made to work on profile face images by using a suitable cascade of Haar features. However, robustly detecting partially occluded faces is still something a computer has a hard time doing (whereas we humans can do it easily). The Eigenfaces approach extracts the key sources of information (principal components) from a face image and combines them into a useful representation on which classification can be performed. This is quite analogous to how the human brain’s visual cortex encodes different local features from a scene into a cohesive pattern we can categorize. This task is made easier by the inherent dimension reduction offered by PCA. However, Eigenfaces does not perform classification between the different labels associated with the overall training dataset. If much of the variance in the training data is created due to external sources such as illumination, the principal components will represent those irrelevant variations instead of variations arising from difference in facial features. That is why Eigenfaces is more sensitive to external conditions, and performs poorly in contrast to Fisherfaces, which does class-specific projection with LDA.

But these two are not the only methods of achieving good face recognition. The scope for our future work involves exploring methods for local feature extraction which promise robustness against partial occlusion, illumination and small sample sizes, such as Local Binary Patterns, Discrete Cosinus Transform, and Gabor Wavelets.

Project Dependencies
-----

<img src="https://static.wixstatic.com/media/4df942_9a744943a3304bd59d9b90bf954e43db.png/v1/fill/w_81,h_100,al_c,usm_0.50_1.20_0.00/4df942_9a744943a3304bd59d9b90bf954e43db.png" alt="OpenCV" height="40" width="40"> &nbsp; &nbsp;
![Python](https://static.wixstatic.com/media/4df942_8017c46cfbbd47a5b157b97f6764562c.png/v1/fill/w_156,h_46,al_c,usm_0.50_1.20_0.00/4df942_8017c46cfbbd47a5b157b97f6764562c.png)

