---
layout: page
title: "3D Sensor Data Fusion"
description: Combining LiDAR and stereo camera pointclouds to build an occupancy grid for navigating an autonomous vehicle.
category: uni
img: /assets/img/MP_grid_vid.gif
importance: 2
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/assets/img/MP_grid_vid.gif" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    In this video you can see the occupancy grid which was constructed from the pointcloud data.
</div>

For this project the pointcloud data of a LiDAR was fused with the pointclouds obtained from a stereo camera. The data required a lot of preprocessing for it to be usable. First the egomotion of the moving vehicle had to be compensated. Some other challenges were the non-synchronous arrival of the different sensor modalities, or the removal of the ground plane for which the [RANSAC algorithm](https://en.wikipedia.org/wiki/Random_sample_consensus) was employed.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="/assets/img/top_view_lidarvsstereo.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    in this image you see the 2 distinct pointclouds. In green the LiDAR pointcloud and in grey (actually RGB) the stereo camera pointcloud.
</div>
