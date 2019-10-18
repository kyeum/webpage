---
title: "Software and Control in Ski Robot Challenge 2018"
date: 2018-05-26 08:26:28 -0400
categories: Humanoid Robotics
---

# Software and Control in Ski Robot Challenge 2018
## Skiing Robot System
![title](/photos/Robot System.png){: width="50%" height="50%"}

Skirobot Software should gather all the thesises and algorithms to get it to fit the ski robot, and we should implement each program sources into one main program. The main system is with MFC dialog C++ based system and it has to be able to use all devices which are involved in Lidar, Zed, Motors. This diagram shows all module's communication in the system


## Main software
![title](/photos/Main software.png){: width="80%" height="80%"}

This is main system in Skirobot using MFC C++ dialog. With mirroring device, user use this program and examine the specific data for better result. This system include Ski thesis, Path algorithm, Flag detection which is main source in the skiing robot.

## Ski Thesis
![title](/photos/Skirobot_thesis.png){: width="30%" height="30%"} ![title](/photos/Skirobot_snowthesis.png){: width="30%" height="30%"}
We did a research on not only ski but also the snow affects.

![title](/photos/ski_inversekinematics.png){: width="80%" height="80%"}
Calculate inversekinematics based on double-four-linkange system in each leg, we would like to determine how skiing works in path planning.

## Path algoritm
![title](/photos/Path algoritm2.png){: width="80%" height="80%"}

Used Dubins’ path planning Algorithms, build predetermined path before having feedback
In geometry, the term Dubins path typically refers to the shortest curve that connects two points in the two-dimensional Euclidean plane (i.e. x-y plane) with a constraint on the curvature of the path and with prescribed initial and terminal tangents to the path, and an assumption that the vehicle traveling the path can only travel forward. If the vehicle can also travel in reverse, then the path follows the Reeds–Shepp curve.

## Skirobot_Balancing
![title](/photos/Skirobot_Loadcell.png){: width="50%" height="50%" ![title](/photos/Skirobot_zmp.png){: width="50%" height="50%"}

Balancing is important part in skiing robot since small disturbance or different center of gravity will change whole skiing thesis and path algorithm. Thus while skiing robot moves, it needs to balance for more accurate path planning. 


![title](/photos/Skirobot_pendulum2.png){: width="50%" height="50%"} ![title](/photos/Skirobot_control.png){: width="50%" height="50%"}



## Flag detection
![title](/photos/Flag detection.png){: width="80%" height="80%"}

There are 5 pairs of flags on the competition slope. Since it was random in the beginning, the robot should detect flags wisely. We use ZED stereo camera to detect colors as well as a distance between flags. Zed camera can detect depth image with in 10m, which can be enough for the skiing flag detection. In process, we parse RGB colors, Erode and Dilation process for removing errors, using point cloud for depth data. With the data already determined, length between two flags, we can detect the center of the two flags. 


![title](/photos/Lidar.png){: width="80%" height="80%"}

Lidar should be good way to improve depth detection. we used Hokuyo 2D lidar sensor. To use wisely, we added the servo motor for reducing tilted data. To get specific center data and depth data, i use k-means lalgorithm in clustering. Algorithm is like this. First, determine perceivable range in lidar. Second,after get multiple data use k-means algorithm to cluster two part. Third get center data in K-means which is for the estimated center data. Based on this mechanism, we can detect two centers of the flags and finally acquired the center of flags.


## Reference for the skiing robot

[1] L. Lahajnar, A. Kos, and B. Nemec, “Skiing robot-design, control, and navigation in unstructured environment,” Robotica, vol. 27, pp. 567–577, July 2009.

[2] B. Nemec and L. Lahajnar, “Control and navigation of the skiing robot,” in Proceedings of the 2009 IEEE/RSJ international conference on Intelligent robots and systems, ser. IROS’09. Piscataway, NJ, USA: IEEE Press, 2009, pp. 2321–2326.

[3] B. Nemec, J. Babic and L. Zlajpah, “Multilayer Control of Skiing Robot” in Proceedings of the 2011 IEEE/RSJ international conference on Intelligent robots and systems.


