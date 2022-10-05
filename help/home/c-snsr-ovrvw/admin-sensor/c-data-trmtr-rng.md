---
description: 경고를 설정하고 센서의 시스템 상태를 확인하는 등의 작업을 통해 전송기가 실행 중인지 확인합니다.
title: 데이터 전송기가 실행 중인지 확인
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
exl-id: 10ba704e-85be-425f-8a5d-9429100f367d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 5%

---

# 데이터 전송기가 실행 중인지 확인{#confirming-that-the-data-transmitter-is-running}

{{eol}}

경고를 설정하고 센서의 시스템 상태를 확인하는 등의 작업을 통해 전송기가 실행 중인지 확인합니다.

**권장 빈도:** 5-10분마다

* [전송 프로세스가 실행 중인지 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Insight Server에서 관리 경고를 설정합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [센서의 시스템 상태 를 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## 송신기 프로세스 확인 {#section-79806fa3b7034a8eaf571a66e24874d7}

송신기가 실행 중인지 확인하는 한 가지 방법은 [!DNL Sensor] 전송 프로세스는 [!DNL Sensor] 인스턴스가 설치됩니다. 전송 프로세스는 웹 서버의 프로세스 목록에 &quot;txlogd&quot;로 표시됩니다. 시스템 모니터링 도구를 사용하여 이 검사를 수행할 수 있습니다.

## Data Workbench 서버에서 관리 경고 설정 {#section-d98e0f18b8fb45a78419fe75610a3b1e}

전송기가 실행 중인지 확인하는 또 다른 방법은 [!DNL data workbench server]. 관리 경고가 구성되면 [!DNL data workbench server] 구성된 사용자 및 이전에 연결된 사용자로부터 데이터를 받지 못한 경우 이메일 경고를 생성합니다 [!DNL Sensor] 에 지정된 기간 내에 [!DNL Sensor] 의 경고 시간 초과(최소) 매개 변수 [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg] 파일. 관리 경고 설정에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서*.

## 센서의 시스템 상태 확인 {#section-de9d7e359242487a9fbead4ed65aebbc}

그러나 송신기가 실행 중인지 확인하는 또 다른 방법은 [!DNL Servers Manager] Data Workbench에서 확인하십시오.

**를 보려면[!DNL Servers Manager]**

* Data Workbench에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]**, 그런 다음 아래에 [!DNL Manage]를 클릭합니다. **[!UICONTROL Servers]**.

아이콘 [!DNL Sensor] 녹색 송신기가 실행 중입니다.

에 대한 자세한 정보 [!DNL Servers Manager]를 참조하려면 *Data Workbench [!DNL Sensor] 안내서*.
