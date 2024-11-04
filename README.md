# Seoul National University Lecture Hall 3D Reconstruction

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
  <img src="./assets/28dong.jpg" alt="Figure 3" style="width:80%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Target building: 28, Seoul National University
  </span>
</p>

<br>
<p align="center">
  <img src="./assets/tree.jpg" alt="Figure 3" style="width:40%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Obstacles: Trees
  </span>
</p>

## Method
1. **Data Collection**

**Images**: 1,000 images were collected using a DJI Mavic 3 Pro drone. Both autonomic and manual flight paths were used to capture images from various angles and distances. The drone was flown at an altitude of 30m, with a 80% overlap between images.
<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
  <div style="text-align: center;">
    <img src="./assets/drone.png" alt="DJI Mavic 3 Pro" style="width: 200px;">
  </div>

  <div style="text-align: center;">
    <img src="./assets/dronepath.png" alt="Autonomous drone flight path" style="width: 400px;">
    <p style="font-size: smaller; margin-top: 5px;">Autonomous drone flight path</p>
  </div>
</div>
<div style="display: flex; justify-content: center; align-items: center; gap: 20px;">
    <div style="text-align: center;">
        <img src="./assets/droneimg1.jpg" alt="DJI Mavic 3 Pro" style="width: 200px;">
    </div>
    <div style="text-align: center;">
        <img src="./assets/droneimg2.jpg" alt="DJI Mavic 3 Pro" style="width: 200px;">
    </div>
    <div style="text-align: center;">
        <img src="./assets/droneimg3.jpg" alt="DJI Mavic 3 Pro" style="width: 200px;">
    </div>
    <div style="text-align: center;">
        <img src="./assets/droneimg4.jpg" alt="DJI Mavic 3 Pro" style="width: 200px;">
    </div>
</div>
<br>

2. **Reconstruction**

Used [Meshroom](https://github.com/alicevision/Meshroom), an open-source software, to reconstruct the 3D model. The software uses the Structure from Motion (SfM) algorithm to create a 3D model from the images.

<br>
<p align="center">
  <img src="./assets/Meshroom.png" alt="Meshroom" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Meshroom 3D reconstruction
  </span>
</p>


3. **Results**

<br>
<p align="center">
  <img src="./assets/Meshroom2.png" alt="Meshroom" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Reconstructed Mesh
  </span>
</p>

<br>
<p align="center">
  <img src="./assets/top.png" alt="Meshroom" style="width:100%;">
</p>
<p align="center">
  <span style="font-size: smaller;">
    Top view
  </span>
</p>