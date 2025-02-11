---
layout: page
title: Leviathan
description: Autonomous underwater vehicle (AUV)
img: assets/img/12.jpeg
importance: 1
category: work
related_publications: false
---

Leviathan is an AUV designed from the ground up at UCR by multidisciplinary teams who work all year long on the project. The goal of Leviathan is to compete in RoboSub, an international competition hosted by Robonation. Leviathan features five degrees of freedom and is designed for efficiency and stability while navigating the underwater environment without any human intervention.  


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="mech team" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="testing..1..2..3" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="software team" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    On the left, the mechanical team works on assembley. Middle, water infiltration tests. Right, software team working on thruster board firmware.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/4.jpg" title="systems diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Leviathan systems diagram 
</div>

Working with both the electrical and the software teams gave me a unique perspective in which I gained a lot of experience in both the hardware and the software that went into Leviathan. 

Along with the electrical team, I would help design the PCBs that went into the PCB housing as shown below. These boards were responsible for voltage conversion between different components, electronic speed control (ESC) for the T100 thrusters, and battery management (BMS) for the power source. I would also help design and render 3D images of the PCBs (also shown below) so the team could see how the final PCB would look before money was spend on having them made.  

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="pcb housing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="thruster pcb" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, 3D render of the PCB housing. Right, 3D render of the thruster board (ESC). 
</div>

With the software team we used gazebo to create and simulate a digital version of Leviathan. This allowed us to write and test both our ROS (robot operating system) nodes and our finite state machines (FSMs) to make sure everything worked as intended before deployment on the real robot which uses a Jetson TX2 running ROS. The ROS nodes are responsible for things like thruster control, camera input, and the inertial measurement unit or IMU for use with dead reckoning. 
{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
