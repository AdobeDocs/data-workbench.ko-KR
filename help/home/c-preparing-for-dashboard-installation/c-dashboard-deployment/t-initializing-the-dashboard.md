---
description: 마지막 단계는 대시보드를 처음으로 실행하여 초기화하도록 하는 것입니다.
title: 대시보드 초기화
uuid: 847ba63e-29d8-4950-aa74-22d825388e2b
exl-id: 47098d73-d8c4-4d14-964f-108a731d3733
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 4%

---

# 대시보드 초기화{#initializing-the-dashboard}

마지막 단계는 대시보드를 처음으로 실행하여 초기화하도록 하는 것입니다.

1. 웹 브라우저를 열고 새로 배포된 사이트의 URL(예: http://localhost/dashboard)을 입력합니다.
1. 처음으로 연결하면 데이터베이스 테이블이 설정되므로 약간 지연될 수 있습니다.
1. 초기 로그온 자격 증명은 다음과 같습니다.

   * **[!UICONTROL Username]**: 관리
   * **[!UICONTROL Password]**: password

1. 첫 번째 로그인에서 **[!UICONTROL User]** > **[!UICONTROL Account Settings]**&#x200B;으로 이동하여 **[!UICONTROL Change Password]**&#x200B;를 선택하여 관리자 암호를 변경합니다.

이제 대시보드 설치가 완료되었습니다. 아직 없는 경우 이 안내서의 Data Workbench 준비 섹션에 설명된 지침에 따라 데이터 워크벤치 서버와의 통신을 구성하고 사용자 및 그룹을 관리합니다.

>[!NOTE]
>
>대시보드 오류 및 감사 로그는 설치 경로 내의 [!DNL logs] 디렉토리에 있습니다.

>[!NOTE]
>
>응용 프로그램 풀 ID를 다른 계정으로 변경해야 하는 경우 데이터베이스에 대한 액세스 권한을 부여하고 설치 경로의 [!DNL logs] 폴더에 ID 읽기/쓰기 액세스 권한을 부여해야 합니다.

>[!NOTE]
>
>데이터베이스의 연결 문자열을 변경해야 하는 경우 **[!UICONTROL IIS Management Console]**&#x200B;을 사용하여 값을 편집하기만 하면 됩니다.
