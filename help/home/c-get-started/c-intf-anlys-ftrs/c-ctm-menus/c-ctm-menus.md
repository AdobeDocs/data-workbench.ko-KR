---
description: 작업 공간에서 마우스 오른쪽 단추를 클릭하여 액세스할 수 있는 작업 공간 창 메뉴 및 지표, 차원 및 맵 레이어를 나열하는 메뉴를 포함하여 메뉴 모양을 사용자 지정할 수 있습니다.
title: 메뉴 사용자 정의
uuid: 8c409c50-40b3-4de3-8048-a825ef4d75f5
exl-id: 7a377d9c-d339-43d8-a71a-a322416b2e60
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# 메뉴 사용자 정의{#customize-a-menu}

{{eol}}

작업 공간에서 마우스 오른쪽 단추를 클릭하여 액세스할 수 있는 작업 공간 창 메뉴 및 지표, 차원 및 맵 레이어를 나열하는 메뉴를 포함하여 메뉴 모양을 사용자 지정할 수 있습니다.

모든 메뉴의 계층 구조는 [!DNL Profile Manager]. 예를 들어 작업 공간 창 메뉴는 메뉴 디렉토리의 구조를 미러링하고 지표 메뉴는 지표 디렉토리의 구조를 반영합니다. 모든 메뉴의 해당 디렉토리에는 다음 항목이 포함될 수 있습니다.

* **파일:** 이러한 파일은 해당 메뉴 항목을 클릭하여 열 수 있는 시각화, 범례, 주석, 관리 인터페이스, 지표, 차원 또는 맵 레이어를 나타냅니다.
* **An [!DNL order.txt] 파일:** 이 파일은 메뉴에 해당 항목이 표시되는 순서를 지정합니다.
* **하위 디렉토리:** 각 하위 디렉토리는 하위 메뉴를 나타냅니다. 각 하위 디렉토리에는 자체 파일, 하위 디렉토리 및 [!DNL order.txt] 파일.

예: [!DNL Add Legend] 메뉴에는 지표, 색상, 값 및 신뢰도 메뉴 항목이 순서대로 포함되어 있습니다. 비교에서 Menu\Add Legend 디렉터리는 [!DNL Profile Manager] 에는 파일이 포함되어 있습니다 [!DNL Color.vw], [!DNL Confidence.vw], [!DNL Metric.vw], 및 [!DNL Value.vw] 파일 및 [!DNL order.txt] 다른 파일의 순서를 제어하는 파일입니다.
