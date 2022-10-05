---
description: 최종 단계는 대시보드를 초기화하도록 처음으로 실행하는 것입니다.
title: 대시보드 초기화
uuid: 847ba63e-29d8-4950-aa74-22d825388e2b
exl-id: 47098d73-d8c4-4d14-964f-108a731d3733
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 4%

---

# 대시보드 초기화{#initializing-the-dashboard}

{{eol}}

최종 단계는 대시보드를 초기화하도록 처음으로 실행하는 것입니다.

1. 웹 브라우저를 열고 새로 배포된 사이트의 URL(예: https://localhost/dashboard)을 입력합니다.
1. 처음으로 연결하면 데이터베이스 테이블이 설정되므로 약간 지연될 수 있습니다.
1. 초기 로그온 자격 증명은 다음과 같습니다.

   * **[!UICONTROL Username]**: 관리
   * **[!UICONTROL Password]**: password

1. 첫 번째 로그인에서 **[!UICONTROL User]** > **[!UICONTROL Account Settings]** 을(를) 선택합니다. **[!UICONTROL Change Password]** 관리자 암호를 변경하려면

이제 대시보드 설치가 완료되었습니다. 아직 없다면 이 안내서의 Data Workbench 준비 섹션에 설명된 지침을 사용하여 Data Workbench 서버와의 통신을 구성하고 사용자 및 그룹을 관리합니다.

>[!NOTE]
>
>대시보드 오류 및 감사 로그는 [!DNL logs] 디렉토리 내의 설치 경로.

>[!NOTE]
>
>응용 프로그램 풀 ID를 다른 계정으로 변경해야 하는 경우 데이터베이스에 대한 액세스 권한을 부여하고 ID에 대한 읽기/쓰기 액세스 권한을 제공해야 합니다 [!DNL logs] 폴더(설치 경로)

>[!NOTE]
>
>데이터베이스의 연결 문자열을 변경해야 하는 경우 **[!UICONTROL IIS Management Console]**.
