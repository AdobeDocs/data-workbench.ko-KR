---
description: Sensor 구성 파일 txlogd.conf에는 Sensor가 Data Workbench 서버와의 연결을 설정하는 데 사용하는 매개 변수가 포함되어 있습니다.
title: Sensor txlogd.conf 파일 편집
uuid: e7f41c14-9047-4e1a-be0f-8acc8ecb1160
exl-id: ed243bb4-cf87-4bcf-89d6-5ff5cec3bc6e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 3%

---

# Sensor txlogd.conf 파일 편집{#editing-the-sensor-txlogd-conf-file}

{{eol}}

Sensor 구성 파일 txlogd.conf에는 Sensor가 Data Workbench 서버와의 연결을 설정하는 데 사용하는 매개 변수가 포함되어 있습니다.

이러한 매개 변수에는 서버의 주소, 포트 번호 및 통신 프로토콜(HTTP 또는 HTTPS)이 포함됩니다. 구성 파일에는 로그 컨텐츠 필터링 옵션과 통제 실험 정보도 포함되어 있습니다. 제어된 실험을 통해 사이트 디자이너는 모든 사이트 방문자의 하위 집합에 대해 컨텐츠 또는 디자인 변경 사항을 테스트하는 실험을 수행할 수 있습니다.

다른 항목을 변경할 때 [!DNL txlogd.conf] 매개 변수(예: [!DNL data workbench server] 또는 의 이름 [!DNL Sensor]를 교체하는 것이 가능하다면 [!DNL txlogd.conf] 업데이트된 버전 및 [!DNL Sensor] 은(는) 자동으로 변경 사항을 선택합니다. 일부 시스템에서는 웹 서버나 전송 프로세스를 중지하지 않고 파일을 편집하거나 바꿀 수 없습니다.

**txlogd.conf를 열고 편집하려면**

1. 다음 위치로 이동합니다. [!DNL Sensor] 설치 디렉토리 및 열기 [!DNL txlogd.conf] 파일을 텍스트 편집기에 저장합니다.
1. 필요에 따라 파일을 편집합니다.
1. 파일을 저장하고 닫습니다.

   * 제어 실험 구성 파일(ExpFile 매개 변수에 의해 정의됨)의 위치입니다 [!DNL txlogd.conf] 파일)은 웹 컨텐츠 개발자가 액세스하거나 컨텐츠 관리 시스템에서 제어하는 웹 서버의 디렉토리에 있어야 합니다.
   * ExpCookieURL 매개 변수의 값은 웹 사이트를 테스트하는 데 사용되는 가상 페이지입니다. 해당 페이지를 방문하는 사용자에게 새 추적 ID가 제공됩니다.

작업 방법에 대한 자세한 내용 [!DNL txlogd.conf], Adobe 컨설팅 서비스에 문의하십시오.
