---
description: Data Workbench는 사용자 컴퓨터에 프로필을 다운로드합니다.
title: 프로필
uuid: 8ea36138-9839-40e5-89e2-4b120f1dd7aa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Profiles{#profiles}

Data Workbench는 사용자 컴퓨터에 프로필을 다운로드합니다.

처음으로 프로파일을 로드하는 경우 Data Workbench가 Data Workbench에서 필요한 파일을 다운로드할 수 있도록 네트워크에 연결되어 [!DNL Data Workbench server] 있고 온라인으로 작업해야 합니다 [!DNL Data Workbench server].

프로필을 다운로드하는 데 몇 분 정도 걸릴 수 있습니다. 데이터 캐시가 채워지기 시작할 때까지 프로필 작업을 시작해서는 안 되지만, 완료될 때까지 기다릴 필요가 없습니다. 프로파일이 로드될 때 상태 표시줄을 확인하여 데이터 캐시의 진행 상황, 프로필 동기화 진행 상황, 가장 최근에 처리된 데이터의 날짜 및 시간을 추적할 수 있습니다.

>[!NOTE]
>
>데이터 캐시가 채워지기 시작할 때까지 추가하는 데이터는 시각화에 표시되지 않습니다.

다음에 프로필을 로드할 때, 프로필과 해당 데이터가 네트워크에 연결되어 있고 온라인으로 작업하는 경우에만 [!DNL Data Workbench server] 업데이트됩니다. 오프라인으로 작업 중인 경우 프로필과 해당 데이터가 시스템의 캐시에서 로드됩니다. 이 경우 프로필의 버전과 마지막으로 프로필에서 온라인으로 작업할 때 다운로드된 데이터를 보고 있습니다. 온라인 및 오프라인 작업에 대한 자세한 내용은 오프라인 [및 온라인 작업을 참조하십시오](../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

또는 를 사용하여 프로파일을 변경해야 하는 경우 [!DNL Profile Manager] [!DNL Server Files Manager]온라인상에서 프로파일을 최신 버전으로 업데이트해야 합니다. 및 [!DNL Profile Manager] 기능에 대한 자세한 [!DNL Server Files Manager]내용은 관리 인터페이스를 [참조하십시오](../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).

프로파일에 액세스하거나 로드할 수 없는 경우 다음을 확인해야 합니다.

* 프로파일이 있는 [!DNL Data Workbench server] 컴퓨터에 네트워크에 연결되어 있습니다.
* 프로필에 액세스할 수 있는 권한이 있습니다.

도움이 필요하면 시스템 관리자에게 문의하십시오.

## 프로파일 로드 또는 전환 {#section-c50499d7d8084d7cadfada52df33f5f4}

1. 데이터 워크벤치를 시작합니다.
1. 사이드 바에서 프로필 이름을 클릭하고 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;을 클릭합니다. 여기서 *프로필 이름은* 작업할 프로필입니다.

   ![](assets/sidebar_profile.png)

선택한 프로필을 처음 로드하는 경우 시각화를 채우는 데 충분한 데이터를 다운로드하는 데 몇 분이 걸릴 수 있습니다.

## 클러스터의 프로필 액세스 {#section-189a0ac04a8f46099c11c0f4f77b6dbb}

Data Workbench 사용자가

데이터 워크벤치 서버 클러스터는 데이터 워크벤치 구성 파일( [!DNL Insight.cfg])에서 마스터 데이터 워크벤치 서버만 식별합니다. 데이터 워크벤치 사용자의 관점에서 프로파일은 하나의 데이터 워크벤치 서버(마스터 데이터 워크벤치 서버)에서만 액세스할 수 있습니다. 그러나 분석가의 쿼리 요청은 클러스터의 데이터 워크벤치 서버로 연결될 수 있습니다.

데이터 워크벤치 서버 클러스터에서 실행되는 프로필에 대한 자세한 내용은 서버 제품 설치 *및 관리 안내서를 참조하십시오*.
