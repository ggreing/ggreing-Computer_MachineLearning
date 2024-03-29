# 기계학습 CH01. 패턴인식의 개요  
----------------------------
### 인공지능의 가능성에 대한 철학적 논쟁  
-----------------------------------------------------
* 패턴인식을 공부하기 전에 생각해볼 문제  
  * 컴퓨터는 단지 계산하는 기계? 컴퓨터도 인간과 같이 생각하고 언어 이해 가능?  
* 언어의 이해는 무엇?  
* ChatGPT의 한계는?  

* 인공지능의 가능성에 대한 긍정적 입장  
  * A.M. Turing  
  * 튜링 테스트(모방게임)  
* 인공지능의 가능성에 대한 부정적 입장  
  * John Searle  
  * 중국어 방 논증  
--------------------------------------------
### 패턴인식의 정의  
-----------------------------------------------------
* 패턴인식이란 무엇인가?  
  * 계산이 가능한 기계적인 장치(컴퓨터)가 어떠한 대상을 인식하는 문제를 다루는 인공지능의 한 분야  
  * 인지과학 - 인공지능 - 패턴인식  
* 패턴인식 시스템의 설계 단계  
  * 1단계 : 데이터 수집 단계  
    * 패턴인식 과정 중 가장 많은 시간 소요  
    * 인정된 패턴인식 성능을 위한 단계  
    * 위를 위해 어느 정도의 표본 데이터가 필요한지 고려하여 데이터 수집  
  * 2단계 : 특징 선택 단계  
    * 패턴인식 시스템의 성능에 결정적인 영향을 미치는 단계  
  * 대상  

--------------------------------------
### 특징과 패턴  
-----------------------------------------------------
* 특징이란?  
  * 어떤 객체가 가지고 있는 객체 고유의 분별 가능한 측면, 질 또는 특성  
* 패턴이란? 
  * 개별 객체의 특색(traits)이나 특징features)들의 집합  
* 좋은 특징과 나쁜 특징  
  * 두 특징이 확실히 `구분될 수 있는 분포로 존재`하여 특징끼리 묶을 수 있는 경우  -> `좋은특징`  
  * 두 특징이 확실히 `구분되지 않고` 모두 섞여있어 해당 특징으로 분포를 구분할 수 없는 경우 -> `나쁜 특징`  
* 패턴의 유형  
  * 선형 분리 가능한 패턴  
  * 비선형 분리 가능한 패턴  
  * 높은 상관을 가진 패턴  
  * 멀티 모달 특성을 가진 패턴 
----------------------------------------
### 패턴인식 시스템의 처리 과정  
-----------------------------------------------------
* 패턴인식 시스템의 처리 과정  
  * 실세계 -> 측정장치(카메라, 마이크 등) -> 전처리(잡음 제거, 특징 추출, 정규화) -> 차원 축소(특징 선택, 특징 사영)  
  -> 인식, 예측(분류, 회귀, 클러스터링, 서술) -> 모델 선택(교차 검증, 부트스트랩) -> 분석 결과  

------------------------------------------
### 패턴인식의 유형  
-----------------------------------------------------
* 문제의 유형  
  * 분류(Classification)  
    * 사전에 정의된 클래스들이 있고 새로운 입력 데이터가 어느 클래스에 속하는지 판단하는 유형  
    * `지도학습`  
  * 군집화(Clustering)  
    * 사전에 정의된 클래스는 없고 입력데이터들의 유사도에 따라 묶어가는 유형  
    * `비지도학습`  
  * 회귀(Regression)  
    * 사전에 제공된 데이터의 상관관계를 분석하여 미래의 데이터를 예측하는 유형  
    * `지도학습`  
-------------------------------------------
### 패턴인식의 분류기  
* 분류기  
  * 패턴인식의 대부분을 이루는 분류작업 -> 분류기(Clasifier)에 의해 이루어짐  
  * 분류 작업 : 특징 벡터들로 이루어진 특징 공간을 이름이 있는 클래스들 간의 결정 영역으로 분할(Partition)하는 것  
  * 결정 영역의 경계 : 결정 경계(Decision Boundary)  
