# Chapter 4 How to Transform Time Series to a Supervised Learning Problem
Time series forecasting은 supervised learning problem으로 접근할 수 있다. 이 때 목표는 input data(x)가 있을 때 해당 데이터에 대한 output data(y)를 예측할 수 있도록 하는 것이다. 
~~~
x, y 
5, 0.9
4, 0.8
5, 1.0
3, 0.7
4, 0.9
~~~
이렇게 정답이 주어진 데이터셋으로 학습하는 방법을 supervised learning이라 하고, 그 종류고 크게 두 가지가 있다.
- Classification : output이 범주형인 경우 
e.g., 사망 여부 등
- Regression : output이 연속형인 격우
e.g., 몸무게 등

## 4.2 Sliding Window
time series의 경우, previous time steps을 input으로 사용하고, next time step을 output으로 사용할 수 있다.
~~~
time, measure
1,    100
2,    110
3,    108
4,    115
5,    120
~~~
e.g., Example of a small contived time series dataset

previous time step 값을 사용하여 next time step의 값을 예측함으로써 supervised learning task로 재구성할 수 있다.
~~~
x, y
?, 100
100, 110
110, 108
108, 115
115, 120
120, ?
~~~
e.g., Example of time series dataset as supervised learning

이렇게 prior time steps을 사용하여 next time step을 예측하는 방법을 sliding window method라고 한다.
(The number of previous time steps is called the window width or size of the lag)


## 4.3 Sliding Window With Multiple Variates
- Univariate : A single variable is observed at each time
- Multivariate : two or more variables are observed at each time
대부분의 시계열 분석 방법들은 univariate에 초점을 맞추고 있으며, multivariate의 경우 univariate 보다 모델링 하기 어렵고 기존 방법이 잘 동작하지 않는다는 어려움이 있다.

## 4.4 Sliding Window With Multiple Steps
- Multi-step Forecast : two or more future time steps are to be predicted


