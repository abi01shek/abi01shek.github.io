---
layout: post
title: CXL 2.0 Switching and Memory Disaggregation
date: 2024-04-17 21:01:00
description: How switching in CXL enables memory disaggregation
tags: CXL
categories: CXL
thumbnail: assets/img/9.jpg
---
## Introduction 
CXL 2.0 introduces switching that allows multiple hosts (CPUs) to access partitions of memory within multiple type 3 devices (that use the CXL.mem protocol). The memory partitions within devices are memory mapped, hosts can make memory requests to these locations which are then routed by the switch to appropriate memory partition.

This switching is reconfigurable and provided by a CXL 2.0 switch that has a standardized fabric manager. The fabric manager provides APIs to bind memory partitions to hosts. Note that for devices that use CXL.cache protocol, there is no switching possible and one host has to be connected to one device.

 In CXL nomenclature, a ***logical device*** is an useful abstraction of a device and its internal memory, which will be described next. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/9.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/7.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A simple, elegant caption looks good between image rows, after each row, or doesn't have to be there at all.
</div>

Images can be made zoomable.
Simply add `data-zoomable` to `<img>` tags that you want to make zoomable.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/8.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/10.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

The rest of the images in this post are all zoomable, arranged into different mini-galleries.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/12.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/7.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
