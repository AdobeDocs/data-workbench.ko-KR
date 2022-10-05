---
description: 사용자는 보고서 포털에 액세스할 때 유효한 계정이 있어야 하며 계정 이름과 암호를 제공해야 합니다.
title: 추가 계정 정의
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
exl-id: 1f267217-a389-431a-ba49-9a9eead0ae83
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# 추가 계정 정의

{{eol}}

사용자는 보고서 포털에 액세스할 때 유효한 계정이 있어야 하며 계정 이름과 암호를 제공해야 합니다.

기본적으로 사용자 인증은에서 활성화됩니다. [!DNL Report Portal].

에 대한 유효한 계정 목록 [!DNL Report Portal] 는 데이터베이스 파일에서 유지되며 [!DNL portal.mdb]. [!DNL Report Portal] 관리자 권한이 있는 하나의 계정으로 설치됩니다.

* 계정 이름: 테스트
* 암호: 사용자

>[!NOTE]
>
>보안상의 이유로 설치 후 이 계정의 암호를 변경하는 것이 좋습니다 [!DNL Report Portal].

사용자 계정을 추가하려면 [!DNL Report Portal] 기존 계정과 관련된 정보를 변경하거나 [!DNL Admin] 탭에서 다음을 수행합니다. [!DNL Report Portal] 사용자 인터페이스.

새 계정을 추가하거나 기존 계정을 편집할 때마다 [!DNL email.asp] 파일을 \*PortalName*\PortalASP 폴더에 저장합니다. 자세한 내용은 [Email.asp 파일 편집](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b).

사용자를 추가하는 단계는 [계정 작업](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d).

>[!NOTE]
>
>선택적으로 사용자 인증을 비활성화하고 익명 액세스를 허용할 수 있습니다 [!DNL Report Portal]. 이 작업을 수행하는 방법은 의 Session(&quot;In&quot;) 매개 변수에 대한 정보를 참조하십시오 [세션 구성 파일 편집](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7).
