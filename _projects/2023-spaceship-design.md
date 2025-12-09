---
layout: project
title: MAE3260 Final Project: Modeling and Control of an Active Suspension System
description:  Our project focuses on modeling, analyzing, and designing control strategies for an automotive active suspension system.
technologies: [MATLAB]
image: /assets/images/active-suspension.png
---


Team members: John Apessos, Usanbolor Amartuvshin, Charles Pearson

#### **Introduction**

The quarter-car suspension model is the simplest representation of vehicle suspension dynamics. It considers only one wheel and the associated portion of the vehicle’s mass — essentially one quarter of the entire car. Because we assume that each wheel behaves symmetrically, modeling a single wheel provides a practical and accurate approximation while significantly simplifying the system. Previously in class, we focused on passive suspension systems, where the motion of the vehicle body is solely dependent on road disturbances and the natural reaction of the springs and dampers. However, our final group work examines an active suspension system, which includes an actuator that applies external input (F). This optimizes the comfort of the driver and gains better control over movement of the car. 

To be able to model the system easily, several assumptions are made. We only consider vertical motion/displacement of the system meaning we will neglect yaw, roll and pitch.  Likewise we ignore aerodynamic impacts such as downforce, body weight shifts or body roll because including them will introduce additional degrees of freedom and becomes more complicated to model. Both masses are assumed to be rigid and constant, and suspension components are modeled as linear, which allows us to utilize the force-displacement and force-velocity relationships. In the real world, each part of course experiences friction, however to make the model simpler we model the system as frictionless. Finally, the road input is treated as a known disturbance acting only on the tire, and the actuator is assumed to perform ideally, without delays, bandwidth limitations, saturation and perfect sensor performance as well. This ensures the control force is applied exactly as commanded.



#### **System Requirements and Assumptions**

- **acceleration:**

$$
|a(t)| < 1.5 \,\text{m/s}^2 \quad \text{(active design)}
$$

- **displacement**

$$
|y(t)| < 0.015\, \text{m}
$$

- **Shock travel constraint**

$$
\text{travel} < 0.10\, \text{m}
$$

![Quarter Car Schematic](/assets/images/active-suspension.png)



