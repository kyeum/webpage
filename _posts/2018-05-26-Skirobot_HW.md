---
title: "Hardware and Design in Ski Robot Challenge 2018"
date: 2018-05-26 08:26:28 -0400
categories: Humanoid Robotics
---

# Hardware and Design in Ski Robot Challenge 2018
## Skiing Robot System
![title](/photos/Skirobot_body.png){: width="40%" height="40%"}

To mimic human skiing motion, we used two four-bar linkage mechanism in one leg for reducing weak parts such as hip and ankle in skiing. We used worm gear for controling ankles getting rid of unnecessary joints for skiing motions. Pendulum and CMG model on the upper waist are used for prevent falling using the zero moment point control. 

## Skiing Robot Leg
![title](/photos/Skirobot_leg.png){: width="50%" height="50%"}

Legs are consisted of double-four linkage system which can make adequate skiing radius. This system can easily produce the motion for the skiing. 

## Skiing Robot Ankle
![title](/photos/Skirobot_ankle.png){: width="40%" height="40%"}

One of important part controlling dynamic motion in humanoid robot is to optimize the factor which impacts the hardware, in this case the ski's radius. Ski radius determined by the length of each legs and alphine ski radius, thus the we do not need to controll all 3 DOF in the mechanism. To remove unparticupar problems such as lack of motor torque, we minimize the axis by eliminating unnecessary skiing joint.

## Skiing Robot Pendulum
![title](/photos/Skirobot_pendulum2.png){: width="50%" height="50%"}

To control center of gravity, we build pendulum based control mechanism in skiing robot. By using linear bush on the backside of the skiing robot, we were able to add CMG(Control Moment of Gyroscope)’s mass to the weight of the pendulum, which optimize robot's hardware for the control.

## Skiing Robot Prototype
![title](/photos/Skirobot_proto.png){: width="30%" height="30%"}

Controling Huge robot and deterimining how it works in huge main robot is hard and dangerous. Thus, we built prototype for examine the test process with same mechanism.

## Skiing Robot Module
![title](/photos/Robot modules.png){: width="50%" height="50%"}

Harsh environment makes the researcher exhausted. To diminish this arduous problem, we suggested Robot module system that we can easily attach and detach each module for examining the process. With these procedure, we can reduce time for testing and optimizing in harsh  and limited environment; skiing resort.

## Motion Tester
![title](/photos/Skirobot_tester.png){: width="50%" height="50%"}

Controller using bluetooth is necessary for control huge robot before build the robot automation.

