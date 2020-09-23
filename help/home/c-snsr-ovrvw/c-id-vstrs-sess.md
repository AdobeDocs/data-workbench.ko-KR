---
description: 웹 서버에서 이벤트 데이터를 수집할 때 센서는 개인적으로 식별 정보를 캡처하지 않고 작은 무작위 식별자를 포함한 각 방문자에 대해 영구 쿠키를 자동으로 설정합니다.
solution: Analytics
title: 센서는 방문자 및 세션을 어떻게 식별합니까?
uuid: 3735ed2d-67c4-469b-8b3e-0fac90cc4c09
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 6%

---


# 센서는 방문자 및 세션을 어떻게 식별합니까?{#how-does-sensor-identify-visitors-and-sessions}

웹 서버에서 이벤트 데이터를 수집할 때 센서는 개인적으로 식별 정보를 캡처하지 않고 작은 무작위 식별자를 포함한 각 방문자에 대해 영구 쿠키를 자동으로 설정합니다.

이 Adobe 쿠키는 고유 방문자 및 모든 관련 세션을 식별하는 데 사용됩니다.

기본적으로 각 HTTP 헤더의 모든 W3C 확장 로그 파일 형식 필드를 [!DNL Sensor] 캡처하지만 클라이언트와 서버 사이에 전송되는 모든 헤더 [!DNL Sensor] 를 캡처하도록 구성할 수 있습니다. 파일에서 수집한 이벤트 데이터 필드 [!DNL Sensor] 에 대한 자세한 내용은 이벤트 데이터 레코드 필드 [!DNL .vsl] 를 [참조하십시오](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44).

일부 방문자의 브라우저는 쿠키를 지속적으로 저장하지 않으며 매우 적은 수의 방문자의 브라우저가 쿠키를 전혀 허용하지 않습니다(세션 쿠키도 포함). 일부 로그 파일 분석 소프트웨어에서 수행한 것처럼, 방문자의 각 페이지 보기가 전체 세션으로 잘못 카운트되면 사이트 전체 트래픽의 일부만을 차지하지만 이러한 방문자의 페이지 보기가 잘못 카운트되면 심각한 오류가 발생할 수 있습니다. Adobe은 쿠키를 사용하지 않고 방문자를 분석할 수 있도록 함으로써 이 문제를 해결합니다.

끊어진 세션 필터에 대한 자세한 내용은 *Data Workbench 센서 안내서를 참조하십시오*.
