---
description: 이 섹션에서는 스키마 디자인 및 구현을 위한 데이터 워크벤치 데이터 세트에 대한 기본 키(추적 ID)를 만드는 방법에 대해 설명합니다.
title: 데이터 처리 - 기본 키 작성
uuid: 7a12950e-6ac0-47d5-b4a8-0b50c48b04fa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 처리 - 기본 키 작성{#data-processing-building-primary-key}

이 섹션에서는 스키마 디자인 및 구현을 위한 데이터 워크벤치 데이터 세트에 대한 기본 키(추적 ID)를 만드는 방법에 대해 설명합니다.

## 추적 ID 이해 {#section-24683031044a4af49988655ccb9a45fd}

디코더를 사용하여 DWB에서 데이터를 읽고 디코딩한 후 첫 번째 단계는 추적 ID와 타임스탬프를 정의하는 것입니다. 추적 ID는 고객 레코드를 고유하게 식별하는 식별자입니다. 이메일 ID, 소셜 보안 번호, 쿠키 ID 등과 같은 피드의 모든 필드가 될 수 있습니다. 추적 ID로 사용할 필드는 검색 세션 중에 클라이언트가 결정합니다. 추적 ID 및 타임스탬프는 필수 필드이며 각 레코드에 대해 정의해야 합니다.

일반적으로 온라인 데이터의 경우 쿠키 ID( *x-visid_high* 및* x-visid_low의 조합)가 고유한 고객 식별을 위한 기본 메커니즘으로 사용되지만 클라이언트의 요구 사항에 따라 변경할 수 있습니다. 요청(또는 이벤트)이 발생하는 날짜와 시간은 *x-timestamp*&#x200B;입니다. DWB의 모든 레코드는 *trackingid* 및 타임스탬프에 의해 정렬됩니다. 필수 필드 [!DNL Definitions.cfg] 파일은 필수 필드를 정의하는 로그 처리 데이터 세트 포함 파일입니다. *x-trackingid* 및 *x-timestamp*.

참고:*DWB의 x-trackingid *는 내장 필드이며 이 이름은 다른 필드에 사용할 수 없습니다.

**예 1**:쿠키 ID를 사용하여 *x-trackingid* 만들기(온라인 데이터만 사용되는 경우)

쿠키 ID를 사용하여 DWB에서 *x-trackingid *를 만들려면, 해시 함수를 사용하여 *파일에 x-trackingid* (추적 ID를 정의하는 것이 좋지만 폴더 아래의 다른 구성 파일에 정의될 수 있음)를 만드는 것이 좋습니다 [!DNL foundation.cfg] [!DNL foundation.cfg] [!DNL Dataset > log processing] .

![](assets/dwb_impl_primary_key1.png)

**예 2**:이메일 ID를 사용하여 *x-trackingid* 만들기(온라인 및 오프라인 데이터를 모두 사용할 수 있는 경우)

오프라인 데이터와 온라인 데이터를 모두 사용할 수 있고(이 예) 이메일 ID를 데이터 소스 모두에서 사용할 수 있다고 가정할 수 있습니다. 이메일 ID는 고객을 고유하게 식별하므로 *x-trackingid를 만드는 데 사용됩니다*.

다음과 같이 Hash 함수를 사용하여 *trackingId* 만들기

![](assets/dwb_impl_primary_key2.png)

