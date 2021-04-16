---
description: Adobe Data Workbench은 GDPR(General Data Protection Regulations)을 준수하는 데 필요한 툴 및 프로세스를 제공합니다.
title: GDPR을 위한 Data Workbench 지원
exl-id: fdc43567-0c57-4851-9073-e295258a8074
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 4%

---

# GDPR을 위한 Data Workbench 지원

Adobe Data Workbench은 [!DNL General Data Protection Regulations](GDPR)을 준수하기 위해 데이터를 준비하는 도구와 프로세스를 제공합니다.

모든 Adobe Analytics 솔루션과 마찬가지로 Data Workbench은 Adobe Analytics 데이터 피드를 처리할 때 분석 변수의 정리, 삭제 및 레이블 지정을 제공하여 GDPR을 지원합니다. GDPR 구현을 지원하기 위해 Adobe을 사용하면 Adobe과의 계약에 명시된 회사 권한에 따라 GDPR에 대한 프로세스를 설정할 수 있습니다. 자세한 내용은 [Adobe Analytics 및 GDPR을 참조하십시오](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/an-gdpr-overview.html).

GDPR 규정은 GDPR 활성화를 담당하는 여러 당사자의 역할과 의무를 식별합니다([GDPR 및 귀하 사업](https://www.adobe.com/kr/privacy/general-data-protection-regulation.html) 참조).

* 조직은 **데이터 컨트롤러** 역할을 하여 사용자의 요구 사항과 제약 조건에 따라 개인 데이터의 컨텍스트 및 보유 여부를 결정합니다. 그런 다음 Adobe은 귀하를 대신하여 이 데이터를 처리하고 저장합니다.
* Adobe은 Adobe과의 계약에 따라 GDPR 요구 사항을 구현하는 소프트웨어와 서비스를 제공하기 위해 **데이터 프로세서** 역할을 합니다.
* GDPR 서비스와 Data Workbench이 통합되고 GDPR 표준에 따라 사이트 방문자(**데이터 주체**)는 데이터 프로세서인 Adobe에서 &quot;잊혀질 권리&quot;를 행사할 수 있습니다. 데이터 컨트롤러가 UI 또는 API에서 문제가 있는 방문자 ID를 Adobe으로 업로드할 수 있으므로 잊어버릴 수 있는 권한을 획득합니다. [액세스 제출 및 요청 삭제](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/gdpr-submit-access-delete.html) 섹션을 비롯한 자세한 내용은 [Adobe Analytics GDPR Workflow](https://docs.adobe.com/help/en/analytics/admin/data-governance/an-gdpr-workflow.html) 설명서를 참조하십시오.

>[!NOTE]
>
>다른 데이터 소스의 경우 조직은 CRM, POS, IVR 및 기타 원시 데이터 소스 등의 다른 로그 소스에서 문제가 있는 방문자 ID를 정리해야 합니다. 사용자 지정 범위 서비스 패키지는 _각 데이터 소스_&#x200B;에 대해 지속적인 서비스 보유자가 지원하거나 유지 관리하는 데 필요한 파일 세트를 모두 대체하여 조직을 지원하는 데 사용할 수 있습니다.

## GDPR 구현을 위한 DWB 업그레이드

컨설턴트는 기존 구현을 준수하도록 적절한 서비스 패키지에 대한 조언을 제공합니다. 자세한 내용은 고객 성공 관리자(CSM)에 문의하십시오.

필요한 경우:

* [최신 ](https://docs.adobe.com/content/help/ko-KR/data-workbench/using/release-notes/release-notes.html) Data Workbench 버전으로 업그레이드하십시오. 최고 수준의 보안을 위해 GDPR 통합에 필요한 DWB 6.7 릴리스에 새로운 인증서 및 보안 기능이 추가되었습니다.
* 레거시 TSV Analytics 이벤트 로그를 사용하는 경우 [Avro 데이터 피드](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2)로 업그레이드하십시오.
* 기존 UCP(통합 고객 프로세스)를 변환에 사용하여 기존 로그를 업데이트하는 경우 현재 프로세스로 업그레이드하십시오. 업데이트된 프로세스는 소스 간에 방문자 ID를 매핑하기 위해 마스터 조회 파일을 직접 생성합니다.
* GDPR 서비스에 맞게 데이터 흐름을 표준화할 수 있습니다.
* 사용자 지정 범위 서비스 패키지를 설정하여 CRM, POS, IVR 및 기타 원시 데이터 소스와 같은 다른 로그 소스를 관리합니다.
* Analytics 계약에서 기본 데이터 보존 기간 25개월 이상을 확인합니다.
