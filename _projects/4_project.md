---
layout: page
title: BB Bandit
description: Open source mini tank 
img: assets/img/31.jpg
importance: 1
category: 
---

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/31.jpg" title="tank" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The completed mini tank... I beg your pardon, but what do you mean naked? 
</div>

For access to the open source code and 3D renders, please refer to my [github](https://github.com/nevinkopp/automated-mini-tank) page!

BB Bandit is an open-source mini tank with autonomous target acquisition. BB Bandit uses a Pixy2 camera and a region-growing algorithm to identify targets. Targets are trained using the hue of specific pixels. For our experimentation, red party cups were used to validate functionality.

BB Bandit is assembled from two main parts: the base and the turret. The base (as shown below) is responsible for moving the robot around. The frame itself was fully designed in SolidWorks and laser cut. The motors, gearboxes, and tank treads were included in a cheap off the shelf kit.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/33.jpg" title="base" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    BB Bandit base 
</div>

The main turret is pictured below. It is composed of a flywheel assembly taken from a Nerf gun and a 3D-printed barrel and magazine. The process starts by first loading the ball into the top feeder (in orange). It can hold approximately five balls, plus one in the chamber.

From there, a linear actuator pulls back a 3D-printed plunger, which loads a ball into the chamber. Once the ball is loaded, it is ready to be fired. When the "fire" command is issued, the flywheels spin up to speed and the plunger pushes the ball into the flywheels.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/34.jpg" title="turret" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    BB Bandit turret
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/37.jpg" title="turret" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Firing mechanism
</div>

<div align="center">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/zwfM17PHtx8" 
    frameborder="0" allowfullscreen></iframe>
</div>



In conclusion, BB Bandit was a very fun project, and we learned a lot. The main challenge was power distribution. In the end, we decided it would be better to use a power bus with two rails: one rail was set to 5 V and the other to 12 V. This allowed the flywheels to spin up to full power while also providing a safe power source for the more sensitive electronics.

Future Scope
While this was mostly a fun project, with more work, it can become a lot more useful. For example, it can currently be taught to recognize certain pixel hues but isn’t able to classify objects. It also isn't able to autonomously roam and must be remote-controlled to move around. 
