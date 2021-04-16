---
description: 전역 시각화에 모든 요소 포인트 레이어를 표시할 수 있도록 하는 단계입니다.
title: 새로운 요소 점 레이어 사용 가능
uuid: 5f4bad2f-e98d-4224-bba8-285ad5e23da9
exl-id: 12797335-0788-4103-a581-41bc3bb3dcc9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 6%

---

# 새로운 요소 점 레이어 사용 가능{#make-a-new-element-point-layer-available}

전역 시각화에 모든 요소 포인트 레이어를 표시할 수 있도록 하는 단계입니다.

1. Data Workbench 서버 설치 디렉토리 내의 Profiles\*profile name*\Maps 폴더에 레이어 파일과 관련 조회 파일을 배치합니다.
1. 요소 포인트 레이어의 새 차원을 정의했지만 아직 데이터 세트를 다시 변형하지 않은 경우 지금 데이터 세트를 다시 변형하십시오.
1. 레이어를 표시할 순서를 반영하도록 Profiles\*profile name*\Maps 폴더의 [!DNL order.txt] 파일을 편집합니다. 기본적으로 레이어는 이름별로 어휘의 순서로 표시됩니다.

   >[!NOTE]
   >
   >[!DNL order.txt] 파일을 편집할 때는 표시하려는 맵 레이어를 덮지 않도록 주의하십시오.

   [!DNL order.txt] 파일 사용에 대한 자세한 내용은 *Data Workbench 사용자 안내서*&#x200B;의 인터페이스 및 분석 기능 구성 장을 참조하십시오.

1. Data Workbench에서 작업 영역 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭하여 원하는 프로필을 선택합니다.
1. 작업 영역 제목 표시줄을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Work Online]**&#x200B;을 클릭합니다. Work Online 옆에 X가 나타납니다.
1. 작업 영역을 열고 글로벌 시각화에서 마우스 오른쪽 버튼을 클릭하여 새 레이어를 선택합니다. 레이어 이름 옆에 X가 나타납니다.
