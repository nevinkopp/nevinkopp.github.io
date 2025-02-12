---
layout: page
title: Underwater object tracking (UOT)
description: Graduate research project
img: assets/img/7.jpg
importance: 2
category: work
related_publications: false
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

From the chart above, it is clear that the sampled SOTA trackers lost a lot of performance when applied to an underwater dataset, and some weren’t much better than a random guess. This is due to many factors, such as low light, poor visibility, light scattering, absorption of light, target blurring, watercolor variations, camouflage, occlusion, and target visibility loss over increasing distances [1]. 

Ideally, researchers would have access to a massive dataset of underwater imagery to train new models. The lack of such a dataset has been one of the major problems with underwater object tracking (UOT) research. The papers involved in this research, however, propose two new datasets for UOT research, the UVOT-400 and LSUI datasets. With these new datasets (among others) and image enhancement techniques, modern SOTA tracker performance can be improved, which is the main inspiration behind this research project. 

The first step in improving the performance of existing tracking models is to train them with a 70/30 split with the new underwater datasets. From there, we can further enhance the images to retrain and further improve performance. Below are the results of training existing models on the UVOT-400 underwater dataset.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/9.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/10.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left, performance tests with no training on UVOT-400. Right, performance tests after training on UVOT-400 (only select models were trained). 
</div>

These results are promising and are better than the initial run, but further improvement is needed to make them comparable to open air (OA) datasets. One way to squeeze out even more performance would be to enhance the images and retrain the models on the enhanced images. There are many image enhancement approaches we could consider, but for this project, a underwater image enhancement algorithm for tracking (UWIE-TR) is proposed. 

This UWIE-TR algorithm is build on a transformer network and is composed of a feature extraction head, UW transformer-based enocder and an output image decoder as shown below [1]. 

Why transformers? 

Transformer based networks, as opposed to convolutional neural networks (CNNs), are more suitable for the underwater domain. This is due to the fact that CNNs have uniform convolution kernels which are not able to characterize inconsistent attenuation within different color channels which is common with underwater imagery [2]. Additionally, CNNs are more focused on local features and are ineffective for long dependent and global feature modeling [2]. 

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/14.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Underwater Image Enhancement for Tracking (UWIE-TR) algorithm. 
</div>

The feature extraction head consists of a convolutional layer with 64 output channels which is then fed into two ResNet blocks which each have two convolutional layers with 64 channels. From here, the transformer based encoder learns the underwater latent space from which the decoder generates the enhanced image [1]. 

The next step is to now train and run the SOTA tracker models on the newly enhanced dataset and see if the performance is increased further. These results are shown below. 

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/13.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Select SOTA tracking models trained and tested on the newly enhanced UVOT-400 dataset. 
</div>

From the graph above, we are able to see further performance improvements (about 5% in the best case as compared to the non enhanced images). 

Future work

Even though performance was increased with both training and image enhancement, there is still about a 20% gap in performance when applying modern SOTA tracker models to underwater images vs open air images (in the best case). This indicates the need for underwater specific trackers in order to obtain more robust models which can be used in the real world. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/15.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/16.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/17.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sample of various results from published image enhancement methods. Red boxes indicate hand picked pseudo groundtruth [2]
</div>

References

[1] Alawode, B., Dharejo, F. A., Ummar, M., Guo, Y., Mahmood, A., Werghi, N., Khan, F. S., Matas, J., & Javed, S.        (2023). Improving underwater visual tracking with a large-scale dataset and image enhancement. arXiv preprint arXiv:2308.15816. https://arxiv.org/pdf/2308.15816

[2] Peng, L., Zhu, C., & Bian, L. (2021). U-shape transformer for underwater image enhancement. arXiv preprint arXiv:2111.11843. https://arxiv.org/pdf/2111.11843