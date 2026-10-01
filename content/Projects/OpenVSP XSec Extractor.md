---
date: 2026-09-28
draft: false
---

After experiencing first hand with our SAE Aero Design entry how quickly a 3D printed fuselage could eat up the weight budget, for my capstone project I decided to use a laminated foam approach similar to that  usually employed to build lifting surfaces. 

Ever since our lab bought a hot-wire foam cutter, the machine was used extensively to fabricate lifting surfaces for all kinds of aircraft. Wings and stabilizers are relatively easy to cut with a 4-DoF machine. Any complex geometry can be approximated as a series of linearly lofted sections, allowing the incorporation of geometric as well as aerodynamic twist along the wingspan. Because of this, most CAM software tailored towards this manufacturing process mostly focuses on wing sections. One notable exception is devFus, part of the [devCAD tool suite](https://www.devcad.com/eng/products_table.asp) that we had already been using for most of our foam cutting G-code.

Like most of the aircraft, the fuselage OML was designed using [OpenVSP](https://openvsp.org/), an open source parametric aircraft geometry tool developed by NASA (that is simply the greatest tool ever for conceptual aircraft design, specially if you are a student). OpenVSP can export geometries in many formats, from solid .STEP models to surface .STL and everything in between, sadly devFus had no way of automatically processing geometry files as it relied of manually traced longitudinal cross-sections to created the tool paths needed for the wire cutter.

In order to bridged the gap between the parametric geometry and the bidimensional cross-sectional patterns that I could use to trace the patterns within devFus I wrote  short pythong script that took the output of the [Planar Slice](https://www.nasa.gov/reference/openvsp-planar-slice/) tool in OpenVSP (usually used to check stuff like the Whitcomb area rule) and processed the points to plot them in a cleaner manner and export them in a devFus-friendly format.


![[m_aeat-05-2025-016814.png]]
*Conceptual overview of the geometry processing pipeline.*

Depending on how accurate one wants the curvature to be the number of slices can be increased or decreased. For my purposes, 10 sections were sufficent. The nose and tail sections, were the curvatures were significantly more complex where printed with foaming plastic.
![[m_aeat-05-2025-016815.png]]
*Resulting fuselage sections in devFus. *

While watching some YouTube videos I ran into the CHANNEL channel. He also uses sections build his fuselages so and seemed to be relying back then in a more manual geometry processing pipeline. I decided to share my script and some instructions on how to use it by uploading a YouTube video:
![](https://www.youtube.com/watch?v=lRTBPSJ5pYQ)

Once I added multi-body funtionality I uploaded a second video explaining the new functionality:
![](https://www.youtube.com/watch?v=4RBH1Hth29k)