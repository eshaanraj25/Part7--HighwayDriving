# Project: Path Planning - Highway Driving

[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

Overview
---
In this project the goal is to safely navigate around a virtual highway with other traffic that is driving +-10 MPH of the 50 MPH speed limit. The car's localization and sensor fusion data is provided. There is also a sparse map list of waypoints around the highway. The car should try to go as close as possible to the 50 MPH speed limit, which means passing slower traffic when possible, The other cars try to change lanes too. The car should avoid hitting other cars at all cost as well as driving inside of the marked road lanes at all times, unless going from one lane to another. The car should be able to make one complete loop around the 6946m highway. Since the car is trying to go 50 MPH, it should take a little over 5 minutes to complete 1 loop. Also the car should not experience total acceleration over 10 m/s^2 and jerk that is greater than 10 m/s^3.

Getting Started
---

The project has been developed on a Linux machine with Python 3.6. The system was provided by Udacity for this particular project.

## Prerequisites
Following are the dependencies:

- cmake >= 3.5
- make >= 4.1
- gcc/g++ >= 5.4
- Udacity's Term 2 Simulator. [Link](https://github.com/udacity/self-driving-car-sim/releases)

To install the dependencies, use the script [install-linux.sh](install-linux.sh)

Using the application
---

## Build
Use the commands to build the project:

```bash
./clean.sh
./build.sh
```

## Run
After building the project, run the project:

```bash
./run.sh
```

## Results

[Youtube](https://youtu.be/j5KdjTNzlbE) video for the same

## Acknowledgements

A really helpful resource for doing this project and creating smooth trajectories was using http://kluge.in-chemnitz.de/opensource/spline/, the spline function is in a single header file is really easy to use.