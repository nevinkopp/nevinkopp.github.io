---
layout: page
title: Autonomous mini tank
description: Seek and mildly annoy 
img: assets/img/31.jpg
importance: 1
category: fun
---

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/35.jpg" title="tank" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The completed mini tank... I beg your pardon, but what do you mean naked? 
</div>

This was my final project for my Robotics Fabrication course at UCR. It was completed in a team of three, and I was mainly responsible for the turret system. The objective of this project was to fabricate a fully working robotic system from the ground up. We only had a few weeks to do it, which is why it looks so... prototypy? But it does complete its objective! The objective was to find red solo cups and shoot them with a foam ball. The choice of red cup was purely happenstance and could've been anything, but we wanted something cheap and easy to hit. 

The mini tank is assembled out of two main parts, the base and the turret. The base (as shown below) is responsible for moving the robot around. The frame itself was completely rendered in SolidWorks and laser cut in the UCR machine shop. We decided to go with tank treads since that was what came with the motor kit and, since it was a self-funded project, we couldn't spare much more expense.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/33.jpg" title="base" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Mini tank base (the part that makes it go). 
</div>

The motors (four in total) are controlled with an Arduino motor shield. Similarly, the turret (shown below) was also completely rendered in SolidWorks and laser cut. For the actual shooty part, I bought a cheap toy gun from Target and ripped out the important bits, which was the flywheel assembly.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/34.jpg" title="turret" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Mini tank turret (do NOT wear red around this thing). 
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/37.jpg" title="turret" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Mini tank turret functionality. 
</div>

The flywheels work by being spun really fast by two DC motors (one each). Once the motors are up to speed, a linear actuator will push a small foam ball into the spinning wheels where it will get launched out of the barrel. From here, the remaining foam balls are suspended inside the top tube, which acts like a magazine. Once the linear actuator retracts far enough, another ball is loaded and the process repeats itself. We found that by playing around with the linear actuator, we can have burst fire, semi-auto, and fully auto modes.

Target acquisition was done using an off-the-shelf PixyCam. It was trained on the color red since that is the color red solo cups are but also a fairly rare color for a classroom to be (such as where we had to demo the robot, we didn't want it to shoot things it shouldn't). Once the PixyCam detects a target, the servo motor controlling the yaw of the turret will aim the barrel at it and start up the flywheels, which will then fire the foam ball at it.

Overall, this was a very fun project and I learned a lot! The most memorable moment for me was when my partner and I were working on it late at night and we started to smell something burning. We looked over and started seeing white smoke coming from the battery pack. My partner quickly unplugged it, and I thought to myself, we are done, the project is dead. Luckily, he just wired the battery pack in wrong and created a short circuit! Aside from some melted plastic, the tank ended up working just fine.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/36.jpg" title="simple times" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    linear actuator testing/troubleshooting/work darn it! 
</div>
