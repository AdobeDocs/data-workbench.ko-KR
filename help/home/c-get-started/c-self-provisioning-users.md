---
description: 워크스테이션을 사용하여 Data Workbench 사용자를 관리합니다.
title: 사용자 셀프 프로비저닝
uuid: e3c10bc4-2fa0-4368-9952-e38a4794aee9
exl-id: fba916bf-66a1-4b69-a1c0-cad5b27bbbba
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 3%

---

# 사용자 셀프 프로비저닝{#self-provisioning-of-users}

{{eol}}

워크스테이션을 사용하여 Data Workbench 사용자를 관리합니다.

Adobe에서 필요한 인증서를 설정하여 워크스테이션을 사용하여 Data Workbench 서버에 연결할 수 있습니다. 이 인증서는 SSL 통신과 라이선스가 있는 리소스 및 기능을 사용할 수 있는 권한 모두에서 지원됩니다. 인증서 기반 인증에서는 여러 시스템에서 워크스테이션을 사용하기 위해 여러 인증서를 획득하고 설정해야 합니다. 또한 Adobe에서 사용자 프로비저닝 및 자격을 관리하며 새 인증서 또는 인증서 해지를 위해 Adobe에 문의해야 합니다.

DWB 6.7부터 워크스테이션은 사용자 이름과 암호를 통해 사용자 인증을 지원합니다.

인증서 기반 인증/인증이 여전히 설정에 대해 작동하지만 최신 자격 증명 기반 인증으로 마이그레이션하는 것이 좋습니다. 최신 접근 방식에서 워크스테이션 사용자는 IMS(Adobe Identity Management 시스템)를 통해 자신을 인증합니다. 워크스테이션을 사용하려면 먼저 [Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html?lang=ko-KR) 조직의 관리자가 생성합니다.

새로운 인증 및 사용자 프로비저닝 모델은 다음과 같은 이점을 제공합니다.

* Admin Console을 통해 사용자 및 그룹의 자체 프로비저닝. Adobe에 연락하여 사용자의 라이선스 자격을 추가, 제거 또는 수정할 필요가 없습니다.
* 자격 증명을 사용하여 로그인함으로써 구성 상태를 잃지 않고 여러 시스템에서 워크스테이션에 액세스합니다. 로컬 캐시가 로그아웃 시 삭제되고 현재 프로필이 닫히고 구성 프로필이 활성 상태가 됩니다.

## 시작하기

시작하기 전에 Adobe에게 연락하여 Admin Console에 조직을 추가하십시오. 구매한 서비스에 따라 Adobe이 조직을 프로비저닝합니다. 예를 들어 조직은 속성 서비스 또는 베타 빌드에 액세스하거나 둘 다에 액세스할 수 있습니다. 조직이 구성되면 조직 관리자가 사용자와 그룹을 추가할 수 있습니다. 자세한 내용은 [Experience Cloud 사용자 및 제품 관리](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) Experience Cloud에서 자세히 알아보십시오. 조직 관리자는 역할에 따라 다양한 사용자에 대한 사용 제한을 구성할 수도 있습니다. 예를 들어 시험판이 아닌 사용자는 베타 빌드에 액세스할 필요가 없습니다.

Admin Console을 통해 이 조직에 추가된 프로비저닝된 각 사용자는 Data Workbench을 사용할 수 있는 액세스 권한을 갖습니다. 하위 서비스는 제품 액세스에 따라 각 사용자에 대해서만 활성화하거나 비활성화할 수 있습니다. 사용자가 인증서에서 IMS로 업그레이드되면 모든 로컬 데이터가 새 IMS 사용자 디렉토리에 복사됩니다.

>[!NOTE]
>
>세션은 서버에서 6시간, 액세스 토큰을 새로 고치지 않으면 클라이언트에서 23시간 동안 지속됩니다. 토큰을 새로 고치면 다시 로그인하지 않고 클라이언트를 사용할 수 있습니다.

Admin Console에서 한 개 이상의 제품 수준 구성을 만들어야 사용자에게 액세스를 제공할 수 있습니다.

부울 플래그 **IMS 사용** 에 추가할 수 있습니다. [!DNL Insight.cfg] 인증서 모드로 폴백하려면 다음을 수행합니다. IMS 사용자를 위한 액세스 제어 구성에 대한 자세한 내용은 [액세스 제어 파일 업데이트](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-dpu/c-updt-accss-ctrl-file.html).

## 충돌 해결

사용자가 동일한 프로필에서 동일한 IMS 계정을 사용하는 여러 시스템에 로그온하고 시스템 중 하나에서 오프라인 모드에 있는 경우, `.conflict` 이(가) 표시되고 팝업 창이 표시됩니다. 이 문제는 파일(작업 공간, 차원, 필터 등)과 컨텐츠가 다를 때 발생합니다. 두 시스템에서 동기화됨 [!DNL User\Profile\] 서버 및 클라이언트에서의 호출 백업은 `.conflict` 파일 및 데이터가 손실되지 않습니다. 의 부울 플래그 [!DNL Insight.cfg] 이 충돌 팝업을 비활성화할 수 있습니다.

플래그: 충돌 알림

작업 공간, 지표, 차원 등에 적용할 수 있습니다. 사용자 폴더 아래에 표시됩니다.
