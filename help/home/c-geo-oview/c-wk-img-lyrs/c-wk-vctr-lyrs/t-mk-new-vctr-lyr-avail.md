---
description: 지구 시각화에 표시할 벡터 레이어를 사용할 수 있도록 하는 절차.
title: 새로운 벡터 레이어 사용 가능
uuid: 7e88f183-b0aa-452d-b124-7cd970be9bb9
exl-id: aaa1a680-3733-43c3-9d14-5aaa5f4aad6e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 6%

---

# 새로운 벡터 레이어 사용 가능{#making-a-new-vector-layer-available}

{{eol}}

지구 시각화에 표시할 벡터 레이어를 사용할 수 있도록 하는 절차.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*profile name*\Map 폴더에 레이어 파일과 [!DNL .vec] 또는 [!DNL .tsv] 파일.
1. 편집 [!DNL order.txt] 파일을 Profiles\*profile name*\Map 폴더에 매핑하여 레이어를 표시할 순서를 반영합니다. 기본적으로 레이어는 해당 이름으로 사전식 순서로 표시됩니다.

   >[!NOTE]
   >
   >편집 시 [!DNL order.txt] 파일에서 표시하려는 맵 레이어를 표시하지 않도록 주의하십시오.

   사용에 대한 자세한 정보 [!DNL order.txt] 파일의 경우 *Data Workbench 사용 안내서*.

1. Data Workbench에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 을 클릭하여 원하는 프로필을 선택합니다 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*.
1. 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]**. 옆에 X가 나타납니다 [!DNL Work Online].
1. 작업 공간을 열고 지구 시각화에서 마우스 오른쪽 단추를 클릭하고 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
