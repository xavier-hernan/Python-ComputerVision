# Python-ComputerVision
This project was developed by Xavier Hernan in the MBD April intake in 2022 as a Computer Vision individual assignment. This notebook includes all the steps of the process of building an object detection pipeline: Training, validation, test, based on YOLOv8 (and also a YOLOv5 model). The initial data and task was taken from PIKTOR dataset available from the following github:

https://github.com/ciber-lab/pictor-ppe#dataset

This study was conducted to evaluate the performance of four different computer vision models for object detection in the PIKTOR dataset. The models were YOLOv8s.pt, YOLOv8m.pt, YOLOv8l.pt, and YOLOv5, with the task being to predict the classes of Hat, Vest, and Worker with the highest Mean Average Precision (MAP) and accuracy possible. The idea was to evaluate which one of the three different YOLOv8 models was performing the best using the same hyperparameters. Some hyperparameters had been applied and modified many times to find a combination that gets the best possible relationship between score and computational time. After that hyperparameters tunning, some of them have been stablished.

The dataset has been created by using Roboflow. The images were uploaded and labeled there, and were pre-processed by flipping them horizontally and vertically, and cropping with 0% Minimum Zoom and 20% Maximum Zoom. This dataset is a bit unbalanced on Vest class, that have led to overfitting and high errors in some cases (I tried to solve that using drop out but at the end the MAP in that class was not right).
