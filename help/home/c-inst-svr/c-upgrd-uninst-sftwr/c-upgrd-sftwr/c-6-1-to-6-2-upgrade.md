---
description: Data Workbench 6.2 및 6.2.2용 서버 구성 요소 업그레이드
title: DWB 서버 업그레이드 6.1에서 6.2로
uuid: 61ecf2c1-9ced-42d3-a010-4a4fec13b987
exl-id: 094b20f0-bc4a-467a-899e-e1800a624508,20e2cf87-519e-4c27-9201-1275550bb72a
source-git-commit: 050468bf6a9ef9c07719ded79c8ab68753d58647
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 18%

---

# DWB 서버 업그레이드: 6.1에서 6.2로{#dwb-server-upgrade-to}

Data Workbench 6.2 및 6.2.2용 서버 구성 요소 업그레이드

## 6.2에 대한 업그레이드 문제 {#section-3cc74d08f7454d698b5a6d3f1dcde282}

* 속성 프로필은 Analytics(SC/Insight) 데이터 피드를 사용하도록 Adobe SC 프로필을 구현한 사용자에 대해 구성됩니다. 기본적으로 마케팅 및 전환 이벤트는 규칙 기반 모델에서 평가된 기본 상호 작용으로 사용됩니다. 자세한 내용은 [속성 프로필 배포](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en)를 참조하십시오.
* Data Workbench 6.2로 업그레이드하는 Adobe SC 프로필 사용자의 경우, 기본 구성을 사용하지 않는 경우 [!DNL SC Fields.cfg] 파일의 [!DNL x-bot_id] 값이 제대로 디코딩되고 [!DNL x-bot_id] 필드가 [!DNL Decoding Instructions.cfg] 및 [!DNL Exclude Hit.cfg] 파일에 올바르게 나열되는지 확인하십시오. 기본 구성에서 구성 파일을 수정한 경우에만 문제가 됩니다.
* Adobe SC 프로필에 대해 [!DNL Dataset > Log Processing > SC Fields.cfg] 파일에서 사용하지 않은 필드를 삭제한 경우 속성 프로필에 사용되는 업데이트된 필드 값을 수용하도록 업데이트해야 합니다( [속성 프로필 배포](https://experienceleague.adobe.com/docs/data-workbench/using/client/attribution-reports/c-attrib-profile-deploy.html?lang=en) 참조).

## 6.2.2에 대한 업그레이드 문제 {#section-8704a9ac358246cd81233dd0982d534f}

* **[!UICONTROL Browsers]** 및 **[!UICONTROL Operating Systems]** 조회 파일은 기존 **[!UICONTROL Traffic]** 프로필(예: [!DNL Lookups\Traffic\Browsers.txt)]) 내에서 업데이트되지 않습니다. 대신 **[!UICONTROL Traffic]** 프로필 구성은 DeviceAtlas 번들( [!DNL Lookups\DeviceAtlas\DeviceAtlas.bundle])을 사용하여 이 구성 정보를 제공합니다.
* 데이터 워크벤치 6.2.1은 32비트 클라이언트 애플리케이션 다운로드를 제공하는 마지막 릴리스 버전입니다. 향후 모든 클라이언트 애플리케이션 다운로드는 64비트로 이루어지며 Windows 7 이후 버전이 요구됩니다. 32비트 애플리케이션의 메모리 제한은 6.1 릴리스에서 시작되는 64비트 애플리케이션의 도입으로 해결됩니다.

>[!NOTE]
>
>32비트 버전의 Data Workbench 클라이언트 응용 프로그램은 클러스터링 및 점수 부여 기능을 사용하여 예측 모델을 실행할 때 메모리 제한 사항과 관련된 잠재적인 문제를 경험할 수 있습니다.
