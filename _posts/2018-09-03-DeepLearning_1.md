---
layout: post
title: "나의 첫 딥러닝"
excerpt_separator:  <!--more-->
categories:
 - Data science
tags:
  - 기계학습
  - 데이터 과학
  - 모두의 딥러닝
---

<!--more-->

# 출처

## 조태호, 『모두의 딥러닝』, (주) 도서출판 길벗(2018-06-08), 18-39p

---

## 01 최고급 요리를 먹을 시간

### 머신러닝(machine learning)

* 사람과 유사한 판단을 컴퓨터가 할 수 있게 하는 가장 효과적인 기법

### 딥러닝

* 머신러닝의 여러 알고리즘들 중 가장 효과적인 알고리즘
* 인공지능 = 음식
* 머신러닝 = 고기
* 딥러닝 = 최고급 스테이크

---

### 01-1 딥러닝 실행을 위한 준비 사항

#### 아나콘다 설치 --> 텐서플로 설치 --> 케라스 설치 --> 파이참 설치

#### 1. [아나콘다 설치](https://www.anaconda.com/download/)

#### 2. Anaconda Prompt 실행

#### 3. `conda create -n tutorial python=3.5 numpy scipy matplotlib spyder pandas seaborn scikit-learn h5py`

* tutorial --> 작업 환경 이름
* python=3.5 --> 파이썬 버전
* numpy ~ h5py --> 필요한 모든 라이브러리 이름

#### 4. `activate tutorial`

생성한 tutorial 환경 활성화 명령

#### 5. `pip install tensorflow`

텐서플로 설치

#### 6. `python`

파이썬 실행

#### 7. `import tensorflow as tf`

#### 8. `print(tf.__version__)`

텐서플로 버전 출력 시 텐서플로 설치 완료

#### 9. `exit()`

#### 10. `pip install keras`

케라스 설치

#### 11. [파이참 설치](https://www.jetbrains.com/pycharm/download/#section=windows)

#### 12. 파이참 실행

#### 13. Create New Project 버튼

#### 14. 경로 뒤에 \deeplearning 입력

#### 15. Project Interpreter... 클릭

#### 16. Existing interpreter 선택 후 오른쪽 끝 ... 클릭

#### 17. Add Local 선택 후 Conda Environment 선택 후 오른쪽 ... 클릭

#### 18. ![image](https://user-images.githubusercontent.com/28076542/44796353-c96da000-abe7-11e8-92e8-03b2e1afe933.png)

위와 같이 경로 입력 후 OK 클릭

#### 19. Create 버튼 클릭

#### 20. 윈도 탐색기로 PycharmProjects 폴더에 deeplearning 폴더 확인

#### 21. [폴더안에 예제 소스 파일 복사](http://www.gilbut.co.kr/book/bookView.aspx?bookcode=BN001909&page=1&TF=T)

