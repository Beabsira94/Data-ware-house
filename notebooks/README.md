# YOLOv5 Object Detection for Telegram-Scraped Images

## Overview

This project utilizes YOLOv5, a state-of-the-art object detection model, to detect objects in images scraped from Ethiopian medical businesses' Telegram channels. The project includes a Python script that automates the process of loading images, running object detection on each image, and saving the results for further analysis. The main goal of this project is to extract valuable insights from image data to assist in data analysis and decision-making for medical businesses.

## Key Features

1. **Object Detection Using YOLOv5**:

   - A pre-trained YOLOv5 model is used to detect objects in images scraped from various Telegram channels.
   - The detected objects are stored with details such as object class, confidence score, and bounding box coordinates.
2. **Data Export**:

   - Detected objects and relevant data are exported to CSV files for each image, facilitating further data analysis.
3. **Image Processing Pipeline**:

   - The project handles image loading using OpenCV, and runs object detection using the YOLOv5 model.
   - It logs the detection results and saves annotated images displaying the detected objects.

## How to Run

1. **Environment Setup**:

   - Ensure you have the required dependencies installed: PyTorch, OpenCV, and YOLOv5.
   - Clone the YOLOv5 repository from GitHub:
     ```bash
     git clone https://github.com/ultralytics/yolov5.git
     cd yolov5
     pip install -r requirements.txt
     ```
2. **Running Object Detection**:

   - Place your images in the `../data` folder.
   - Run the Python script to perform object detection on all images in the folder:
     ```python
     python detect.py
     ```
3. **View Results**:

   - The detected objects will be shown on the images, and the results will be saved in the `detection_results/` folder.
   - CSV files containing detection results (object class, confidence score, bounding box) are also saved for each image.

## Description of the Code

The code in this notebook performs object detection on images scraped from Telegram channels using a pre-trained YOLOv5 model. The images are processed using OpenCV, and YOLOv5 is applied to detect objects, returning a Pandas DataFrame containing object names, confidence scores, and bounding box coordinates. The detection results are displayed and saved in a separate directory, with corresponding CSV files for easy analysis. This pipeline facilitates automatic object detection and data storage for further analysis in the Ethiopian medical business context.
