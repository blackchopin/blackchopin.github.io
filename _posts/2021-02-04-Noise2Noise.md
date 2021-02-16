---
layout: single
title: "[논문리뷰] Noise2Noise - Learning Image Restoration without Clean Data"
tage: [Denoising]
comments: true
published: true
categories: Denoising
use_math: true
typora-copy-images-to: ..\images\N2N
---

<br/>

[논문리뷰] Noise2Noise - Learning Image Restoration without Clean Data

<br/>

## 1. Introduction

<br/>

![image-20210216101831233](/images/N2N/image-20210216101831233.png)

<br/>

<br/>

## **2. Theoretical Background**

<br/>

![image-20210216101848502](/images/N2N/image-20210216101848502.png)

<br/>

![image-20210216101905883](/images/N2N/image-20210216101905883.png)

<br/>

z = denoised image

x, y 모두 corrupted image

Averge gradient를 통해 주위의 noisy target으로 부터 clean target을 얻음

<br/>

<br/>

## **3** **. Practical Experiments**

<br/>

![image-20210216101937596](/images/N2N/image-20210216101937596.png)

<br/>

*"clean targets are unnecessary in this application"*

<br/>

![image-20210216102009044](/images/N2N/image-20210216102009044.png)

<br/>

![image-20210216102022520](/images/N2N/image-20210216102022520.png)

3종류 noise의 결과영상

<br/>

![image-20210216102045120](/images/N2N/image-20210216102045120.png)



<br/>

![image-20210216102059527](/images/N2N/image-20210216102059527.png)