-------------------------------------------------
### 패턴인식의 성능 평가  
--------------------------------------------------
* 혼동행렬  
 * `True Positive(TP)` : 실제 True인 정답을 True라고 예측(정답)  
 * `False Positive(FP)` : 실제 False인 정답을 True라고 예측(오답)  
 * `False Negative(FN)` : 실제 True인 정답을 False라고 예측(오답)  
 * `True Negative(TN)` : 실제 False인 정답을 False라고 예측(정답)  
* `재현율` : 실제 True인 것 중에서 모델이 True 라고 예측한 것의 비율  
* `정밀도` : 모델이 True라고 분류한 것 중에서 실제 True인 것의 비율  
* `FPR(False Positive Rate)` : 실제 False인 data 중에서 모델이 True라고 예측한 비율  
* 혼동행렬 계산  
  * 취소율(recall rate) = TP / (TP + FN)  
  * 정밀도(precision) = TP / (TP + FP)  
  * 참 긍정률(TPR, True Positive Rate) = TP / (TP + FN)  
  * 거짓 긍정률(FPR, False Positive Rate) = FP / (FP + TN)  
------------------------------------------------------
* 벤 다이어그램(Venn-diagram) 
* ROC 곡선  
-----------------------------------------------------
### 패턴인식 접근법
-----------------------------------------------------  
- 패턴인식의 접근법  
  - 템플립 정합법(template matching)  
    * 패턴인식에서 가장 오래되고 가장 쉬운 접근법  
    * 비교 대상 패턴에 대한 템플릿(형틀)을 미리 마련해두고 인식하고자 하는 패털을 템플릿 구성 조건에 맞추는 정규화 과정을 거쳐서 상화상관 혹은거리와 같은 유사도를 척도로 하여 패턴을 인식하는 방법  
    * 동일한 카테고리에 속한 다양한 데이터에서 그 카테고리를 가장 잘 설명하는 일반화된 템플릿을 마련하는 과정이 가장 중요  
    * 알고리즘이 간단하여 `계산 속도가 빠르지만`, `대상 패턴의 특징 변화`에 민감  
  * 통계적 접근법(statistical)  
    * 각 클래스에 속하는 패턴 집합의 통계적 분포에서 생성되는 결정 경계를 기반하여 미지의 패턴이 속한 클래스를 결정하는 방법  
    * 패턴들의 통계적 모델은 해당 클래스에서의 확률밀도함수 P(x|c_i)가 됨  
    * 통계적인 모수로 이루어진 각 클래스에 대한 확률밀도함수를 생성하는 과정을 학습이라고 함  
  * 신경망 접근법(neural networks)  
    * 생물학적 신경세포의 연결 결합 관계를 모델링하여 입력 자극에 대한 처리 단위인 뉴런(neuron)으로 구성된 망(network)의 응답 과정으로 패턴을 분류  
    * 패턴의 정보(knowledge)는 시냅스의 연결 강도 가중치들로 저장됨  
    * 학습이 가능하고, 알고리즘적이지 않으며, 블랙박스와 같이 취급  
    * 사전 지식을 최소화하고, 뉴런의 층이 충분하면 이론적으로 어떠한 복잡한 결정 영역도 만들 수 있는 매우 매력적인 접근법  
  * 구조적 접근법(structure)  
    * 패턴의 양적 특징들에 따른 분석을 하지 않고 패턴을 구성하는 기본 원형들 사이의 관계서에 관심을 두는 접근법  
    * 연구 대상이 되는 대표 패턴 : 문자, 지문, 염색체  
* 패턴인식의 응용 분야(PDF 확인!! 필수!!)  
  * 문자인식 분야  
  * 생체 인시과 인간 행동 패턴 분석 분야  
  * 진단 시스템 분야  
  * 예시 -> 간단한 영문자 인식 시스템, 자동 어류 분류 시스템, 등등  

 


























