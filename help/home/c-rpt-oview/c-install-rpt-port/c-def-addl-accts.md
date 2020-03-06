---
description: 사용자는 올바른 계정을 가지고 있어야 하며 보고서 포털에 액세스할 때 계정 이름과 암호를 제공해야 합니다.
solution: Analytics
title: 추가 계정 정의
topic: Data workbench
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 추가 계정 정의{#define-additional-accounts}

사용자는 올바른 계정을 가지고 있어야 하며 보고서 포털에 액세스할 때 계정 이름과 암호를 제공해야 합니다.

기본적으로 사용자 인증은 에서 활성화됩니다 [!DNL Report Portal].

에 대한 유효한 계정 목록은 데이터베이스 [!DNL Report Portal] 파일에서 유지됩니다 [!DNL portal.mdb]. [!DNL Report Portal] 관리 권한이 있는 하나의 계정으로 설치됨:

* 계정 이름:test
* 암호:user

>[!NOTE]
>
>보안상의 이유로 설치 후 이 계정의 암호를 변경하는 것이 좋습니다 [!DNL Report Portal].

사용자 계정을 추가 [!DNL Report Portal] 또는 기존 계정과 관련된 정보를 변경하려면 [!DNL Admin] 사용자 인터페이스의 [!DNL Report Portal] 탭을 사용합니다.

새 계정을 추가하거나 기존 계정을 편집할 때마다 \*PortalName*\PortalASP 폴더의 [!DNL email.asp] 파일에 지정된 대로 확인 이메일이 전송됩니다. 자세한 내용은 Email.asp [파일 편집을 참조하십시오](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b).

사용자를 추가하는 단계는 계정 [작업을 참조하십시오](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d).

>[!NOTE]
>
>선택적으로 사용자 인증을 비활성화하고 익명 액세스를 허용할 수 [!DNL Report Portal]있습니다. 이를 위한 단계는 세션 구성 파일 편집에서 Session(&quot;In&quot;) 매개 변수에 [대한 정보를 참조하십시오](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7).

