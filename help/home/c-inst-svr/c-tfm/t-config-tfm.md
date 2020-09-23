---
description: 변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.
solution: Analytics
title: 변형 구성
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---


# 변형 구성{#configuring-transform}

변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.

[!DNL Transform] 파일, 로그 파일, XML 파일 및 ODBC 데이터를 읽고 데이터 웨어하우스 로딩 루틴, 감사 기관 또는 기타 대상에 사용할 수 있는 파일, 텍스트 파일 또는 구분된 텍스트 파일 [!DNL .vsl] [!DNL .vsl] 로 데이터를 내보낼 수 있습니다. 데이터 추출 및 변환은 연속 또는 기타 예약된 기준으로 수행할 수 있습니다. 변경된 이벤트 데이터의 출력을 제공하는 각 [!DNL Insight Server] FSU는 실행해야 합니다 [!DNL Transform].

>[!NOTE]
>
>일반적으로 FSU [!DNL Transform] 에 [!DNL Insight Server] 설치됩니다. 그러나 구현에 DPU를 설치해야 할 수 [!DNL Insight Server] 있습니다. 자세한 내용은 Adobe에 문의하십시오.

설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 내용 [!DNL Transform]은 *최소 시스템 요구 사항* 문서를 참조하십시오.

Adobe은 릴리스 패키지의 파일 내 [!DNL Transform] 프로필 [!DNL .zip] [!DNL Insight Server] 으로 기능을 배포합니다. 프로파일은 [!DNL Transform] 추가적인 기능을 제공하는 내부 프로필입니다 [!DNL Insight Server]. Adobe에서 제공하는 기타 모든 내부 프로필과 마찬가지로 프로필을 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 이루어져야 합니다.

프로필은 다음 파일로 구성됩니다.

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* 로그 처리 데이터 세트에 파일 포함

이러한 파일은 모두 프로필의 [!DNL Dataset] 폴더에 있습니다.

**프로필을 설치하려면[!DNL Transform][!DNL Insight Server]**

>[!NOTE]
>
>다음 설치 지침에서는 설치 중인 사용자와 설치 중인 사용자 간 [!DNL Insight] 의 연결 [!DNL Insight] 을 설치하고 설정했다고 가정합니다 [!DNL Insight Server] [!DNL Transform]. 아직 설치하지 않은 경우 * [!DNL Insight] 사용 안내서*를 참조하십시오.

1. 릴리스 패키지의 [!DNL .zip] 파일을 열고 해당 [!DNL Insight Server] 파일 [!DNL Profiles] [!DNL .zip] 내의 폴더를 엽니다.
1. 설치 디렉토리 [!DNL Transform] 의 [!DNL Profiles] 폴더에 [!DNL Insight Server] 폴더를 복사합니다. 다음 예제와 같이 [!DNL ...\Profiles\Transform] 폴더가 사용자 [!DNL Insight Server] 에 있는 것으로 끝납니다.

   ![단계 정보](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >설치 단계를 모두 수행한 경우 [!DNL Insight Server] (Insight [Server](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)참조) 프로필 디렉토리에 [!DNL Transform] 폴더가 이미 있을 수 있습니다.

1. 다음 단계에 따라 사용할 프로필의 [!DNL profile.cfg] 파일을 업데이트하십시오 [!DNL Transform]. 데이터 세트는 이러한 단계를 완료하면 재처리됩니다.

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL profile.cfg] 을 클릭합니다 **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 열에 [!DNL User] 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > 를 클릭합니다 **[!UICONTROL in Insight]**. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창 [!DNL profile.cfg]에서 마우스 오른쪽 단추를 클릭하고 > **[!UICONTROL Directories]** 를 **[!UICONTROL Add new]** 클릭합니다 **[!UICONTROL Directory]**.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > 를 클릭합니다 **[!UICONTROL Directory]**.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL Transform]
   1. 창 위쪽 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 열 [!DNL Profile Manager]에 있는 확인 표시 [!DNL profile.cfg] 를 마우스 오른쪽 단추로 클릭한 다음 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL profile name]**를 클릭합니다*.

      >[!NOTE]
      >
      >이러한 프로필에 대한 업데이트를 설치할 때 변경 사항을 덮어쓸 경우 수정된 구성 파일을 Adobe(프로필 포함)에서 제공하는 내부 프로필에 저장하지 마십시오.

