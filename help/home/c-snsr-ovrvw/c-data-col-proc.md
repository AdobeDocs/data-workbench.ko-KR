---
description: 센서는 전통적으로 데이터 수집과 관련된 많은 인적 인력을 없애고 인터넷 채널에서 데이터 획득을 자동화합니다.
solution: Analytics
title: 데이터 수집 프로세스는 어떻게 수행됩니까?
uuid: d34e5938-217b-4a1e-b96e-55a02b1c3af0
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 4%

---


# 데이터 수집 프로세스는 어떻게 수행됩니까?{#how-does-the-data-collection-process-work}

센서는 전통적으로 데이터 수집과 관련된 많은 인적 인력을 없애고 인터넷 채널에서 데이터 획득을 자동화합니다.

대부분의 경우 데이터 관리 프로세스를 크게 간소화할 [!DNL Sensor] 수 있습니다.

오늘날의 대형 인터넷, 엑스트라넷 및 인트라넷 사이트는 종종 다양한 웹 서버에서 실행됩니다. 생성되는 로그 및 데이터는 매우 크고 관리하기 어려울 수 있습니다. 예를 들어 사이트에서 30개의 웹 서버를 실행 중인 경우 일반적으로 직원(또는 아웃소싱 서비스 제공업체의 직원) 중 한 명이 각 로그 파일을 가져와서 30개의 서버에 통합한 다음 그에 대한 보고서를 실행합니다. 웹 서버 [!DNL Sensor] 에 설치하는 작업은 이 전체 프로세스를 자동화하여 비용을 줄이고 데이터를 실시간으로 사용할 수 있습니다.

이 프로세스를 자동화하려면 각 웹 서버에서 직접 웹 사이트의 트래픽에 대한 원시 정보를 수집합니다 [!DNL Sensor] . 캡처하는 원시 데이터를 이벤트 데이터라고 하며 웹 서버가 로그 파일에 기록하는 데이터 유형과 비슷합니다. [!DNL Sensor]

이 데이터를 캡처하려면 웹 서버가 처리하는 각 HTTP 요청에 대한 정보 내에 계기를 [!DNL Sensor] 삽입합니다. [!DNL Sensor] 그런 다음 정보를 버퍼링하여 네트워크 장애로부터 보호하고 HTTP/S를 통해 지정한 주소로 정보를 안전하게 전송합니다 [!DNL data workbench server] .

데이터 [!DNL data workbench server] 를 받은 후 로그 파일을 압축률이 높은 [!DNL .vsl] 포맷 파일로 처리 및 저장하므로 저렴한 하드웨어에서 대량의 데이터를 손쉽게 유지 관리할 수 있습니다.

파일에서 수집한 이벤트 데이터 필드 [!DNL Sensor] 에 대한 자세한 내용은 이벤트 데이터 레코드 필드 [!DNL .vsl] 를 [참조하십시오](../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-evnt-data-rcd-flds.md#concept-ed2a8797cb5b4995b55ffd50a9f12a44).
