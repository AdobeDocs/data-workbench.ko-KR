---
description: 이벤트의 데이터는 회사의 일반적인 백업 시스템과 재해 복구 절차를 사용하여 매일 백업해야 합니다.
title: 이벤트 데이터 백업
uuid: 1b9e5dfe-0bf2-4ee9-bf70-1dd320a678d6
exl-id: 5afeb3a2-a2e7-4155-8fb9-1abc9c22c3c6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---

# 이벤트 데이터 백업{#backing-up-event-data}

{{eol}}

이벤트의 데이터는 회사의 일반적인 백업 시스템과 재해 복구 절차를 사용하여 매일 백업해야 합니다.

**권장 빈도:** 일별

[!DNL Insight Server] 는 매일 오전 12시 GMT에 새 로그 파일을 시작합니다. Adobe은 이전 날짜의 모든 데이터를 캡처하도록 매일 오전 12시 GMT 직후 로그 파일을 백업하는 것을 권장합니다. 예를 들어, 12월 15일 오전 12시 5분 GMT에 모든 로그 파일을 백업하면 12월 14일의 모든 데이터를 캡처합니다. [!DNL Insight Server] 는 로그 파일 백업 중에 중지할 필요가 없으며 모든 기능을 사용할 수 있습니다.

## 통합, 운영 체제, 출력 및 시스템 데이터 백업 {#section-217e52a99f944d8e83a3cc98f3d06e7e}

**권장 빈도:** 일별

통합, 운영 체제, 출력 및 시스템 데이터는 회사의 일반적인 백업 및 재해 복구 시스템을 사용하여 정기적으로 자주 백업해야 합니다.
