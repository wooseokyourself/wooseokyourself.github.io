---
layout: post
comments: true
use_math: true
title: Indoor Passer Counter using Image Processing
categories: ["PROJECTS"]
---

**아직 작성중이라능!**   

## Description
*2019. 09 ~ 2019. 12*   
본 프로젝트는 실내의 일직선상의 통로에서 특정 방향으로 지나간 사람의 수를 세는 프로젝트로서, 본 프로그램이 임베드된 라즈베리파이와 카메라모듈을 건물 천장에 부착하여 사용하도록 고안되었다. 특정 조건을 만족하는 출입구에 부착하면 실내에 존재하는 사람의 수를 세는 프로그램으로의 확장도 가능하다.

[Video](https://www.youtube.com/watch?v=Qzbkb-v91pE)

### Constraints
+ 하드웨어를 최대한 저비용으로 구성할 수 있어야 함
+ 최대한 저전력으로 장시간 유지되어야 함

### Stack
+ Raspberry Pi
+ OpenCV
+ C++ 

------------------

## Contents
1. Image Processing
2. 

### Image Processing
![image]({{ site.baseurl }}/_posts/images/2019-12-18-1.png)
천장에 설치한 카메라를 통해 통행하는 사람의 수를 세기 위해서는 영상을 실시간으로 촬영하고 처리해야 한다. 일반적으로 이미지에서 사람을 검출하는 데에는 Object Detection을 수행하는 머신러닝 솔루션을 적용하지만, 라즈베리파이라는 단일보드 하드웨어 특성상 머신러닝 등의 고연산을 요하는 작업을 실시간으로 수행하는 것은 불가능했다. 때문에 더욱 효율적인 방법을 찾기 위해 먼저 카메라가 촬영하는 영상의 특징을 분석하였고, 다음과 같은 특징들을 얻을 수 있었다.   
1. 영상 내에서 사람의 이동은 일직선이다.
2. 영상 내에서 사람의 차지하는 크기는 어느 위치에 존재하더라도 대부분 일정하다.
위에서 다양한 

#### 