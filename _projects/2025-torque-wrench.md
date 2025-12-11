---
layout: project
title: Torque Wrench Design
description: Created a detailed CAD model of a torque wrench in Fusion 360 and conducted finite element analysis in ANSYS to assess structural integrity, stress concentrations, and load-bearing performance. 
technologies: [Autodesk Fusion, ANSYS, MATLAB]
image: /assets/images/torque-wrench.png
---

For MAE3270 (Materials), we were tasked with designing a non-ratcheting, 3/8-inch drive instrumented torque wrench rated for 600 in-lbf. The wrench was to be strain-gauged, with sensors bonded to high-strain regions on the outer surface. Our analysis included analytical hand calculations supported by MATLAB, as well as finite element simulations to evaluate stress distribution, strain behavior, and overall structural performance.

---

#### Main Dimensions & Material

![Schematic of Torque Wrench]({{ "/assets/images/torque-wrench2.png" | relative_url }}){: .inline-image-l}
- L = 14 in
- b = 0.75 in
- h = 0.6 in
- c = 1 in



**Material Selection**

For our design we used aluminum 7075-T651 as it has high strength while being light which is great for lightweight and high performance applications. With a tensile strength of 70,000 psi, it can withstand significant mechanical loads without substantial deformation. In addition, its lower density compared to steel helps reduce overall weight, resulting in a lighter, more ergonomic design that is easier for users to handle.

---

#### FEM applied boundary conditions and loads

We held the drive end at constant by setting the displacement components equal to 0. Then we  applied 42.86lbf = Torque/Length at the end face in y direction. 
![]({{ "/assets/images/fem1.png" | relative_url }}){: .inline-image-center}

---

#### FEM Results

- **Normal Strain Contour**
![]({{ "/assets/images/fem2.png" | relative_url }}){: .inline-image-center}

- **Contour Plot of Maximum Principle Stress**
![]({{ "/assets/images/fem3.png" | relative_url }}){: .inline-image-center}

**Result Summary**
We found that the maximum normal stress in the structure reaches 41,400 psi, while the maximum deflection at the load point is 0.459 inches. At the strain gauge location, the FEM predicts a stress of 12,690 psi, which aligns closely with our MATLAB calculation of 13,333 psi. 

---

#### Torque Wrench Sensitivity (mV/V)
- Strain gauge factor (K): 2
- Strain at strain gauge location from FEM result: 1.238e-3

mV/V = 1000*strain = 1000* 1.238e-3 = **1.238**

---

#### Strain Gauge Selection
**Strain Gauge:** SGD- 2/350-LY11
- Normal resistance: 350 omega
- Gauger factor = 2
- Active grid length: 2mm (0.118 in)
- Active grid width: 2.5mm (0.098 in)
- Matrix length: 7.6 mm (0.299 in)
- Matrix width: 5.8 mm (0.228 in)

Note: Our design cross section where the gauge will be applied is 0.75x0.6 in, providing us with enough space for the gauges to bond. 






