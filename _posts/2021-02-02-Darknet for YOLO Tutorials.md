---
layout: page
comments: true
title: Darknet for YOLO Tutorials - Data Processing, Training, and Validation.
categories: [Machine Learning, Object Detection, YOLO]
---
# Description
Object Detection 알고리즘인 YOLO의 모델을 Darknet 프레임워크에서 학습하고 모델의 성능을 평가하는 과정을 담았다.   
[AlexeyAB's Darknet](https://github.com/AlexeyAB/darknet)

# Data Processing
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