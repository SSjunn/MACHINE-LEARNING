## 기계학습이란

기계학습 : 인공지능 초창기 사무엘의 정의

인공지능의 주도권 전환

지식기반 → 기계학습

기계학습 : **데이터 중심** 접근방법

예측(prediction)문제

임의의 시간이 주어지면 이때 이동체의 위치는?

회귀(regression)문제와 분류(classification)문제로 나뉨

회귀는 목표치가 실수 분류는 분류값

### 훈련집합

기로축은 특징, 세로축은 목표치
관측한 4개의 점이 훈련집합을 구성함

![Untitled](https://github.com/user-attachments/assets/21e5f4a4-f169-4817-a93f-623e3e00b6b4)

### 데이터를 어떻게 모델링할 것인가

눈대중으로 보면 직선을 이루므로 직선을 선택 → 모델로 직선을 선택한 셈

직선 모델의 수식

2개의 매개변수 w와 b

![Untitled](https://github.com/user-attachments/assets/b56c1c0e-dc3c-4c71-ac34-6f4d981d11a9)

기계 학습은

가장 정확하게 예측할 수 있는, 즉 **최적의 매개변수를 찾는 작업** (w와 b를 찾는것)

처음에는 최적값을 모르므로 임의의 값에서 시작하고, 점점 성능을 개선하여 최적에 도달

[그림 1-4]의 예에서는 f1에서 시작하여 f1 → f2 → f3

 최적인 f3 은 w = 0.5 와 b = 0.2

기계 학습의 궁극적인 목표

1. 훈련집합에 없는 새로운 샘플에 대한 오류를 최소화(새로운 샘플 집합 : 테스트 집합)
2. 테스트 집합에 대한 높은 성능을 **일반화** 능력이라고 부름

#테스트 집합으로 논문도 쓰고 성능 제시도 가능함

기계학습은 동시에 하나밖에 못한다. 동시에 하는 알고리즘도 있지만 기본적으로는 하나의 과업만 가능하다

![KakaoTalk_20240718_142428985](https://github.com/user-attachments/assets/fe834ad6-d49c-43da-bac3-47b503999961)

## 특징 공간에 대한 이해

특징 공간 : 관측 값들이 있는 공간. 이 특징 공간은 여러 차원으로 구성이 될 수 있음

![Untitled (1)](https://github.com/user-attachments/assets/62cbbc28-25a9-4bb2-8c2a-2b9de1450179)
![Untitled (2)](https://github.com/user-attachments/assets/2d4f55f9-a0cd-4c4e-b34f-e2cb6d7efb6d)

모델이 복잡해지면 기계학습이 추정해야 되는 매개변수의 수가 아주 많아진다.

### 특징 공간 변환과 표현 학습
![Untitled (3)](https://github.com/user-attachments/assets/75b75b23-f5c4-4b33-98bc-4a2cc210c1ba)
![Untitled (4)](https://github.com/user-attachments/assets/96dc0965-e268-44ab-834b-b0ec0f977187)

### 표현 학습
![Untitled (5)](https://github.com/user-attachments/assets/2bd91c24-7513-4a2d-90ba-791ef8834d08)

## 데이터에 대한 이해

**과학 기술의 발전 과정**

데이터 수집 → 모델 정립 → 예측 의 사이클을 돈다.

**기계학습**

1. 기계학습이 푸는 문제는 훨씬 복잡
2. 단순한 수학 공식으로 표현 불가능
3. 자동으로 모델을 찾아내는 과정이 필수

**실제 기계 학습 문제**

1. 데이터 생성 과정을 알 수 없음
2. 단지 주어진 훈련집합 X,Y(벡터)로 예측 모델 또는 생성 모델을 근사 추정할 수 있을 뿐

**데이터베이스의 품질**

1. 주어진 응용에 맞는 충분히 다양한 데이터를 충분한 양만큼 수집 → 추정 정확도 높아짐
2. 주어진 응용 환경을 자세히 살핀 다음 그에 맞는 데이터베이스 확보는 아주 중요함

**데이터 가시화** 

1. 4차원 이상의 초공안은 한꺼번에 가시화 불가능
2. TSNG 기법이 지금 제일 유명

## 간단한 기계학습의 예

**매개변수 세타**
![Untitled (6)](https://github.com/user-attachments/assets/708d50b7-d892-46c9-968b-c9c96dc49fd7)
![Untitled (7)](https://github.com/user-attachments/assets/905175ae-f1f9-4cba-9731-cc7826a3edc6)


목적 함수(objective function) or 비용 함수(cost function)
![Untitled (8)](https://github.com/user-attachments/assets/77f31422-49d7-4cfb-99be-5677f00a9d50)
![Untitled (9)](https://github.com/user-attachments/assets/7554f093-f2ca-4323-9a46-6784d3446263)

공개 된 데이터베이스

위키피디아 :  list of datasets for machine learning research

UCI 리퍼지토리
