# Enhanced V-J Vehicle detection method from UAV imagery

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
