---
layout: post
title:  "USC Racing Vehicle Undertray"
date:   2023-05-21 10:00:00 -0700
categories: USC-Racing
image:  /assets/scr23-endurance.jpeg
---

![VehicleUndertrayInRoll]({{ "/assets/scr23-undertray-roll.png" | relative_url}})
<figcaption>Undertray Integrated onto Vehicle. Rebel T6. Ramakrishna Senthil.</figcaption>
<br>
I am currently the Aerodynamics Lead Engineer of USC Racing, my school's Formula Student team. As the Lead Aerodynamics Engineer, I am responsible for the design, analysis, manufacturing, and validation of the vehicle’s aerodynamics package. In this post, I describe the design cycle for the development of the team’s first successful undertray in which I had direct and immense involvement throughout. This work was conducted between Aug 2022-May 2023 with the competition May 17-21, 2023 at Michigan. We placed 3rd/120 teams at design finals in the Aerodynamics category.

## Contents:
1. [Summary](#summary)
2. [Introduction](#introduction)
3. [Context](#context)
4. [Methodology](#methodology)<br>
    a. [Trade Studies](#trade-studies)<br>
    b. [Prototyping](#prototyping)<br>
    c. [Prototype Validation](#prototype-validation)<br>
    d. [Redesign](#redesign)<br>
    e. [Manufacturing](#manufacturing)<br>
    f. [Integration](#integration)<br>
    g. [Final Validation](#final-validation)<br>
5. [References](#references)<br>

### Summary
I owned the design, prototyping, redesigning, manufacturing, integrating, and validation of a vehicle undertray to enhance track performance. The first two steps were done as part of my senior design project where I led our group in the initial trades, initial design, manufacturing a prototype out of sheet metal, integrating and testing our design on track. Unfortunately this initial design was not effective, not producing enough downforce to justify the added weight. I then redesigned the undertray to enhance aerodynamic performance myself and achieved the target parameters. I led the development of a new mold-making process speeding up the timeline from weeks to a single weekend and manufactured the final design out of carbon fiber with a honeycomb sandwich core. I integrated it onto our racecar and experimentally confirmed the static pressures that were expected from CFD. 
<br>

### Introduction
As part of USC Racing, the goal is design, build, and compete with a high-performance racecar every year. We compete in multiple competitions throughout the year with the main event being Formula Student Michigan held in May. The goal of the aerodynamics subteam is to manage the external airflow around the vehicle for downforce/drag optimization as well as ducting for cooling purposes. 
<br>

### Context
![undertray-tire-forces](https://ram-senthil.github.io/assets/undertray-tire-forces.png){:style="display:block; margin-left:auto; margin-right:auto"}
<figcaption style="text-align: center;">Fig. 1: Forces & Moments a Tire Experiences While Interacting with Ground Plane [1]</figcaption>
<br>

A vehicle undertray's purpose is to increase track performance of a racecar. This is accomplished by adding downforce which increases the normal load on the tires. The different loads and moments a tire experiences is shown in Fig. 1. This added normal load provides more lateral load allowed to be extracted meaning more grip and thus ability to corner faster as shown in Fig. 2. The added downforce essentially allows the vehicle to handle more centripetal acceleration without sliding. However, with any added aerodynamic component intended to add downforce, penalties of drag and weight must be analyzed and weighed against the potential benefits. An advantage undertrays have over external aerodynamic elements such as a front wing or a rear wing is the reduced frontal area meaning inherently less of a drag penalty.

![undertray-tire-slip-angle](https://ram-senthil.github.io/assets/undertray-tire-slip-angle.png){:style="display:block; margin-left:auto; margin-right:auto"}
<figcaption style="text-align: center;">Fig. 2: Normal Load Influence on Tire Lateral Force vs Slip Angle [2]</figcaption>
<br>

### Methodology
a. [Trade Studies](#trade-studies)<br>
b. [Prototyping](#prototyping)<br>
c. [Prototype Validation](#prototype-validation)<br>
d. [Redesign](#redesign)<br>
e. [Manufacturing](#manufacturing)<br>
f. [Integration](#integration)<br>
g. [Final Validation](#final-validation)<br>
<br>

#### Trade Studies
We first started by conducting trade studies to identify a design space. Though more downforce is generally better, the more aerodynamic components added to achieve higher downforce usually means increased drag and weight penalties as well. 
We use Optimum Lap, a point-mass lap-time simulation software to predict how changing certain parameters will affect lap-time around a certain track model. We calibrated our digital model by tuning the model to track data of a simple track such as an oval. Grounding the simulation with real data allows us to better trust the predicted lap-times for more complex tracks. Since the majority of points are attributed to autocross style tracks, trade studies were conducted with those historically recent competition tracks. 

Below is an example of predicted lap-times for the three parameters downforce, drag, and vehicle mass for the following track in Fig. 3. 

![undertray-laptime-track](https://ram-senthil.github.io/assets/undertray-laptime-track.png){:style="display:block; margin-left:auto; margin-right:auto"}
<figcaption style="text-align: center;">Fig. 3: FSAE Lincoln 2019 Endurance Track</figcaption>
<br>

![undertray-laptime-df-drag](https://ram-senthil.github.io/assets/undertray-laptime-df-drag.png) ![undertray-laptime-df-mass](https://ram-senthil.github.io/assets/undertray-laptime-df-mass.png)
<figcaption style="text-align: center;">Fig. 4: Downforce Coefficient vs Drag Coefficient and Vehicle Mass</figcaption>


**Terminology in Fig. 4:**
- SCR22: 2022 USC Racing Vehicle <br>
- SCR23: 2023 USC Racing Vehicle <br>
- FW: Front Wing <br>
- RW: Rear Wing <br>


Even with more weight and drag an inclusion of undertray improves vehicle performance by ~2% which singificantly adds up over multiple laps especially in the endurance event which is 22 km. This quantitatively proved the necessity of working on designing an undertray and provided quantitative targets to achieve.
<br>

#### Prototyping
I expedited an initial design intended to be manufactured out of sheet metal for rapid manufacturing. This design was not iterated much due to a tight timeline and Computational Fluid Dynamics (CFD) simulations predicted it to have poor performance. Though the goal was to design a geoemtry that would be aerodynamically effective, moreso the intention of the prototype was to validate the accuracy of CFD in predicting flow underneath the vehicle. Additionally, the mass of the sheet metal prototype was much higher than the design target, but this was expected because the final design was to be manufactured using composites for high-strength low-weight. The prototype in CAD is shown below in Fig. 5 with the manufactured sheet metal version in Fig. 6.

![undertray-prototype-cad](https://ram-senthil.github.io/assets/undertray-prototype-cad.png){:style="display:block; margin-left:auto; margin-right:auto"}
<figcaption style="text-align: center;">Fig. 5: Undertray Prototype CAD Model</figcaption>
<br>


![undertray-prototype-manufactured](https://ram-senthil.github.io/assets/undertray-prototype-manufactured.png){:style="display:block; margin-left:auto; margin-right:auto"}
<figcaption style="text-align: center;">Fig. 6: Undertray Prototype Manufactured</figcaption>
<br>


#### Prototype Validation
Since at the time our team did not have a pressure scanner, I convinced the Aerospace & Mechanical Engineering Dept. to purchase 8 port pressure scanner on behalf of my senior design project. 
For data validation of my “senior design project”, but I used it extensively for non-senior design USC Racing purposes 
Within error, experimental matches CFD; first time in USC Racing History validating CFD!
<br>

#### Redesign
Singlehandedly redesigned undertray over winter break to improve performance & achieve trade study targets
Designed chassis integration system to be speedy to ensure maintainability of vehicle underbody
Mounts allow undertray to be “slid” into place and pinned down with clevis/cotter pins
No tools required to mount or dismount!
<br>

#### Manufacturing
Carbon fiber (CFRP) product required considering weight constraints
Conventional high density foam cost significant amount of money for the raw material and machining labor
Lead times for machining are weeks at the minimum
Innovated a completely unique method to create a precise 2-d curvature mold using sheet metal (donated for free) and waterjetting in-house
Manufactured composites in-house
Slotted all curved sections into endplates
In this condition, extremely fragile because joint sections have no support in bending  Layup composite over joint sections!
<br>

#### Integration
Constantly interfaced with chassis team to ensure the design height target of undertray would be met
Finished undertray integration in time!
<br>

#### Final Validation
Aerodynamic testing with tufts on rear wing & pressure taps on undertray shown on right

### References
[1] Gonçalves, J.P.C., Ambrósio, J.A.C. Road Vehicle Modeling Requirements for Optimization of Ride and Handling. Multibody Syst Dyn 13, 3–23 (2005). https://doi.org/10.1007/s11044-005-2528-5<br>
[2] Katz, Joseph. Race Car Aerodynamics : Designing for Speed. Cambridge, Ma, R. Bentley, 2006.