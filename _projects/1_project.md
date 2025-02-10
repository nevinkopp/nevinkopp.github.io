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
    On the left, the mechanical team works on assembley. Middle, water inflitration tests. Right, software team working on thruster board firmware.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/4.jpg" title="systems diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Leviathan systems diagram 
</div>

Working with both the electrical and the software teams gave me a unique perspective in which I gained a lot of experience in both the hardware and the software that went into Leviathan. With the electrical team, I would design the PCBs that went into the PCB housing as shown below. These boards were responsible for voltage conversion, electronic speed control (ESC), and battery management (BMS). I would also design and render 3D images of the PCBs (also shown below) so the team could see how the final PCB would look before money was spend on having them made. 

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

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
