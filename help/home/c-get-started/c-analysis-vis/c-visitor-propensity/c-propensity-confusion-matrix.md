---
description: 성향 점수에 대한 통계 계산이 정의됩니다.
title: 성향 점수 계산
uuid: 67270864-0468-4cc9-b48b-0e880f813555
exl-id: 679e1363-fd10-4a44-a85a-ef0daefaf303
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# 성향 점수 계산{#calculating-propensity-scoring}

성향 점수에 대한 통계 계산이 정의됩니다.

개념적으로, 각 방문자에 대해 계산된 점수는 지정된 이벤트(대상 필터에 의해 정의됨)가 발생할 수 있는 예상 확률로, 0에서 100% 사이의 점수 값 범위가 설정됩니다. 점수부여 프로시저는 기존 샘플을 훈련 데이터로 사용하여 이벤트 확률과 선택된 관심 독립 변수 간의 관계를 찾습니다.

수학적으로, 이러한 관계는 각 독립 변수에 연결된 각 수량 값에 반영됩니다. 이러한 값을 모델 계수라고 합니다. ScoreDim은 현재 IRLS(Interially Reweighted Least Squares) 알고리즘을 사용하여 모델 계수를 예측합니다. IRLS는 현재 패스와 이전 패스의 계수차가 1.0e-6보다 작을 때까지 샘플을 여러 번 거치하며, 이때 **converged**. 그러나 데이터에 따라 IRLS는 컨버전스에 도달하지 못할 수 있습니다.

이 경우 모델 교육 이터레이션은

* 계수 차이가 더 작은 대신 더 커지죠
* 1,000개의 패스에 도달했거나
* 수학 오류로 인해 반복을 계속할 수 없습니다.

IRLS가 수렴되지 않으면 SGD(Stochatic Gradient Gradient)라는 백업 알고리즘이 사용됩니다. SGD는 또한 여러 번 훈련 견본을 살펴볼 것입니다. 그러나 IRLS와 달리 SGD 모델 계수는 제어되므로 반복간의 차이가 항상 기하급수적으로 줄어듭니다. 마찬가지로, SGD는 계수 차이가 1.0e-6 또는 100,000 가공 패스에 도달하면 종료됩니다. IRLS 및 SGD 참여 실패가 추적 로그에 기록됩니다.

두 알고리즘 모두에 대해 모든 샘플이 모델 훈련에 들어가는 것은 아닙니다. 현재 80%가 모델을 훈련하는데 사용되고 있다. 모델 교육을 마친 후 나머지 20% 샘플을 사용하여 혼동 매트릭스에서 계산된 정확도, 회수 및 정밀도 측면에서 모델 강도를 평가하게 됩니다. 100%에 가까울수록 점수 모델이 향상됩니다.
