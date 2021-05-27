---
description: 통제 실험은 실험 샘플 그룹에서 얻은 결과를 표준 통제 그룹의 결과와 비교할 수 있도록 하는 테스트입니다.
solution: Analytics,Analytics
title: Data Workbench 통제 실험
uuid: 5fce2d9e-4975-44e4-a7c0-11064d8d28b4
exl-id: 40bcf6a4-c722-427c-81ac-45dec1eae0b5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# Data Workbench 통제 실험{#data-workbench-controlled-experiments}

통제 실험은 실험 샘플 그룹에서 얻은 결과를 표준 통제 그룹의 결과와 비교할 수 있도록 하는 테스트입니다.

Site를 사용하면 통제 가능한 실험 및 결과가 웹 사이트의 다양한 측면과 관련될 때 이를 구현, 측정 및 분석할 수 있습니다. 이렇게 하면 제안된 변경 사항을 완전히 구현하는 데 상당한 시간이나 비용을 소비하기 전에 웹 사이트 성능 향상에 대한 가설을 테스트할 수 있습니다.

>[!NOTE]
>
>사이트 실험은 사용 중인 방문자를 식별하는 유일한 방법이 [!DNL Sensor] 설정된 영구 쿠키 방법인 데이터 세트에서만 분석할 수 있습니다. J2EE 서버(JBoss, Tomcat, WebLogic 및 WebSphere)에서 실행되는 센서는 통제 실험을 지원하지 않습니다. 자세한 내용은 다음 섹션을 참조하십시오.

사이트를 사용하면 A/B, A/B/A 및 다변량 제어 실험을 구현하여 현재 웹 사이트 성능에 영향을 주지 않고 통계적으로 정확한 데이터를 제공하여 가설을 세부 평가할 수 있도록 합니다.
