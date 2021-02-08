---
layout: post
comments: true
use_math: true
title: Indoor Passer Counter using Image Processing
categories: ["PROJECTS"]
---

**아직 작성중이라능!**   

## Contents
1. Description
2. Conceptual Design

------------------

## 1. Description
**수행기간: *2019. 09 ~ 2019. 12***   
   
[Demo Video](https://www.youtube.com/watch?v=Qzbkb-v91pE)
   
*본 프로젝트는 실내의 일직선상의 통로에서 특정 방향으로 지나간 사람의 수를 세는 프로젝트로서, 본 프로그램이 임베드된 라즈베리파이와 카메라모듈을 건물 천장에 부착하여 사용하도록 고안되었다.*

### Stack
+ Raspberry Pi
+ OpenCV
+ C++ 

------------------


## 2. Conceptual Design

제약사항은 다음과 같았다.
+ 라즈베리파이 사용 및 엣지 컴퓨팅 (저전력, 저비용)

일반적으로 이미지에서 사람을 검출하는 데에는 Object Detection을 수행하는 머신러닝 솔루션을 적용하지만, 라즈베리파이라는 단일보드 하드웨어 특성상 머신러닝 등의 고연산을 요하는 작업을 실시간으로 수행하는 것은 불가능했다. 때문에 더욱 효율적인 방법을 찾기 위해 먼저 카메라가 촬영하는 영상의 특징을 분석하였고, 다음과 같은 특징들을 얻을 수 있었다. 아래 이미지는 실제 라즈베리파이 카메라를 천장에 부착하여 지나가는 사람을 촬영한 영상이다.   
![image]({{"/assets/images/2019-12-18-1.png"| relative_url}})   
1. 영상 내에서 사람의 이동은 일직선이다.
2. 영상 내에서 사람이 차지하는 크기는 어느 위치에 존재하더라도 대부분 일정하다.
   
위 두 가지 특징을 토대로, 필요한 기능은 다음과 같았다.
+ 사람 감지하기: 이전 프레임과 현재 프레임간의 차이를 이용하는 차영상 기법 이용
+ 감지된 사람 추적하기: Mean Shift 알고리즘 이용
+ 지나간 사람 수 세기: 감지된 사람의 초기 위치와 이동방향을 토대로 사람 수를 계산

## 3. 