# Facial-expression

## Introduction

- This project aims to classify the emotion on a person's face into one of five categories, using deep convolutional neural networks. This repository is an implementation of this research paper. The model is trained on the FER-2013 dataset which was published on International Conference on Machine Learning (ICML). This dataset consists of 35887 grayscale, 48x48 sized face images with five emotions - angry,
happy, neutral, sad and surprised.

## Dependencies
- Python 3, OpenCV, Tensorflow 
- To install the required packages, run pip install -r requirements.txt.

## Basic Usage
The repository is currently compatible with tensorflow-2.0 and makes use of the Keras API using the tensorflow.keras library.

- Download the FER-2013 dataset from here and unzip it inside the src folder. This will create the folder data.
- The folder structure is of the form:
  - data (folder)
  - detector.py (file)
  - CNN_Model.py (file)
  - haarcascade_frontalface_default.xml (file)
  - Emotion_little_vgg.h5 (file)
  
## Data Preparation (optional)
- The original FER2013 dataset in Kaggle is available as a single csv file. I had converted into a dataset of images in the PNG format for training/testing.

## Algorithm
- First, the haar cascade method is used to detect faces in each frame of the webcam feed.
- The region of image containing the face is resized to 48x48 and is passed as input to the CNN.
- The network outputs a list of softmax scores for the five classes of emotions.
- The emotion with maximum score is displayed on the screen.

