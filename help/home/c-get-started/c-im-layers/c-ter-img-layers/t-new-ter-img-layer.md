---
description: 지구 시각화에 표시할 수 있는 모든 지형 레이어를 만드는 단계입니다.
title: 새로운 지형 이미지 레이어 사용 가능
uuid: 8fb98a3e-6335-4922-a1e6-35c92b19e2ec
exl-id: bf0e6b37-4c8a-4d50-8bc9-eb70ca1cbb23
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 7%

---

# 새로운 지형 이미지 레이어 사용 가능{#make-a-new-terrain-image-layer-available}

{{eol}}

지구 시각화에 표시할 수 있는 모든 지형 레이어를 만드는 단계입니다.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*profile name*\Maps 폴더에 레이어 파일과 지원 이미지 파일을 배치합니다.
1. 편집 [!DNL order.txt] 파일을 Profiles\*profile name*\Map 폴더에 매핑하여 레이어를 표시할 순서를 반영합니다. 기본적으로 레이어는 해당 이름으로 사전식 순서로 표시됩니다.

   >[!NOTE]
   >
   >편집 시 [!DNL order.txt] 파일에서 표시하려는 맵 레이어를 표시하지 않도록 주의하십시오.

   사용에 대한 자세한 정보 [!DNL order.txt] 파일의 경우 *Data Workbench 사용 안내서*.

1. Data Workbench에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 을 클릭하여 원하는 프로필을 선택합니다 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]**. Work Online 옆에 X가 나타납니다.
1. 작업 공간을 열고 지구 시각화에서 마우스 오른쪽 단추를 클릭하고 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
