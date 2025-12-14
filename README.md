# Introduction
This repo contains the code developed for the third project of my 3D perception university course

# Content
The code provided in the repo is a simple implementation of the paper:</br>
Caltagirone, L., Bellone, M., Svensson, L., & Wahde, M. (2019). 
LIDAR–camera fusion for road detection using fully convolutional neural networks. Robotics and Autonomous Systems, 111, 125–131. 
https://doi.org/10.1016/j.robot.2018.11.002 </br>
This project aims to perform drivable-area segmentation by a fully convolutional network that fuses the information from a camera and a LiDAR sensor.
In my implementation I just focused on the cross-fusion approach leaving for feature development the camera-only, LiDAR-only, early-fusion and the late-fusion approaches

# Implementation
The project tries to follow the choices presented in the paper with some degree of freedom in the LiDAR densification phase and in the evaluation phase
> [!NOTE]
> The network weights provided are obtained training the network on the dataset in this repo and considering a batch_size=1 and 100 epochs

## Dataset
In this repo i provided the KITTI Road dataset that I used to train/evaluate the network.
> [!IMPORTANT]
> The datasrt is slightly modified from the original KITTI Road dataset because i borrowed 51 images from the training dataset to
> create a validation dataset to evaluate the network performances since the testing dataset doesn't provide any ground truth label

# How to use
To test the drivable-area segmentation you can just clone the repo, adjust the dataset path, load the net weights 
(be careful to change the paths, since by now the paths refers to the Kaggle environment i which i developed this project)
and then run the Evaluation and Testing section of the notebook
