---
description: 변환 기능은 Insight Server FSU 시스템에서 실행되므로 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.
title: 변형 구성
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
exl-id: 5dbd70e4-55fc-4446-b687-525e7957209b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---

# 변형 구성{#configuring-transform}

변환 기능은 Insight Server FSU 시스템에서 실행되므로 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.

[!DNL Transform] 파일,  [!DNL .vsl] 로그 파일, XML 파일 및 ODBC 데이터를 읽고 데이터 웨어하우스 로딩 루틴, 감사 기관 또는 기타 대상에 사용할 수 있는  [!DNL .vsl] 파일, 텍스트 파일 또는 구분된 텍스트 파일로 데이터를 내보낼 수 있습니다. 데이터 추출 및 변환은 연속 또는 기타 예약된 기준으로 수행할 수 있습니다. 변경된 이벤트 데이터의 출력을 제공하는 각 [!DNL Insight Server] FSU는 [!DNL Transform]을(를) 실행해야 합니다.

>[!NOTE]
>
>일반적으로 [!DNL Transform]은 [!DNL Insight Server] FSU에 설치됩니다. 그러나 구현에 [!DNL Insight Server] DPU를 설치해야 할 수 있습니다. 자세한 내용은 Adobe에 문의하십시오.

[!DNL Transform] 설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 내용은 *최소 시스템 요구 사항* 문서를 참조하십시오.

Adobe은 [!DNL Insight Server] 릴리스 패키지에 대해 [!DNL .zip] 파일 내의 프로필로 [!DNL Transform] 기능을 배포합니다. [!DNL Transform] 프로필은 [!DNL Insight Server]에 추가 기능을 제공하는 내부 프로필입니다. Adobe에서 제공하는 다른 모든 내부 프로필과 마찬가지로 프로필을 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

프로필은 다음 파일로 구성됩니다.

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] 변형 모드.cfg]
* 로그 처리 데이터 세트에 파일이 포함됩니다.

이러한 모든 파일은 프로필의 [!DNL Dataset] 폴더에 있습니다.

**프로필을  [!DNL Transform] 설치하려면[!DNL Insight Server]**

>[!NOTE]
>
>다음 설치 지침은 [!DNL Insight]을(를) 설치하고 [!DNL Insight]과 [!DNL Transform]을(를) 설치하는 [!DNL Insight Server] 사이에 연결을 설정했다고 가정합니다. 아직 설치하지 않은 경우 * [!DNL Insight] 사용 안내서*를 참조하십시오.

1. [!DNL Insight Server] 릴리스 패키지의 [!DNL .zip] 파일을 열고 해당 [!DNL .zip] 파일 내에서 [!DNL Profiles] 폴더를 엽니다.
1. [!DNL Transform] 폴더를 [!DNL Insight Server] 설치 디렉토리의 [!DNL Profiles] 폴더에 복사합니다. 다음 예제와 같이 [!DNL Insight Server]에 [!DNL ...\Profiles\Transform] 폴더로 끝내려는 것입니다.

   ![단계 정보](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >[!DNL Insight Server] 설치([Insight Server](../../../home/c-inst-svr/c-msr-server/c-msr-server.md) 참조)를 위한 모든 단계를 수행한 경우 이미 프로필 디렉토리에 [!DNL Transform] 폴더가 있을 수 있습니다.

1. 다음 단계를 사용하여 [!DNL Transform]을(를) 사용할 프로필의 [!DNL profile.cfg] 파일을 업데이트합니다. 데이터 세트는 이러한 단계를 완료하면 재처리됩니다.

   1.  [!DNL Profile Manager].
   1. [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 을 클릭합니다. 이 파일의 확인 표시는 [!DNL User] 열에 표시됩니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. [!DNL profile.cfg] 창이 나타납니다.

   1. [!DNL profile.cfg]창에서 **[!UICONTROL Directories]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;을 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다.[!DNL Transform]
   1. 창 위쪽에 있는 **[!UICONTROL (modified)]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]**&#x200B;을 클릭합니다.

   1. [!DNL Profile Manager]에서 [!DNL User] 열의 [!DNL profile.cfg]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]***&#x200B;을 클릭합니다.

      >[!NOTE]
      >
      >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰면 Adobe(프로파일 포함)에서 제공하는 내부 프로파일에 수정된 구성 파일을 저장하지 마십시오.
