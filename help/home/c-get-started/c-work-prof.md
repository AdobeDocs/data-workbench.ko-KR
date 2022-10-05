---
description: Data Workbench은 프로필을 컴퓨터에 다운로드합니다.
title: 프로필
uuid: 8ea36138-9839-40e5-89e2-4b120f1dd7aa
exl-id: a140f549-448c-4e34-8eae-ad154fa01f1f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 프로필{#profiles}

{{eol}}

Data Workbench은 프로필을 컴퓨터에 다운로드합니다.

처음으로 프로필을 로드하는 경우 네트워크에 연결해야 합니다 [!DNL Data Workbench server] Data Workbench이 [!DNL Data Workbench server].

프로필을 다운로드하는 데 몇 분 정도 걸릴 수 있습니다. 데이터 캐시 채우기가 시작될 때까지 프로필 작업을 시작하지 않아야 하지만 프로필이 가득 찰 때까지 기다리지 않아도 됩니다. 프로필 로드 시 상태 표시줄을 보고 데이터 캐시의 진행 상태, 프로필 동기화 진행 상태, 가장 최근에 처리된 데이터의 날짜 및 시간을 추적할 수 있습니다.

>[!NOTE]
>
>데이터 캐시가 채워지기 시작할 때까지 추가하는 데이터가 시각화에 표시되지 않습니다.

다음에 프로필을 로드할 때, 프로필에 네트워크로 연결된 경우에만 프로필 및 해당 데이터가 다운로드됩니다 [!DNL Data Workbench server] 그리고 온라인으로 작업 중입니다. 오프라인으로 작업하는 경우 프로필과 해당 데이터가 컴퓨터의 캐시에서 로드됩니다. 이 경우, 프로필과 함께 마지막으로 온라인으로 작업했을 때 다운로드한 프로필의 버전과 데이터를 보고 있습니다. 온라인 및 오프라인 작업에 대한 자세한 내용은 [오프라인 및 온라인 작업](../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

프로필을 변경해야 하는 경우( [!DNL Profile Manager] 또는 [!DNL Server Files Manager])에서 온라인으로 작업하여 최신 버전의 프로필을 사용해야 합니다. 에 대한 자세한 정보 [!DNL Profile Manager] 그리고 [!DNL Server Files Manager]를 참조하십시오. [관리 인터페이스](../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).

프로필에 액세스하거나 로드할 수 없는 경우 다음을 확인해야 할 수 있습니다.

* 에 네트워크 연결이 있습니다. [!DNL Data Workbench server] 프로필이 상주하는 시스템입니다.
* 프로필에 액세스할 수 있는 적절한 권한이 있습니다.

도움이 필요하면 시스템 관리자에게 문의하십시오.

## 프로필 로드 또는 전환 {#section-c50499d7d8084d7cadfada52df33f5f4}

1. Data Workbench 시작.
1. 측면 막대에서 프로필 이름을 클릭하고 를 클릭합니다 **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*, 위치 *프로필 이름* 은 작업할 프로필입니다.

   ![](assets/sidebar_profile.png)

선택한 프로필을 처음 로드하는 경우 시각화를 채우기에 충분한 데이터를 다운로드하는 데 몇 분이 걸릴 수 있습니다.

## 클러스터의 프로필 액세스 {#section-189a0ac04a8f46099c11c0f4f77b6dbb}

에서 실행 중인 프로필에 액세스하는 Data Workbench 사용자

data workbench 서버 클러스터는 Data Workbench 구성 파일( [!DNL Insight.cfg]). Data Workbench 사용자의 관점에서 프로파일은 하나의 Data Workbench 서버(마스터 Data Workbench 서버)에서만 액세스할 수 있습니다. 그러나 분석가의 쿼리 요청은 클러스터의 Data Workbench 서버로 전달될 수 있습니다.

Data Workbench 서버 클러스터에서 실행 중인 프로필에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*.
