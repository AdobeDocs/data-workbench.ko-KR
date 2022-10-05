---
description: 내역 데이터 피드를 확인하고 설정하는 데 필요한 최소 단계에 대한 빠른 안내서입니다.
title: 내역 데이터 피드 유효성 확인
uuid: 83d2d48b-0966-4f4e-9c9c-60473c4546b2
exl-id: 5a5e2cca-2fab-48a0-b58d-a8c46114b9a0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 5%

---

# 내역 데이터 피드 유효성 확인{#validating-historical-data-feeds}

{{eol}}

내역 데이터 피드를 확인하고 설정하는 데 필요한 최소 단계에 대한 빠른 안내서입니다.

## 데이터 피드의 일관성을 위한 유효성 검사 단계 {#section-777b2c627a354627a02feb9461e23038}

1. 에 로그인합니다. *치열* (https://oasis.omniture.com/drteeth/)
1. SiteCatalyst 관리자 -> 데이터 피드 정의(신규)로 이동합니다.
1. 서버 위치로 이동(예: 달라스, 런던..) 조직이 있는 위치에 따라 다릅니다.
1. RSID를 제공하고 피드 유형 인사이트를 선택한 다음 를 클릭합니다 *검색*.

   ![](assets/dwb_impl_historical.png)

1. 클라이언트의 실제 피드 이름을 식별합니다.
1. 작업 섹션에서 기록 을 클릭합니다. ![](assets/dwb_impl_historical1.png)

   상태 필드에서 오류가 있는지 확인하고 일부 피드가 오류 상태인 경우 피드를 선택하고 재처리를 클릭합니다. 여러 요청에 대해 오류가 발생한 경우 이메일을 *`dataworkbench@adobe.com`* 피드 ID 및 보고서 세트 세부 사항을 재처리할 수 있습니다.

1. 사후 유효성 검사는 NAS 위치의 원시 폴더에서 로그를 확인합니다.
