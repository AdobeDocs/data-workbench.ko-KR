---
description: 필요한 최소 방문자 수가 실험에 참여하기 전까지 실험을 실행한 후에는 실험 결과를 평가할 수 있는 충분한 통계 신뢰도를 확보할 수 있습니다.
solution: Analytics,Analytics
title: 실험 평가
uuid: 88fd81bc-b944-48ea-bd4d-8716979ec69e
exl-id: 5add2168-f6bc-45c5-bf1d-1191a38c5bac
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---

# 실험 평가{#evaluating-the-experiment}

필요한 최소 방문자 수가 실험에 참여하기 전까지 실험을 실행한 후에는 실험 결과를 평가할 수 있는 충분한 통계 신뢰도를 확보할 수 있습니다.

[!DNL Insight] 을 사용하여 가설의 일부로 정의된 지표나 주요 성능 지표를 비교하여 실험이 성공했는지 여부(즉, 가설이 지정된 신뢰도로 검증되었는지 여부)를 확인합니다.

이 예제 실험에서는 방문자 전환이 이전에 정의한 성공 기준인 1.5% 이상 증가하면 우리의 가설이 올바르게 증명됩니다.

다음 작업 공간 예제에서는 index2 테스트 그룹의 변환 비율이 실제로 제어 그룹의 변환 수치보다 1.8% 높음을 보여 주어 가설을 입증했습니다.

![](assets/experimentresults.png)

* [실험 결과 요약](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-24a496c080a04e929764094acb00bab7)
* [결과에 따라 조치 수행](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-1623e26ced524fd9beab48ac1f9165d9)
* [작업 모니터링](../../../home/c-undst-ctrld-exp/c-vw-rslts/c-ev-exp.md#section-1954311950c34637800cbd7c0711983f)

## 실험 결과 요약 {#section-24a496c080a04e929764094acb00bab7}

[!DNL Insight] 을 사용하여 상세한 보고서를 만들어 실험 결과를 요약하고 설명할 수 있습니다.

그런 다음 다음 다음 다음 예와 같이 보고서를 사용하여 보고서에 제공한 시각적 정보로 백업된 결과를 기반으로 권장 사항을 만들 수 있습니다.

![](assets/experimentresults2.png)

## 결과 {#section-1623e26ced524fd9beab48ac1f9165d9}에 따라 작업을 수행하는 중

결과가 명확해지면 테스트한 페이지에 프로덕션 수준을 변경하고, 웹 사이트의 다른 영역에 동일한 변경 사항을 적용하고, 테스트, 결과 및 수행한 변경 사항을 완전히 문서화하여 그러한 결과에 대해 작업할 준비가 됩니다.

## 작업 모니터링 {#section-1954311950c34637800cbd7c0711983f}

통제 실험이 완료되고 적절한 변경 사항을 구현한 후에는 유효성 검사 지표 보기, 제어 차트 만들기 및 대시보드 지표 제공과 같이 사용자가 변경한 내용을 계속 모니터링해야 합니다.

테스트하고 변경한 내용이 원래 결과를 반영하지 않는다고 생각되면 항상 가설을 다시 테스트할 준비를 하십시오.
