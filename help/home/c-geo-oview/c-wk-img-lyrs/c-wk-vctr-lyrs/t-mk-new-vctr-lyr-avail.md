---
description: 지구 시각화에 표시할 벡터 레이어를 만드는 단계입니다.
title: 새로운 벡터 레이어 사용 가능
uuid: 7e88f183-b0aa-452d-b124-7cd970be9bb9
exl-id: aaa1a680-3733-43c3-9d14-5aaa5f4aad6e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 6%

---

# 새로운 벡터 레이어 사용 가능{#making-a-new-vector-layer-available}

지구 시각화에 표시할 벡터 레이어를 만드는 단계입니다.

1. 데이터 워크벤치 서버 설치 디렉토리 내의 Profiles\*profile name*\Maps 폴더에 레이어 파일과 [!DNL .vec] 또는 [!DNL .tsv] 파일을 배치합니다.
1. 레이어를 표시할 순서를 반영하도록 Profiles\*profile name*\Maps 폴더의 [!DNL order.txt] 파일을 편집합니다. 기본적으로 레이어는 이름별로 어휘의 순서로 표시됩니다.

   >[!NOTE]
   >
   >[!DNL order.txt] 파일을 편집할 때는 표시하려는 맵 레이어를 덮지 않도록 주의하십시오.

   [!DNL order.txt] 파일 사용에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

1. 데이터 워크벤치에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭하여 원하는 프로필을 선택합니다.
1. 작업 영역 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]**&#x200B;을 클릭합니다. [!DNL Work Online] 옆에 X가 나타납니다.
1. 작업 영역을 열고 글로벌 시각화에서 마우스 오른쪽 버튼을 클릭하여 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
