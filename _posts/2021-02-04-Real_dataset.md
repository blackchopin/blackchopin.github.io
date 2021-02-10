---
layout: single
title: "[논문리뷰] Real Denoising dataset 관련 논문"
tage: [Denoising]
comments: true
published: true
categories: Denoising
use_math: true
typora-copy-images-to: ..\images\Real_dataset
---

<br/>

**[논문리뷰] Real Denoising dataset 관련 논문**

<br/>

## A Holistic Approach to Cross-Channel Image Noise Modeling and its Application to Image Denoising

<br/>

![image-20210210135558707](/images/Real_dataset/image-20210210135558707.png)

<br/>

- Nikon D800 (ISO=1600, 3200, 6400), Nikon D600(ISO=3200), Canon 5D Mark III (ISO=3200) 으로 얻은 7030x4912 크기의 dataset

- Training 영상으로 11개의 static scene에 대해 scene당 500개의 JPEG 영상을 사용

- 모든 scene의 평균을 ground truth noise-free 영상으로 사용

  <br/>

<img src="/images/Real_dataset/image-20210210135627147.png" alt="image-20210210135627147" style="zoom:80%;" />

<br/>

<br/>

## Benchmarking Denoising Algorithms with Real Photographs

<br/>

#### **Darmstadt Noise Dataset (DND)**

<br/>

- 기존의 Denoising method 들은 Gaussian noise 를 clean image로 변환
- 같은 scene에 대해 Analog gains (ISO 값)을 달리하여 촬영
- Low-ISO image를 GT로 사용하는 대신, 전처리 거침

![image-20210210135748431](/images/Real_dataset/image-20210210135748431.png)

<br/>

![image-20210210135809609](/images/Real_dataset/image-20210210135809609.png)

<br/>

<br/>

## Learning to See in the Dark

<br/>

#### **See-in-the-Dark (SID) dataset**

<br/>

![image-20210210135835434](/images/Real_dataset/image-20210210135835434.png)

<br/>

- 5904개의 raw short-exposure image와 long-exposure image를 포함

- Indoor, outdoor image로 구성되어있으며, outdoor image에서의 조도는 0.2~5lux이고 indoor image는 0.03~0.3lux

- Sony는 4240x2832, Fuji는 6000x4000

  

<br/>

<img src="/images/Real_dataset/image-20210210135902485.png" alt="image-20210210135902485" style="zoom:80%;" />

<br/>

<br/>

## RENOIR - A Dataset for Real Low-Light Image Noise Reduction

<br/>

![image-20210210135937833](/images/Real_dataset/image-20210210135937833.png)

<br/>

- Sensor size가 다른 Canon Rebel T3i, Canon S90, Xiaomi T3i(mobile phone)로 촬영

   (각각 40scene씩 총 120scene)

- Low light sensitivity, long exposure time으로 low noise image 얻음 (reference image)


- light sensitivity↑, exposure time↓으로 noisy image 얻음

- 다시 reference image와 같은 조건에서 clean image 얻음

<br/>

Reference → Noisy → Clean (Sandwich 전략)

<br/>

![image-20210210140050927](/images/Real_dataset/image-20210210140050927.png)

<br/>

<br/>

## Real-world Noisy Image Denoising: A New Benchmark

<br/>

#### 기존 dataset의 단점

<br/>

<img src="/images/Real_dataset/image-20210210140130443.png" alt="image-20210210140130443" style="zoom:80%;" />

<br/>

![image-20210210140156547](/images/Real_dataset/image-20210210140156547.png)