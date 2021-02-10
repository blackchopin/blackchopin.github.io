---
layout: single
title: "[논문리뷰] EfficientNet- Rethinking Model Scaling for Convolutional Neural Networks"
tage: [ImageRecognition]
comments: true
published: true
categories: ImageRecognition
use_math: true
typora-copy-images-to: ..\images\EfficientNet
---

<br/>

**[논문리뷰] EfficientNet： Rethinking Model Scaling for Convolutional Neural Networks**

<br/>

## **Model** **Size** **vs.** **Accuracy**

<br/>

![image-20210208170931630](/images/EfficientNet/image-20210208170931630.png)

<br/>

파랑 : 성능에 중점을 둔 network

점선 : 효율에 중점을 둔 network

<br/>

<br/>

## **Model** **scaling**

<br/>

![image-20210208171011903](/images/EfficientNet/image-20210208171011903.png)

<br/>

(b) 필터 수 증가

(c) 네트워크 깊이 증가

(d) input의 resolution 증가

(e) 위 3 요소 혼합

<br/>

<br/>

## **Scaling up a baseline model**

<br/>

![image-20210208171039387](/images/EfficientNet/image-20210208171039387.png)

<br/>

<br/>

## Baseline network

<br/>

![image-20210208171058186](/images/EfficientNet/image-20210208171058186.png)

<br/>

depth : $d = α^ϕ$     width : $w = β^ϕ$     resolution : $r = γ^ϕ$

$α∙β∙γ ≈ 2 $    $(α≥1, β≥1, γ≥1)$

α,β,γ는 grid search를 통해 결정. compound coefficient ϕ는 사용자가 설정함 

MBConv : mobile inverted bottleneck

<br/>

![image-20210208171434310](/images/EfficientNet/image-20210208171434310.png)

<br/>

MnasNet의 구조와 Mbconv의 구조. Depthwise convolution 사용

<br/>

<br/>

## EfficientNet의 구조

<br/>

![image-20210208171501243](/images/EfficientNet/image-20210208171501243.png)

<br/>

1. ϕ=1로 고정하고 조건을 만족하는 범위에서 grid search로 α, β, γ 를 구한다.

  ( EfficientNet-B0 의 경우 α=1.2, β=1.1, γ=1.15 )

2. α, β, γ 를 고정 후 ϕ를 증가시켜가며 네트워크 스케일 확장 

<br/>

<br/>

## **Appling compound scaling**

<br/>

![image-20210208171536957](/images/EfficientNet/image-20210208171536957.png)

<br/>

다른 구조에도 적용 할 수 있다.

비슷한 정확도를 보인 모델들과 비교



