---
description: 전역 시각화에 표시할 수 있는 벡터 레이어를 만드는 단계입니다.
title: 새로운 벡터 레이어 사용 가능
uuid: 7bfbae0d-e5db-4aa2-8a8b-15b4980aadb5
exl-id: 6c084bac-1a6d-452a-bf07-e502d0f2145a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# 새로운 벡터 레이어 사용 가능{#make-a-new-vector-layer-available}

전역 시각화에 표시할 수 있는 벡터 레이어를 만드는 단계입니다.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*profile name*\Maps 폴더에 레이어 파일과 [!DNL .vec] 또는 [!DNL .tsv] 파일을 배치합니다.
1. Profiles\*profile name*\Map 폴더에서 [!DNL order.txt] 파일을 편집하여 레이어를 표시할 순서를 반영합니다. 기본적으로 레이어는 해당 이름으로 사전식 순서로 표시됩니다.

   >[!NOTE]
   >
   >[!DNL order.txt] 파일을 편집할 때는 표시하려는 맵 레이어를 표시하지 않도록 주의하십시오.

   [!DNL order.txt] 파일 사용에 대한 자세한 내용은 [Order.txt 파일을 사용하여 메뉴 사용자 정의](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999)를 참조하십시오.

1. Insight에서 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]*** 를 클릭하여 원하는 프로필을 선택합니다.
1. 작업 공간 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]** 을 클릭합니다. Work Online 옆에 X가 나타납니다.
1. 작업 공간을 열고 지구 시각화에서 마우스 오른쪽 단추를 클릭하고 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
