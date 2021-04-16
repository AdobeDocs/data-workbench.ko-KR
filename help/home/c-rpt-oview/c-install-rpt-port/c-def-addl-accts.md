---
description: 사용자는 보고서 포털에 액세스할 때 유효한 계정을 가지고 있어야 하며 계정 이름과 암호를 제공해야 합니다.
title: 추가 계정 정의
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
exl-id: 1f267217-a389-431a-ba49-9a9eead0ae83
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---

# 추가 계정 정의

사용자는 보고서 포털에 액세스할 때 유효한 계정을 가지고 있어야 하며 계정 이름과 암호를 제공해야 합니다.

기본적으로 사용자 인증은 [!DNL Report Portal]에서 활성화됩니다.

[!DNL Report Portal]에 대한 유효한 계정 목록은 데이터베이스 파일인 [!DNL portal.mdb]에서 유지 관리됩니다. [!DNL Report Portal] 관리 권한이 있는 하나의 계정으로 설치됨:

* 계정 이름:test
* 암호:user

>[!NOTE]
>
>보안상의 이유로 [!DNL Report Portal]을(를) 설치한 후 이 계정의 암호를 변경하는 것이 좋습니다.

[!DNL Report Portal]에 사용자 계정을 추가하거나 기존 계정과 관련된 정보를 변경하려면 [!DNL Report Portal] 사용자 인터페이스에서 [!DNL Admin] 탭을 사용합니다.

새 계정을 추가하거나 기존 계정을 편집할 때마다 \*PortalName*\PortalASP 폴더의 [!DNL email.asp] 파일에 지정된 확인 이메일이 전송됩니다. 자세한 내용은 [Email.asp 파일 편집](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b)을 참조하십시오.

추가 사용자를 추가하는 단계는 [계정 작업](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d)을 참조하십시오.

>[!NOTE]
>
>선택적으로 사용자 인증을 비활성화하고 [!DNL Report Portal]에 대한 익명 액세스를 허용할 수 있습니다. 이 작업을 수행하려면 [세션 구성 파일 편집](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)의 Session(&quot;In&quot;) 매개 변수에 대한 정보를 참조하십시오.
