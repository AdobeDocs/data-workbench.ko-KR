---
description: 내역 데이터 피드의 유효성을 확인하고 설정하는 데 필요한 최소 단계에 대한 빠른 가이드입니다.
title: 내역 데이터 피드 유효성 확인
uuid: 83d2d48b-0966-4f4e-9c9c-60473c4546b2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 내역 데이터 피드 유효성 확인{#validating-historical-data-feeds}

내역 데이터 피드의 유효성을 확인하고 설정하는 데 필요한 최소 단계에 대한 빠른 가이드입니다.

## 데이터 피드의 일관성을 위한 유효성 검사 단계 {#section-777b2c627a354627a02feb9461e23038}

1. 드라이브에 *로그인* (https://oasis.omniture.com/drteeth/)
1. SiteCatalyst 관리자로 이동 -> 데이터 피드 정의(신규)
1. 서버 위치로 이동(예: 달라스, 런던...) 조직의 위치에 따라 다릅니다.
1. RSID를 제공하고 피드 유형 인사이트를 선택하고 *검색을*&#x200B;클릭합니다.

   ![](assets/dwb_impl_historical.png)

1. 클라이언트의 실제 피드 이름을 식별합니다.
1. 작업 섹션에서 내역을 클릭합니다. ![](assets/dwb_impl_historical1.png)

   상태 필드에 오류가 있는지 확인합니다. 일부 피드가 오류 상태인 경우 피드를 선택하고 재처리를 클릭합니다. 여러 요청에 대해 오류가 발생한 경우 피드 ID 및 보고서 세트 세부 정보가 *`dataworkbench@adobe.com`* 있는 이메일을 전송하여 재처리합니다.

1. 사후 확인은 NAS 위치의 원시 폴더에 있는 로그를 확인합니다.

