---
description: 변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.
solution: Insight
title: 변형 구성
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 변형 구성{#configuring-transform}

변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.

[!DNL Transform] 파일, 로그 파일, XML 파일 및 ODBC 데이터를 읽고 데이터 웨어하우스 로딩 루틴, 감사 기관 또는 기타 대상에 사용할 수 있는 파일, 텍스트 파일 또는 구분된 텍스트 파일로 데이터를 내보낼 수 있습니다. [!DNL .vsl] [!DNL .vsl] 데이터 추출 및 변환은 연속 또는 다른 예약된 기준으로 수행할 수 있습니다. 변경된 [!DNL Insight Server] 이벤트 데이터의 출력을 제공하는 각 FSU는 실행해야 합니다 [!DNL Transform].

>[!NOTE]
>
>일반적으로 FSU에 [!DNL Transform] 설치됩니다 [!DNL Insight Server] . 그러나 구현에 DPU를 설치해야 할 수 [!DNL Insight Server] 있습니다. 자세한 내용은 Adobe에 문의하십시오.

설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 [!DNL Transform]내용은 최소 시스템 요구 *사항 문서를 참조하십시오* .

Adobe는 이 [!DNL Transform] 기능을 릴리스 패키지의 [!DNL .zip] 파일 내에 프로파일로 배포합니다 [!DNL Insight Server] . 이 [!DNL Transform] 프로필은 추가 기능을 제공하는 내부 프로필입니다 [!DNL Insight Server]. Adobe에서 제공한 다른 모든 내부 프로필과 마찬가지로 프로필을 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

프로필은 다음 파일로 구성됩니다.

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* 로그 처리 데이터 세트에 파일 포함

이러한 파일은 모두 프로필의 [!DNL Dataset] 폴더에 있습니다.

**프로필을 설치하려면[!DNL Transform][!DNL Insight Server]**

>[!NOTE]
>
>다음 설치 지침은 설치 중인 버전과 설치 중인 제품 사이의 연결을 설치 [!DNL Insight] 및 설정한 [!DNL Insight] [!DNL Insight Server] [!DNL Transform]것으로 가정합니다. 아직 설치하지 않은 경우 * 사용 [!DNL Insight] 안내서*를 참조하십시오.

1. 릴리스 패키지의 [!DNL .zip] 파일을 열고 해당 [!DNL Insight Server] 파일 내의 [!DNL Profiles] [!DNL .zip] 폴더를 엽니다.
1. 폴더를 [!DNL Transform] 설치 디렉토리의 [!DNL Profiles] [!DNL Insight Server] 폴더에 복사합니다. 다음 예와 같이 [!DNL ...\Profiles\Transform] 폴더가 [!DNL Insight Server] 표시됩니다.

   ![단계 정보](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >설치를 위한 모든 단계를 수행한 [!DNL Insight Server] (Insight [Server 참조](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)) 경우 이미 프로필 [!DNL Transform] 디렉토리에 폴더가 있을 수 있습니다.

1. 다음 단계에 따라 사용할 프로필의 [!DNL profile.cfg] 파일을 업데이트합니다 [!DNL Transform]. 데이터 세트는 이러한 단계를 완료하면 재처리됩니다.

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 [!DNL profile.cfg] 클릭하고 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. 창이 [!DNL profile.cfg] 나타납니다.

   1. 창에서 [!DNL profile.cfg]마우스 오른쪽 단추를 **[!UICONTROL Directories]** 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

      디렉토리 목록 끝에 새 디렉토리를 추가하려면 목록에서 마지막 디렉토리의 번호나 이름을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**&#x200B;를 클릭합니다.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL Transform]
   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]열의 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 [!DNL profile.cfg] > [!DNL User] &lt; **[!UICONTROL Save to]** > *을 클릭합니다&#x200B;**[!UICONTROL profile name]***.

      >[!NOTE]
      >
      >이러한 프로파일에 대한 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로 수정된 구성 파일을 Adobe가 제공한 내부 프로필(프로필 포함)에 저장하지 마십시오.
