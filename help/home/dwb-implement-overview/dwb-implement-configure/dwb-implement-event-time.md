---
description: 이 섹션에서는 Data Workbench 데이터 세트에 대한 타임스탬프를 만드는 방법을 설명합니다.
title: 이벤트 시간 설정
uuid: 0230154d-05a2-44cf-9456-0a27e55f58ef
exl-id: 9632e713-5cf9-4acf-aafa-bfdf79a51ad9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 2%

---

# 이벤트 시간 설정{#setting-up-event-time}

{{eol}}

이 섹션에서는 Data Workbench 데이터 세트에 대한 타임스탬프를 만드는 방법을 설명합니다.

## 이벤트 시간 이해 {#section-e10ef2b5b6244dc5b215836e3c77d663}

이벤트 시간은 요청(또는 이벤트)이 발생하는 날짜 및 시간입니다.

일반적으로 온라인 데이터의 경우 *x_hit_time_gmt* 은 타임스탬프 필드로 사용됩니다. 호출 시간을 오프라인 데이터(예: 콜 센터 데이터)에 대한 타임스탬프로 사용할 수 있습니다. 필수 필드이며 모든 데이터 소스에는 타임스탬프로 사용할 수 있는 필드가 하나 있어야 합니다. 이 정보는 조직이 제공해야 합니다.

DWB에서 다음 사전 정의된 변수가 타임스탬프를 캡처합니다.

<table id="table_C24BD56CEB4E42F68D645EBB65585D16"> 
 <tbody> 
  <tr> 
   <td colname="col1"><i>x-timestamp</i> </td> 
   <td colname="col2"> <p> 서버에서 요청을 받은 날짜 및 시간(GMT)입니다. 이 시간은 1600년 1월 1일 이후 100나노초 수로 표시됩니다. </p> <p>예: 127710989320000000 <i>x-timestamp</i> 11에 대한 값:28:2005년 9월 13일 화요일 52.0000000 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><i>x-timestring</i> </td> 
   <td colname="col2"> <i>x-timestamp</i> yyyy-MM-DD HH 형식으로:MM:음.. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><i>x-unixtime</i> </td> 
   <td colname="col2"> <i>x-unixtime</i> 는 1970년 1월 1일 이후 시간(초)을 00으로 나타내는 epoc 시간입니다:00:01. </td> 
  </tr> 
 </tbody> 
</table>

날짜 필드의 형식을 기반으로 x-timestamp 또는 x-unixtime 또는 x-timestring이 사용됩니다. 예를 들어 수신 데이터가 YYYY-MM-DD 형식의 경우 x-timestring을 사용해야 합니다.

타임스탬프는 형식 중 하나로 정의되며 DWB는 내부적으로 다른 두 형식을 생성합니다. 또한 이러한 필드는 사전 정의된 DWB 필드이며 다른 필드에 동일한 이름을 사용할 수 없습니다.

## DWB에 정의된 시간대 {#section-3cdd12254342442b917376661e1d9c9f}

날짜 필드에 위에서 언급한 시간대가 포함되어 있는 경우, DWB는 해당 특정 시간대의 전체 행을 고려합니다. 예를 들어, 하나의 파일에 2015-01-01 00으로 정의된 날짜가 있습니다:00:00gmtand 다른 파일의 값은 2015-01-01 00입니다.:00:첫 번째 파일의 날짜는 GMT 시간대로, 두 번째 파일의 날짜는 CST 시간대로 간주됩니다.

| 코드 | 시간대 |
|---|---|
| gmt | 그리니치 평균 |
| est | 동부 표준 |
| 편집 | 동부 일광 |
| cst | Central Standard |
| cdt | 중앙 일광 |
| mst | Mountain Standard |
| mdt | 일광 |
| pst | 태평양 표준 |
| pdt | 태평양 일광 |

>[!NOTE]
>
>DWB는 위에 언급된 시간대만 처리합니다.

## 사용자 지정 시간대 설정 {#section-7c351921f22b439b81c73f40d5b47536}

DWB는 시간대에서 오프셋을 처리하지 않습니다. 시간대에서 오프셋을 고려하려면 해당 오프셋 시간대에서 데이터 형식을 지정해야 합니다.

예: CST 표준 시간대에서 날짜 형식을 고려하려면 데이터가 YYYY-MM-DD HH로 와야 합니다.:MM:클라이언트의 SS UTC +/-HMM 형식입니다.

2015-10-18 05:00:00 UTC -0200

## 이벤트 시간/타임스탬프를 설정하는 방법 {#section-81507080f0b44ae6b83d3650ba019812}

날짜 필드 형식을 기준으로 하면, *x-timestamp, x-unixtime* 또는 *x-timestring* 변수가 사용됩니다. 아래 예에서는 *x-hit_time_gmt* unix epoc 형식으로 제공되며, *x-unixtime* 이 사용됩니다.

DWB에서 [!DNL foundation.cfg] 파일(또는 데이터 집합 로그 처리 폴더 아래의 다른 구성 파일)에서는 복사 변환을 사용하여 다음과 같이 이벤트 시간을 설정합니다.

날짜 필드 형식을 기반으로, x-timestamp, x-unixtime 또는 x-timestring 변수가 사용됩니다. 아래 예에서는 x-hit_time_gmt가 unix epoc 형식으로 제공되므로 x-unixtime이 사용됩니다.

insight foundation.cfg(또는 Datasetà 로그 처리 폴더 아래의 다른 구성)에서 복사 변환 을 사용하여 다음과 같이 이벤트 시간을 설정합니다. ![](assets/dwb_impl_timestamp1.png)

의 날짜가 YYYY-MM-DD HH인 경우:MM:SS.mmm 형식, x-timestring이 사용됩니다. ![](assets/dwb_impl_timestamp2.png)예: 날짜 필드가 DWB와 YYYY/MM/DD와 같은 다른 형식의 경우 먼저 DWB에서 허용하는 타임스탬프 형식 중 하나로 형식을 지정한 다음 해당 변수에 지정합니다. 아래 스크린샷에서는 날짜가 먼저 YYYY-MM-DD 형식으로 변환되고 *x-timestring *변수에 할당됩니다. ![](assets/dwb_impl_timestamp3.png)
