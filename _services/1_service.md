---
layout: page
title: Tutoring
#description: 
img: assets/img/47.png
importance: 1
#category: university
#related_publications: false
---

Test  

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/1.jpg" title="mech" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/3.jpg" title="tests" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, Mechanical team works on assembly. Right, Water infiltration tests.. 
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="software team" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     Software team working on thruster board firmware.
</div>
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/4.jpg" title="systems diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Leviathan systems diagram 
</div>

Working with both the electrical and the software teams gave me a unique perspective in which I gained a lot of experience in both the hardware and the software that went into Leviathan. 

Along with the electrical team, I would help design the PCBs that went into the PCB housing as shown below. These boards were responsible for voltage conversion between different components, electronic speed control (ESC) for the T100 thrusters, and battery management (BMS) for the power source. I would also help design and render 3D images of the PCBs (also shown below) so the team could see how the final PCB would look before money was spent on having them made.  

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="pcb housing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="thruster pcb" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, 3D render of the PCB housing. Right, 3D render of the thruster board (ESC). 
</div>

With the software team we used gazebo to create and simulate a digital version of Leviathan. This allowed us to write and test both our ROS (robot operating system) nodes and our finite state machines (FSMs) to make sure everything worked as intended before deployment on the real robot which uses a Jetson TX2 running ROS. The ROS nodes are responsible for things like thruster control, camera input, and the inertial measurement unit or IMU for use with dead reckoning. 

<div class="row justify-content-sm-center">
    <div class="col-sm-9 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2.jpg" title="gazebo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Gazebo screenshot of Leviathan running the mission control node 
</div>

Future scope

With AUVs, we are able to explore the underwater world in a way that is not only cheaper than manned explorations, but also much safer. With AUVs, we can create useful maps of the seafloor which can help commercial companies plan on where to build infrastructure with minimal impact on the environment. Additionally, AUVs can be equipped with all sorts of sensors and devices that can help scientists study lakes and oceans. 

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/12.jpg" title="leviathan" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
     
</div>