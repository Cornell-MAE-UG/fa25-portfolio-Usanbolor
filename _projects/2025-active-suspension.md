---
layout: project
title: MAE3260 Final Project, Modeling and Control of an Active Suspension System
technologies: [MATLAB]
image: /assets/images/active-suspension.png
---

**Team Members:** Usanbolor Amartuvshin, John Apessos, Charles Pearson

The quarter-car suspension model is the simplest representation of vehicle suspension dynamics. It considers only one wheel and the associated portion of the vehicle’s mass — essentially one quarter of the entire car. Because we assume that each wheel behaves symmetrically, modeling a single wheel provides a practical and accurate approximation while significantly simplifying the system. Previously in class, we focused on passive suspension systems, where the motion of the vehicle body is solely dependent on road disturbances and the natural reaction of the springs and dampers. However, our final group work examines an active suspension system, which includes an actuator that applies external input (F). This optimizes the comfort of the driver and gains better control over movement of the car. 

To be able to model the system easily, several assumptions are made. We only consider vertical motion/displacement of the system meaning we will neglect yaw, roll and pitch.  Likewise we ignore aerodynamic impacts such as downforce, body weight shifts or body roll because including them will introduce additional degrees of freedom and becomes more complicated to model. Both masses are assumed to be rigid and constant, and suspension components are modeled as linear, which allows us to utilize the force-displacement and force-velocity relationships. In the real world, each part of course experiences friction, however to make the model simpler we model the system as frictionless. Finally, the road input is treated as a known disturbance acting only on the tire, and the actuator is assumed to perform ideally, without delays, bandwidth limitations, saturation and perfect sensor performance as well. This ensures the control force is applied exactly as commanded.

---

#### Design Requirements
- **driver acceleration** a(t) <1.5 m/s^2
- **body displacement** y(t) < 1cm
- **shock travel** less than 10cm

---

#### State Space Model
- **Governing ODE**
![Force balance on sprung and unsprung masses]({{ "/assets/images/system-equation1.png" | relative_url }}){: .inline-image-center style="width: 500px"}

- **State Vector**
![]({{ "/assets/images/system-equation2.png" | relative_url }}){: .inline-image-center style="width: 100px"}

- **Inputs**
![]({{ "/assets/images/system-equation3.png" | relative_url }}){: .inline-image-center style="width: 100px"}

- **Outputs**
![]({{ "/assets/images/system-equation4.png" | relative_url }}){: .inline-image-center style="width: 100px"}

- **State Space Model**
![]({{ "/assets/images/system-equation6.png" | relative_url }}){: .inline-image-center style="width: 350px"}
![]({{ "/assets/images/system-equation7.png" | relative_url }}){: .inline-image-center style="width: 350px"}

---

#### Transfer Function Model
- **Transfer Function**
![]({{ "/assets/images/system-equation8.png" | relative_url }}){: .inline-image-center style="width: 200px"}

- **System Poles**
![]({{ "/assets/images/system-equation9.png" | relative_url }}){: .inline-image-center style="width: 100px"}

---

#### Closed Loop Analysis
- **Closed Loop Block Diagram of the System**
![]({{ "/assets/images/system-equation5.png" | relative_url }}){: .inline-image-center style="width: 500px"}

- **State Vector with Closed Loop Control**
![]({{ "/assets/images/system-equation10.png" | relative_url }}){: .inline-image-center style="width: 350px"}

---

#### Simulation Parameters
- Sprung Mass (M_1) = 300 kg
- Unsprung Mass (M_2) = 60 kg
- Suspenstion Stiffness (k_1) = 17,000 N/m
- Suspension Dampping (b_1) = 2500 Ns/m
- Tire Stiffness (k_2) = 190,000 N/m
- Road Step = 0.05m

---

#### Simulation Results

Here is a performance comparison between suspension with no control and a suspension with skyhook control. 
![Open loop vs closed loop suspension responce]({{ "/assets/images/system-result.png" | relative_url }}){: .inline-image-center style="width: 600px"}

---

#### Conclusion

The active suspension system with skyhook control demonstrates clear improvements over the passive model, providing reduced body displacement and a more comfortable ride. Using a state-space modeling approach allowed us to simplify the system representation and gain better insight for improving the overall design.

---






