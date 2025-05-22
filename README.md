# Autonomous Driving: Pedestrians and Vehicles Detection using YOLOv11

This project is part of the Data Science and AI Course at Faculty of Electrical Engineering Sarajevo. We utilize the YOLO (You Only Look Once) object detection model to detect pedestrians and vehicles in driving scenarios, classify traffic lights and track lane, primarily using dashcam footage and images. Different configurations and sizes of the YOLO model were explored to evaluate performance.<br>

**Team Members:**
* [Emin Hadžiabdić] - ([GitHub Profile](https://github.com/ehadziabdic))
* [Armin Memišević] - ([GitHub Profile](https://github.com/arminn2206))
* [Muhamed Pašić] - ([GitHub Profile](https://github.com/MuhaxD))
* [Bakir Kosovac] - ([GitHub Profile](https://github.com/bkosovac1))


---
## Datasets

[Pedestrian and Vehicle Detection](https://docs.ultralytics.com/datasets/detect/coco/)<br>
We did not train model for pedestrian and vehicle detection because YOLOv11 model is pre-trained on COCO dataset. It consists of approximately 330K frames capturing many classes, but primary annotated classes relevant to this project are `pedestrian`, `car`, `truck`, `bus`, `motorcycle`, `bicycle`.

[Traffic Lights Detection](https://universe.roboflow.com/autodrivemodels/traffic-light-detection-v1/dataset/1)<br>
The dataset used for training and evaluation of traffic lights detection is available on RoboFlow. It consists of approximately 732 frames of traffic lights and classes relevant to this project are `green-lights`, `red-lights`, `yellow-lights`

[Lane Segmentation](https://universe.roboflow.com/autodrivemodels/lane-segmentation-5yla7-trsxa/dataset/3)<br>
The dataset used for training and evaluation is available on RoboFlow. It consists of approximately 1927 frames capturing roads and side-lines. Classes are `lane` and `road`.

## Training 
Training was done on nano and large size of YOLOv11 model. The training process was optimised with recommended optimizer for that specific dataset.
Following are the training parameters and results of all models. 
Training was conducted using various sizes of the YOLOv11 model (`nano` and `large`). Key training parameters and validation results are summarized below:

|         **Model**        | **YOLO Size** | **Epochs** | **Batch Size** | **Learning Rate** |  **Optimizer**  | **Momentum** |  **Dropout**  | **Precision (P)** | **Recall (R)** | **mAP50** | **mAP50-95** |
|:------------------------:|:-------------:|:----------:|:--------------:|:-----------------:|:---------------:|:------------:|:-------------:|:-----------------:|:--------------:|:---------:|:------------:|
| Traffic Lights Detection |    `large`    |    `50`    |      `16`      |     `0.001429`    |  `Auto: AdamW`  |     `0.9`    |     `0.0`     |      `81.4%`      |     `87.4%`    |  `91.0%`  |    `47.9%`   | 
| Traffic Lights Detection |    `nano`     |    `100`   |      `64`      |     `0.001429`    |  `Auto: AdamW`  |     `0.9`    |     `0.0`     |      `91.1%`      |     `89.2%`    |  `94.1%`  |    `50.1%`   | 
|     Lane Segmentation    |    `large`    |    `50`    |      `16`      |     `0.001667`    |  `Auto: AdamW`  |     `0.9`    |     `0.0`     |      `83.2%`      |     `86.4%`    |  `85.8%`  |    `77.2%`   | 
|     Lane Segmentation    |    `nano`     |    `100`   |      `64`      |     `0.001667`    |  `Auto: AdamW`  |     `0.9`    |     `0.0`     |      `82.9%`      |     `88.9%`    |  `86.8%`  |    `78.7%`   |

## Results
Below are some key performance indicators and visualizations from our training runs.

### 1. Traffic Lights Detection with Large YOLOv11 model

* **Precision-Confidence Curve:**

    <img src=".\data\analytics\trafficlights_large\P_curve.png" alt="P Curve ID1" width="720"/>

* **Recall-Confidence Curve:**

    <img src=".\data\analytics\trafficlights_large\R_curve.png" alt="R Curve ID1" width="720"/>

* **Precision-Recall Curve:**

    <img src=".\data\analytics\trafficlights_large\PR_curve.png" alt="PR Curve ID1" width="720"/>

* **Confusion Matrix:**

    <img src=".\data\analytics\trafficlights_large\confusion_matrix_normalized.png" alt="Confusion Matrix ID1" width="720"/>

* **Results:**

    <img src=".\data\analytics\trafficlights_large\results.png" alt="Results ID1" width="720"/>

* **Example Detections:**

    - Model Labels

    <img src=".\data\analytics\trafficlights_large\val_batch0_labels.jpg" alt="Batch Labels ID1" width="720"/>

    - Model Prediction

    <img src=".\data\analytics\trafficlights_large\val_batch0_pred.jpg" alt="Batch Prediction ID1" width="720"/>

### 2. Traffic Lights Detection with Nano YOLOv11 model

* **Precision-Confidence Curve:**

    <img src=".\data\analytics\trafficlights_nano\P_curve.png" alt="P Curve ID2" width="720"/>

* **Recall-Confidence Curve:**

    <img src=".\data\analytics\trafficlights_nano\R_curve.png" alt="R Curve ID2" width="720"/>

* **Precision-Recall Curve:**

    <img src=".\data\analytics\trafficlights_nano\PR_curve.png" alt="PR Curve ID2" width="720"/>

* **Confusion Matrix:**

    <img src=".\data\analytics\trafficlights_nano\confusion_matrix_normalized.png" alt="Confusion Matrix ID2" width="720"/>

* **Results:**

    <img src=".\data\analytics\trafficlights_nano\results.png" alt="Results ID2" width="720"/>

* **Example Detections:**

    - Model Labels

    <img src=".\data\analytics\trafficlights_nano\val_batch0_labels.jpg" alt="Batch Labels ID2" width="720"/>

    - Model Prediction

    <img src=".\data\analytics\trafficlights_nano\val_batch0_pred.jpg" alt="Batch Prediction ID2" width="720"/>

### 3. Lane Segmentation with Large YOLOv11 model

* **Precision-Confidence Curve:**

    <img src=".\data\analytics\lane_large\BoxP_curve.png" alt="P Curve ID3" width="720"/>

* **Recall-Confidence Curve:**

    <img src=".\data\analytics\lane_large\BoxR_curve.png" alt="R Curve ID3" width="720"/>


* **Precision-Recall Curve:**

    <img src=".\data\analytics\lane_large\BoxPR_curve.png" alt="PR Curve ID3" width="720"/>

* **Confusion Matrix:**

    <img src=".\data\analytics\lane_large\confusion_matrix.png" alt="Confusion Matrix ID3" width="720"/>

* **Results:**

    <img src=".\data\analytics\lane_large\results.png" alt="Results ID3" width="720"/>

* **Example Detections:**

    - Model Labels

    <img src=".\data\analytics\lane_large\val_batch0_labels.jpg" alt="Batch Labels ID3" width="720"/>

    - Model Prediction

    <img src=".\data\analytics\lane_large\val_batch0_pred.jpg" alt="Batch Prediction ID3" width="720"/>

### 4. Lane Segmentation with Nano YOLOv11 model

* **Precision-Confidence Curve:**

    <img src=".\data\analytics\lane_nano\BoxP_curve.png" alt="P Curve ID4" width="720"/>

* **Recall-Confidence Curve:**

    <img src=".\data\analytics\lane_nano\BoxR_curve.png" alt="R Curve ID4" width="720"/>

* **Precision-Recall Curve:**

    <img src=".\data\analytics\lane_nano\BoxPR_curve.png" alt="PR Curve ID4" width="720"/>

* **Confusion Matrix:**

    <img src=".\data\analytics\lane_nano\confusion_matrix.png" alt="Confusion Matrix ID4" width="720"/>

* **Results:**

    <img src=".\data\analytics\lane_nano\results.png" alt="Results ID4" width="720"/>

* **Example Detections:**

    - Model Labels

    <img src=".\data\analytics\lane_nano\val_batch0_labels.jpg" alt="Batch Labels ID4" width="720"/>

    - Model Prediction
    
    <img src=".\data\analytics\lane_nano\val_batch0_pred.jpg" alt="Batch Prediction ID4" width="720"/>