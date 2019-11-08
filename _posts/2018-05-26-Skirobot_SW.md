---
title: "Software and Control in Ski Robot Challenge 2018"
date: 2018-05-26 08:26:28 -0400
categories: Humanoid Robotics
---

# Software and Control in Ski Robot Challenge 2018
## Skiing Robot System
![title](/photos/Robot System.png){: width="50%" height="50%"}

This is whole skirobot software architecture, which gather all the thesises and algorithms to get fit as a optimal system. We implemented each program sources into one main program for calculated thesis based robot system. We are using Visual studio 2015 MFC dialog C++ based system and it help to be able for using all devices. Lidar(Hokuyo 2D Lidar), Stereocamera(ZED Stereo camera) is for the detecting the flags. Motors(Maxon motor and Apex speed reducer) for the leg, Motors(Robotis Dynamixel) is for the arm, neck. We also use GPS, and FT sensor for accurate calculation. This diagram shows all module's communication in the system.

## Main software
![title](/photos/Main software.png){: width="80%" height="80%"}

In main system, we use CPU(i7-6700) with GPU(Geforce 1060) for controlling skiing robot. Following is MFC C++ dialog what our robot based on. With mirroring device(pokerty), we mirror the system how it works and examine the specific data for better result while realtime programming. This main system includes Path algoritm based on alphine-ski-thesis, Flag detection using Lidar and Stereo camera, and gather and calculate all communication data.


## Ski Thesis
![title](/photos/Skirobot_thesis.png){: width="30%" height="30%"} ![title](/photos/Skirobot_snowthesis.png){: width="30%" height="30%"}

Based on Alphine Ski thesis, the radius can be determined by the ski radius(depends on which ski you use). Since we need to get as small radius as possible, we decided to use children's ski for accurate ski path planning. Based on thermal status, the snow can impact this system a lot in respect to the radius. Thus, we needed to make a variables for snow to set up, which can be upgraded next version with the research based on ski edge pressure related to thermal status.


![title](/photos/ski_inversekinematics.png){: width="80%" height="80%"}

We use double-four-linkage system in each leg. With the help of the Ski thesis, we can easily calculate each angle of the joint using inverse kinematics. So to speak, path can be determined by each legs angle position.

## Path algoritm
![title](/photos/Path algoritm2.png){: width="80%" height="80%"}

We selected Dubins’ path planning Algorithms; making any route using radius and straight line; typically used for cargo ship. This algorithm makes predetermined path before any sensor feedback. Specifically, In geometry, the term Dubins path typically refers to the shortest curve that connects two points in the two-dimensional Euclidean plane (i.e. x-y plane) with a constraint on the curvature of the path and with prescribed initial and terminal tangents to the path, and an assumption that the vehicle traveling the path can only travel forward. If the vehicle can also travel in reverse, then the path follows the Reeds–Shepp curve.


## Skirobot_Balancing
![title](/photos/Skirobot_Loadcell.png){: width="50%" height="50%" ![title](/photos/Skirobot_zmp.png){: width="50%" height="50%"}

Balancing is important part in skiing robot since small disturbance or different center of gravity will change whole skiing thesis and path algorithm. The humanoid robot needs to balance for more accurate path planning. Each leg has force sensor on bottom for ZMP control
and the body have a pendulum system to compensate any disturabance.

![title](/photos/Skirobot_pendulum2.png){: width="50%" height="50%"} 

![title](/photos/Skirobot_control.png){: width="80%" height="80%"}

Zero moment point is a concept related with dynamics and control of legged locomotion, e.g., for humanoid robots. It specifies the point with respect to which dynamic reaction force at the contact of the foot with the ground does not produce any moment in the horizontal direction, i.e. the point where the total of horizontal inertia and gravity forces equals 0 (zero). The concept assumes the contact area is planar and has sufficiently high friction to keep the feet from sliding.


## Flag detection
![title](/photos/Flag detection.png){: width="80%" height="80%"}

There are 5 pairs of flags on the competition slope. Since it was random in the beginning, the robot should detect flags wisely. We use ZED stereo camera to detect colors as well as a distance. Zed camera can detect depth image with in 10m, which can be enough for the skiing flag detection, but we also use lidar sensor for more accurate depth data. The vison process follows like this.

1. Parsed RGB colors and change to HSV(Since the environment changes, we add funtion automatically check HSV data in that circumstances)
2. Erode and Dilation process for removing errors.
3. USE point cloud for depth data in ZED stereocamera. 

With this data, we can get length between two flags based on robot orientation.

![title](/photos/Lidar.png){: width="80%" height="80%"}

Lidar should be good way to improve depth detection. we used Hokuyo 2D lidar sensor for wisely detect the flags. We added the servo motor for reducing and examine tilted data with encoder in the motor. To get specific center data and depth data, I added k-means deep learning algorithm in clustering.

1. Determine perceivable range in lidar. 
2. Use k-means algorithm to cluster two part of the scanned data. 
3. Get center data in K-means which is for the estimated center data. Based on this mechanism, we can detect two centers of the flags and finally acquired the center of flags.


## Reference for the skiing robot

[1] L. Lahajnar, A. Kos, and B. Nemec, “Skiing robot-design, control, and navigation in unstructured environment,” Robotica, vol. 27, pp. 567–577, July 2009.

[2] B. Nemec and L. Lahajnar, “Control and navigation of the skiing robot,” in Proceedings of the 2009 IEEE/RSJ international conference on Intelligent robots and systems, ser. IROS’09. Piscataway, NJ, USA: IEEE Press, 2009, pp. 2321–2326.

[3] B. Nemec, J. Babic and L. Zlajpah, “Multilayer Control of Skiing Robot” in Proceedings of the 2011 IEEE/RSJ international conference on Intelligent robots and systems,

[4] M. Walker, H. Culbertson, M. Raitor and M. Okamura “Haptic Orientation Guidance Using Two Parallel Double-Gimbal Control Moment Gyroscopes“ IEEE TRANSACTIONS ON HAPTICS, JUNE 2017

[5] Ski sidecut radius and radius of a carved turn from
http://diginfo.ru/en/alpine-ski/ski-sidecut-radius-and-radius-of-a-carved-turn/

[6] Ski Turn radius from http://www.brentaski.com/skiradius/

[7] Hyun Gyu Shin, Young Soo Kim “A Study about Identity of Teaching Skill Terminology for Alpine Skiing” Journal of Sport and Leisure Studies, 2008

[8] 오경현 “ A study on the attitude control of quad-rotor using CMG” RISS, 2014

[9] “Global robot market outlook”IFR, 2015

