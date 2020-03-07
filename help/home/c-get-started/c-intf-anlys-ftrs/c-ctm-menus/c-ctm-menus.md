---
description: 작업 공간에서 마우스 오른쪽 단추를 클릭하여 액세스하는 작업 영역 창 메뉴, 지표, 차원 및 맵 레이어를 나열하는 메뉴 등 메뉴의 모양을 사용자 정의할 수 있습니다.
solution: Analytics
title: 메뉴 사용자 정의
topic: Data workbench
uuid: 8c409c50-40b3-4de3-8048-a825ef4d75f5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 메뉴 사용자 정의{#customize-a-menu}

작업 공간에서 마우스 오른쪽 단추를 클릭하여 액세스하는 작업 영역 창 메뉴, 지표, 차원 및 맵 레이어를 나열하는 메뉴 등 메뉴의 모양을 사용자 정의할 수 있습니다.

메뉴의 계층 구조는 에 있는 해당 디렉토리의 구조를 반영합니다 [!DNL Profile Manager]. 예를 들어 작업 영역 창 메뉴는 메뉴 디렉토리의 구조를 미러링하고 지표 메뉴는 지표 디렉토리의 구조를 반영합니다. 모든 메뉴의 경우 해당 디렉토리에 다음 항목이 포함될 수 있습니다.

* **파일:** 이러한 파일은 해당 메뉴 항목을 클릭하여 열 수 있는 시각화, 범례, 주석, 관리 인터페이스, 지표, 차원 또는 맵 레이어를 나타냅니다.
* **파일[!DNL order.txt]:** 이 파일은 메뉴에 해당 항목이 표시되는 순서를 지정합니다.
* **하위 디렉토리:** 각 하위 디렉토리는 하위 메뉴를 나타냅니다. 각 하위 디렉토리에는 자체 파일, 하위 디렉토리 및 [!DNL order.txt] 파일이 포함될 수 있습니다.

예를 들어, 메뉴에는 지표, 색상, 값 및 신뢰도 메뉴 항목이 순서대로 포함되어 있습니다. [!DNL Add Legend] 반면, 의 Menu\Add Legend 디렉토리에는 파일 [!DNL Profile Manager] , [!DNL Color.vw][!DNL Confidence.vw], [!DNL Metric.vw]파일 및 다른 파일의 순서를 제어하는 [!DNL Value.vw] [!DNL order.txt] 파일이 알파벳순으로 들어 있습니다.
