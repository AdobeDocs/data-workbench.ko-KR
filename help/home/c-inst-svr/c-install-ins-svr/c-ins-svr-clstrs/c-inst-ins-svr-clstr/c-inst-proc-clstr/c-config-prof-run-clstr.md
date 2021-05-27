---
description: Insight Server 클러스터에서 실행되도록 데이터 세트 프로필을 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 세트 구성 파일을 공유합니다.
title: 클러스터에서 실행할 프로필 구성
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
exl-id: be8090fc-b3da-41c4-a5d4-c6eb85b8a84d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%

---

# 클러스터에서 실행할 프로필 구성{#configuring-a-profile-to-run-on-a-cluster}

Insight Server 클러스터에서 실행되도록 데이터 세트 프로필을 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 세트 구성 파일을 공유합니다.

따라서 이러한 파일의 매개 변수에 대한 항목은 클러스터의 모든 [!DNL Insight Servers]에 적용할 수 있어야 합니다. 예를 들어, 읽을 로그 파일의 위치, [!DNL Insight Server]에서 사용할 조회 파일 및 [!DNL Insight Server]에서 출력되는 데이터 출력의 위치는 클러스터의 모든 컴퓨터에서 동일해야 합니다.

구성 파일을 편집하는 데 사용하는 [!DNL Insight Server]인 클러스터의 마스터 [!DNL Insight Server]에서 모든 구성 작업을 수행합니다. 마스터 [!DNL Insight Server]에 수행된 모든 저장된 구성 파일 변경 내용은 클러스터의 처리 [!DNL Insight Servers]에 있는 파일에 자동으로 동기화됩니다.

[!DNL Insight Server] 클러스터에서 데이터 집합 프로필을 실행하려면 나열된 순서로 다음 프로세스를 수행해야 합니다.

1. [이벤트 데이터를 처리하는 Insight Server 확인](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [Profile.cfg에서 처리 서버 지정](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (필요한 경우) [프로필](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)에 대한 데이터 집합 구성 파일 수정

## 이벤트 데이터를 처리하는 Insight Server 확인 {#section-59b8e3f2b34f49739d544c8740a62fba}

클러스터 프로세스 이벤트 데이터의 모든 [!DNL Insight Servers]이 필요하지 않습니다. 클러스터에서 하나의 [!DNL Insight Server]을(를) 소스 파일(VSL 및 로그 파일)을 저장하고 클러스터의 모든 데이터 처리 단위(처리 서버)에 파일을 제공하는 파일 서버 단위로 지정할 수 있습니다. 이 설정은 단일 이벤트 데이터 리포지토리의 이점을 제공하며 클러스터의 모든 처리 서버의 처리 능력을 활용합니다. 처리 서버는 데이터 파일을 데이터 파일로 나누어 동일한 파일이 두 번 이상 처리되지 않도록 합니다.

파일 서버 단위로 실행할 [!DNL Insight Server] 지정에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;의 로그 처리 구성 파일 장을 참조하십시오.

단일 파일 서버 단위가 아닌 각 처리 서버에 소스 데이터 파일을 저장하기로 결정한 경우, 파일을 처리 서버 간에 균등하게 분할해야 합니다. 각 처리 서버에 데이터 세트의 소스 파일을 모두 저장하지 마십시오. 동일한 파일의 여러 복사본을 여러 처리 서버에서 사용할 수 있는 경우 데이터는 여러 번(각 컴퓨터에서 한 번) 읽고 데이터를 왜곡합니다.

로그 파일을 처리할 [!DNL Insight Servers]을 결정하는 데 도움이 필요하면 Adobe 컨설팅 팀에 문의하십시오.

## Profile.cfg {#section-99664e072c21462f91fbafb6d893fcf9}에서 처리 서버 지정

[!DNL profile.cfg] 파일에서 프로필에 대한 데이터를 처리하는 처리 서버를 지정합니다.

**profile.cfg 파일에 액세스하려면**

[!DNL Insight]에서 [!DNL Profile Manager]을 사용하여 프로필 구성 파일에 액세스합니다.

1. 데이터 세트 프로필에서 작업하는 동안 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]**&#x200B;을 클릭하거나 [!DNL Admin] 탭에서 프로필 관리 작업 공간을 열어 [!DNL Profile Manager] 을 엽니다.

1. [!DNL Profile Manager]에서 [!DNL profile.cfg] 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]** 를 클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]** 를 클릭합니다. 프로파일 구성 창이 나타납니다.

**처리 서버를 추가하려면**

1. [!DNL profile.cfg] 파일에서 **[!UICONTROL Profile]** 를 클릭한 다음 **[!UICONTROL Processing Servers]** 를 클릭하여 해당 콘텐츠를 표시합니다.

1. **[!UICONTROL Processing Servers]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add new]** > **[!UICONTROL Processing Server]** 를 클릭합니다.

1. Common Name 매개 변수에서 클러스터의 첫 번째 처리 서버에 대한 공통 이름을 입력합니다. 예: [!DNL server1.mycompany.com]
1. 클러스터에 있는 모든 처리 서버의 공통 이름을 추가할 때까지 2단계와 3단계를 반복합니다.

   >[!NOTE]
   >
   >마스터 [!DNL Insight Server]가 데이터를 처리하는 경우 추가해야 합니다.

1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

1. [!DNL profile.cfg] 옆의 [!DNL User] 열에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## 프로필 {#section-99bf9248e4e5483cb518f453b0a2f278}에 대한 데이터 집합 구성 파일 수정

**데이터 집합 구성 파일을 수정하려면**

데이터 집합 구성 파일( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], 데이터 집합에 파일 포함, [!DNL Log Processing Mode.cfg] 등)을 변경해야 하는 경우 마스터 [!DNL Insight Server]에서만 이 작업을 수행합니다.

1. 수정할 파일에 액세스합니다.

   파일에 액세스하는 방법에 대한 지침은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
1. 변경 작업을 수행합니다. 구성 파일 내의 매개 변수에 대한 자세한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
1. 파일을 저장합니다.

   1. 창 상단에서 **[!UICONTROL (modified)]** 을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save]** 를 클릭합니다.

   1. 파일 이름 옆에 있는 [!DNL User] 열의 확인 표시를 마우스 오른쪽 단추로 클릭합니다.
   1. **[!UICONTROL Save to]** 을 클릭하고 원하는 프로필을 선택합니다.

>[!NOTE]
>
>[!DNL Insight] 클러스터에서 실행 중인 데이터 집합 프로필에 액세스하는 사용자는  [!DNL Insight Server] 구성 파일(  [!DNL Insight]   [!DNL insight.cfg])의 마스터만 식별합니다. [!DNL Insight] 사용자의 관점에서 프로파일은 하나의 [!DNL Insight Server](마스터 [!DNL Insight Server])에서만 액세스할 수 있습니다.그러나 분석가의 쿼리 요청은 클러스터의 [!DNL Insight Servers] 중 하나로 보낼 수 있습니다.

[!DNL Insight Server] 클러스터는 FSU(File Server Unit)라는 단일 [!DNL Insight Server] 컴퓨터에 있는 [!DNL .vsl] 로그 파일의 중앙 저장소를 허용합니다. [!DNL Sensor] FSU 설치에 대한 자세한 내용은 [Insight Server FSU에 대한 설치 절차](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016)를 참조하십시오. FSU 구성에 대한 내용은 *데이터 집합 구성 안내서*&#x200B;를 참조하십시오.
