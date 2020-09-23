---
description: 필요한 최소 방문자 수가 실험에 참여하도록 테스트를 실행한 후 실험 결과를 평가할 수 있도록 충분한 통계 신뢰도를 확보할 수 있습니다.
solution: Analytics,Analytics
title: 실험 평가
topic: Data workbench
uuid: 88fd81bc-b944-48ea-bd4d-8716979ec69e
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# 실험 평가{#evaluating-the-experiment}

필요한 최소 방문자 수가 실험에 참여하도록 테스트를 실행한 후 실험 결과를 평가할 수 있도록 충분한 통계 신뢰도를 확보할 수 있습니다.

를 사용하여 가설 [!DNL Insight]의 일부로 정의된 지표나 주요 성능 지표를 비교하여 실험이 성공했는지(즉, 가설이 지정된 신뢰로 검증되었는지 여부)를 확인합니다.

예제 테스트에서 방문자 전환이 1.5% 이상 증가하면 앞서 정의한 성공 기준인 가설이 올바르게 증명되었습니다.

다음 작업 공간 예는 index2 테스트 그룹의 변환이 제어 그룹보다 실제로 1.8% 더 높은 것으로 가설을 입증한 것을 보여줍니다.

![](assets/experimentresults.png)

* [실험 결과 요약](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-24a496c080a04e929764094acb00bab7)
* [결과에 따라 조치 수행](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-1623e26ced524fd9beab48ac1f9165d9)
* [작업 모니터링](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-1954311950c34637800cbd7c0711983f)

## 실험 결과 요약 {#section-24a496c080a04e929764094acb00bab7}

를 사용하여 자세한 보고서 [!DNL Insight]를 만들어 실험 결과를 요약하고 표현할 수 있습니다.

그런 다음 다음 다음 예제와 같이 보고서를 사용하여 보고서에서 제공한 시각적 정보로 백업된 결과를 기준으로 권장 사항을 만들 수 있습니다.

![](assets/experimentresults2.png)

## 결과에 따라 조치 수행 {#section-1623e26ced524fd9beab48ac1f9165d9}

결과가 명확해지면 테스트된 페이지에 프로덕션 수준의 변경을 적용하고 웹 사이트의 다른 영역에 동일한 변경 사항을 적용하고 테스트, 결과 및 변경 내용을 완벽하게 문서화하여 이러한 결과에 대응할 수 있습니다.

## 작업 모니터링 {#section-1954311950c34637800cbd7c0711983f}

제어 실험이 완료되고 적절한 변경 사항을 구현한 후에는 유효성 검사 지표 보기, 제어 차트 만들기, 대시보드 지표 제공 등의 변경 사항을 계속 모니터링해야 합니다.

테스트하고 수행한 변경 사항이 원본 결과를 준수하지 않는다고 생각되면 언제든지 가설을 재테스트할 수 있습니다.
