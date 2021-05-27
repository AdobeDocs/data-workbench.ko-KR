---
description: 지구 시각화에 표시할 수 있는 새로운 지형 레이어를 만드는 단계입니다.
title: 새로운 지형 이미지 레이어 사용 가능
uuid: aeeb4ab0-f55c-47b8-96e4-eafd4df4d68a
exl-id: 76374298-ed65-4fcf-b40b-be7c15784f40
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 새로운 지형 이미지 레이어 사용 가능{#making-a-new-terrain-image-layer-available}

지구 시각화에 표시할 수 있는 새로운 지형 레이어를 만드는 단계입니다.

1. **[!UICONTROL Insight Server]** 설치 디렉토리 내의 Profiles\*profile name*\Maps 폴더에 레이어 파일과 지원 이미지 파일을 배치합니다.
1. Profiles\*profile name*\Map 폴더에서 [!DNL order.txt] 파일을 편집하여 레이어를 표시할 순서를 반영합니다. 기본적으로 레이어는 해당 이름으로 사전식 순서로 표시됩니다.

   >[!NOTE]
   >
   >[!DNL order.txt] 파일을 편집할 때는 표시하려는 맵 레이어를 표시하지 않도록 주의하십시오.

   [!DNL order.txt] 파일 사용에 대한 자세한 내용은 *Data Workbench 사용 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

1. Data Workbench에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]*** 를 클릭하여 원하는 프로필을 선택합니다.
1. 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]** 을 클릭합니다. [!DNL Work Online] 옆에 X가 나타납니다.
1. 작업 공간을 열고 지구 시각화에서 마우스 오른쪽 단추를 클릭하고 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
