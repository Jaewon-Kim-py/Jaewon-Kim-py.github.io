---
layout: single
title:  "Time Series - basic"
categories : 'Time Series'
tag : basic, TS
---
# Chapter 1 : Promise of Deep Learning for Time Series Forecasting
딥 러닝은 입력에서 출력으로의 복잡한 매핑을 자동으로 학습하고 multiple input과 output을 지원한다. 이는 시계열 예측, 특히 complex-nonliniear dependencies, multivalent inputs and multi-step forecasting을 가능하게 한다.
## 1.1 Time Series Forecasting
분류나 회귀와 같은 단순한 task와는 다르게, 시계열의 경우 complexity of order, temporal dependence between observations 등을 고려해야 한다. 이를 위해서는 데이터에 추가적인 전처리가 필요하며, 기존에는 ARIMA와 같은 통계적(선형)방법을 사용하였다. 이러한 통계적 방법은 다음과 같은 한계점이 존재한다.
- Focus on complete data : 결측값이 없어야 한다
- Focus on linear relationships
- Focus on fixed temporal dependence : relationship between observations at different times를 살펴볼 때 time lag에 대한 정보가 반드시 명시되어야 한다.
- Focus on univariate data
- Focus on one-step forecasts

반면 Machine learning method의 경우, multiple input variables, complex nonlinear relationships, missing data를 효과적으로 처리할 수 있다.

## 1.2 Multilayer Perceptrons for Time Series

## 1.3 Convolutional Neural Networks for Time Series

## 1.4 Recurrent Neural Networks for Time seires

## 1.5 Promise of Deep Learning


