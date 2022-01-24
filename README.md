# 1.Enhanced V-J Vehicle detection method from UAV imagery

The aim is to track the vehicles on the road from an UAV using
Viola-Jones technique. First the images are obtained from the 
video and transformed into gray scale image. Since most of the
object detection algorithm such as V-J can only detect vehicle
in similar oreintation. To do so the line segment on the road
is detected and orientation of each detected line segment is 
calculated. The angle corresponding to the maximum distribution
frequeny of realtive histogram will be the oreintaion of the 
road. To minimize the in-plane rotation jitters, the final
rotation angle for frame is smoothed by the first-order lag 
filtering algorithm, which considers the roation angle from the
last frame.

## Advantages

This method has the best tracking speed when compared to other
methods such as Particle filter, Kalman Filter, Templte Macthing
, KLT Tracker and KCF tracker.
This method also has the best correctness.
It can be used for position prediction.

## Disadvantages

The method is sensitive to lighting condition. So the captured 
images should be pre-processed to overcome illumnation variation.


# 2.Vehicle Detectin using Cascaded Support Vector Machine and Gaussian Mixture Model

The aim of the system is to develop an algorithm that will autonomously
detect vehicles from UAV images. Here the background of the image
is removed first suign GMM which will reduce computational complexity by 
reducing the search space. The next step is feature extraction by means
of edge detection, corner detection, color transformation and classification.
The third step is SVM based vehicle classification.SVM provides a robust, 
accurate and effective technique for pattern recognition and classification.
The last step is Detection enhancement using GMM which is kind of fine
tuning to get hign performance.

## Advantages

The cascaded SVM-GMM classifier method ensure higher performance when 
compared to the single classifier based vehicle detection algorithm.
Proposed system gives 87.5% hit rate, 94.7% accuracy and 100% precision 
values.

## Disadvantages

The main challenge is the dataset complexity. Since the image inputs 
are depending upon the height, Position and Tilting of Cameras.
