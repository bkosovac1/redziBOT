# Autonomous Driving: Pedestrians and Vehicles Detection using YOLOv11

This project is part of the Data Science and AI Course at Faculty of Electrical Engineering Sarajevo. We utilize the YOLO (You Only Look Once) object detection model to detect pedestrians and vehicles in driving scenarios, classify traffic lights and track lane, primarily using dashcam footage and images. Different configurations and sizes of the YOLO model were explored to evaluate performance.<br>

**Team Members:**
* [Emin Hadziabdic] - ([GitHub Profile](https://github.com/ehadziabdic))
* [Armin Memisevic] - ([GitHub Profile](https://github.com/arminn2206))
* [Muhamed Pasic] - ([GitHub Profile](https://github.com/))
* [Bakir Kosovac] - ([GitHub Profile](https://github.com/bkosovac1))


---
## Datasets

[Pedestrian and Vehicle Detection](https://docs.ultralytics.com/datasets/detect/coco/)<br>
We did not train model for pedestrian and vehicle detection because YOLOv11 model is pre-trained on COCO dataset. It consists of approximately 330K frames capturing many classes, but primary annotated classes relevant to this project are `pedestrian`, `car`, `truck`, `bus`, `motorcycle`, `bicycle`. 

[Traffic Lights Detection](https://universe.roboflow.com/avenue-oqzgk/traffic-light-detection-vfr2s)<br>
The dataset used for training and evaluation of traffic lights detectionwas sourced from RoboFlow. It consists of approximately 732 frames of traffic lights and classes relevant to this project are `green-lights`, `red-lights`, `yellow-lights`

[Lane Segmentation](https://universe.roboflow.com/jk-nanu0/final2-xiiin)<br>
The dataset used for training and evaluation was sourced from RoboFlow. It consists of approximately 1927 frames capturing roads and side-lines. Classes are `lane` and `road`.

## Training 
Training was done on nano and large size of YOLOv11 model. The training process was optimised with recommended optimizer for that specific dataset.
Following are the training parameters and results of all models. 
Training was conducted using various sizes of the YOLOv11 model (`nano` and `large`). Key training parameters and validation results are summarized below:

| **Run ID** | **YOLO Size** | **Epochs** | **Batch Size** | **Learning Rate** | **Optimizer** | **Workers** | **Momentum** | **Precision (P)** | **Recall (R)** |
|:----------:|:-------------:|:----------:|:--------------:|:-----------------:|:-------------:|:-----------:|:------------:|:-----------------:|:--------------:|
|      1     |    `large`    |    `50`    |      `16`      |      `0.01429`    |    `AdamW`    |     `8`     |    `0.9`     |      `[Num]%`     |     `[Num]%`   | 
|      2     |    `nano`     |    `100`   |      `16`      |      `0.00000`    |    `AdamW`    |     `0`     |    `0.0`     |      `[Num]%`     |     `[Num]%`   |
|      3     |    `large`    |    `50`    |      `16`      |      `0.00000`    |    `AdamW`    |     `0`     |    `0.0`     |      `[Num]%`     |     `[Num]%`   |
|      3     |    `nano`     |    `100`   |      `16`      |      `0.00000`    |    `AdamW`    |     `0`     |    `0.0`     |      `[Num]%`     |     `[Num]%`   |

## Results
Below are some key performance indicators and visualizations from our training runs.

### 1. Traffic Light Detection with Large YOLOv11 model (Run ID 1)

* **Precision-Recall Curve:**
    ![PR Curve]([Link to your PR Curve Image])

* **Confusion Matrix:**
    ![Confusion Matrix]([Link to your Confusion Matrix Image])

* **Example Detections:**
    ![Example Detection 1]([Link to an Example Detection Image/Video Frame])
    ![Example Detection 2]([Link to another Example Detection Image/Video Frame])

### 2. Traffic Light Detection with Nano YOLOv11 model (Run ID 2)

* **Precision-Recall Curve:**
    ![PR Curve]([Link to your PR Curve Image])

* **Confusion Matrix:**
    ![Confusion Matrix]([Link to your Confusion Matrix Image])

* **Example Detections:**
    ![Example Detection 1]([Link to an Example Detection Image/Video Frame])
    ![Example Detection 2]([Link to another Example Detection Image/Video Frame])

### 3. Lane Segmentation with Large YOLOv11 model (Run ID 3)

* **Precision-Recall Curve:**
    ![PR Curve]([Link to your PR Curve Image])

* **Confusion Matrix:**
    ![Confusion Matrix]([Link to your Confusion Matrix Image])

* **Example Detections:**
    ![Example Detection 1]([Link to an Example Detection Image/Video Frame])
    ![Example Detection 2]([Link to another Example Detection Image/Video Frame])

### 4. Lane Segmentation with Nano YOLOv11 model (Run ID 4)

* **Precision-Recall Curve:**
    ![PR Curve]([Link to your PR Curve Image])

* **Confusion Matrix:**
    ![Confusion Matrix]([Link to your Confusion Matrix Image])

* **Example Detections:**
    ![Example Detection 1]([Link to an Example Detection Image/Video Frame])
    ![Example Detection 2]([Link to another Example Detection Image/Video Frame])