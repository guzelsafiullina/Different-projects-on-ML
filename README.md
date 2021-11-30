# Different-projects-on-ML
This repo contains solution of the second task for ML course. 
## notebook.ipynb 
This file contains solution of the following projects
### Iris detection
Eyes are considered to be the most salient and stable feature in the computer vision community. 
Automatic extraction of eyes plays an important role in many real-world applications such as gaze tracking, face alignment, driver drowsiness detection, face recognition, and human–computer interaction, etc. Several factors that make challenging to detect and track eyes are head poses, lighting conditions, shape and color of eyes, iris movement, imagining quality and conditions, etc.
A lot of works have been performed to solve the above problems but still, it remains an open area of research in the computer vision community. 
In this task we are going to implement CNN for calculating human iris center.

The solution is inspired by this [article](https://ieeexplore.ieee.org/abstract/document/8803121). 

[GI4E](https://www.unavarra.es/gi4e/databases/gi4e/) dataset was used. 

The solution icnludes following steps:
- Images preprocessing
  1.  Converting them to gray
  2.  Normalizing images
  3.  Cropping eye regions, resizing them to be (48x48) image with the help of eye corners
- Building a CNN model using PyTorch. 
- Compiling and training CNN with different optimizers [sgd, adam, adamax, rmsprop], loss functions [mse,
mae] and activations [tanh, relu, sigmoid].
- Making a prediction for 10 test images. Drawing predicted centers on them and visualize it. 

### Intrusion detection
Anomalies, also referred to as outliers, are defined as a set of patterns which significantly deviate from the normal or expected pattern. In our digital age, anomalies are an integral part of many applications including cyber security , manufacturing, fraud detection, health-care systems and numerous other fields. For instance, in cyber security, intrusion detection system can identify an anomalous pattern like unauthorized access to sensitive information or security violation. One of the major challenges include the scarcity of anomalous labelled data. Most of the systems do not have or few anomalous patterns and make the learning task difficult. To solve this situation, unsupervised anomaly detection model has the ability to learn the model without anomalous data patterns. There are already high performing proposed solution for anomaly binary classification in the domain of cyber security. To better design a defence system it is important to identify the types or clusters of the anomalies. In this task we will be using an unsupervised approach to cluster network intrusions.

Here we work with unsupervised learning problem, so we will use k-means algorithm with number of clusters equals 6 (An Analysis of K-means Algorithm Based Network Intrusion Detection System Yi Yi Aung , Myat Myat Min).

The solution includes following steps:
- Data preprocessing
  1. Encoding categorical features
  2. Scaling
  3. Reducing dimensions with PCA
 - K-means clustering
  1. Finding the best k with Elbow method
  2. K-means algorithm
 - DBscan clustering and detecting outliers
 
### Design Patterns Detection 
The impact of design patterns on quality attributes has been extensively evaluated in studies with different perspectives, objectives, metrics, and quality attributes, leading to contradictive and hard to compare results. Knowing that a particular module implements a design pattern is a shortcut to design comprehension. Manually detecting design patterns is a time consuming and challenging task; therefore, researchers have proposed automatic design patterns detection techniques which include machine learning based approaches. We will implement a machine learning based approach for detecting design patterns category from open source projects. The dataset is a subset of source code metrics for each an every java project. Each project in the dataset belongs to one of 3 categories: Structural, Behavioral, Creational.

The solution includes 
-Data preprocessing
- Random Forest algorithm
- ADAboost Gragient boosting classifier

