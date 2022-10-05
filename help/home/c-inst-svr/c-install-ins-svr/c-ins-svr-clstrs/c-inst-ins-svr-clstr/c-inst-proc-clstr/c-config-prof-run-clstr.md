---
description: Insight Server 클러스터에서 실행되도록 데이터 세트 프로필을 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 세트 구성 파일을 공유합니다.
title: 클러스터에서 실행할 프로필 구성
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
exl-id: be8090fc-b3da-41c4-a5d4-c6eb85b8a84d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%

---

# 클러스터에서 실행할 프로필 구성{#configuring-a-profile-to-run-on-a-cluster}

{{eol}}

Insight Server 클러스터에서 실행되도록 데이터 세트 프로필을 구성하면 클러스터의 모든 컴퓨터가 해당 프로필에 대한 모든 데이터 세트 구성 파일을 공유합니다.

따라서 이러한 파일의 매개 변수에 대한 항목은 모든 파일에 적용할 수 있어야 합니다 [!DNL Insight Servers] 입니다. 예를 들어, 읽을 로그 파일의 위치, 사용자가 사용할 조회 파일 [!DNL Insight Server], 및에서 데이터 출력의 위치 [!DNL Insight Server] 클러스터의 모든 컴퓨터에서 동일해야 합니다.

클러스터의 마스터에서 모든 구성 작업을 수행합니다 [!DNL Insight Server]: [!DNL Insight Server] 를 사용하여 구성 파일을 편집합니다. 마스터에서 수행된 모든 저장된 구성 파일 변경 사항 [!DNL Insight Server] 처리 중인 파일에 자동으로 동기화됩니다 [!DNL Insight Servers] 입니다.

에서 데이터 집합 프로필을 실행하려면 [!DNL Insight Server] cluster에서 나열된 순서로 다음 프로세스를 수행해야 합니다.

1. [이벤트 데이터를 처리하는 Insight Server 확인](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [Profile.cfg에서 처리 서버 지정](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (필요한 경우) [프로필에 대한 데이터 집합 구성 파일 수정](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)

## 이벤트 데이터를 처리하는 Insight Server 확인 {#section-59b8e3f2b34f49739d544c8740a62fba}

모든 것이 필요한 것은 아닙니다 [!DNL Insight Servers] 클러스터 프로세스 이벤트 데이터에서 하나를 지정할 수 있습니다 [!DNL Insight Server] 클러스터에서 소스 파일(VSL 및 로그 파일)을 저장하고 클러스터의 모든 데이터 처리 단위(처리 서버)에 파일을 제공하는 파일 서버 단위로 이 설정은 단일 이벤트 데이터 리포지토리의 이점을 제공하며 클러스터의 모든 처리 서버의 처리 능력을 활용합니다. 처리 서버는 데이터 파일을 데이터 파일로 나누어 동일한 파일이 두 번 이상 처리되지 않도록 합니다.

를 지정하는 방법에 대한 자세한 정보 [!DNL Insight Server] 파일 서버 단위로 실행하려면 *데이터 집합 구성 안내서*.

단일 파일 서버 단위가 아닌 각 처리 서버에 소스 데이터 파일을 저장하기로 결정한 경우, 파일을 처리 서버 간에 균등하게 분할해야 합니다. 각 처리 서버에 데이터 세트의 소스 파일을 모두 저장하지 마십시오. 동일한 파일의 여러 복사본을 여러 처리 서버에서 사용할 수 있는 경우 데이터는 여러 번(각 컴퓨터에서 한 번) 읽고 데이터를 왜곡합니다.

지원 여부 확인 [!DNL Insight Servers] 로그 파일을 처리해야 합니다. Adobe 컨설팅 팀에 문의하십시오.

## Profile.cfg에서 처리 서버 지정 {#section-99664e072c21462f91fbafb6d893fcf9}

에서 [!DNL profile.cfg] 파일에서 프로파일에 대한 데이터를 처리하는 처리 서버를 지정합니다.

**profile.cfg 파일에 액세스하려면**

를 사용하여 프로필 구성 파일에 액세스합니다 [!DNL Profile Manager] in [!DNL Insight].

1. 데이터 세트 프로필에서 작업하는 동안 [!DNL Profile Manager] 작업 공간 내에서 마우스 오른쪽 단추 클릭 및 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]**&#x200B;또는 의 [!DNL Admin] 탭.

1. 에서 [!DNL Profile Manager]옆의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL profile.cfg] 을(를) 클릭합니다. **[!UICONTROL Make Local]**. 이 파일에 대한 확인 표시가 [!DNL User] 열.

1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. 프로파일 구성 창이 나타납니다.

**처리 서버를 추가하려면**

1. 에서 [!DNL profile.cfg] 파일, **[!UICONTROL Profile]**&#x200B;를 클릭한 다음 **[!UICONTROL Processing Servers]** 콘텐츠를 표시합니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL Processing Servers]** 을(를) 클릭합니다. **[!UICONTROL Add new]** > **[!UICONTROL Processing Server]**.

1. Common Name 매개 변수에서 클러스터의 첫 번째 처리 서버에 대한 공통 이름을 입력합니다. 예: [!DNL server1.mycompany.com]
1. 클러스터에 있는 모든 처리 서버의 공통 이름을 추가할 때까지 2단계와 3단계를 반복합니다.

   >[!NOTE]
   >
   >마스터가 [!DNL Insight Server] 데이터를 처리하고, 추가도 해야 합니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 옆에 있는 열 [!DNL profile.cfg]. 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## 프로필에 대한 데이터 집합 구성 파일 수정 {#section-99bf9248e4e5483cb518f453b0a2f278}

**데이터 집합 구성 파일을 수정하려면**

데이터 집합 구성 파일( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], 데이터 집합에 파일 포함 [!DNL Log Processing Mode.cfg]등)만 마스터에서 수행합니다 [!DNL Insight Server].

1. 수정할 파일에 액세스합니다.

   파일에 액세스하는 방법에 대한 지침은 *데이터 집합 구성 안내서*.
1. 변경 작업을 수행합니다. 자세한 내용은 *데이터 집합 구성 안내서* 구성 파일 내의 매개 변수에 대한 자세한 내용을 참조하십시오.
1. 파일을 저장합니다.

   1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (modified)]** 창 상단에서 을(를) 클릭하고 **[!UICONTROL Save]**.

   1. 에서 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 옆에 있는 를 클릭합니다.
   1. 클릭 **[!UICONTROL Save to]** 원하는 프로필을 선택합니다.

>[!NOTE]
>
>[!DNL Insight] 클러스터에서 실행 중인 데이터 집합 프로필에 액세스하는 사용자는 마스터만 식별합니다 [!DNL Insight Server] 에서 [!DNL Insight] 구성 파일 ( [!DNL insight.cfg]). 의 관점에서 [!DNL Insight] 사용자, 프로필은 한 개만 액세스할 수 있습니다 [!DNL Insight Server] (마스터 [!DNL Insight Server]); 그러나 분석가로부터의 쿼리 요청은 어느 것이든 전달할 수 있습니다 [!DNL Insight Servers] 입니다.

An [!DNL Insight Server] 클러스터는 [!DNL .vsl] 로그 파일( [!DNL Sensor]) [!DNL Insight Server] 파일 서버 유닛(FSU)이라는 컴퓨터 FSU 설치에 대한 자세한 내용은 [Insight Server FSU의 설치 절차](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016). FSU 구성에 대한 자세한 내용은 *데이터 집합 구성 안내서*.
