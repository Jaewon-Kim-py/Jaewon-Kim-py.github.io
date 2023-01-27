---
layout: single
title:  "확률 기초"
categories : Basic
tag : basic
---

### Likelihood
데이터가 추정한 분포로 부터 나왔을 가능성
(각 데이터 샘플에서 후보 분포에 대한 높이(likelihood, 확률)를 계산해서 곱한 값)
$P(x \mid \theta)=\prod_{k=1}^n P\left(x_k \mid \theta\right)$
=>가지고 있는 표본을 가장 잘 설명하는 모수를 찾는 함수라 할 수 있다.
### MLE(Maximum Likelihood Estimation)
파라미터 $\theta = (\theta _{1},\cdots  ,\theta _{m})$로 구성된 확률밀도함수 $P(x|\theta)$의 데이터 표본을 $x = (x_{1},\cdots ,x_{n})$라 할 때, 이 표본들로부터  $\theta = (\theta _{1},\cdots  ,\theta _{m})$를 추정하는 방법
=> likelihood를 최대로 하는 추정값 $ \hat{\theta}$를 찾는 과정이라 할 수 있다.


