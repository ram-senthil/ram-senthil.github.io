---
layout: post
title:  "Smart Gardener"
date:   2023-05-01 10:00:00 -0700
categories: Personal
image:  /assets/smart-gardener-overall.jpeg
---

We have a large garden in our backyard which requires a significant amount of time to water frequently. Instead of having to physically be present, a smart gardener system could take care of this for you. It would have sensors to detect moisture as well as a water pump to water the plants. I created a prototype version of this with a [Particle Argon](https://docs.particle.io/argon/) which can connect to WiFi to enable IoT.

Here are some demonstration videos:
<iframe width="560" height="315" src="https://www.youtube.com/embed/ItYOKiYdOhU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


<iframe width="560" height="315" src="https://www.youtube.com/embed/w8A8DcIpAec" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

To design the prototype, I first created a wiring schematic shown here:
![smart-gardener-schematic]({{ "/assets/smart-gardener-schematic.jpg" | relative_url}})
<figcaption>Smart Gardener Schematic</figcaption>
<br>

From there, I created the prototype and integrated cloud functionality with the Particle such that a dashboard could be viewed from anywhere to monitor environment and plant conditions. Additionally, I created an application interface using the Blynk app, so that you could control whether or not to water your plants and also keep tabs on environment conditions through a mobile interface. 

![smart-gardener-cloud-dashboard]({{ "/assets/smart-gardener-cloud-dashboard.png" | relative_url}})
<figcaption>Smart Gardener Cloud Dashboard</figcaption>
<br>

![smart-gardener-app]({{ "/assets/smart-gardener-app.jpg" | relative_url}})
<figcaption>Smart Gardener Mobile Application</figcaption>
<br>