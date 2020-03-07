---
description: 데이터 워크벤치 6.2 및 6.2.2용 서버 구성 요소를 업그레이드합니다.
title: DWB Server 업그레이드 6.1 - 6.2
uuid: 61ecf2c1-9ced-42d3-a010-4a4fec13b987
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# DWB Server 업그레이드:6.1 - 6.2{#dwb-server-upgrade-to}

데이터 워크벤치 6.2 및 6.2.2용 서버 구성 요소를 업그레이드합니다.

## 6.2에 대한 업그레이드 문제 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* 속성 프로필은 Analytics(SC/Insight) 데이터 피드를 사용하도록 Adobe SC 프로필을 구현한 사용자에 대해 구성됩니다. 기본적으로 마케팅 및 전환 이벤트는 규칙 기반 모델에서 평가된 기본 상호 작용으로 사용됩니다. 자세한 [내용은 속성](https://docs.adobe.com/help/en/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html) 프로필 배포를 참조하십시오.
* Data Workbench 6.2로 업그레이드하는 Adobe SC 프로필의 사용자에 대해 기본 구성을 사용하고 있지 않은 경우 파일의 [!DNL x-bot_id] 값이 [!DNL SC Fields.cfg] 제대로 디코딩되고 있으며 필드가 [!DNL x-bot_id] 및 [!DNL Decoding Instructions.cfg] [!DNL Exclude Hit.cfg] 파일에 제대로 나열되는지 확인하십시오. 이 문제는 기본 구성에서 구성 파일을 수정한 경우에만 발생합니다.
* Adobe SC 프로필에 대한 [!DNL Dataset > Log Processing > SC Fields.cfg] 파일에서 사용되지 않은 필드를 삭제한 경우 속성 프로필에 사용되는 업데이트된 필드 값을 수용하도록 업데이트해야 [합니다(속성 프로필 배포 참조](https://docs.adobe.com/help/en/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html)).

## 6.2.2에 대한 업그레이드 문제 {#section-8704a9ac358246cd81233dd0982d534f}

* 및 **[!UICONTROL Browsers]** 조회 파일은 기존 **[!UICONTROL Operating Systems]** 프로필 내에서 업데이트되지 않습니다(예: **[!UICONTROL Traffic]** [!DNL Lookups\Traffic\Browsers.txt)]). Instead, configuration of the **[!UICONTROL Traffic]** profile will utilize the DeviceAtlas bundle ( [!DNL Lookups\DeviceAtlas\DeviceAtlas.bundle]) to provide this configuration information.
* 데이터 워크벤치 6.2.1은 32비트 클라이언트 애플리케이션 다운로드를 제공하는 마지막 릴리스 버전입니다. 향후 모든 클라이언트 애플리케이션 다운로드는 64비트로 이루어지며 Windows 7 이후 버전이 요구됩니다. 32비트 애플리케이션의 메모리 제한은 6.1 릴리스에서 시작되는 64비트 애플리케이션의 도입으로 해결됩니다.

>[!NOTE]
>
>데이터 워크벤치 클라이언트 애플리케이션의 32비트 버전은 클러스터링 및 점수 지정 기능을 사용하여 예측 모델을 실행할 때 메모리 제한과 관련된 잠재적 문제를 경험할 수 있습니다.

