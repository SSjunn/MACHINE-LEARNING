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


# 모델 선택


### 과소적합과 과잉적합
---------
![image](https://github.com/user-attachments/assets/125e7033-0344-4010-bece-f526c5704d09)

1차 모델은 ${\textsf{\color{blue}과소적합}}$
* 모델의 용량이 작아 오차 발생

12차의 경우 1차와는 다르게 후련집합에 대해 거의 완벽하게 근사화 하였다
하지만 새로운 데이터를 예측한다면 큰 문제가 발생한다.
**WHY?**
학습과정에서 작은 잡음까지 전부 모델링을 하여 용량의 크기때문이다.  → 이러한 현상을 과잉적합(overfitting)으로 부른다.

1~2차는 훈련집합과 테스트집합 모두 낮은 성능.
3~4차는 룬련집합에 대해 12차보다는 낮지만 테스트집합에는 높은 성능 → 높은 일반화 능력
12차는 훈련집합에 높은 성능을 보이나 테스트 집함에서는 낮은 성능 → 낮은 일반화 능력


### 바이어스와 분산
----

![image](https://github.com/user-attachments/assets/c6bd4f89-7bcf-4556-af32-1d08ee35e699)

바이어스(bias) : 모델을 통해 얻은 예측값과 실제 정답과의 차이의 평균

2차는 매번 큰 오차 → 바이어스가 크다. 하지만 훈련집합이 바뀌더라도 비슷한 모델을 얻을 수 있다. → 낮은 분산
12차는 매번 작은 오차 → 바이어스가 작다. 훈련집합이 바뀌게 되면 다른 모델을 얻을 수 있다. → 높은 분산
**일반적으로 용량이 작은 모델은 바이어스는 크고 분산은 작다. 복잡한 모델은 바이어스는 작고 분산은 크다.**

기계학습의 목표 : 낮은 바이어스와 낮은 분산을 가진 예측기 제작이 목표

![image](https://github.com/user-attachments/assets/41b4261c-7b5e-4958-b106-f37b7f6c0ae5)

바이어스와 분산은 트레이드오프 관계
**중요** 바이어스 희생을 최소로 유지하면서 분산을 최대로 낮추는 전략이 필요

## 검증집합과 교차검증을 이용한 모델 선택 알고리즘

### 검증집합
훈련집합과 테스트 집합으로 만든 모델집합을 여러 모델을 독립적으로 학습시킨후 그중 가장 작은 모델을 선택하기 위해 검증집합을 만들어 성능을 측정
![image](https://github.com/user-attachments/assets/2f21b7bd-f917-4047-8021-6f3e73de1b34)

### 교차검증(Cross-Validation)
비용 문제로 별도의 검증집합이 없는 상황에 유용한 모델 선택 기법이며 훈련집합을 등분하여, 학습과 평가 과정을 여러 번 반복한 후 평균 사용
![image](https://github.com/user-attachments/assets/169b6e98-e933-46df-bf1e-a2851dab8d70)






공개 된 데이터베이스

위키피디아 :  list of datasets for machine learning research
*
UCI 리퍼지토리
