---
description: Adobe Data Workbench은 GDPR(일반 데이터 보호 규정)을 준수하도록 데이터를 준비하는 도구와 프로세스를 제공합니다.
title: GDPR을 위한 Data Workbench 지원
exl-id: fdc43567-0c57-4851-9073-e295258a8074
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 4%

---

# GDPR을 위한 Data Workbench 지원

Adobe Data Workbench은 [!DNL General Data Protection Regulations] (GDPR)을 준수하도록 데이터를 준비하도록 도구와 프로세스를 제공합니다.

모든 Adobe Analytics 솔루션과 마찬가지로, Data Workbench은 Adobe Analytics의 데이터 피드를 처리할 때 분석 변수의 정리, 삭제 및 레이블 지정을 제공하여 GDPR을 지원합니다. GDPR 구현을 지원하기 위해 Adobe을 사용하면 Adobe과의 계약에 설정된 회사의 권한에 따라 GDPR에 대한 프로세스를 설정할 수 있습니다. 추가 정보](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/an-gdpr-overview.html)는 [Adobe Analytics 및 GDPR을 참조하십시오.

GDPR 규정은 GDPR 활성화를 담당하는 서로 다른 당사자의 역할 및 의무를 식별합니다([GDPR 및 비즈니스](https://www.adobe.com/kr/privacy/general-data-protection-regulation.html) 참조).

* 조직은 **데이터 컨트롤러** 역할을 하여 사용자의 요구 사항과 제한에 따라 개인 데이터의 컨텍스트 및 보존을 결정합니다. Adobe이 귀하를 대신하여 이 데이터를 처리하고 저장합니다.
* Adobe은 **데이터 프로세서** 역할을 하여 Adobe과의 계약에 따라 GDPR 요구 사항을 구현하는 소프트웨어 및 서비스를 제공합니다.
* GDPR 서비스와 Data Workbench을 통합한 후 GDPR 표준에 따라 사이트(**데이터 주체**)를 방문하는 사용자는 데이터 처리자인 Adobe이 &quot;잊혀질 권리&quot;를 행사할 수 있습니다. 잊혀질 권리를 달성하기 위해 데이터 제어자는 UI 또는 API에서 Adobe에 대해 문제가 있는 방문자 ID를 업로드할 수 있습니다. [액세스 및 삭제 요청 제출](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/gdpr-submit-access-delete.html) 섹션을 포함한 자세한 내용은 [Adobe Analytics GDPR 워크플로우](https://docs.adobe.com/help/en/analytics/admin/data-governance/an-gdpr-workflow.html) 설명서를 참조하십시오.

>[!NOTE]
>
>다른 데이터 소스의 경우 조직은 CRM, POS, IVR 및 기타 원시 데이터 소스 등의 다른 로그 소스에서 문제가 있는 방문자 ID를 정리해야 합니다. 사용자 지정 범위 서비스 패키지는 _각 데이터 소스_&#x200B;에 대해 지속적인 서비스 보유자가 지원 또는 유지 관리하는 데 필요한 전체 파일 대체 세트를 제공하여 조직에 대한 지원을 제공하는 데 사용할 수 있습니다.

## GDPR 구현을 위한 DWB 업그레이드

컨설팅 팀에서는 기존 구현을 준수하도록 적절한 서비스 패키지에 대해 조언을 제공합니다. 자세한 내용은 고객 성공 관리자(CSM)에게 문의하십시오.

필요한 경우:

* [최신 버전의 ](https://docs.adobe.com/content/help/ko-KR/data-workbench/using/release-notes/release-notes.html) Data Workbench으로 업그레이드하십시오. 가장 높은 보안을 위해 GDPR 통합에 필요한 DWB 6.7 릴리스에 새 인증서 및 보안 기능이 추가되었습니다.
* 기존 TSV Analytics 이벤트 로그를 사용하는 경우 [Avro 데이터 피드](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2)로 업그레이드하십시오.
* 기존 로그를 업데이트하기 위해 변환과 함께 기존 UCP(Unified Customer Process)를 사용하는 경우 현재 프로세스로 업그레이드하십시오. 업데이트된 프로세스는 소스 간에 방문자 ID를 매핑하기 위한 마스터 조회 파일을 직접 생성합니다.
* GDPR 서비스를 수용하도록 데이터 흐름을 표준화합니다.
* CRM, POS, IVR 및 기타 원시 데이터 소스와 같은 다른 로그 소스를 관리하려면 사용자 지정 범위 서비스 패키지를 설정하십시오.
* Analytics 계약에서 기본 데이터 보존 기간이 25개월 이상인지 확인합니다.
