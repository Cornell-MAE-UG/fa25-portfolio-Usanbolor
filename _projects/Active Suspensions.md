---
layout: project
title: MAE3260 Final Project: Modeling and Control of an Active Suspension System
description: Our project focuses on modeling, analyzing, and designing control strategies for an automotive active suspension system.
technologies: [MATLAB]
image: /assets/images/active-suspension.png
---

**Team Members:** Usanbolor Amartuvshin, John Apessos, Charles Pearson

#### **Introduction**
The quarter-car suspension model is the simplest representation of vehicle suspension dynamics. It considers only one wheel and the associated portion of the vehicle’s mass — essentially one quarter of the entire car. Because we assume that each wheel behaves symmetrically, modeling a single wheel provides a practical and accurate approximation while significantly simplifying the system. Previously in class, we focused on passive suspension systems, where the motion of the vehicle body is solely dependent on road disturbances and the natural reaction of the springs and dampers. However, our final group work examines an active suspension system, which includes an actuator that applies external input (F). This optimizes the comfort of the driver and gains better control over movement of the car. 

To be able to model the system easily, several assumptions are made. We only consider vertical motion/displacement of the system meaning we will neglect yaw, roll and pitch.  Likewise we ignore aerodynamic impacts such as downforce, body weight shifts or body roll because including them will introduce additional degrees of freedom and becomes more complicated to model. Both masses are assumed to be rigid and constant, and suspension components are modeled as linear, which allows us to utilize the force-displacement and force-velocity relationships. In the real world, each part of course experiences friction, however to make the model simpler we model the system as frictionless. Finally, the road input is treated as a known disturbance acting only on the tire, and the actuator is assumed to perform ideally, without delays, bandwidth limitations, saturation and perfect sensor performance as well. This ensures the control force is applied exactly as commanded.

![Quarter Car Schematic]({{ "/assets/images/active-suspension.png" | relative_url }}){: .inline-image-r style="width: 200px"}

Nulla et magna urna. Morbi a ipsum sollicitudin, rhoncus risus volutpat, ultricies nunc. Quisque mollis finibus ante id imperdiet. Quisque vehicula elit sit amet felis facilisis fermentum.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

I was inspired by this old radio when I made this rendering:

![Photo of old radio]({{ "/assets/images/old-radio.jpg" | relative_url }}){: .inline-image-l}

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.

Aenean tincidunt aliquam arcu, in euismod dui dapibus eu. In placerat, mi et ultrices consequat, quam ligula cursus mauris, in semper neque nibh at est. Maecenas hendrerit dignissim porta. Phasellus nec fringilla dolor. Etiam efficitur nisi sit amet velit pharetra feugiat. Etiam ultrices turpis at leo semper, eleifend scelerisque neque malesuada. Aliquam molestie congue rhoncus. Donec blandit neque dolor, nec tristique mi pretium ac. Mauris tincidunt ullamcorper magna, nec pellentesque mi sagittis quis.
