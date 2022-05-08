# Model Documentation

All the code for the project is present in `main.cpp` file, along with some
helper functions in `helpers.h`, and the spline generation function in 
`spline.h`.

## Analyzing Car Trajectories
Lines(108 - 159). This part of the code analyzes the other cars on the highway.
Three boolean variables are declared to determine if there are any cars on the
front, to the left or to the right of the ego car.

Looping over all the cars in the sensor data one by one, their respective lanes
are determined and their speeds are calculated. Using these two data, the
above three boolean values are calculated, if the other vehicle is in the +30
or -30 range, left, right or center.

## Deciding Next State
Lines(161 - 191). This part of the code decides the next state for the robot to
be in, after analyzing the other cars on the highway. The first decision is
made about lane change if there is a car in front of the robot. If there are no
cars on the left, then left lane is taken. If there are no cars on the right,
then right lane is taken. If a lane change is not possible, then the robot car
is slowed down.

Also, if there are no cars in front of the robot, then the robot tries to move towards the center lane and speeds up if possible.

## Generate Trajectory Points
Lines(193 - 310). This part of the code generates a Spline trajectory for the
robot to follow. This code is mainly taken from the starter code that is
provided. 

First path smoothing is done, by taking some initial points from the previous
planned trajectory. Then, next waypoints are decided by making use of Frenet
Frame method, and added to the list of points. Then a spline is generated from
these points and these points are added to the trajectory for the robot to
follow next.