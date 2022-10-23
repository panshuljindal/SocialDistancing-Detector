# SocialDistancing-Detector


With the help of computer vision and deep learning algorithm by using the
OpenCV, Tensor flow library we propose a system that focuses on how to
identify the person on a stream of image or video whether the social distancing
is maintained or not.

<h1>Approach</h1>
● With yolov3, detect human figures.
● Whoever and how many ever people are detected in the frame,
calculates the distances between each one of them.
● Display the number of people at high, neutral and low risk.

<h1>Target Audience</h1>
Mainly Small Businessman, wine shop owners, schools and colleges,
Government offices.
● Help our police force to maintain law and order of social distancing.
● Can be used in Temples, Mosques, church and other religious places,
where maintaining social distancing is a very difficult problem for the
government.

<h1>Module Description</h1></br>
● Calibration: It is the first step of the pipeline, which works by computing
the transform, into a box view. In this process, the simplest calibration
method involves selecting four points in the perspective view and
mapping them to the corners of a rectangle in the box view. There is the
assumption that each and every person is standing on the same flat
ground plane.</br>
● Detection of Objects: The second step is the detection of the pipeline
that involves applying a pedestrian detector to the perspective views to
draw a bounding box around each pedestrian. For this process, the
company used an opensource pedestrian detection network based on
the DNN architecture.<br>
● Measurement of Distance: The third step of the pipeline is where the
(x, y) location of the bounding box for each person has been estimated
in the box view. In order to scale the factor estimated from calibration,
then the last step becomes to compute the box-view distance between
every pair of people and also scale the distances. When the distance
between the people is below the minimum acceptable distance has been
depicted in red, and the rest are colored as green, and a line is drawn
between the people to emphasize this measure.<br>
● Feature Extraction: Feature Extraction is the fourth step of the
pipeline, which works after objects has been identified. This module
separates the human beings from all the other objects that are captured
in the image. In this we are making use of Dark Net Architecture for
making our work easier. We are using edge detection for implementing
this work.<br>
● Tracking: It is the fifth step of the pipeline. In this module we are
assigning the human beings relative spatial 2D coordinates with respect
to the closest person i.e., the largest possible image. Treat them as
vertices of the complete polygon with n vertices, where n is the number
of vertices it possesses and it will therefore have n*(n-1)/2 edges. <br>
● Verification: It is the sixth and the last step of the pipeline. As in the
above module we have find all the possible edges i.e., n*(n-1)/2 edges
with n persons, Therefore, we now check for all the possible edges and
then validate, if (distance >= 6feet) -> green box else red box.
