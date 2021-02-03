---
layout: post
comments: true
title: Object Detection Camera
categories: ["PROJECTS"]
---
### Description
1. Training YOLO Models
2. Detection Mode Configuration 
3. Admin Mode Configuration

------------------

### Training YOLO Models
#### Stack
+ Used [AlexeyAB's Darknet](https://github.com/AlexeyAB/darknet) for deep learning framework.
+ Used [YOLOv4](https://arxiv.org/abs/2004.10934) object detection network.

#### Data Processing
Darknet 에서의 학습을 위해 아래와 같은 구조의 데이터셋을 먼저 구성해야 한다.

```
mydata
├── dataset
│   ├── 00001.jpg
│   ├── 00001.txt
│   ├── 00002.jpg
│   ├── 00003.txt
│   └── ...
├── readme.txt
├── mydata.names
├── mydata.data
├── test.txt
├── train.txt
└── valid.txt
```

------------------

### Detection Mode Configuration
#### Stack
+ Used Raspberry Pi 4B as a device with Raspberry Pi OS.
+ Used CAT.M1 as a modem.
+ Used OpenCV 4 for taking picture and image processing.
+ C++ based.

------------------

### Admin Mode Configuration
#### Stack
