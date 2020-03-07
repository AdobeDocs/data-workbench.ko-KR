---
description: 모델 뷰어를 사용하면 성향 점수 지정 기능을 사용하여 로지스틱 회귀 모델을 생성할 수 있습니다.
solution: Analytics
title: 모델 뷰어
topic: Data workbench
uuid: 7ee8ff29-21c2-4721-804a-c7a5d101b50b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Model Viewer{#model-viewer}

모델 뷰어를 사용하면 성향 점수 지정 기능을 사용하여 로지스틱 회귀 모델을 생성할 수 있습니다.

모델 뷰어는 각 입력 변수의 계수 가중치(상수 용어 포함)와 통계 오류 범위를 표시합니다. 높은 절대 계수 및 작은 오차 여백을 표시하는 입력 변수는 모델에서 가장 중요한 예측자입니다.

**모델 뷰어 차트 열기**

1. 선택 [!DNL Add Visualization > Predictive Analytics > Scoring] .
1. 저장된 점수의 모델 완료 위로 마우스를 가져갑니다.

![](assets/propensity_model_viewer.png)

계수 >= 1이 있는 입력 변수는 성향 모델에 긍정적인 영향을 줍니다. 1보다 작은 계수는 성향 모델에 부정적인 영향을 줍니다. 괄호 안에 정의된 범위는 오류이며 성공적인 모집단 전체에서 입력 변수의 일관성을 나타냅니다.
