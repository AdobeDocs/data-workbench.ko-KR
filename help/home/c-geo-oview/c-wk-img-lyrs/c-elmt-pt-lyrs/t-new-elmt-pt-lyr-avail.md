---
description: 지구본 시각화에 표시할 요소 점 레이어를 사용할 수 있도록 하는 절차.
title: 새 요소 점 레이어 사용 가능
uuid: 7880de63-d206-4c56-b8cf-75882d867ace
exl-id: 9001f6b6-5d25-48a0-9381-04f679e0ff4d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 6%

---

# 새 요소 점 레이어 사용 가능{#making-a-new-element-point-layer-available}

지구본 시각화에 표시할 요소 점 레이어를 사용할 수 있도록 하는 절차.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*profile name*\Map 폴더에 레이어 파일과 관련 조회 파일을 배치합니다.
1. 요소 점 레이어에 대한 새 차원을 정의했지만 아직 데이터 세트를 다시 변형하지 않은 경우 지금 데이터 세트를 다시 변환합니다.
1. Profiles\*profile name*\Map 폴더에서 [!DNL order.txt] 파일을 편집하여 레이어를 표시할 순서를 반영합니다. 기본적으로 레이어는 해당 이름으로 사전식 순서로 표시됩니다.

   >[!NOTE]
   >
   >[!DNL order.txt] 파일을 편집할 때는 표시하려는 맵 레이어를 표시하지 않도록 주의하십시오.

   [!DNL order.txt] 파일 사용에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

1. Data Workbench에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]*** 를 클릭하여 원하는 프로필을 선택합니다.
1. 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]** 을 클릭합니다. [!DNL Work Online] 옆에 X가 나타납니다.
1. 작업 공간을 열고 지구 시각화에서 마우스 오른쪽 단추를 클릭하고 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
