
Assignment 3 Exercise: Object Detection and Segmentation
Part 1- Object Segmentation
Object detection is a task in computer vision that involves identifying the presence, location, and type of one or more objects in a given image. In order to have an accurate object detection model, we need to train a model based of thousands or millions of images related to that object and this makes the task even more challenging. As was mentioned in week 2, even after finding appropriate data, training the model is not an easy task. We discussed one solution which was using pre-trained models. COCO is a large-scale object detection, segmentation, and captioning dataset.
a) Load the image dataset oxford_iiit from tf
b) Create the segmentation mask on the first 3 samples in the dataset. Show both the image and the segmented version of it. Remember to map the images into 128x128. 

Now we can start designing the model. We stop this part here and leave the rest of it to Lab 3.1.
Part 2 Annotation
One important aspect of data segmentation and object detection is to have the annotation of the images. In this part, we want to look into annotations of a sample dataset. Download the dataset from here:

https://github.com/experiencor/raccoon_dataset 
a) Like before, show some samples of the images. 

b) A class of fubctions is provided for you that creates mask and images. Use the provided class and create a sample of image and its mask.

Part 3 YOLO 
In 2016, researchers at Washington University, Allen Institute for AI, and Facebook AI Research proposed “You Only Look Once” (YOLO), a family of neural networks that improved the speed and accuracy of object detection with deep learning.
The main improvement in YOLO is the integration of the entire object detection and classification process in a single network. Instead of extracting features and regions separately, YOLO performs everything in a single pass through a single network, hence the name “You Only Look Once.”
YOLOv10, developed by researchers at Tsinghua University using the Ultralytics Python package, offers a novel approach to real-time object detection. It addresses post-processing and model architecture shortcomings found in previous YOLO versions. By removing non-maximum suppression (NMS) and optimizing various model components, YOLOv10 achieves state-of-the-art performance with significantly reduced computational overhead. Extensive experiments highlight its superior accuracy-latency trade-offs across multiple model scales. You can read more about it here.
a)  For the first part of the assignment, we want to see how to create the annotation for a custom dataset. You can use the provided html file (annotation_tool.html). When you open the file, upload an image of your desire and assign the proper class. Here you see an image of a raccoon and its chosen class.

b)  Download required yolo10 tools and check dependencies. Please follow the instructions in this Github page for the information:  https://github.com/ultralytics/ultralytics
Start with installing the required packages and loading the weights associated with the default pre-trained models.
import os
HOME = os.getcwd()
!pip install -q git+https://github.com/THU-MIG/yolov10.git
!mkdir -p {HOME}/weights
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10n.pt
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10s.pt
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10m.pt
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10b.pt
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10x.pt
!wget -P {HOME}/weights -q https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10l.pt

c)  Now, we want to test the model out of box. There is an image stored in: “/content/yolov10/ultralytics/assets/bus.jpg”. Apply YOLO10 command to make predictions. 
After making the prediction, the result will be stored in “/content/runs/detect/predict/bus.jpg”. Call the image and show the result of prediction.
d)  Now, is the time to try to fine-tune the model. Train the Yolo10n model on coco128.ml. For this part use 10 epochs and 32 batches. Show the confusion matrix which is stored in: 
{HOME}/runs/detect/train/confusion_matrix.png
Next, show the learning curves which are stored in: {HOME}/runs/detect/train/results.png
e)  Explain what you see in the learning curves and confusion matrix. 
