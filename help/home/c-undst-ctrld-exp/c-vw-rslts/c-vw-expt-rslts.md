---
description: Log Processing.cfg에 새 필드를 추가하고 새로운 분할 변환 및 확장 차원을 만든 후 데이터 재처리의 빠른 입력 단계가 완료되는 즉시 새로 생성된 확장 차원을 볼 수 있습니다.
solution: Insight,Analytics
title: 실험 결과 보기
topic: Data workbench
uuid: c0468cad-fb8d-4ecf-8912-bf80b44b0a65
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 실험 결과 보기{#viewing-the-experiment-results}

Log Processing.cfg에 새 필드를 추가하고 새로운 분할 변환 및 확장 차원을 만든 후 데이터 재처리의 빠른 입력 단계가 완료되는 즉시 새로 생성된 확장 차원을 볼 수 있습니다.

이 차원은 기본적으로 각 실험 그룹에 대한 세션 수를 표시합니다.

**실험 차원을 보려면**

* 의 모든 작업 영역에서 만든 실험 차원이 있는 테이블을 [!DNL Insight]엽니다.

   현재 실행 중인 각 실험 및 각 실험 내의 각 그룹을 나타내는 실험 차원 요소는 각 그룹에 대한 현재 세션 수와 함께 표시됩니다. 각 그룹의 이름은 실험 이름 다음에 그룹 이름을 사용하여 다음 형식으로 지정됩니다.

   *실험 이름.그룹 이름*

   예: [!DNL New Homepage.Control]

다음 표에서는 실험 및 각 실험 및 해당 그룹에서 생성된 제어 실험 그룹 차원을 [!DNL Transformation.cfg] 보여 줍니다.

새 홈 페이지 실험은 테이블 하단에 다음과 같은 두 그룹이 표시됩니다.Control 및 index2.

![](assets/controlledexpgrps.png)

이제 실험 차원 및 관련 지표를 사용하여 실험 결과를 탐색 및 해석하고 이러한 결과를 설명하는 유용한 보고서를 만들 수 있습니다.