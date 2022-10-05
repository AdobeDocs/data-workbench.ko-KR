---
description: 변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.
title: 변형 구성
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
exl-id: 5dbd70e4-55fc-4446-b687-525e7957209b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 1%

---

# 변형 구성{#configuring-transform}

{{eol}}

변환 기능은 Insight Server FSU 시스템에서 실행되어 다른 애플리케이션에서 사용할 로그 소스 데이터를 내보낼 수 있습니다.

[!DNL Transform] 읽을 수 있음 [!DNL .vsl] 파일, 로그 파일, XML 파일 및 ODBC 데이터를 파일로 내보내고 [!DNL .vsl] 데이터 웨어하우스 로드 루틴, 감사 기관 또는 기타 대상에서 사용할 수 있는 파일, 텍스트 파일 또는 구분된 텍스트 파일입니다. 데이터 추출 및 변환은 연속 또는 기타 스케줄링된 기반으로 수행할 수 있다. 각 [!DNL Insight Server] 변경된 이벤트 데이터의 출력을 제공하는 FSU는 실행해야 합니다 [!DNL Transform].

>[!NOTE]
>
>일반적으로 [!DNL Transform] 이(가) [!DNL Insight Server] FSU. 그러나 구현에 를 설치해야 할 수 있습니다 [!DNL Insight Server] DPU. 자세한 내용은 Adobe에게 문의하십시오.

설치, 구성 및 운영을 위한 시스템 요구 사항에 대한 자세한 정보 [!DNL Transform]를 참조하고 *최소 시스템 요구 사항* 문서.

Adobe이 배포 [!DNL Transform] 내에서 프로필로 사용할 수 있는 기능 [!DNL .zip] 파일 [!DNL Insight Server] 릴리스 패키지. 다음 [!DNL Transform] 프로필은 추가적인 기능을 제공하는 내부 프로필입니다 [!DNL Insight Server]. Adobe이 제공하는 다른 모든 내부 프로필과 마찬가지로 프로필을 변경하면 안 됩니다. 모든 사용자 지정은 데이터 세트 또는 역할별 프로필 또는 사용자가 만드는 기타 프로필에서 수행해야 합니다.

프로필은 다음 파일로 구성됩니다.

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* 로그 처리 데이터 집합에 파일 포함

이러한 모든 파일은 [!DNL Dataset] 폴더에 배치합니다.

**를 설치하려면 [!DNL Transform] 프로파일[!DNL Insight Server]**

>[!NOTE]
>
>다음 설치 지침은 설치 사실을 가정합니다 [!DNL Insight] 연결 설정 [!DNL Insight] 그리고 [!DNL Insight Server] 설치 대상 [!DNL Transform]. 아직 수행하지 않았다면 *를 참조하십시오. [!DNL Insight] 사용 안내서*.

1. 를 엽니다. [!DNL .zip] 파일 [!DNL Insight Server] 릴리스 패키지를 열고 [!DNL Profiles] 해당 내의 폴더 [!DNL .zip] 파일.
1. 를 복사합니다. [!DNL Transform] 폴더 [!DNL Profiles] 폴더의 [!DNL Insight Server] 설치 디렉토리. 이제 다음을 통해 [!DNL ...\Profiles\Transform] 폴더의 [!DNL Insight Server] 다음 예와 같이,

   ![단계 정보](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >설치 단계를 모두 수행한 경우 [!DNL Insight Server] 자세한 내용은 [Insight Server](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)), 이미 [!DNL Transform] Profiles 디렉토리의 폴더에 있습니다.

1. 다음 단계를 사용하여 를 업데이트합니다 [!DNL profile.cfg] 사용할 프로필의 파일입니다. [!DNL Transform]. 데이터 세트는 이러한 단계를 완료하면 재처리됩니다.

   1.  [!DNL Profile Manager].
   1. 옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

   1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. 다음 [!DNL profile.cfg] 창이 나타납니다.

   1. 에서 [!DNL profile.cfg]창, 마우스 오른쪽 단추 클릭 **[!UICONTROL Directories]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      디렉터리 목록에 새 디렉터리를 추가하려면 목록에서 마지막 디렉터리의 번호나 이름을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. 새 디렉토리의 이름을 입력합니다. [!DNL Transform]
   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 [!DNL Profile Manager]에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 에서 [!DNL User] 열을 누른 다음 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >이러한 프로필에 업데이트를 설치할 때 변경 사항을 덮어쓰게 되므로, 수정된 구성 파일을 Adobe이 제공한 내부 프로필(프로필 포함)에 저장하지 마십시오.
