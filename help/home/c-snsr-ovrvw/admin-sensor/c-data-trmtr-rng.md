---
description: 경고를 설정하고 센서의 시스템 상태를 확인하여 전송기가 실행되고 있는지 확인합니다.
solution: Analytics
title: 데이터 전송기가 실행 중인지 확인
uuid: 8dd6307c-e7d2-4800-88c7-f93385b33ca5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 5%

---


# 데이터 전송기가 실행 중인지 확인{#confirming-that-the-data-transmitter-is-running}

경고를 설정하고 센서의 시스템 상태를 확인하여 전송기가 실행되고 있는지 확인합니다.

**권장 빈도:** 5-10분마다

* [송신기 프로세스가 실행 중인지 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-79806fa3b7034a8eaf571a66e24874d7)
* [Insight Server에서 관리 경고를 설정합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-d98e0f18b8fb45a78419fe75610a3b1e)
* [센서의 시스템 상태를 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-trmtr-rng.md#section-de9d7e359242487a9fbead4ed65aebbc)

## 송신기 프로세스 확인 {#section-79806fa3b7034a8eaf571a66e24874d7}

전송기가 실행 중인지 확인하는 한 가지 방법은 인스턴스가 설치된 각 웹 서버에서 [!DNL Sensor] 전송기 프로세스가 실행 중인지 확인하는 [!DNL Sensor] 것입니다. 전송기 프로세스는 웹 서버의 프로세스 목록에 &quot;txlogd&quot;로 표시됩니다. 시스템 모니터링 도구를 사용하여 이 검사를 수행할 수 있습니다.

## Data Workbench 서버에서 관리 경고 설정 {#section-d98e0f18b8fb45a78419fe75610a3b1e}

송신기가 실행 중인지 확인하는 또 다른 방법은 에서 자동화된 관리 경고를 설정하는 것입니다 [!DNL data workbench server]. 관리 경고가 구성된 경우, 관리자 [!DNL data workbench server] 는 [!DNL Sensor] 파일 [!DNL Sensor] [!DNL data workbench server’s] [!DNL Administrative Alerts.cfg] 의 경고 시간 제한(최소) 매개 변수에 지정된 기간 내에 구성되거나 이전에 연결된 데이터로부터 데이터를 받지 못하면 이메일 경고를 생성합니다. 관리 경고 설정에 대한 자세한 내용은 *서버 제품 설치 및 관리 안내서를 참조하십시오*.

## 센서의 시스템 상태 확인 {#section-de9d7e359242487a9fbead4ed65aebbc}

하지만 송신기가 실행 중임을 확인하는 또 다른 방법은 Data Workbench [!DNL Servers Manager] 에서 수동으로 체크하는 것입니다.

**To view the[!DNL Servers Manager]**

* Data Workbench에서 작업 공간 내에서 마우스 오른쪽 버튼을 클릭하고 을 클릭한 **[!UICONTROL Admin]**&#x200B;다음 아래에서 을 [!DNL Manage]클릭합니다 **[!UICONTROL Servers]**.

아이콘의 아이콘 [!DNL Sensor] 이 녹색이면 송신기가 실행 중입니다.

자세한 내용은 [!DNL Servers Manager]Data Workbench *안내서[!DNL Sensor]*&#x200B;의 관리 인터페이스 장을 참조하십시오.
