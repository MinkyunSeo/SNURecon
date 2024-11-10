# Seoul National University Lecture Hall 3D Reconstruction
## Abstract

This project investigates the challenges and limitations of photo-based 3D reconstruction in densely built and obstacle-rich environments. Using a DJI Mavic 3 Pro drone, 1,000 images were captured through both autonomic and manual flight paths, and the 3D reconstruction was performed using Meshroom, an open-source software employing Structure from Motion (SfM) algorithms. The results highlight significant obstacles such as occlusions caused by natural and man-made structures, difficulties in maintaining image continuity during manual flights, and poor feature matching between autonomic and manual captures. To overcome these challenges, a potential improvement is proposed: separately reconstructing obstructed areas and integrating them into the overall model using point cloud registration. This approach aims to enhance the continuity and accuracy of reconstructions in complex urban settings, paving the way for more robust and scalable reconstruction methodologies.

<br>
<p align="center">
  <img src="./assets/snu28dong.gif" alt="Figure 1" style="width:100%;">
</p>

## Introduction

<br>
<p align="center">
  <img src="./assets/SNU.png" alt="Figure 2" style="width:100%;">
</p>
Seoul National University is situated in a mountainous area, surrounded by numerous natural obstacles, and its buildings are closely situated to each other, which poses significant challenges for photo-based 3D reconstruction. This project explores the conditions necessary for successful reconstruction and examines the current limitations of reconstruction technologies in such complex and densely built environments. Through this study, I aim to identify key factors that contribute to accurate reconstructions and understand the constraints of present-day methods.


<br>
<p align="center">
  <img src="./assets/28dong.png" alt="Figure 3" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Target building: 28, Seoul National University
  </span>
</p>
<br>

## Method
1. **Data Collection**

**Images**: 1,000 images were collected using a DJI Mavic 3 Pro drone. Both autonomic and manual flight paths were used to capture images from various angles and distances. The drone was flown at an altitude of 30m, with a 80% overlap between images.
  <div style="text-align: center;">
    <img src="./assets/drone.png" alt="DJI Mavic 3 Pro" style="width: 100%;">
  </div>
<br>

2. **Reconstruction**

Used [Meshroom](https://github.com/alicevision/Meshroom), an open-source software, to reconstruct the 3D model. The software uses the Structure from Motion (SfM) algorithm to create a 3D model from the images.

<br>
<p align="center">
  <img src="./assets/meshroom.png" alt="Meshroom" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Meshroom 3D reconstruction
  </span>
</p>


## Results

*	Although it is difficult to capture high-angle (aerial) shots due to limited coverage, expanding the shooting range and shooting angles as much as possible can overcome some challenges.

* When manually controlling drone, it is crucial to maintain continuity between images, which is difficult when obstacles such as trees and walls surround buildings. Maintaining continuity is challenging, and it becomes difficult to match features accurately between the automatic and manual shots, resulting in poor feature matching.

* The mismatch in continuity between automatic and manual captures poses an issue. To address this, would it be possible to merge reconstructions after using Point Cloud Registration?

<br>
<p align="center">
  <img src="./assets/recon.png" alt="Meshroom" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Reconstructed Mesh and Top view
  </span>
</p>

<br>
<p align="center">
  <img src="./assets/front.png" alt="front1" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Front view
  </span>
</p>

<br>
<p align="center">
  <img src="./assets/side.png" alt="side1" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Side view
  </span>
</p>

**Improvement Suggestion**


<br>
<p align="center">
  <img src="./assets/solution.png" alt="solution" style="width:100%;">
</p>

One of the key challenges identified in this project is the loss of continuity in the reconstruction process due to obstacles obstructing the view. To address this issue, a potential solution is to separately reconstruct each obstructed area or surface and then merge these reconstructions using point cloud registration. This method would allow for a more complete and continuous 3D model by focusing on individual surfaces impacted by obstacles, followed by a careful alignment and integration with the overall model.
