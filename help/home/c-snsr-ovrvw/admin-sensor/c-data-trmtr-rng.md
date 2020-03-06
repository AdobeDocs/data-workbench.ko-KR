---
description: 경고를 설정하고 센서의 시스템 상태를 확인하여 송신기가 실행되고 있는지 확인합니다.
solution: Insight
title: 데이터 전송기가 실행 중인지 확인
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 전송기가 실행 중인지 확인{#confirming-that-the-data-transmitter-is-running}

경고를 설정하고 센서의 시스템 상태를 확인하여 송신기가 실행되고 있는지 확인합니다.

**권장 빈도:** 5-10분마다

* [송신기 프로세스가 실행 중인지 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Insight Server에서 관리 경고를 설정합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [센서의 시스템 상태를 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## 송신기 프로세스 확인 {#section-79806fa3b7034a8eaf571a66e24874d7}

송신기가 실행 중인지 확인하는 한 가지 방법은 인스턴스가 설치된 각 웹 서버에서 [!DNL Sensor] 송신기 프로세스가 실행 중인지 확인하는 [!DNL Sensor] 것입니다. 전송기 프로세스는 웹 서버의 프로세스 목록에 &quot;txlogd&quot;로 표시됩니다. 시스템 모니터링 도구를 사용하여 이 검사를 수행할 수 있습니다.

## 데이터 워크벤치 서버에서 관리 경고 설정 {#section-d98e0f18b8fb45a78419fe75610a3b1e}

송신기가 실행 중인지 확인하는 또 다른 방법은 에서 자동 관리 경고를 설정하는 [!DNL data workbench server]것입니다. 관리 경고가 구성되면 [!DNL data workbench server] 는 [!DNL Sensor] 파일의 경고 시간 초과(최소) 매개 변수에 지정된 기간 [!DNL Sensor] 내에 구성되거나 이전에 연결된 데이터로부터 데이터를 받지 못하면 이메일 경고를 [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg] 생성합니다. 관리 경고 설정에 대한 자세한 내용은 서버 제품 설치 *및 관리 안내서를 참조하십시오*.

## 센서의 시스템 상태 확인 {#section-de9d7e359242487a9fbead4ed65aebbc}

그러나 전송기가 실행 중인지 확인하는 또 다른 방법은 데이터 워크벤치에서 수동으로 [!DNL Servers Manager] 체크하는 것입니다.

**To view the[!DNL Servers Manager]**

* 데이터 워크벤치에서 작업 공간 내에서 마우스 오른쪽 단추를 클릭하고 **[!UICONTROL Admin]**&#x200B;클릭한 다음 [!DNL Manage]아래에서 을 **[!UICONTROL Servers]**&#x200B;클릭합니다.

아이콘의 아이콘이 [!DNL Sensor] 녹색이면 송신기가 실행 중입니다.

자세한 내용은 데이터 워크벤치 [!DNL Servers Manager]안내서의 관리 *인터페이스 장을[!DNL Sensor]참조하십시오*.
