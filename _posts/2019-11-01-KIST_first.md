---
title: "Korea Institute of Science and Technology 2019.11 ~ 2020.09"
date: 2019-11-01 08:26:28 -0400
categories: KIST
---

## Bionics department at Korea Institute of Science and Technology
2019.11 ~ 2020.09

## Main Project
# Design and analysis soft wearable devices for the patients with the accurate and up to date devices.
- Specific 1 :  Design robot orthotic device to help the stroke patient and analysis using soft actuators.
- Specific 2 :  Build whole DAQ system for gait analysis which includes FSR sensors and UWB sensors on foot, IMU sensors on waist, and pc. This DAQ system accumulate datas in 100HZ, and the data will in use for Gait Analysis.

![title](/photos/Center for bionics.png){: width="70%" height="70%"}

## Project's Goal
Next generation of soft wearable robots will use innovative textiles and creative mechanisms to provide a more conformal, unobtrusive. Until now, Researchers tried to use acutators to linearlly and efficiently optimizely control the machines without efficiency. Currently we are looking for underactuated, or other soft actuators, which is cheap and effective to control the bulky machines.

As compared to a traditional exoskeleton, next generation's system has several advantages: the wearer's joints are unconstrained by external rigid structures, and the worn part of the suit is extremely light.  These properties minimize the suit's unintentional interference with the body's natural biomechanics and allow for more synergistic interaction with the wearer.

For above goals, we need several ways to integrate for this system.

1. Modeling of soft actuators and wearable robots
- SMA(Shape Memory Alloy), Soft actuators and Texture.

2. Comfortable Human machine Interface DAQ system.
- Cheap, Mobile, overcome the Motion capture system(traditional approach)

## 1. Soft Texture like Actuator with SMA
:Having actuators in normal exoskeleton are getting a limits to be industrialize. Further research in material and chemical will be necessary to overcome issues of current hard exoskeleton mechanism. Soft sensors, Soft actuators will lead next generation for the industry and for the human.

![title](/photos/KIST/SMAARM.png){: width="40%" height="40%"}
![title](/photos/kist_research2.png){: width="40%" height="40%"}

: SMA is one good example for starting a soft robotics. It has not good efficiency but, it will have cheap and powerful solution for the exoskeleton. Thus control actuator of SMA, which has 1~2HZ(human locomotion) will be beneficial for further research.

## 2. Design DAQ system and UWB sensors
: Aquiring the stroke patients' data for analysis is tricky, and we wish to accumulate universial data not only from patients but also from normal people. For those reasons, I build up to date DAQ systems, which easily attach to the patients' shoes and belts. This includes, 3 sets UWB senosors and 5 FSR sets in one Insole shoee, and with the BT and UWB communication system, I designed 100hz(10ms) DAQ system. 

![title](/photos/KIST/DAQ device.png){: width="40%" height="40%"}
![title](/photos/KIST/UWB sensors.png){: width="40%" height="40%"}

Insole system uses STM32- M4 board and UWB sensors. And, this system will be compared to the Laboratory's Motion capture system.

![title](/photos/KIST/Testbed.png){: width="50%" height="50%"}

There are multiple algorithms for the UWB sensors. Based on this Algorithm and UWB sensor sets, we can get the coordinates of one foot!

![title](/photos/KIST/UWB Algorithms.png){: width="50%" height="50%"}

## 3. Machine Learning and Gait Analysis
: By above system, we can get daily bases bulky data sets from human's gait. With this data, we can try to analyse and classify which state of the human's gait.

![title](/photos/KIST/GaitCycle.jpeg){: width="80%" height="80%"}


## reference
- Shap e Memory Alloys and their Application to Actuators for Deployable Structures - University of Cambridge Department of Engineering
- New Design of a Soft Robotics Wearable Elbow Exoskeleton Based on Shape Memory Alloy Wire Actuators - Department of Systems Engineering and Automation, Carlos III University of Madrid, Madrid, Spain
- Stroke rehabilitation - Peter Langhorne, Julie Bernhardt, Gert Kwakkel