![image](https://user-images.githubusercontent.com/28076542/44796561-2bc6a080-abe8-11e8-9a28-0ad09ffd78ea.png)

#### 22. ![image](https://user-images.githubusercontent.com/28076542/44796643-5e709900-abe8-11e8-8777-cc108bb77d3d.png)

#### 23. deep_code 폴더 > 01_My_First_Deeplearning.py 선택

#### 24. 메뉴의 Run > Run 클릭 --> 여기서 interpreter 설정 또 할 수도 있음

#### 25. 실행 결과 확인

```bash
C:\Users\kai01\Anaconda3\envs\tutorial\python.exe C:/Users/kai01/PycharmProjects/deeplearning/deep_code/01_My_First_Deeplearning.py
Using TensorFlow backend.
Epoch 1/30
2018-08-30 00:09:53.995181: I T:\src\github\tensorflow\tensorflow\core\platform\cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2

 10/470 [..............................] - ETA: 7s - loss: 1.0000 - acc: 0.0000e+00
470/470 [==============================] - 0s 386us/step - loss: 0.6611 - acc: 0.3149
Epoch 2/30

 10/470 [..............................] - ETA: 0s - loss: 0.0994 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1488 - acc: 0.8511
Epoch 3/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 72us/step - loss: 0.1488 - acc: 0.8511
Epoch 4/30

 10/470 [..............................] - ETA: 0s - loss: 0.3980 - acc: 0.6000
470/470 [==============================] - 0s 66us/step - loss: 0.1488 - acc: 0.8511
Epoch 5/30

 10/470 [..............................] - ETA: 0s - loss: 2.2996e-12 - acc: 1.0000
470/470 [==============================] - 0s 64us/step - loss: 0.1488 - acc: 0.8511
Epoch 6/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1487 - acc: 0.8511
Epoch 7/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 62us/step - loss: 0.1487 - acc: 0.8511
Epoch 8/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1487 - acc: 0.8511
Epoch 9/30

 10/470 [..............................] - ETA: 0s - loss: 5.3299e-07 - acc: 1.0000
470/470 [==============================] - 0s 64us/step - loss: 0.1487 - acc: 0.8511
Epoch 10/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 70us/step - loss: 0.1486 - acc: 0.8511
Epoch 11/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 76us/step - loss: 0.1498 - acc: 0.8447
Epoch 12/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 74us/step - loss: 0.1486 - acc: 0.8511
Epoch 13/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 68us/step - loss: 0.1485 - acc: 0.8511
Epoch 14/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 70us/step - loss: 0.1483 - acc: 0.8511
Epoch 15/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 59us/step - loss: 0.1485 - acc: 0.8511
Epoch 16/30

 10/470 [..............................] - ETA: 0s - loss: 0.1015 - acc: 0.9000
470/470 [==============================] - 0s 68us/step - loss: 0.1490 - acc: 0.8447
Epoch 17/30

 10/470 [..............................] - ETA: 0s - loss: 2.0702e-15 - acc: 1.0000
470/470 [==============================] - 0s 66us/step - loss: 0.1479 - acc: 0.8489
Epoch 18/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 74us/step - loss: 0.1482 - acc: 0.8468
Epoch 19/30

 10/470 [..............................] - ETA: 0s - loss: 0.3000 - acc: 0.7000
470/470 [==============================] - 0s 66us/step - loss: 0.1476 - acc: 0.8511
Epoch 20/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 62us/step - loss: 0.1480 - acc: 0.8511
Epoch 21/30

 10/470 [..............................] - ETA: 0s - loss: 0.2997 - acc: 0.7000
470/470 [==============================] - 0s 68us/step - loss: 0.1475 - acc: 0.8511
Epoch 22/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1469 - acc: 0.8511
Epoch 23/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1466 - acc: 0.8511
Epoch 24/30

 10/470 [..............................] - ETA: 0s - loss: 0.2083 - acc: 0.8000
470/470 [==============================] - 0s 70us/step - loss: 0.1475 - acc: 0.8489
Epoch 25/30

 10/470 [..............................] - ETA: 0s - loss: 0.2996 - acc: 0.7000
470/470 [==============================] - 0s 57us/step - loss: 0.1470 - acc: 0.8511
Epoch 26/30

 10/470 [..............................] - ETA: 0s - loss: 2.6178e-05 - acc: 1.0000
470/470 [==============================] - 0s 57us/step - loss: 0.1466 - acc: 0.8511
Epoch 27/30

 10/470 [..............................] - ETA: 0s - loss: 0.3000 - acc: 0.7000
470/470 [==============================] - 0s 57us/step - loss: 0.1472 - acc: 0.8511
Epoch 28/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1471 - acc: 0.8511
Epoch 29/30

 10/470 [..............................] - ETA: 0s - loss: 0.1991 - acc: 0.8000
470/470 [==============================] - 0s 57us/step - loss: 0.1470 - acc: 0.8489
Epoch 30/30

 10/470 [..............................] - ETA: 0s - loss: 8.9039e-07 - acc: 1.0000
470/470 [==============================] - 0s 55us/step - loss: 0.1461 - acc: 0.8532

 32/470 [=>............................] - ETA: 0s
470/470 [==============================] - 0s 68us/step

 Accuracy: 0.8511

Process finished with exit code 0
```

---

## 02 처음 해 보는 딥러닝

### 02-1 미지의 일을 예측하는 힘

* 학습: 데이터가 입력되고 패턴이 분석되는 과정
* 예측: 학습을 통해 경계선을 긋는 것
* 머신러닝의 예측 성공률은 **얼마나 정확한 경계선을 긋느냐에 달림**

### 02-2 폐암 수술 환자의 생존율 예측하기

### 01_My_First_Deeplearning.py

```python
# -*- coding: utf-8 -*-
# 코드 내부에 한글을 사용가능 하게 해주는 부분입니다.

# 딥러닝을 구동하는 데 필요한 케라스 함수를 불러옵니다.
from keras.models import Sequential
from keras.layers import Dense

# 필요한 라이브러리를 불러옵니다.
import numpy
import tensorflow as tf

# 실행할 때마다 같은 결과를 출력하기 위해 설정하는 부분입니다.
seed = 0
numpy.random.seed(seed)
tf.set_random_seed(seed)

# 준비된 수술 환자 데이터를 불러들입니다.
Data_set = numpy.loadtxt("../dataset/ThoraricSurgery.csv", delimiter=",")

# 환자의 기록과 수술 결과를 X와 Y로 구분하여 저장합니다.
X = Data_set[:,0:17]
Y = Data_set[:,17]

# 딥러닝 구조를 결정합니다(모델을 설정하고 실행하는 부분입니다).
model = Sequential()
model.add(Dense(30, input_dim=17, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

# 딥러닝을 실행합니다.
model.compile(loss='mean_squared_error', optimizer='adam', metrics=['accuracy'])
model.fit(X, Y, epochs=30, batch_size=10)

# 결과를 출력합니다.
print("\n Accuracy: %.4f" % (model.evaluate(X, Y)[1]))
```

### 실행결과

```bash
C:\Users\kai01\Anaconda3\envs\tutorial\python.exe C:/Users/kai01/PycharmProjects/deeplearning/deep_code/01_My_First_Deeplearning.py
Using TensorFlow backend.
Epoch 1/30
2018-08-30 00:09:53.995181: I T:\src\github\tensorflow\tensorflow\core\platform\cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2

 10/470 [..............................] - ETA: 7s - loss: 1.0000 - acc: 0.0000e+00
470/470 [==============================] - 0s 386us/step - loss: 0.6611 - acc: 0.3149
Epoch 2/30

 10/470 [..............................] - ETA: 0s - loss: 0.0994 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1488 - acc: 0.8511
Epoch 3/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 72us/step - loss: 0.1488 - acc: 0.8511
Epoch 4/30

 10/470 [..............................] - ETA: 0s - loss: 0.3980 - acc: 0.6000
470/470 [==============================] - 0s 66us/step - loss: 0.1488 - acc: 0.8511
Epoch 5/30

 10/470 [..............................] - ETA: 0s - loss: 2.2996e-12 - acc: 1.0000
470/470 [==============================] - 0s 64us/step - loss: 0.1488 - acc: 0.8511
Epoch 6/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1487 - acc: 0.8511
Epoch 7/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 62us/step - loss: 0.1487 - acc: 0.8511
Epoch 8/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1487 - acc: 0.8511
Epoch 9/30

 10/470 [..............................] - ETA: 0s - loss: 5.3299e-07 - acc: 1.0000
470/470 [==============================] - 0s 64us/step - loss: 0.1487 - acc: 0.8511
Epoch 10/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 70us/step - loss: 0.1486 - acc: 0.8511
Epoch 11/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 76us/step - loss: 0.1498 - acc: 0.8447
Epoch 12/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 74us/step - loss: 0.1486 - acc: 0.8511
Epoch 13/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 68us/step - loss: 0.1485 - acc: 0.8511
Epoch 14/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 70us/step - loss: 0.1483 - acc: 0.8511
Epoch 15/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 59us/step - loss: 0.1485 - acc: 0.8511
Epoch 16/30

 10/470 [..............................] - ETA: 0s - loss: 0.1015 - acc: 0.9000
470/470 [==============================] - 0s 68us/step - loss: 0.1490 - acc: 0.8447
Epoch 17/30

 10/470 [..............................] - ETA: 0s - loss: 2.0702e-15 - acc: 1.0000
470/470 [==============================] - 0s 66us/step - loss: 0.1479 - acc: 0.8489
Epoch 18/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 74us/step - loss: 0.1482 - acc: 0.8468
Epoch 19/30

 10/470 [..............................] - ETA: 0s - loss: 0.3000 - acc: 0.7000
470/470 [==============================] - 0s 66us/step - loss: 0.1476 - acc: 0.8511
Epoch 20/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 62us/step - loss: 0.1480 - acc: 0.8511
Epoch 21/30

 10/470 [..............................] - ETA: 0s - loss: 0.2997 - acc: 0.7000
470/470 [==============================] - 0s 68us/step - loss: 0.1475 - acc: 0.8511
Epoch 22/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1469 - acc: 0.8511
Epoch 23/30

 10/470 [..............................] - ETA: 0s - loss: 0.1000 - acc: 0.9000
470/470 [==============================] - 0s 64us/step - loss: 0.1466 - acc: 0.8511
Epoch 24/30

 10/470 [..............................] - ETA: 0s - loss: 0.2083 - acc: 0.8000
470/470 [==============================] - 0s 70us/step - loss: 0.1475 - acc: 0.8489
Epoch 25/30

 10/470 [..............................] - ETA: 0s - loss: 0.2996 - acc: 0.7000
470/470 [==============================] - 0s 57us/step - loss: 0.1470 - acc: 0.8511
Epoch 26/30

 10/470 [..............................] - ETA: 0s - loss: 2.6178e-05 - acc: 1.0000
470/470 [==============================] - 0s 57us/step - loss: 0.1466 - acc: 0.8511
Epoch 27/30

 10/470 [..............................] - ETA: 0s - loss: 0.3000 - acc: 0.7000
470/470 [==============================] - 0s 57us/step - loss: 0.1472 - acc: 0.8511
Epoch 28/30

 10/470 [..............................] - ETA: 0s - loss: 0.2000 - acc: 0.8000
470/470 [==============================] - 0s 59us/step - loss: 0.1471 - acc: 0.8511
Epoch 29/30

 10/470 [..............................] - ETA: 0s - loss: 0.1991 - acc: 0.8000
470/470 [==============================] - 0s 57us/step - loss: 0.1470 - acc: 0.8489
Epoch 30/30

 10/470 [..............................] - ETA: 0s - loss: 8.9039e-07 - acc: 1.0000
470/470 [==============================] - 0s 55us/step - loss: 0.1461 - acc: 0.8532

 32/470 [=>............................] - ETA: 0s
470/470 [==============================] - 0s 68us/step

 Accuracy: 0.8511

Process finished with exit code 0
```

눈여겨 볼 부분은 **정확도(Accuracy)**

`acc: 0.8532`는 정확도가 85.32%라는 것

### 02-3 딥러닝 코드 분석

위 코드의 단계 세 단계로 구성되어 있음  

#### 데이터 분석과 입력 --> 딥러닝 실행 --> 결과 출력

#### 첫 번째 부분: 데이터 분석과 입력

```python
# 필요한 라이브러리를 불러옵니다.
import numpy

(중략)

# 준비된 수술 환자 데이터를 불러들입니다.
Data_set = numpy.loadtxt("../dataset/ThoraricSurgery.csv", delimiter=",")

# 환자의 기록과 수술 결과를 X와 Y로 구분하여 저장합니다.
X = Data_set[:,0:17]
Y = Data_set[:,17]
```

`import numpy`

넘파이(numpy)는 수치 계산을 위해 만들어진 라이브러리  
데이터 분석에 많이 사용

`Data_set = numpy.loadtxt("../dataset/ThoraricSurgery.csv", delimiter=",")`

`Data_set`에 `ThoraricSurgery.csv` 외부 데이터셋을 `loadtxt()`로 불러오기

#### ThoraricSurgery.csv

```bash
293,1,3.8,2.8,0,0,0,0,0,0,12,0,0,0,1,0,62,0
1,2,2.88,2.16,1,0,0,0,1,1,14,0,0,0,1,0,60,0
8,2,3.19,2.5,1,0,0,0,1,0,11,0,0,1,1,0,66,1
14,2,3.98,3.06,2,0,0,0,1,1,14,0,0,0,1,0,80,1
17,2,2.21,1.88,0,0,1,0,0,0,12,0,0,0,1,0,56,0
18,2,2.96,1.67,0,0,0,0,0,0,12,0,0,0,1,0,61,0
35,2,2.76,2.2,1,0,0,0,1,0,11,0,0,0,0,0,76,0
42,2,3.24,2.52,1,0,0,0,1,0,12,0,0,0,1,0,63,1
65,2,3.15,2.76,1,0,1,0,1,0,12,0,0,0,1,0,59,0
111,2,4.48,4.2,0,0,0,0,0,0,12,0,0,0,1,0,55,0
121,2,3.84,2.56,1,0,0,0,1,0,11,0,0,0,0,0,59,0
123,2,2.8,2.12,1,0,0,1,1,0,13,0,0,0,1,0,80,0
130,2,5.6,4.64,1,0,0,0,1,0,11,0,0,0,1,0,45,0
132,2,2.12,1.72,1,0,0,0,0,0,12,0,0,0,1,0,74,0
133,2,2.5,71.1,0,0,0,1,0,0,13,0,0,0,1,0,64,1
137,2,3.76,3.08,1,0,0,0,1,0,13,0,0,0,1,0,54,0
141,2,2.16,1.56,1,0,0,0,1,0,11,0,0,0,1,0,63,0
145,2,3.64,2.48,2,0,0,0,1,1,11,0,0,0,1,0,70,0
164,2,2.4,1.96,1,0,0,0,1,0,12,0,0,0,0,0,73,0
165,2,3,2.4,1,0,0,0,1,0,14,0,0,0,1,0,58,0
167,2,3.4,2.12,1,0,0,0,1,1,11,0,0,0,1,0,62,0
172,2,2.88,2.2,0,0,0,0,0,0,12,1,0,0,1,0,62,0
173,2,3.16,2.56,1,0,1,1,1,0,12,0,0,1,1,0,62,0
193,2,3.08,2.48,1,0,0,0,1,0,11,0,0,0,0,0,49,0
203,2,4.08,2.56,1,1,1,0,0,0,13,0,0,0,1,0,54,0
204,2,3.6,3.92,0,0,0,0,0,0,12,0,0,0,1,0,56,0
210,2,2.8,1.6,1,0,1,0,1,1,12,0,0,0,1,0,53,1
216,2,2.66,8.56,1,0,1,0,1,0,12,0,0,0,1,0,61,0
217,2,3.24,1.88,1,0,0,0,1,0,12,0,0,0,1,0,61,0
243,2,4.88,3.44,0,0,1,0,1,0,14,0,0,0,1,0,75,1
275,2,4.04,2.76,1,0,0,0,1,0,12,0,0,0,1,0,55,1
284,2,2.32,1.68,1,0,1,0,1,0,12,0,0,0,1,0,64,0
295,2,2.64,1.92,1,0,0,0,1,0,11,1,0,0,1,0,63,0
316,2,3.4,2.76,1,0,1,0,1,0,12,0,0,0,1,0,56,0
324,2,2.58,1.64,2,0,1,0,1,1,12,0,0,0,1,0,63,0
331,2,2.94,76,1,0,1,1,1,0,12,0,0,0,0,0,61,0
335,2,4,3.12,1,0,0,0,1,0,12,0,0,0,1,0,67,1
346,2,3.12,2.72,2,0,0,0,1,1,14,0,0,0,1,0,70,0
347,2,3.48,2.84,1,0,0,0,0,1,11,0,0,0,1,0,58,0
349,2,4.2,3.6,1,0,0,0,0,1,11,0,0,0,1,0,39,1
390,2,3.8,2.67,1,0,0,0,1,0,14,0,0,0,1,0,48,0
392,2,1.84,1.36,1,0,1,0,1,0,12,0,0,0,1,0,57,0
399,2,2.96,2.33,1,0,0,0,1,0,11,0,0,0,1,0,72,0
405,2,2.96,2.24,0,0,0,0,1,0,12,0,0,0,1,0,57,1
408,2,2.72,2.08,0,0,0,0,0,0,12,0,0,0,1,0,67,0
411,2,2.48,2,1,0,0,0,1,0,12,0,0,0,1,0,60,1
414,2,2.48,2.08,1,0,1,0,0,0,12,0,0,0,1,0,60,0
419,2,2.6,2.04,0,1,1,0,0,0,12,0,0,0,0,0,70,0
422,2,3.76,2.96,1,0,0,0,1,0,14,1,0,0,0,0,64,1
442,2,4.44,3.64,0,0,0,0,0,0,12,0,0,0,0,0,62,0
443,2,4.08,2.24,1,0,0,1,1,0,12,0,0,0,0,0,61,0
448,2,4.4,3.72,1,0,0,0,1,1,12,0,0,0,1,0,52,0
466,2,3.88,2.12,1,0,0,0,1,0,13,0,0,0,1,0,63,0
2,3,3.4,1.88,0,0,0,0,0,0,12,0,0,0,1,0,51,0
3,3,2.76,2.08,1,0,0,0,1,0,11,0,0,0,1,0,59,0
4,3,3.68,3.04,0,0,0,0,0,0,11,0,0,0,0,0,54,0
5,3,2.44,0.96,2,0,1,0,1,1,11,0,0,0,1,0,73,1
6,3,2.48,1.88,1,0,0,0,1,0,11,0,0,0,0,0,51,0
7,3,4.36,3.28,1,0,0,0,1,0,12,1,0,0,1,0,59,1
9,3,3.16,2.64,2,0,0,0,1,1,11,0,0,0,1,0,68,0
10,3,2.32,2.16,1,0,0,0,1,0,11,0,0,0,1,0,54,0
11,3,2.56,2.32,0,0,1,0,1,0,12,0,0,0,0,0,60,0
12,3,4.28,4.44,1,0,0,0,0,0,12,0,0,0,1,0,58,0
13,3,3,2.36,1,0,0,0,1,1,11,0,0,0,1,0,68,0
15,3,1.96,1.4,1,0,0,0,1,0,11,0,0,0,1,0,77,0
16,3,4.68,4.16,1,0,0,0,1,0,12,0,0,0,1,0,62,0
19,3,2.6,1.68,1,0,0,0,1,0,12,0,0,0,1,0,70,0
20,3,2.88,2.48,0,0,0,0,0,0,11,0,0,0,1,0,71,0
21,3,4.48,3.48,0,0,0,0,0,0,12,0,0,0,1,0,51,0
23,3,2.36,1.68,0,0,0,0,0,0,12,0,0,0,1,0,62,0
24,3,3.68,2.32,0,0,0,0,0,0,11,0,0,0,1,0,62,0
27,3,3.24,3.08,1,0,0,0,1,0,11,0,0,0,1,0,60,0
28,3,3.4,3.06,1,0,0,0,1,1,11,0,0,0,1,0,68,1
29,3,3.16,2.69,1,0,0,0,1,1,11,0,0,0,1,0,56,0
31,3,3.24,2.4,1,1,1,0,0,0,14,0,0,0,1,0,55,1
32,3,4.44,3.48,1,0,0,0,1,0,12,0,0,0,0,0,52,0
34,3,1.81,1.4,1,0,0,0,1,0,12,1,0,0,0,0,68,0
36,3,2.36,1.6,0,0,0,0,0,0,11,0,0,0,1,0,58,0
37,3,2.2,1.96,1,0,0,0,1,0,12,0,0,0,1,0,71,0
38,3,3.68,2.44,1,0,1,1,0,0,12,1,0,0,0,0,61,0
39,3,4.2,3.08,0,0,0,0,0,0,11,0,0,0,1,0,56,0
40,3,4.6,3.52,1,0,0,0,1,0,11,0,0,0,1,0,52,0
43,3,3.2,2.82,1,0,0,0,1,0,12,0,0,0,1,0,68,0
45,3,3.56,2.68,1,1,0,0,1,0,12,0,0,0,1,0,60,0
46,3,2.48,2.08,0,0,0,0,0,0,11,0,0,0,1,0,60,0
47,3,4.16,3.28,1,0,0,0,1,0,12,0,0,0,1,0,67,0
48,3,2.64,2.12,1,0,0,0,1,0,12,0,0,0,1,0,72,1
49,3,4.44,3.12,2,0,0,0,1,1,12,0,0,0,1,0,59,0
50,3,4.56,3.92,0,0,0,0,0,0,12,0,0,0,0,0,55,0
51,3,2.52,1.96,1,0,0,0,1,0,12,0,0,0,0,0,79,0
52,3,4,2.88,1,0,0,0,1,0,11,0,0,0,1,0,69,0
53,3,3.2,2.52,2,1,1,1,1,0,12,0,0,0,1,0,68,0
55,3,3.68,3.08,1,0,0,0,1,0,12,0,0,0,1,0,63,0
57,3,3.72,2.88,1,0,0,1,1,0,11,0,0,0,0,0,37,0
58,3,3.4,2.8,1,1,0,0,1,1,11,1,0,0,1,0,64,1
60,3,3.84,3.72,0,0,0,0,0,0,12,0,0,0,1,0,58,0
61,3,3.52,2.28,0,0,0,0,0,0,13,0,0,0,1,0,51,1
62,3,3.04,2.04,2,0,0,0,1,1,12,0,0,0,1,0,77,0
63,3,4.96,3.6,0,0,0,0,0,0,11,0,0,0,1,0,56,0
64,3,3.72,2.84,0,0,0,0,0,0,11,1,0,0,0,0,55,0
66,3,2.88,2.6,1,0,0,0,1,0,12,0,0,0,0,0,54,0
67,3,2.36,2,0,0,0,0,0,0,11,0,0,0,0,0,39,0
69,3,2.72,2.2,1,0,0,0,1,0,12,0,0,0,1,0,61,0
70,3,3.08,1.8,1,0,1,0,1,0,12,0,0,0,1,0,70,0
71,3,3.48,2.72,1,0,1,0,0,0,11,0,0,0,0,0,53,0
72,3,3.6,2.6,1,0,0,0,1,0,12,1,0,0,1,0,71,0
73,3,3.52,2.92,0,0,0,0,0,0,11,0,0,0,1,0,63,0
75,3,4.6,3.28,1,0,0,0,1,0,11,0,0,0,1,0,55,0
76,3,3.4,2.8,1,0,0,0,1,0,14,0,0,0,1,0,41,1
77,3,1.84,1.28,1,0,0,0,1,1,11,0,0,0,1,0,66,0
78,3,3.04,3.6,1,0,0,0,1,0,12,0,0,0,1,0,62,1
79,3,2.2,1.44,1,0,0,0,1,0,12,0,0,0,1,0,54,0
80,3,3.04,2.16,1,0,0,0,1,0,12,0,0,0,0,0,78,0
81,3,3.68,2.88,1,0,0,0,1,0,12,0,0,0,1,0,58,0
82,3,1.96,1.68,1,0,0,0,1,0,14,0,0,0,1,0,59,0
83,3,3.24,1.64,1,0,0,0,1,0,12,0,0,0,1,0,63,0
84,3,2.84,2.36,1,0,0,0,1,0,11,1,0,0,0,0,62,0
85,3,4.28,3.28,0,0,0,0,0,0,12,0,0,0,1,0,51,0
86,3,3.76,2.72,1,0,0,0,1,0,12,0,0,0,1,0,58,0
87,3,4.9,4.19,0,0,0,1,1,0,12,0,0,0,0,0,52,0
88,3,2.36,2,1,0,0,1,0,0,12,0,0,1,1,0,67,0
90,3,2.83,66.4,1,1,1,1,1,0,12,0,0,0,1,0,75,0
92,3,2.6,2,1,0,0,0,1,0,11,0,0,0,1,0,73,0
93,3,3.6,2.48,1,0,0,0,1,0,12,0,0,0,1,0,60,1
94,3,6.08,4.92,0,0,0,0,0,0,11,0,0,0,1,0,50,0
95,3,1.88,1.44,2,0,0,0,1,1,12,0,0,0,1,0,87,0
96,3,4.56,3.6,1,0,0,0,1,0,11,0,0,0,1,0,54,0
99,3,2.63,67.3,1,0,0,1,1,0,11,0,0,0,1,0,54,0
100,3,4.6,2.92,1,0,1,1,1,0,12,0,0,0,1,0,57,1
101,3,3.36,2.67,1,0,0,0,1,0,11,0,0,0,1,0,72,0
102,3,1.84,1.64,1,0,0,0,1,1,12,1,0,0,1,0,72,0
104,3,2.35,1.64,1,0,0,0,1,0,11,0,0,0,0,1,59,0
105,3,2.84,1.88,1,0,0,0,1,0,11,0,0,0,0,0,53,0
107,3,2.48,2.08,1,0,0,0,1,0,12,0,0,0,1,0,55,0
108,3,3.6,2.6,1,0,0,0,1,0,12,0,0,0,1,0,54,0
109,3,3.16,2.96,0,0,0,0,0,0,11,0,0,0,0,0,63,0
110,3,3.24,2.36,1,0,0,1,1,0,12,0,0,0,1,0,74,0
112,3,4,2.6,1,0,0,0,1,0,12,1,0,0,1,0,58,0
113,3,3.68,64.1,0,0,0,0,0,0,12,0,0,0,1,0,60,0
114,3,4.68,3.48,0,0,0,0,0,0,11,0,0,0,1,0,52,0
115,3,4.52,3.32,0,0,0,0,1,0,12,0,0,0,1,0,58,0
118,3,2.84,2.16,1,0,0,0,1,0,12,1,0,0,1,0,53,0
120,3,2.56,1.6,1,0,0,0,1,1,12,0,0,0,1,0,75,0
122,3,3.56,2.76,1,0,0,0,1,0,12,0,0,0,1,0,74,0
125,3,3.36,2.8,1,0,0,0,1,1,12,0,0,0,1,0,76,0
126,3,2.83,1.96,1,0,0,0,1,0,12,0,0,0,1,0,71,0
127,3,4.56,2.68,1,0,0,0,1,0,11,0,0,0,1,0,62,0
128,3,2,1,1,0,1,0,1,1,11,1,0,0,1,0,73,1
131,3,3.32,2.87,1,0,0,0,1,0,11,0,0,0,1,0,63,0
134,3,2,1.44,0,0,0,0,0,0,11,0,0,0,1,0,63,0
135,3,4.84,3.48,1,0,0,0,1,0,12,0,0,0,1,0,56,0
136,3,2.92,2.28,1,0,0,0,1,0,11,0,0,0,1,0,63,0
138,3,2.08,1.52,1,0,0,0,1,0,14,0,0,0,1,0,49,1
139,3,2.44,2.08,1,0,0,0,1,0,12,0,0,0,1,0,57,0
140,3,3.72,3.12,1,0,1,0,0,0,12,0,0,0,0,0,52,0
142,3,4.2,3.24,1,0,1,0,1,0,12,0,0,0,1,0,73,0
143,3,5.17,4.3,1,0,0,0,0,0,11,0,0,0,0,0,47,0
146,3,3.96,2.96,1,0,0,0,1,0,12,0,0,0,1,0,60,0
147,3,3.92,3.08,1,0,0,0,1,0,11,0,0,0,0,0,70,0
148,3,2.92,2.2,1,0,0,0,1,0,12,0,0,0,1,0,68,0
149,3,3.64,2.76,1,0,0,0,1,0,12,0,0,0,1,0,74,0
150,3,2.72,2.36,0,0,0,0,0,0,11,0,0,0,1,0,71,0
151,3,2.6,2.24,0,0,0,0,0,0,12,0,0,0,0,0,56,0
152,3,3.88,2.84,1,0,1,0,1,0,11,0,0,0,1,0,66,1
153,3,2.72,2.04,1,1,0,0,0,0,12,0,0,0,0,0,76,1
154,3,3.44,3.13,1,0,0,0,1,1,12,0,0,0,1,0,78,0
155,3,3.12,3.24,1,0,0,0,1,0,12,0,0,0,1,0,68,0
156,3,2.6,2.32,1,0,0,0,0,1,12,1,0,0,0,0,66,0
157,3,3.28,2.32,1,0,0,1,1,0,13,0,0,0,1,0,67,0
158,3,2.76,1.6,1,0,0,0,1,1,12,0,1,0,1,0,60,0
159,3,3.08,2.32,1,0,1,0,1,1,12,0,0,1,1,0,61,0
160,3,2.2,1.7,1,0,0,0,1,0,11,0,0,0,1,0,58,0
161,3,2.92,1.88,0,0,0,0,0,0,12,0,0,0,0,0,76,0
162,3,2.88,2.36,0,0,0,0,0,0,11,0,0,0,1,0,56,0
163,3,3.2,2.28,1,1,1,0,1,0,12,0,0,0,1,0,67,0
166,3,3.2,2.21,1,0,1,1,1,0,12,0,0,0,1,0,54,0
168,3,2.57,1.72,1,0,0,0,1,1,11,0,0,0,1,0,81,0
169,3,2.28,2.08,0,0,0,0,0,0,11,1,0,0,1,0,56,0
170,3,2.44,1.96,1,0,1,1,1,0,13,0,0,0,0,0,60,1
171,3,4.04,1.88,1,0,0,0,1,0,12,0,0,0,1,0,66,0
174,3,2.6,2.36,1,0,0,0,1,0,11,0,0,0,1,0,55,1
175,3,1.44,1.04,1,0,0,0,1,1,11,0,0,0,1,0,62,0
176,3,3.68,2.36,0,0,0,1,1,0,12,0,0,0,1,0,71,1
177,3,3.2,2.72,2,0,0,0,1,0,14,0,0,0,1,0,52,0
178,3,3.04,2.32,1,0,0,0,1,0,12,0,0,0,1,0,59,0
179,3,4.32,4.32,1,0,1,0,1,1,12,0,0,0,1,0,48,0
180,3,3,2.36,2,0,0,0,1,1,12,0,0,0,1,0,60,0
181,3,3.64,2.88,1,0,0,0,1,1,12,0,0,0,1,0,61,0
182,3,5.08,4.08,1,0,0,0,1,0,12,0,0,0,1,0,59,0
183,3,3.16,2.36,1,0,0,0,1,0,11,0,0,0,1,0,64,0
184,3,2.8,3.36,1,0,0,0,1,0,12,0,0,0,1,0,56,0
185,3,2.52,2.08,0,0,0,0,0,0,11,0,0,0,0,0,58,0
187,3,3.32,2.15,1,0,0,0,1,0,11,0,0,0,1,0,64,0
189,3,2.28,1.24,1,0,0,0,1,0,11,0,0,0,1,0,72,0
191,3,2.6,1.56,0,0,0,0,0,0,12,0,0,0,1,1,61,0
192,3,2.68,2.4,0,0,0,0,0,0,11,0,0,0,1,0,60,1
194,3,3.84,3.36,0,0,0,0,0,0,12,0,0,0,1,0,53,0
195,3,3.52,2.8,0,0,0,0,0,0,11,0,0,0,1,0,58,0
196,3,2.73,2.11,1,0,1,0,1,0,12,0,0,0,1,0,61,1
197,3,2.84,2.24,1,1,1,0,0,0,12,0,0,0,1,0,68,1
198,3,2.98,2.64,1,0,0,0,1,0,12,0,0,0,0,0,60,0
199,3,3.52,2.72,1,0,0,0,0,0,11,0,0,0,1,0,72,0
201,3,2.36,2.08,1,0,0,0,1,0,12,0,0,0,1,0,57,0
202,3,2.76,2.28,0,0,0,0,0,0,11,0,0,0,1,0,51,0
205,3,3.12,2.9,0,0,0,0,0,0,12,0,0,0,0,0,77,0
206,3,2.24,1.76,0,0,0,0,0,0,12,0,0,0,1,0,64,0
207,3,3.96,2.88,0,0,0,0,0,0,11,0,0,0,1,0,57,0
208,3,2.6,1.92,1,0,0,0,1,0,11,0,0,0,1,0,66,0
209,3,4.2,3.24,0,0,0,0,0,0,12,0,0,0,1,0,70,0
211,3,4.72,4.56,0,0,0,0,0,0,11,0,0,0,1,0,51,0
212,3,3.58,2.64,1,0,0,0,1,0,12,0,0,0,1,0,58,1
213,3,2.44,2.12,1,1,1,1,0,0,11,0,0,0,1,0,58,0
214,3,2.22,1.36,0,0,0,0,0,0,12,1,0,0,1,0,63,1
215,3,2.96,2.32,0,0,0,0,0,0,11,0,0,0,1,0,51,0
218,3,4.52,3.6,1,0,0,0,1,0,12,0,0,0,1,0,76,0
219,3,4,3.08,1,0,0,0,1,0,11,0,0,0,1,0,71,0
220,3,2.84,2.12,0,0,0,0,0,0,11,0,0,0,1,0,69,0
223,3,4.8,3.41,1,0,0,1,1,0,12,0,0,0,1,0,54,0
224,3,3.72,3.04,0,0,0,0,0,0,11,0,0,1,1,0,63,0
225,3,4.96,3.48,1,0,0,0,1,0,12,0,0,0,1,0,47,0
227,3,2.96,2.44,1,0,0,0,1,1,12,0,0,0,1,0,65,0
228,3,2.64,2.44,1,0,0,0,1,0,12,0,0,0,1,0,63,1
229,3,2.4,1.64,0,0,0,0,0,0,11,0,0,0,0,0,64,0
230,3,2.64,2.08,1,0,0,0,1,0,12,1,0,0,1,0,65,1
231,3,4.76,3.31,1,0,0,1,1,0,11,0,0,0,1,0,51,0
233,3,2.32,1.76,1,0,0,0,1,0,11,0,0,0,1,0,70,0
234,3,2.6,2,1,0,0,0,1,0,12,0,0,0,1,0,58,0
235,3,2.46,1.76,1,0,0,0,1,1,11,0,0,0,1,0,67,0
236,3,4.16,3.64,1,0,0,0,1,0,12,0,0,0,1,0,62,0
237,3,3.2,1.8,1,0,0,0,1,1,12,0,0,0,1,0,74,0
238,3,3.24,2.64,0,0,0,0,1,0,11,0,0,0,1,0,69,0
240,3,3.52,2.52,1,0,0,0,1,0,12,0,0,0,1,0,60,1
241,3,4.36,3.76,0,0,0,0,0,0,11,0,0,0,1,0,72,0
242,3,5.52,3.56,1,0,0,0,1,0,12,0,0,0,1,0,64,0
244,3,4.36,3.92,1,0,0,0,0,0,11,0,0,0,1,0,47,0
245,3,3.56,2.64,1,0,0,0,1,0,11,0,1,0,1,0,57,0
246,3,5.49,2.97,1,0,0,0,1,0,12,0,0,0,1,0,56,0
248,3,4.08,3.2,0,0,0,0,1,0,12,0,0,0,1,0,55,0
250,3,2.56,1.8,1,0,0,0,1,0,12,0,0,0,1,0,73,0
251,3,3.8,2.82,1,0,0,0,1,0,12,0,0,0,1,0,68,0
252,3,3.04,2.24,2,0,0,0,1,1,11,0,0,0,1,0,75,1
253,3,3.81,2.94,1,0,0,0,1,0,12,0,0,0,1,0,63,0
254,3,3.92,2.36,1,0,0,0,1,0,12,0,0,0,1,0,61,0
255,3,3.44,3.52,1,1,0,0,0,0,11,0,0,0,1,0,62,0
256,3,3.72,78.3,0,1,0,0,1,0,12,0,0,0,1,0,44,0
257,3,2.8,1.88,1,0,0,0,1,0,11,0,0,0,1,0,56,0
258,3,2.92,2.32,0,0,0,0,0,0,11,0,0,0,1,0,54,0
259,3,3.72,2.48,1,0,1,0,1,0,11,0,0,0,1,0,57,0
260,3,3.64,2.52,0,0,0,0,0,0,12,0,0,0,1,0,56,0
261,3,2.72,2.09,0,0,0,0,0,0,14,0,0,0,0,0,69,1
262,3,1.84,1.12,1,0,0,0,1,0,12,0,0,0,1,0,72,0
263,3,2.96,1.72,0,0,1,0,1,0,11,0,0,0,1,0,59,0
265,3,2.6,1.92,1,0,0,0,1,0,11,0,0,0,1,0,64,0
266,3,2.92,2.52,0,0,0,0,0,0,12,0,0,0,1,0,61,0
267,3,3.8,2.84,1,0,0,0,1,0,12,0,0,0,1,0,72,0
268,3,3.32,2.92,2,0,0,0,1,1,13,0,0,0,1,0,63,0
269,3,2.52,1.72,2,0,0,1,1,1,12,0,0,0,1,0,74,1
270,3,4.28,3.28,1,1,0,0,1,0,11,0,0,0,1,0,71,0
271,3,2.52,1.72,1,0,0,0,1,1,12,0,0,0,1,0,71,1
273,3,2.07,1.6,0,0,1,0,0,0,12,0,0,0,0,0,77,0
276,3,1.7,1.36,1,0,0,0,0,1,12,0,0,0,1,0,65,0
277,3,3.04,2.04,1,0,0,0,1,0,12,0,0,0,1,0,67,0
278,3,3.36,2.64,1,0,0,0,1,0,12,1,0,0,1,0,69,0
279,3,4.57,4.57,1,0,0,0,1,0,11,0,0,0,0,0,55,0
280,3,4.12,2.32,1,0,0,0,1,0,11,0,0,0,1,0,51,0
281,3,2,1.36,1,0,0,0,1,0,11,0,0,0,1,0,64,0
282,3,3.8,3.68,0,0,0,0,0,0,12,0,0,0,0,0,63,0
283,3,3.16,2.6,1,1,0,0,1,0,12,0,0,0,0,0,69,0
285,3,2.32,1.92,0,0,0,0,0,0,11,0,0,0,1,0,59,0
286,3,2.48,1.4,1,0,0,0,1,0,11,0,0,0,1,0,73,0
288,3,2.96,2.2,1,0,0,0,1,0,12,0,0,0,1,0,63,0
289,3,2.96,1.88,1,0,0,0,1,1,14,0,0,0,1,0,60,0
290,3,3.52,2.36,1,0,0,0,1,0,12,0,0,0,1,0,74,0
291,3,4.12,3.16,1,0,0,0,1,1,12,0,0,0,1,0,65,0
292,3,2.68,2.32,1,0,0,0,1,1,11,1,0,0,1,0,79,0
294,3,4.12,2.88,1,0,0,0,1,0,12,0,0,1,1,0,71,0
296,3,3.68,2.96,1,0,1,0,1,0,12,0,0,0,1,0,67,0
297,3,2.48,1.84,1,0,0,0,1,0,12,0,0,0,1,0,55,1
298,3,4.36,3.24,1,1,0,1,1,0,12,0,0,0,1,0,54,1
299,3,4.32,2.72,2,0,1,0,1,1,11,0,0,0,1,0,77,0
300,3,3.4,1.92,0,0,0,0,0,0,12,0,0,0,1,0,58,0
301,3,4.24,3.04,1,0,1,0,1,1,12,0,0,0,1,0,64,0
302,3,3.28,1.96,0,0,0,0,0,0,12,0,0,0,0,0,61,0
303,3,4.59,3.02,2,1,0,0,1,1,13,0,0,0,0,0,62,1
304,3,4.16,3.44,1,0,1,0,1,1,12,0,0,0,1,0,67,0
305,3,5.16,4.28,0,0,0,0,0,0,12,0,0,0,1,0,56,0
306,3,2.76,1.8,1,0,0,0,1,0,12,0,0,0,1,0,70,1
308,3,2.8,2.32,1,0,0,0,1,0,12,0,0,0,1,0,57,0
309,3,2.32,1.96,1,0,0,0,1,0,11,0,0,0,1,0,61,0
310,3,1.98,1.57,1,0,0,0,0,1,11,0,0,0,1,0,77,0
312,3,2.4,1.64,1,0,1,0,1,1,12,0,0,0,0,0,62,0
313,3,3.12,2.52,1,1,0,0,1,0,12,0,0,0,1,0,59,1
314,3,2.6,1.84,1,0,0,0,1,0,12,0,0,0,1,0,70,0
317,3,3.6,2.64,1,0,0,0,1,0,12,0,0,0,0,0,57,0
318,3,2.48,2.12,1,0,0,1,1,0,12,0,0,0,1,0,78,0
319,3,2.4,1.96,1,0,0,0,1,0,11,0,0,0,1,0,64,0
320,3,2.1,69.1,0,0,0,0,0,0,11,0,0,0,1,0,62,0
321,3,5.12,4,1,0,0,0,1,0,14,0,0,0,1,0,49,0
322,3,4.65,3.78,1,0,0,0,1,0,12,0,0,0,1,0,77,1
323,3,2.72,2.36,1,0,0,0,1,0,11,0,0,0,1,0,64,0
327,3,3.2,2.52,1,0,0,0,1,1,12,0,0,0,1,0,75,0
328,3,2.52,1.92,2,0,1,0,1,1,11,0,0,0,1,0,70,0
329,3,1.96,1.48,1,0,0,0,1,0,12,0,0,0,1,0,59,0
332,3,3.52,3.12,0,0,0,0,0,0,11,0,0,0,1,0,64,0
333,3,2.6,1.92,0,0,0,0,0,0,11,0,0,0,1,0,59,0
336,3,2.4,1.8,1,0,0,0,1,0,11,0,0,0,1,0,64,0
337,3,2.32,1.32,1,0,1,0,1,1,11,0,0,0,1,0,68,0
339,3,4,3.08,0,0,0,0,0,0,11,0,0,0,1,0,64,0
340,3,2.96,2,1,0,0,0,1,0,12,0,0,0,1,0,59,0
341,3,3.88,2.92,0,0,0,0,0,0,11,0,0,0,1,0,67,1
342,3,2.36,1.76,1,0,1,0,0,0,12,0,0,0,1,0,74,0
344,3,2.96,2.44,1,0,0,0,1,1,11,0,0,0,1,0,60,0
345,3,3.64,3.12,1,0,0,0,1,0,12,0,0,0,1,0,64,0
348,3,4.16,3.44,1,1,0,0,1,0,13,0,0,0,1,0,59,0
351,3,2.64,2.16,1,0,1,0,1,0,12,0,0,0,1,0,71,1
352,3,3.05,1.3,1,0,0,0,1,0,11,0,0,0,1,0,70,0
353,3,2.94,73.3,1,0,1,1,0,0,12,0,0,0,0,0,60,0
354,3,3.24,52.3,0,0,0,0,0,0,12,1,0,0,1,0,55,0
355,3,4.28,3.52,1,0,0,0,1,0,11,0,0,0,1,0,60,0
356,3,3.68,3.2,1,0,0,0,1,0,12,0,0,0,1,0,55,0
357,3,2.8,2.44,1,0,0,1,1,0,12,0,0,0,1,0,55,0
358,3,2,1.36,0,0,0,0,0,0,12,0,0,0,1,0,70,1
359,3,2.4,2.04,1,0,0,0,1,0,12,0,0,0,1,0,63,0
361,3,2.6,2.12,1,0,0,0,1,0,12,0,0,0,1,0,55,0
362,3,2.84,2.4,1,0,0,0,1,0,11,0,0,0,1,0,49,0
363,3,3.08,1.72,1,0,0,0,1,1,12,1,0,0,1,0,58,1
364,3,2.2,1.6,1,0,1,0,1,0,12,0,0,0,1,0,59,0
365,3,2.32,1.72,2,0,0,0,1,1,11,0,0,0,1,0,56,0
366,3,2.04,1.8,0,0,0,0,0,0,12,0,0,0,1,0,64,0
367,3,2.56,2.2,1,0,0,0,1,0,11,0,0,0,1,0,62,0
370,3,3.8,3.16,0,0,0,0,0,0,12,0,0,0,1,0,59,0
371,3,2.88,2.16,0,0,0,0,0,0,12,0,0,0,1,0,59,0
372,3,2.32,1.76,0,0,0,0,0,0,12,0,0,0,0,0,55,0
373,3,2.92,2.4,1,0,0,0,1,0,11,0,0,0,1,0,46,0
374,3,2,1.52,0,0,1,0,1,0,14,1,0,0,1,0,60,0
375,3,2.4,2.16,1,0,0,0,1,0,12,0,0,0,1,0,69,0
376,3,4.56,3.84,0,0,0,0,0,0,12,0,0,0,1,0,74,0
377,3,4.03,3.09,1,0,0,0,1,0,11,0,0,0,1,0,59,0
378,3,2.16,1.88,0,0,0,0,0,0,12,0,0,0,1,0,63,0
379,3,4.52,3.36,1,0,0,0,0,1,12,0,0,0,1,0,63,0
381,3,3.76,1,0,0,1,0,0,0,12,0,0,0,1,0,52,0
382,3,5,3.88,0,0,0,0,0,0,11,0,0,0,1,0,51,0
384,3,2.4,1.88,1,0,0,0,1,0,11,0,0,0,0,0,53,0
385,3,2,1.64,1,0,0,0,1,0,12,0,0,0,0,0,61,0
386,3,2.52,1.96,1,0,0,0,1,0,12,1,0,0,1,0,72,0
387,3,4.4,3.56,1,0,0,1,1,1,11,0,0,0,1,0,60,1
389,3,1.96,1.4,1,0,0,0,1,0,13,0,0,0,1,0,69,0
391,3,2.92,2.28,1,0,0,0,1,0,12,0,0,0,1,0,75,0
394,3,3.72,3,1,0,0,0,1,0,12,0,0,0,1,0,61,0
397,3,2.76,2.08,0,0,0,0,0,0,12,0,0,0,0,0,21,0
398,3,4.56,3.48,1,0,0,0,1,0,12,0,0,0,1,0,60,0
400,3,2.7,1.9,1,0,0,0,1,0,11,0,0,0,1,0,65,0
401,3,2.48,1.6,0,0,0,0,0,0,11,0,0,0,0,0,61,0
402,3,3.56,2.8,0,0,0,0,0,0,12,0,0,0,0,0,69,0
403,3,2.96,2.2,1,0,0,0,1,0,12,0,0,0,1,0,53,0
404,3,4.04,2.56,1,0,1,0,1,0,12,0,0,0,1,0,55,0
407,3,3.44,2.92,1,0,0,0,1,0,11,0,0,0,1,0,56,0
409,3,3.08,2.24,1,0,0,0,1,0,12,1,0,0,1,0,59,0
410,3,2.64,2.15,0,0,0,0,0,0,11,0,0,0,1,0,59,0
412,3,4.64,4.16,1,1,0,0,1,0,13,0,0,0,1,0,56,0
413,3,3.32,2.52,0,0,0,0,0,0,11,0,0,0,0,0,56,0
415,3,1.46,1,1,0,1,0,1,0,11,0,0,0,1,0,68,0
416,3,3.4,2.39,0,0,0,0,0,0,11,0,0,0,0,0,63,0
417,3,3.44,2.4,1,0,0,0,1,1,11,1,0,0,1,0,77,0
418,3,5.16,4.28,1,0,0,0,0,0,12,0,0,0,1,0,52,0
423,3,2.68,2.16,0,0,0,0,0,0,12,0,0,0,1,0,70,0
424,3,5,4.04,0,0,1,0,1,0,12,0,0,0,0,0,60,0
426,3,3.18,2.73,1,0,0,0,1,0,12,0,0,0,1,0,47,0
427,3,2.48,2.08,1,0,0,0,1,0,13,0,0,0,1,0,54,1
428,3,3.44,2.72,1,1,1,0,1,0,11,0,0,0,0,0,73,0
429,3,3.12,2.12,1,0,0,0,1,1,12,0,0,0,1,0,62,0
430,3,3.48,2.52,1,0,0,0,1,0,14,1,0,0,1,0,72,0
431,3,3.87,2.68,0,0,0,0,0,0,12,0,0,0,1,0,63,0
432,3,1.44,1.2,1,0,0,0,1,0,11,0,0,0,1,0,58,0
433,3,2.28,1.82,0,0,0,0,0,0,11,1,0,0,0,0,69,0
434,3,4.28,2.72,1,1,1,0,1,0,11,0,0,0,1,0,66,0
435,3,3.08,2.28,1,0,0,0,1,0,11,0,0,0,1,0,57,0
436,3,2.96,2.04,1,0,0,0,1,0,11,0,0,0,1,0,56,0
437,3,4.8,3.32,1,0,0,1,1,0,12,0,0,0,1,0,54,0
438,3,4.08,3.2,1,0,0,0,1,0,12,0,0,0,1,0,40,0
440,3,2.36,1.6,1,0,0,0,1,1,11,0,0,1,1,0,54,0
441,3,3,2.44,1,0,0,0,1,1,12,0,0,0,1,0,65,0
444,3,4.12,3.2,2,0,0,0,1,1,11,0,0,0,0,0,76,0
445,3,2.56,60.9,0,0,0,0,0,0,11,0,0,0,1,0,50,0
446,3,2.72,1.76,0,0,0,0,0,0,11,0,0,0,1,0,63,0
449,3,2.96,2.24,0,0,0,0,0,0,12,0,0,0,1,0,69,0
450,3,2.84,1.88,1,0,0,0,1,0,12,0,0,0,1,0,53,1
451,3,2.28,1.68,2,0,0,0,1,1,11,0,0,0,0,0,77,0
453,3,2.8,2.24,1,1,0,0,1,0,13,0,0,0,1,0,70,0
454,3,2.84,2.32,1,0,1,0,1,1,11,0,0,0,1,0,72,0
455,3,3.24,2.76,0,0,0,0,0,0,11,0,0,0,1,0,70,0
457,3,2.4,1.24,1,0,0,0,1,0,12,0,0,0,1,0,62,0
458,3,4.56,3.2,0,0,0,0,1,0,11,0,0,0,1,0,61,0
459,3,3.6,3,1,0,0,0,1,0,11,0,0,0,0,0,46,0
460,3,4.28,3.16,0,0,0,0,1,0,12,0,0,0,0,0,66,0
462,3,1.84,1.56,1,1,1,0,1,0,12,0,0,0,0,0,72,0
463,3,2.12,1.68,2,1,1,0,0,0,11,0,0,0,1,0,74,0
465,3,3.08,2.16,1,0,0,0,1,1,13,0,0,0,1,0,79,0
467,3,3.76,3.12,0,0,0,0,0,0,11,0,0,0,1,0,61,0
468,3,3.04,2.08,1,0,0,0,1,0,13,0,0,0,0,0,52,0
469,3,1.96,1.68,1,0,0,0,1,1,12,0,0,0,1,0,79,0
470,3,4.72,3.56,0,0,0,0,0,0,12,0,0,0,1,0,51,0
22,4,3.32,2.84,0,0,0,0,0,0,12,0,0,0,1,0,62,0
54,4,3.76,2.52,1,0,0,0,1,0,12,0,0,0,1,0,75,0
56,4,3.28,2.36,1,0,0,0,1,0,12,0,0,0,1,0,65,0
59,4,5.12,4.28,0,0,0,0,0,0,12,0,0,0,1,0,62,0
68,4,2.32,1.76,1,0,1,0,1,1,11,0,0,0,1,0,62,1
74,4,6.3,5.48,0,0,0,0,0,0,11,0,0,0,0,0,45,0
91,4,3.52,2.72,1,0,1,0,1,0,12,0,0,0,1,0,80,0
97,4,2.68,2,1,0,0,0,1,0,12,0,0,0,1,0,70,1
103,4,4.32,3.24,1,0,0,0,1,0,12,0,0,0,1,0,76,0
116,4,2.76,1.76,1,0,1,0,1,0,11,1,0,0,1,0,61,1
117,4,2.88,2.24,1,0,0,0,1,1,12,0,0,0,1,0,73,0
119,4,3.48,2.56,1,0,0,0,0,0,11,0,0,0,1,0,57,0
124,4,3.3,2.56,0,0,0,0,0,0,11,0,0,0,1,0,67,0
129,4,3.31,2,2,0,0,1,1,0,12,0,0,0,1,0,81,1
144,4,2.08,1.76,0,0,0,0,0,0,12,0,0,0,1,0,69,1
188,4,3.28,1.64,1,0,0,0,1,0,11,0,0,0,1,0,62,0
190,4,4.92,3.72,0,0,0,0,0,0,12,0,0,0,1,0,60,0
200,4,2.44,1.64,1,0,0,0,1,1,11,0,0,0,1,0,72,0
222,4,4.24,3.68,1,0,0,0,1,0,12,0,0,0,1,0,67,0
226,4,2.76,2.16,1,1,0,0,0,0,12,1,0,0,1,0,62,0
247,4,5.56,4.32,0,0,0,0,0,0,12,0,0,0,1,0,68,0
249,4,4.56,3.68,1,0,0,0,1,0,12,0,0,0,1,0,62,0
264,4,3.04,2.88,0,0,0,0,0,0,11,0,0,0,0,0,70,0
274,4,3.36,2.72,2,0,0,0,1,1,11,1,0,0,1,0,72,0
287,4,4.9,3.96,1,0,0,0,1,0,12,0,0,0,1,0,55,0
311,4,3.4,2.92,0,0,0,0,0,0,11,0,0,0,0,0,63,0
315,4,2.12,1.36,1,0,0,0,1,0,12,0,0,0,1,0,71,0
325,4,5.16,4.96,1,0,0,0,0,0,11,0,0,0,1,0,54,0
326,4,5.03,79.3,1,0,0,1,0,0,11,0,0,0,0,0,38,0
330,4,2.08,1.84,0,0,0,0,0,0,12,0,0,0,0,0,77,0
334,4,2.2,1.8,0,0,0,0,0,0,11,0,0,0,0,0,71,0
338,4,3.24,2.6,1,0,0,0,1,0,12,0,0,0,1,0,69,0
343,4,2.5,1.4,1,0,1,0,1,0,11,0,0,0,1,0,77,0
350,4,1.82,86.3,0,0,0,0,0,0,12,0,0,0,0,0,67,0
360,4,2.84,2.12,0,0,0,0,0,0,12,0,0,0,0,0,64,0
380,4,2.72,2.04,1,0,0,0,1,0,11,0,0,0,1,0,75,0
383,4,3.4,2.16,1,1,1,0,1,0,12,0,0,0,0,0,68,0
388,4,4.2,3.32,0,0,0,0,0,0,12,0,0,0,1,0,58,0
393,4,3.56,2.6,1,0,0,0,1,0,13,0,0,0,1,0,68,0
395,4,3.96,2.44,1,0,0,0,1,1,11,0,0,0,1,0,44,0
396,4,3.04,3.68,1,0,0,0,1,0,11,1,0,0,1,0,64,0
420,4,2.44,2.08,2,0,0,0,1,1,12,0,0,0,1,0,72,1
425,4,2.81,2.31,1,1,0,0,0,0,12,0,0,0,1,0,58,0
452,4,3.04,2.36,1,0,0,0,1,0,12,0,0,0,1,0,59,0
456,4,2.92,1.92,1,0,0,0,1,0,12,0,0,0,1,0,70,0
461,4,4.65,3.78,1,0,0,0,1,0,12,0,0,0,0,0,55,0
464,4,3.44,2.16,1,0,0,0,1,1,12,1,0,0,1,0,57,1
26,5,4.56,72.8,0,1,1,0,1,0,12,0,0,0,1,0,57,0
33,5,2.48,1.95,1,1,0,0,0,0,12,1,0,0,0,0,72,0
41,5,3.8,2.98,1,0,0,0,1,0,11,0,0,0,1,0,60,1
44,5,2.68,2.12,0,0,0,0,1,0,12,0,0,0,1,0,51,1
89,5,2.68,1.76,2,0,1,0,1,1,11,0,0,0,1,0,76,0
106,5,4.95,4.12,1,0,0,0,0,1,11,0,0,0,0,0,57,0
186,5,3.52,2.56,0,0,0,1,0,0,12,0,0,0,0,0,81,1
221,5,2.87,2.08,1,0,0,0,1,0,13,0,0,0,1,0,56,1
232,5,2.88,2.52,1,0,0,0,1,0,12,0,0,0,1,0,56,0
239,5,3.4,2.08,1,0,0,0,0,1,11,0,0,0,1,0,55,1
272,5,3,2.16,0,0,0,0,0,0,11,0,0,0,1,0,72,0
307,5,3.3,2.4,1,0,0,0,1,1,12,0,0,0,1,0,70,0
368,5,2.38,1.72,1,0,1,0,1,0,12,1,0,1,1,0,87,1
421,5,4.96,4.16,1,0,0,0,1,0,11,0,0,0,1,0,62,1
439,5,3.67,76.8,0,1,1,0,1,0,12,0,0,0,0,0,61,0
30,6,3.96,3.28,0,0,0,0,0,0,11,0,0,0,1,0,61,0
98,6,3.04,2.4,2,0,0,0,1,0,11,0,0,0,1,0,76,0
369,6,3.88,2.72,1,0,0,0,1,0,12,0,0,0,1,0,77,0
406,6,5.36,3.96,1,0,0,0,1,0,12,0,0,0,0,0,62,0
25,8,4.32,3.2,0,0,0,0,0,0,11,0,0,0,0,0,58,1
447,8,5.2,4.1,0,0,0,0,0,0,12,0,0,0,0,0,49,0
```

* 실제 폐암 수술 환자의 수술 전 진단 데이터와 수술 후 생존 결과 의료 기록 데이터
* 가로는 17개의 **속성(attribute)**과 1개의 **클래스(class)**
* 세로는 470개의 항목으로 구성되어 있음(환자)
* 1~17 속성은 환자의 의료 정보, 18 클래스는 수술 후 사망 여부(0 사망, 1 생존)
* 속성을 데이터셋으로 만들고 클래스를 만들 데이터셋은 따로 만들어야 함

`X = Data_set[:,0:17]`

--> 속성 데이터셋 **X**

`Y = Data_set[:,17]`

--> 클래스 데이터셋 **Y**

#### 두 번째 부분: 딥러닝 실행

```python
# 딥러닝을 구동하는 데 필요한 케라스 함수를 불러옵니다.
from keras.models import Sequential
from keras.layers import Dense

(중략)

# 딥러닝 구조를 결정합니다(모델을 설정하고 실행하는 부분입니다).
model = Sequential()
model.add(Dense(30, input_dim=17, activation='relu'))
model.add(Dense(1, activation='sigmoid'))

# 딥러닝을 실행합니다.
model.compile(loss='mean_squared_error', optimizer='adam', metrics=['accuracy'])
model.fit(X, Y, epochs=30, batch_size=10)
```

**케라스(keras)**: 딥러닝을 실힝시켜 주는 라이브러리, 텐서플로(TensorFlow)가 필요함  
딥러닝 프로젝트가 여행이라면  
텐서플로는 비행기  
케라스는 파일럿

```python
from keras.models import Sequential
from keras.layers import Dense
```

Sequential 함수와 Dense 함수를 keras 라이브러리에서 불러옴  
Sequential 함수는 딥러닝의 구조를 한 층 한 층 쌓는 구조 --> `model.add()` 함수 사용

```python
model = Sequential()
model.add(Dense(30, input_dim=17, activation='relu'))
model.add(Dense(1, activation='sigmoid'))
```

`model.add()` 함수 안에는 `Dense()` 함수가 포함  
**dense**: 조밀하게 모여있는 집합  
이후 `compile()` 함수 실행

```python
model.compile(loss='mean_squared_error', optimizer='adam', metrics=['accuracy'])
model.fit(X, Y, epochs=30, batch_size=10)
```

#### 핵심 키워드

* activation: 다음 층으로 어떻게 값을 넘길지 결정하는 부분, relu와 sigmoid 함수를 자주 사용
* loss: 한 번 신경망이 실행될 때마다 오차 값을 추적하는 함수
* optimizer: 오차를 어떻게 줄여 나갈지 정하는 함수

#### 마지막 부분: 결과 출력

```python
print("\n Accuracy: %.4f" % (model.evaluate(X, Y)[1]))
```

`model.evaluate()` 함수를 이용해 딥러닝의 모델이 어느 정도 정확하게 예측하는지 점검

#### 이 코드에서의 정확도(Accuracy)

학습 대상이 되는 기존 환자들의 데이터 중에 일부를 랜덤하게 추출하고  
새 환자인 것으로 가정하고 테스트한 결과

### 02-4 '블랙박스'를 극복하려면?

위에 한 것은 그저 코드를 실행해서 결과를 확인한 것 뿐  
내부 구조를 알아야 할 필요성이 있음  
**선형 회귀, 로지스틱 함수, 신경망, 역전파**의 개념을 알아야 함