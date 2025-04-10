# Autonomous Driving: Pedestrians and Vehicles Detection using YOLOv11

This project is part of the Data Science and AI Course at Faculty of Electrical Engineering Sarajevo. We utilize the YOLO (You Only Look Once) object detection model to detect and classify pedestrians and vehicles in driving scenarios, primarily using dashcam footage and images. Different configurations and sizes of the YOLO model were explored to evaluate performance.<br>

**Team Members:**
* [Emin Hadziabdic] - ([GitHub Profile](https://github.com/ehadziabdic))
* [Armin Memisevic] - ([GitHub Profile](https://github.com/arminn2206))
* [Muhamed Pasic] - ([GitHub Profile](https://github.com/))
* [Bakir Kosovac] - ([GitHub Profile](https://github.com/bkosovac1))


---
## Dataset 
[Link To Dataset](https://www.kaggle.com)<br>
The dataset used for training and evaluation was sourced from [Name of the Dataset Source]. It consists of approximately [Number] images/video frames capturing diverse driving conditions. The primary annotated classes relevant to this project are `pedestrian`, `car`, `truck`, `bus`, `motorcycle`, `bicycle`. 

## Training 
Training was done on nano and medium size of YOLOv8 model. The training process was optimised with various choice of Optimizers like Adam, Adamax and RMSprop. 
Following are the training parameters and results. 
Training was conducted using various sizes of the YOLOv11 model (`small`, `medium`, and `large`). Key training parameters and validation results are summarized below:

| **Run ID** | **YOLO Size** | **Epochs** | **Batch Size** | **Learning Rate** | **Optimizer** | **Precision (P)** | **Recall (R)** | **mAP50** | **mAP50-95** |
|:----------:|:-------------:|:----------:|:--------------:|:-----------------:|:-------------:|:-----------------:|:--------------:|:---------:|:------------:|
|      1     |   `[small]`   |   `[Num]`  |     `[Num]`    |      `[Value]`    |   `[Name]`    |      `[Num]%`     |     `[Num]%`   |  `[Num]%` |    `[Num]%`  |
|      2     |   `[medium]`  |   `[Num]`  |     `[Num]`    |      `[Value]`    |   `[Name]`    |      `[Num]%`     |     `[Num]%`   |  `[Num]%` |    `[Num]%`  |
|      3     |   `[large]`   |   `[Num]`  |     `[Num]`    |      `[Value]`    |   `[Name]`    |      `[Num]%`     |     `[Num]%`   |  `[Num]%` |    `[Num]%`  |
|    ...     |      ...      |     ...    |       ...      |        ...        |      ...      |        ...        |       ...      |    ...    |      ...     |

## Results
Below are some key performance indicators and visualizations from our training runs.

### 1. [YOLO Size] model with [Optimizer Name] Optimizer (Run ID 1)

* **Precision-Recall Curve:**
    ![PR Curve Run 1]([Link to your PR Curve Image for Run 1])

* **Confusion Matrix:**
    ![Confusion Matrix Run 1]([Link to your Confusion Matrix Image for Run 1])

* **Example Detections:**
    ![Example Detection 1.1]([Link to an Example Detection Image/Video Frame for Run 1])
    ![Example Detection 1.2]([Link to another Example Detection Image/Video Frame for Run 1])