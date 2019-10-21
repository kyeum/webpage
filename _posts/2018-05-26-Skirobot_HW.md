---
title: "Hardware and Design in Ski Robot Challenge 2018"
date: 2018-05-26 08:26:28 -0400
categories: Humanoid Robotics
---

# Hardware and Design in Ski Robot Challenge 2018
## Skiing Robot System
![title](/photos/Skirobot_body.png){: width="40%" height="40%"}

To mimic human motion, we used two four-bar linkage mechanism in one leg to reduce weak parts such as hip and ankle. We also used worm gear to control the ankles to get rid of unnecessary actuators and to make skiing motions. Pendulum and CMG model on the upper waist are used for prevent falling with the zero moment point control. 

## Skiing Robot Leg
![title](/photos/Skirobot_leg.png){: width="50%" height="50%"}

Legs are consisted of double-four linkage system which can reduce weak joint in human body where there is a lot of force that might harm while skiing.

## Skiing Robot Ankle
![title](/photos/Skirobot_ankle.png){: width="40%" height="40%"}

One of importatnt part in controlling skiing robot is to optimize the factor which impacts the skiing, in this case the ski's radius and center of gravity. To remove unparticupar problems such as lack of motor torque, we minimize the axis by eliminating unnecessary skiing joint such as the ankle.

## Skiing Robot Pendulum
![title](/photos/Skirobot_pendulum2.png){: width="50%" height="50%"}

Since robot should use the radius of the ski, the center of gravity should be controlled. By using linear bush on the backside of the skiing robot, we were able to add CMG(Control Moment of Gyroscope)’s mass to the weight of the pendulum, which can be beneficial for the control.

## Skiing Robot Prototype
![title](/photos/Skirobot_proto.png){: width="30%" height="30%"}

Controling Huge robot and deterimine how it works just using main robot is hard as well as dangerous. Thus, we built prototype for examine the test process and get the test data.

## Skiing Robot Module
![title](/photos/Robot modules.png){: width="50%" height="50%"}

This project had hard circumstances since there is no place to verify the data and test. Because it is not possible to make laboratory system like real environment, making modules and test may seems reasonable in the reasearch procedure.

Build modules to easily attach to the main system.

## Motion Tester
![title](/photos/Skirobot_tester.png){: width="50%" height="50%"}

Tester using bluetooth to examine how the ski robot move, whcih should be necessary testing before flag detection.

