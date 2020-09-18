---
title: "Korea Institute of Science and Technology 2019.11 ~ 2020.09"
date: 2019-11-01 08:26:28 -0400
categories: KIST
---

## Bionics department at Korea Institute of Science and Technology
2019.11 ~ 2020.09

Main Project : Design and analysis soft wearable devices for the patients with the accurate and up to date 
- Specific 1 :  Design robot orthotic device to help the stroke patient and analysis using soft actuators.
- Specific 2 :  Build whole DAQ system for gait analysis which includes FSR sensors and UWB sensors on foot, IMU on waist, and pc programming. This DAQ system accumulate datas in 100HZ, and the data will be used for ML.

![title](/photos/Center for bionics.png){: width="70%" height="70%"}

Skimatic for Gait Analysis and System.

## Project's Goal
Next generation of soft wearable robots will use innovative textiles and creative mechanisms to provide a more conformal, unobtrusive and compliant means to interface to the human body.

As compared to a traditional exoskeleton, next generation's system has several advantages: the wearer's joints are unconstrained by external rigid structures, and the worn part of the suit is extremely light.  These properties minimize the suit's unintentional interference with the body's natural biomechanics and allow for more synergistic interaction with the wearer.

For above goals, we need several ways to integrate for this system.

1. Modeling of soft actuators and wearable robots
- SMA(Shape Memory Alloy), Soft actuators and Texture.

2. Comfortable Human machine Interface DAQ system.
- Cheap, Mobile, overcome the Motion capture system(traditional approach)


## 1. Soft Texture like Actuator with SMA
:Having actuators in normal exoskeleton are getting a limits to be industrialize. Further research in material and chemical will be necessary to overcome issues of current hard exoskeleton mechanism. Soft sensors, Soft actuators will lead next generation for the industry and for the human.

![title](/photos/kist_research1.png){: width="30%" height="30%"}
![title](/photos/kist_research2.png){: width="30%" height="30%"}

: SMA is one good example for starting a soft robotics. It has not good efficiency but, it will have cheap and powerful solution for the exoskeleton. Thus control actuator of SMA, which has 1~2HZ(human locomotion) will be beneficial for further research.

## 2. Design DAQ system and UWB sensors
: It is hard to get use the patients' data. Not only they matters what they are not good to be, but also they care other's view, which might hinder the analysis. For those reasons, we build up to date DAQ systems, which easily attach to the patients' shoes and belts shortening burdens for them. 

![title](/photos/KIST/DAQ device.png){: width="30%" height="30%"}
![title](/photos/KIST/UWB sensors.png){: width="30%" height="30%"}

Our DAQ system combines with Insole devices using STM32- M4 board and UWB sensors. And, this system will be compared to the Laboratory's Motion capture system.

![title](/photos/KIST/Testbed.png){: width="30%" height="30%"}

There are multiple algorithms for the UWB sensors.
![title](/photos/KIST/UWB Algorithms.png){: width="30%" height="30%"}


## reference
- Shap e Memory Alloys and their Application to Actuators for Deployable Structures - University of Cambridge Department of Engineering
- New Design of a Soft Robotics Wearable Elbow Exoskeleton Based on Shape Memory Alloy Wire Actuators - Department of Systems Engineering and Automation, Carlos III University of Madrid, Madrid, Spain
- Stroke rehabilitation - Peter Langhorne, Julie Bernhardt, Gert Kwakkel
