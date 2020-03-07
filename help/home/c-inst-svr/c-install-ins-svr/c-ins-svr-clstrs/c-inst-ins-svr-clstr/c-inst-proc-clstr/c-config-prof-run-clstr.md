---
description: 데이터 집합 프로필을 Insight Server 클러스터에서 실행하도록 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 집합 구성 파일을 공유합니다.
solution: Insight
title: 클러스터에서 실행할 프로필 구성
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 클러스터에서 실행할 프로필 구성{#configuring-a-profile-to-run-on-a-cluster}

데이터 집합 프로필을 Insight Server 클러스터에서 실행하도록 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 집합 구성 파일을 공유합니다.

따라서 이러한 파일의 매개 변수 항목은 클러스터의 모든 [!DNL Insight Servers] 구성원에 적용되어야 합니다. 예를 들어 읽을 로그 파일의 위치, 에서 사용할 조회 파일 [!DNL Insight Server]및 데이터 출력 위치는 클러스터의 모든 컴퓨터에서 동일해야 [!DNL Insight Server] 합니다.

클러스터의 마스터에서 모든 구성 작업을 수행합니다. [!DNL Insight Server]이 작업은 구성 파일을 편집하는 데 [!DNL Insight Server] 사용합니다. 마스터에서 수행된 모든 저장된 구성 파일 변경 [!DNL Insight Server] [!DNL Insight Servers] 사항은 클러스터의 처리 중인 파일에 자동으로 동기화됩니다.

클러스터에서 데이터 집합 프로필을 실행하려면 나열된 순서대로 다음 프로세스를 수행해야 합니다. [!DNL Insight Server]

1. [이벤트 데이터를 처리하는 Insight 서버 확인](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [Profile.cfg에서 처리 서버 지정](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (필요한 경우) [프로필의 데이터 집합 구성 파일 수정](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)

## 이벤트 데이터를 처리하는 Insight 서버 확인 {#section-59b8e3f2b34f49739d544c8740a62fba}

클러스터의 모든 [!DNL Insight Servers] 프로세스에서 이벤트 데이터는 필요하지 않습니다. 클러스터의 소스 파일(VSL 및 로그 파일) [!DNL Insight Server] 을 저장하고 클러스터의 모든 데이터 처리 단위(처리 서버)에 파일을 제공하는 파일 서버 장치로 지정할 수 있습니다. 이 설정은 단일 이벤트 데이터 저장소의 이점을 제공하며 클러스터의 모든 처리 서버의 처리 능력을 활용합니다. 처리 서버는 데이터 파일을 데이터 파일로 나누어 동일한 파일이 두 번 이상 처리되지 않도록 합니다.

파일 서버 장치로 실행할 파일을 지정하는 방법에 대한 자세한 내용은 데이터 세트 구성 안내서의 로그 처리 구성 파일 [!DNL Insight Server] 장을 참조하십시오 **.

단일 파일 서버 단위가 아닌 각 처리 서버에 소스 데이터 파일을 저장하기로 결정한 경우 해당 파일을 처리 서버 간에 균등하게 분할해야 합니다. 모든 데이터 집합의 소스 파일을 각 처리 서버에 저장하지 마십시오. 동일한 파일의 여러 복사본을 여러 처리 서버에서 사용할 수 있는 경우, 데이터는 여러 번(각 컴퓨터마다 한 번) 읽고 데이터를 왜곡합니다.

로그 파일을 처리할 [!DNL Insight Servers] 항목을 결정하는 데 도움이 필요하면 Adobe Consulting에 문의하십시오.

## Profile.cfg에서 처리 서버 지정 {#section-99664e072c21462f91fbafb6d893fcf9}

파일에서 프로필의 데이터를 처리하는 처리 서버를 [!DNL profile.cfg] 지정합니다.

**profile.cfg 파일에 액세스하려면**

를 사용하여 프로필 구성 파일에 액세스할 [!DNL Profile Manager] 수 [!DNL Insight]있습니다.

1. 데이터 집합 프로필에서 작업하는 동안 작업 영역 내에서 마우스 오른쪽 단추를 [!DNL Profile Manager] 클릭하여 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]**&#x200B;를 클릭하거나 [!DNL Admin] 탭에서 프로필 관리 작업 영역을 열어 보십시오.

1. 에서 [!DNL Profile Manager]옆에 있는 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL profile.cfg] 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**&#x200B;를 클릭합니다. 프로필 구성 창이 나타납니다.

**처리 서버를 추가하려면**

1. 파일에서 아이콘을 클릭한 [!DNL profile.cfg] 다음 을 **[!UICONTROL Profile]****[!UICONTROL Processing Servers]** 클릭하여 내용을 표시합니다.

1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Processing Servers]** > **[!UICONTROL Add new]** **[!UICONTROL Processing Server]**&#x200B;를 클릭합니다.

1. Common Name 매개 변수에 클러스터의 첫 번째 처리 서버에 대한 공통 이름을 입력합니다. 예: [!DNL server1.mycompany.com]
1. 클러스터에 있는 모든 처리 서버의 공통 이름을 추가할 때까지 2단계와 3단계를 반복합니다.

   >[!NOTE]
   >
   >마스터가 데이터를 [!DNL Insight Server] 처리하는 경우 데이터를 추가해야 합니다.

1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

1. 옆에 있는 [!DNL User] 열에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다 [!DNL profile.cfg]. 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## 프로필에 대한 데이터 집합 구성 파일 수정 {#section-99bf9248e4e5483cb518f453b0a2f278}

**데이터 세트 구성 파일을 수정하려면**

데이터 세트 구성 파일( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], 데이터 세트에 파일 포함 [!DNL Log Processing Mode.cfg]등)을 변경해야 하는 경우 마스터에서만 [!DNL Insight Server]변경합니다.

1. 수정할 파일에 액세스:

   파일에 액세스하는 방법에 대한 지침은 데이터 세트 구성 *안내서를 참조하십시오*.
1. 변경 작업을 수행합니다. 구성 *파일 내의 매개 변수에* 대한 자세한 내용은 데이터 집합 구성 안내서를 참조하십시오.
1. 파일을 저장합니다.

   1. 창 **[!UICONTROL (modified)]** 상단에서 마우스 오른쪽 버튼을 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

   1. 파일 이름 옆의 [!DNL User] 열에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. 아이콘을 **[!UICONTROL Save to]** 클릭하고 원하는 프로파일을 선택합니다.

>[!NOTE]
>
>[!DNL Insight] 클러스터에서 실행 중인 데이터 집합 프로필에 액세스하는 사용자는 [!DNL Insight Server] 구성 파일( [!DNL Insight] [!DNL insight.cfg])의 마스터만 식별합니다. 사용자의 관점에서 [!DNL Insight] 프로파일은 하나의 [!DNL Insight Server] (마스터 [!DNL Insight Server])에서만 액세스할 수 있습니다.그러나 분석가의 쿼리 요청은 클러스터 내 모든 [!DNL Insight Servers] 서버로 연결될 수 있습니다.

클러스터는 FSU(File Server Unit) [!DNL Insight Server] 라는 단일 [!DNL .vsl] [!DNL Sensor][!DNL Insight Server] 시스템에서 로그 파일의 중앙 집중식 저장을 허용합니다. FSU 설치에 대한 자세한 내용은 Insight [Server FSU의 설치 절차를 참조하십시오](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016). FSU 구성에 대한 자세한 내용은 데이터 세트 구성 *안내서를 참조하십시오*.
