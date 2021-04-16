---
description: 작업 상자의 각 탭 또는 하위 탭은 대시보드, 활동, 획득 등과 같은 특정 유형의 정보에 해당합니다.
title: worktop 탭 사용자 정의
uuid: f1f557c8-f4cb-4789-8162-39cc7c52c943
exl-id: 529c6d8d-fc42-4c2b-a111-b8eea4665d8b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---

# worktop 탭 사용자 정의{#customize-a-worktop-tab}

작업 상자의 각 탭 또는 하위 탭은 대시보드, 활동, 획득 등과 같은 특정 유형의 정보에 해당합니다.

예를 들어 [!DNL Acquisition] 탭에는 참조 도메인, 검색 엔진 및 캠페인에 대한 데이터를 제공하는 작업 영역이 포함될 수 있습니다.

[!DNL Worktop]에 나타나는 각 탭은 Data Workbench 설치 디렉토리 내의 *작업 프로필 이름*\Workspaces 폴더의 폴더에 해당합니다. [!DNL Worktop]의 탭 순서는 동일한 폴더의 [!DNL order.txt] 파일에 의해 제어됩니다. 예를 들어 Workspaces 폴더에 Acquisition 하위 폴더가 있고 Acquisition을 [!DNL order.txt] 파일의 첫 번째 항목으로 추가하는 경우 [!DNL Acquisition]은 [!DNL Worktop]의 첫 번째 탭이고 해당 하위 폴더의 모든 항목은 [!DNL Acquisition] 탭에 표시됩니다.

>[!NOTE]
>
>[!DNL order.txt] 파일을 사용하여 작업 영역 창 메뉴 사용자 지정에 대한 자세한 내용은 [메뉴 사용자 지정](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/c-ctm-menus.md#concept-93d4c09cb7f34cd293b7b64fba1cf894)을 참조하십시오.
