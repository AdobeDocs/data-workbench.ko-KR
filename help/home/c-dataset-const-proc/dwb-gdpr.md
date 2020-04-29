---
description: Adobe Data Workbench는 GDPR(General Data Protection Regulations)을 준수하는 데이터를 준비할 수 있는 도구와 프로세스를 제공합니다.
solution: Analytics
title: GDPR에 대한 데이터 워크벤치 지원
topic: Data workbench
translation-type: tm+mt
source-git-commit: 4002d01c4c9aaa7d8833415aba3fa5105cb7ac1f

---


# GDPR에 대한 데이터 워크벤치 지원

Adobe Data Workbench는 [!DNL General Data Protection Regulations] (GDPR) 준수를 위해 데이터를 준비할 수 있는 툴과 프로세스를 제공합니다.

모든 Adobe Analytics 솔루션과 마찬가지로 데이터 워크벤치에서는 Adobe Analytics의 데이터 피드를 처리할 때 분석 변수의 정리, 삭제 및 레이블 지정을 제공하여 GDPR을 지원합니다. Adobe는 GDPR 구현을 지원하기 위해 Adobe와의 계약에 명시된 회사 권한에 따라 GDPR에 대한 프로세스를 설정할 수 있도록 해줍니다. 자세한 [내용은 Adobe Analytics 및 GDPR을](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/an-gdpr-overview.html)참조하십시오.

GDPR 규정에서는 GDPR 활성화를 담당하는 여러 당사자의 역할과 책임을 식별합니다(GDPR 및 [귀하의 비즈니스 참조](https://www.adobe.com/kr/privacy/general-data-protection-regulation.html)).

* 조직은 **데이터 관리자** 역할을 하여 요구 사항 및 제한 사항에 따라 개인 데이터의 컨텍스트 및 보유 여부를 결정합니다. 그런 다음 Adobe는 사용자를 대신하여 이 데이터를 처리하고 저장합니다.
* Adobe는 **데이터 프로세서** 역할을 하여 Adobe와의 계약에 따라 GDPR 요구 사항을 구현하는 소프트웨어와 서비스를 제공합니다.
* Data Workbench와 GDPR 서비스가 통합되고 GDPR 표준에 따라 사이트 방문자( **데이터 주체**)는 데이터 프로세서인 Adobe에서 &quot;잊어버릴 권리&quot;를 행사할 수 있습니다. 데이터 컨트롤러가 UI 또는 API에서 문제가 있는 방문자 ID를 Adobe로 업로드할 수 있으므로 잊어버릴 수 있는 권한을 얻을 수 있습니다. 액세스 [제출 및 요청](https://docs.adobe.com/help/en/analytics/admin/data-governance/an-gdpr-workflow.html) 삭제 섹션을 비롯한 자세한 내용은 Adobe Analytics GDPR 워크플로우 [](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/gdpr-submit-access-delete.html) 설명서를 참조하십시오.

>[!NOTE]
>
>다른 데이터 소스의 경우 조직은 CRM, POS, IVR 및 기타 원시 데이터 소스와 같은 다른 로그 소스에서 문제가 있는 방문자 ID를 정리해야 합니다. 사용자 지정 범위 서비스 패키지는 각 데이터 소스 _또는 기타 사용자 지정 옵션에 대한 전체 파일 세트를_ 제공하여 조직에 대한 지원을 제공하는 데 사용할 수 있습니다.

## GDPR 구현을 위한 DWB 업그레이드

컨설팅은 기존 구현을 규정 준수를 위해 적합한 서비스 패키지에 대해 알려드립니다. 자세한 내용은 고객 성공 관리자(CSM)에 문의하십시오.

필요한 경우:

* [데이터 워크벤치의 최신 버전으로](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) 업그레이드합니다. 최고 수준의 보안을 위해 GDPR 통합에 필요한 새로운 인증서 및 보안 기능이 DWB 6.7 릴리스에 추가되었습니다.
* 레거시 TSV Analytics 이벤트 로그를 사용하는 경우 Avro [데이터 피드로](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2)업그레이드하십시오.
* 기존 UCP(Unified Customer Process)를 Transform과 함께 사용하여 기존 로그를 업데이트하는 경우 현재 프로세스로 업그레이드하십시오. 업데이트된 프로세스는 소스 간에 방문자 ID를 매핑하기 위한 마스터 조회 파일을 직접 생성합니다.
* GDPR 서비스를 수용하기 위해 데이터 흐름을 표준화할 수 있습니다.
* 사용자 지정 범위 서비스 패키지를 설정하여 CRM, POS, IVR 및 기타 원시 데이터 소스와 같은 다른 로그 소스를 관리합니다.
* Analytics 계약에서 기본 데이터 보존 기간을 25개월 이상으로 확인합니다.
