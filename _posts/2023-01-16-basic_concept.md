---
layout: single
title:  "파이썬 기초 개면"
categories : 'Programming'
tag : basic, python
---

## funtion과 method

### 변수
변수(객체)는 데이터 값이라 할 수 있다.
e.g., 
```
a = [1,2,3]
```
예시에서 [1,2,3]이라는 데이터는, a라는 변수(객체)에 저장된다. 
### function
### method



$f^{\prime}(x)-2 x=0 $ 
$\Leftrightarrow \frac{d f}{d x}-2 x=0$ 
$\Leftrightarrow y^{\prime}-2 x=0$

\( f^{\prime}(x)=2 x \)
$f(x)=x^2+C$


## class
### 개념
class : 틀과 같이, 똑같은 무언가를 계속해서 만들어 낼 수 있는 설계 도면
object : 클래스로 만든 결과물
->클래스로 만든 객체는 객체마다 고유한 성격을 가지고 있으며, 클래스가 객체의 영향을 받지 않는다.

### 구조
class 안에 구현된 함수는 메서드(Method)라 지칭.
~~~
class Fourcal:
    def setdata(self,first,second):
        self.first = first
        self.second = second
~~~
이후 a 객체를 만들고, a를 통해 setdata 메서드를 다음과 같이 호출
~~~
a = Fourcal()
a.setdata(4,2)
~~~
이 때 객체에 생성되는 객체만의 변수를 객체변수라고 부르며, 현재 a 객체에 객체변수 first와 second이 생성 된 것을 확인 할 수 있음.
~~~
print(a.first)
=> 4
print(a.second)
=> 2
~~~

다른 예시
~~~
class FourCal:
    def setdata(self,first,second):
        self.first = first
        self.second = second
    def add(self):
        result = self.first + self.second
            return result
~~~

~~~
a = FourCal()
a.setdata(4,2) # first와 second에 각각 4와 2가 저장
print(a.add())
=> 6
~~~

### 생성자
초기값을 설정할 필요가 있을 때, 생성자를 구현
=> 생성자 : 객체가 생성될 때 자동으로 호출되는 메서드를 의미

class FourCal의 경우, 초기값 first,second이 필요하지만 따로 선언하지 않고 메서드 add를 사용하게 되면 아래와 같은 에러가 발생한다. 이러한 실수를 방지하기 위해, 처음부터 필요한 초기값을 미리 선언해주는 것이 좋다.
~~~
a = FourCal()
>>> a.add()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 6, in add
AttributeError: 'FourCal' object has no attribute 'first'

~~~

e.g., 생성자 예시
~~~
class FourCal:
  def __init__(self, first, second):
    self.first = first
    self.second = second
  def setdata(self, first, second):
    self.first = first
    self.second = second
  def add(self):
    result = self.first + self.second
    return result
~~~

### 상속
기존 클래스의 기능을 변경하지 않으면서 기능을 추가할 때 사용한다.
super를 통해서 기존 클래스를 상속 받음