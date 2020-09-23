---
description: 회사의 일반적인 백업 시스템과 재해 복구 절차를 사용하여 매일 이벤트 데이터를 백업해야 합니다.
solution: Analytics
title: 이벤트 데이터 백업
uuid: 1b9e5dfe-0bf2-4ee9-bf70-1dd320a678d6
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# 이벤트 데이터 백업{#backing-up-event-data}

회사의 일반적인 백업 시스템과 재해 복구 절차를 사용하여 매일 이벤트 데이터를 백업해야 합니다.

**권장 빈도:** 일별

[!DNL Insight Server] 매일 오전 12:00에 새 로그 파일을 시작합니다. Adobe은 이전 날짜의 모든 데이터를 캡처할 수 있도록 오전 12시 00분 GMT 직후 매일 로그 파일을 백업하는 것이 좋습니다. 예를 들어 12월 15일 오전 12시 05분에 모든 로그 파일을 백업하면 12월 14일부터 모든 데이터가 캡처됩니다. [!DNL Insight Server] 은 로그 파일 백업 중에 중지할 필요가 없으며 모든 기능을 사용할 수 있습니다.

## 통합, 운영 체제, 출력 및 시스템 데이터 백업 {#section-217e52a99f944d8e83a3cc98f3d06e7e}

**권장 빈도:** 일별

통합, 운영 체제, 출력 및 시스템 데이터는 회사의 일반적인 백업 및 재해 복구 시스템을 사용하여 정기적으로 그리고 성실하게 백업해야 합니다.
