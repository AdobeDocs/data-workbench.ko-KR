---
description: 센서의 컨텐츠 유형 필터링 기능의 목적은 분석 용도로 유용하지 않은 정보를 저장하고 처리할 필요가 없는 것입니다.
title: 콘텐츠 유형별 필터링
uuid: 8a3b567b-8c7b-4ca2-bfcb-74a1addda2bd
exl-id: 0ed93a18-ef47-462b-8609-3ec98b037e6b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 4%

---

# 콘텐츠 유형별 필터링{#filtering-by-content-type}

{{eol}}

센서의 컨텐츠 유형 필터링 기능의 목적은 분석 용도로 유용하지 않은 정보를 저장하고 처리할 필요가 없는 것입니다.

웹 서버의 API를 통해 사용할 수 있는 요청 데이터의 대부분은 비즈니스 분석에 유용하지 않습니다. 스토리지 및 처리 비용이 비싸고 [!DNL Sensor’s] 컨텐츠 유형 필터링을 사용하면 불필요한 저장 및 처리를 방지할 수 있습니다.

웹 로그 데이터 처리 성능을 극대화하고 저장해야 하는 측정 데이터 양을 줄이려면 [!DNL Site] 에 의해 Data Workbench 서버로 전송되기 전에 필터링된 명시적으로 나열된 컨텐츠 유형(예: 계단식 스타일 시트, 이미지 요청 등)을 제외하고 모든 웹 컨텐츠 유형 요청에 대한 측정 데이터(요청 데이터, 로그 항목, 로그 데이터 등)를 획득합니다. [!DNL Sensor]. 이 필터링은 전체 웹 서버에 대해 비활성화할 수 있으며, 특정 포함된 개체의 쿼리 문자열에 이름-값 쌍 &quot;Log=1&quot;을 추가하여 특정 콘텐츠 개체에 대해 재정의할 수도 있습니다(예: [!DNL https://www.mysite.com/advertisement.gif?Log=1]).
