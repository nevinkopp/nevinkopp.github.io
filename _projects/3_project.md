---
layout: page
title: Bread Recipe Autonomous Device (BRAD)
description: Automated bread maker 
img: assets/img/18.jpg
#redirect: https://unsplash.com
importance: 3
category: work
---

The Bread Recipe Autonomous Device (BRAD), is my undergraduate senior design project aimed at simplifying the bread making process by automating the dispensing, mixing, kneading, and baking stages. Our team’s motivation behind this project was to provide a more convenient and accessible way for consumers to make and enjoy fresh, healthy bread at home.

BRAD is composed of various subsystems, such as the solid dispensing subsystem, the liquid dispensing subsystem, the bread machine interface, lid opening and closing mechanism, and the logic circuitry. The key features of BRAD include a remote connection to the device through a virtual private network that can be accessible through the internet, a bread pan with a durable non-stick coating for easy cleaning, and the ability to add new recipes and ingredients using simple, 3D printed containers. The actual bread machine itself is a standard off the shelf bread maker, this project simply automates the process of using it. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/19.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/20.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/21.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Various parts of the dispensing system. Left, base of the ingredient container. Middle, auger housing. Right, auger bit. 
</div>

The base of the ingredient container feeds into the auger housing where a Nema 17 stepper motor spins the auger bit which pushes out the ingredient and pours it into the bread maker. 

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/22.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overall hardware block diagram.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/23.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Overall software block diagram based on finite state machines (FSMs).
</div>

Following the flow of the FSMs, BRAD waits for human input before starting the process. For our project, human input comes in the form of a web app as shown below. The user has the option to make either light or dark white bread in both small or large batches. In future revisions, more bread recipies can be easily added as BRAD is designed to be highly modular. Once a button is pressed, the process is started and can be cacelled at any time through the web app. 

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/29.jpg" title="phone app" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Screenshots of the web app showing the currently available options for the user.
</div>

Once the user selects their desired option, the FSMs move to the recipes state where the bread machine interface (shown below) simulates the button presses on the bread machine as a human would.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/27.jpg" title="bmi" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hardware layout of the bread machine interface (BMI). NPN transistors are used to send a 5 V signal to the specific buttons involved in the user selected option. 
</div>

Once the desired buttons are pressed, it is time to load in the ingredients. We start with opening the lid which is controlled by the lid control system. The lid control system as shown below, consists of an A4988 motor driver and Nema 17 stepper motor. The motor spins a 3D printed bit that holds some fishing line that is connected to the lid. As the motor spins, the string winds up and the lid opens. Closing is similar but in the other direction. 

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/26.jpg" title="lid control" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hardware layout of the lid control system. 
</div>

