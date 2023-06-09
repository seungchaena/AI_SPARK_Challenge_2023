# AI_SPARK_Challenge_2023

## Competition Explanation
- 대회 목표: 산업기기 이상 전조증상을 예측하여 기기 고장을 예방하고 그로 인한 사고를 예방하는 모델을 개발하는 것
- 요약: training data(only normal data), test data(normal + abnormal data) 로 구성된 일반적인 비지도 학습기반의 anomaly detection문제.
- 대회 기간: 2023/03/07 ~ 2023/04/21
- 최종 점수(macro f1-score): 0.9538864792
- [https://aifactory.space/competition/detail/2299](https://aifactory.space/competition/detail/2226)

## Approach Method
![image](https://github.com/Naseungchae/AI_SPARK_Challenge_2023/assets/90239125/f450c02b-29ce-4669-83e5-70728c315f33)

- 절차소개
1. 테스트 데이터로부터 대해 이상치(abnormal data)의 분포를 가정한다. 
2. 가정에 대한 실험을 진행하기 위해 가정을 잘 반영할 수 있는 데이터의 형태로 데이터를 변환한다.  
3. 거리로 재구성된 training data와 test data에 대한 전처리를 진행한다. 
4. Kernel Densitiy Estimaion을 진행한다.
5. 모델을 학습하고 submission file을 제출한다.

## Result
매우 단순하고 직관적인 가정임에도 실험결과 0.9538864792의 우수한 성능을 낼 수 있었다.

## For more datailed infromatio
Please read a "Median_distance_based_KDE.ipynb" in this repository.
