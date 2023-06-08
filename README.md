# Construction-Site-Safety-Gears-Detection
Safety gears detection of 10 different classes of construction site workers. This repo contains the custom object detection notebook, models, dataset, results using YoloV8. You can customize the training models with your own dataset using the notebook provided
# Introduction
This repository contains code and resources for training and deploying a deep learning model to detect and recognize construction safety gears in images and videos. The objective of this project was to detect the safety gears of constructio workers, so that it can be used in workers safety inspection, tracking and more. The model is trained to identify various safety gears such as hardhats, masks, safety vests, gloves, and safety boots, with the goal of promoting safety and compliance in construction sites.
# Features
* Training code for custom object detection using YoloV8.

* Pretrained models for construction safety gear detection.

* Dataset preparation and augmentation scripts.

* Inference code for real-time detection on images, videos, and webcam feeds.

* Evaluation metrics and visualization tools.
# Setup
The code was run on Google Colab, with a T4 GPU. We installed ultralytics library by [Ultralytics](http://docs.ultralytics.com/), imported ultralytics and IPython library to run YoloV8 custom object detection on custom dataset.
# Dataset
We used a self made dataset which is provided on Roboflow on [Construction Safety Gears Dataset](https://universe.roboflow.com/construction-ppe-dataset/construction-safety-gears-vcbdq). The dataset consists of 424 images with labels. The images are split into train:360, valid:30, test:34 sets, each folder consisting of imagesand labels folders. 

Totatl of 10 classes has been used for detection:
'Gloves', 'Hardhat', 'Mask', 'NO-Gloves', 'NO-Hardhat', 'NO-Mask', 'NO-Safety Boot', 'NO-Safety Vest', 'Person', 'Safety Boot', 'Safety Vest'

data folder consists of the .yaml file required for training. It also contains 3 folders train, valid and test. Each of these folders have 2 subfolders images (with .jpg files) and labels (with .txt annotations).
# MODELS
# Pretrained Model
We have included pretrained model yolov8s.pt to traine our custom construction safety gear dataset. You can find the download links and instructions for using these models in the [Pretrained Models](https://docs.ultralytics.com/tasks/detect/).
# Customed Trained Model 
Using the pretrained model yolov8s.pt, we trained our dataset and created the customed trained model best.pt.

Both pretrained model yolov8s.pt and best.pt are provided in the models folder. best.pt can be used for detecting the construction workers safety gears inspection.
# source_files
SOource_file folder consists of the test images used to evaluation of our custom trained model.
# Results
results folder consists of 2 folders train and val. train folder consists visualiztion of train batches, confusion matrix for trainig, F1_curve, P_curve, PR_curve, R_curve of training results. Similarly val consists visualiztion of validation batches, confusion matrix for trainig, F1_curve, P_curve, PR_curve, R_curve of validation results.

The training of YoloV8n model was done for 100 epochs and was completed in 0.613 hours. After training, we get the following results:

(results/train/confusion_matrix.png)
