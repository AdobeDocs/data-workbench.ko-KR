---
description: 제어된 실험은 실험 샘플 그룹에서 얻은 결과와 표준 제어 그룹의 결과를 비교할 수 있는 테스트입니다.
solution: Insight,Analytics
title: 데이터 워크벤치 제어 실험
topic: Data workbench
uuid: 5fce2d9e-4975-44e4-a7c0-11064d8d28b4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 워크벤치 제어 실험{#data-workbench-controlled-experiments}

제어된 실험은 실험 샘플 그룹에서 얻은 결과와 표준 제어 그룹의 결과를 비교할 수 있는 테스트입니다.

사이트를 통해 제어된 실험과 실험 결과가 웹 사이트의 다른 측면과 관련될 때 이를 구현, 측정 및 분석할 수 있습니다. 이렇게 하면 제안된 변경 사항을 완전히 구현하는 데 상당한 시간과 비용을 소비하기 전에 웹 사이트 성능 향상과 관련된 가설을 테스트할 수 있습니다.

>[!NOTE]
>
>사이트 실험은 사용 중인 방문자 식별 방법만 [!DNL Sensor] 설정된 영구 쿠키 방법인 데이터 세트에서만 분석할 수 있습니다. J2EE 서버(JBoss, Tomcat, WebLogic 및 WebSphere)에서 실행되는 센서는 제어된 실험을 지원하지 않습니다. 자세한 내용은 다음 섹션을 참조하십시오.

사이트를 사용하면 A/B, A/B/A 및 다변량 제어 실험을 구현하여 현 웹 사이트 성능에 영향을 주지 않고 통계적으로 정확한 데이터를 제공하여 가설을 세부적으로 평가할 수 있는 충분한 테스트 데이터를 수집할 수 있습니다.
