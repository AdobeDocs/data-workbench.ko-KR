---
description: 모델 뷰어를 사용하면 성향 점수 기능을 사용하여 논리적인 회귀 모델을 생성할 수 있습니다.
title: 모델 뷰어
uuid: 7ee8ff29-21c2-4721-804a-c7a5d101b50b
exl-id: e0e4acd4-76a2-436a-993b-2bb7ca91ae1a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---

# 모델 뷰어{#model-viewer}

{{eol}}

모델 뷰어를 사용하면 성향 점수 기능을 사용하여 논리적인 회귀 모델을 생성할 수 있습니다.

모델 뷰어는 각 입력 변수의 계수 가중치(상수 용어 포함)와 통계 오류 범위를 표시합니다. 절대 계수와 작은 오차 마진을 보여주는 입력 변수는 모델에서 가장 중요한 예측자입니다.

**모델 뷰어 차트를 열려면**

1. [!DNL Add Visualization > Predictive Analytics > Scoring]을 선택합니다.
1. 저장된 점수의 모델 완료 위로 마우스를 가져갑니다.

![](assets/propensity_model_viewer.png)

계수 = 1이 있는 입력 변수는 성향 모델에 긍정적인 영향을 줍니다. 1 미만인 계수는 성향 모델에 부정적인 영향을 줍니다. 괄호 내에 정의된 범위는 오류이며, 성공적인 모집단에서 입력 변수의 일관성을 나타냅니다.
