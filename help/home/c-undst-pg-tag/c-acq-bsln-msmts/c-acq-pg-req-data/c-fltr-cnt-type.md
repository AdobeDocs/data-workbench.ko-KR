---
description: 센서의 컨텐츠 유형 필터링 기능의 목적은 분석용으로 유용하지 않은 정보를 저장 및 처리할 필요가 없다는 것입니다.
solution: Analytics
title: 콘텐츠 유형별 필터링
topic: Data workbench
uuid: 8a3b567b-8c7b-4ca2-bfcb-74a1addda2bd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 콘텐츠 유형별 필터링{#filtering-by-content-type}

센서의 컨텐츠 유형 필터링 기능의 목적은 분석용으로 유용하지 않은 정보를 저장 및 처리할 필요가 없다는 것입니다.

웹 서버의 API를 통해 사용할 수 있는 요청 데이터의 대부분은 비즈니스 분석에서 유용하지 않습니다. 저장 및 처리는 비용이 많이 들고 [!DNL Sensor’s] 컨텐츠 유형 필터링을 통해 불필요한 저장 및 처리를 방지할 수 있습니다.

웹 로그 데이터 처리 성능을 최대화하고 저장해야 하는 측정 데이터의 양을 줄이기 위해 [!DNL Site] 데이터 워크벤치 서버로 전송되기 전에 필터링된 특별히 나열된 컨텐츠 유형(예: CSS, 이미지 요청 등)을 제외하고 모든 웹 컨텐츠 유형 요청에 대한 측정 데이터(요청 데이터, 로그 항목, 로그 데이터 등)를 [!DNL Sensor]가져옵니다. 전체 웹 서버에 대해 이 필터링을 비활성화할 수 있으며 특정 포함된 객체의 쿼리 문자열(예: [!DNL http://www.mysite.com/advertisement.gif?Log=1])에 이름-값 쌍 &quot;Log=1&quot;을 추가하여 특정 컨텐츠 객체에 대해 재정의할 수도 있습니다.
