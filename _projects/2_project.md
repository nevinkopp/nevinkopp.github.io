---
layout: page
title: Underwater object tracking (UOT)
description: Graduate research project
img: assets/img/7.jpg
importance: 2
category: work
related_publications: true
---

This research project implementation focuses on improving the performance of modern state of the art (SOTA) trackers for use in underwater autonomous vehicle (AUV) applications. Since many modern SOTA trackers were trained with open air (OA) datasets and are intended for use with aerial robotics, they tend to perform poorly when used in the underwater domain as shown below [1].   

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/8.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Y-axis represents the success rate (AUC-ROC) where 1 is perfect and anything equal to or less than 0.5 is a random guess. X-axis represents a particular SOTA tracker. Each point on the graph represents the success rate of a particular SOTA tracker on three separate datasets (TrackingNet, LaSOT, and UW-VOT400), where VOT400 contains underwater imagery. 
</div>

From the chart above, it is clear that the sampled SOTA trackers lost a lot of performance when applied to an underwater dataset and weren't much better than a random guess. This is due to many factors, such as low light, poor visability, light scattering, absorption of light, target blurring, watercolor variations, camouflage, occlusion, and target visibility loss over increasing distances [1]. 

Ideally, researchers would have access to a massive dataset of underwater imagery in order to train new models. The lack of such a dataset has been one of the major problems with underwater object tracking (UOT) research. The papers involved in this research however, propose two new datasets for UOT research, the UVOT-400 and LSUI datasets. With these new datasets (among others) and image enhancement techniques, modern SOTA tracker performance can be improved which is the main inspiration behind this research project. 

The first step in improving the performance of existing tracking models is to train them with a 70/30 split with the new underwater datasets. From there, we can further enhance the images to further improve performance. Below are the results of training existing models on the UVOT-400 underwater dataset.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, performance tests with no training on UVOT-400. Right, performance tests after training on UVOT-400. 
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.


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
