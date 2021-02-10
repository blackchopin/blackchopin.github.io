---
layout: single
title: "[논문리뷰] Deep Near Infrared Colorization with Semantic Segmentation and Transfer Learning"
tage: [Segmentation]
comments: true
published: true
categories: Segmentation
use_math: true
typora-copy-images-to: ..\images\Deep_Near_Infrared
---

<br/>

**[논문리뷰] Deep Near Infrared Colorization with Semantic Segmentation and Transfer Learning**

<br/>

## Network architecture

<br/>

![image-20210210142836812](F:/images/Deep_Near_Infrared/image-20210210142836812.png)

<br/>

- Feature-level 과 semantics-level의 두 branch로 구성. 
- Feature-level branch에선, 다중 스케일에서의 feature들을 얻기 위해 dense block을 네트워크의 기본 단위로 사용한다.
- Skip connection을 사용해 얕고 깊은 feature들을 concatenate 해준다.
- Semantics-level branch에선, global 한 정보를 얻기 위해 RefineNet을 사용한다.
- Input HxW -> feature map 1/8 (HxW) 를 통해 Multiscale informamtion을 얻음

<br/>

2688 RGB images 가 있는 SiftFlow dataset 사용

<br/>

<br/>

## **RefineNet**

<br/>

![image-20210210143110659](/images/Deep_Near_Infrared/image-20210210143110659.png)

<br/>

<br/>

## **Dense** **block**

<br/>

![image-20210210143120339](/images/Deep_Near_Infrared/image-20210210143120339.png)

<br/>

- $B_M= f_{rec}(N)$, $M=4$
- 3x3 conv 사용
- Gate unit은 채널수를 낮추는데 사용된다.

<br/>

<br/>

## **Skip connection**

<br/>


- 각각의 layer에서 feature을 재사용하기 위해 skip connection 사용
- Concat하는 형식으로 skip connection 사용
- Concat으로 인해 이전의 edge, detail한 정보들을 얻을 수 있음.

<br/>

<br/>

## **Segmentation Map**

<br/>

- 제안하는 구조가 encoder-decoder구조이기 때문에, semantic segmentation이 NIR colorization에 도움이 됨.
- Semantic segmentation 을 위해 RefineNet 사용
- Multiple object에서 RefineNet이 좋은 성능을 보임
- Semantic feature map 을 얻은 후 segmentation map을 conv layer를 통해 1/8 크기로 줄인다.
- Initial feature map을 encoder의 결과와 cascade한다.