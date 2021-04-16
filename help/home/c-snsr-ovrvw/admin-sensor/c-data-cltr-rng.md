---
description: 컬렉터가 다른 메서드를 사용하여 실행되고 있는지 확인합니다.
title: 데이터 수집기가 실행 중인지 확인
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
exl-id: 1235d741-1ddf-4a65-8377-3d8a9b4ba0d3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 3%

---

# 데이터 수집기가 실행 중인지 확인{#confirming-that-the-data-collector-is-running}

컬렉터가 다른 메서드를 사용하여 실행되고 있는지 확인합니다.

**권장 빈도:** 5-10분마다

* [전송기에서 사이트 테스트 기능을 사용합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [쿠키  [!DNL Sensor] 설정 여부를 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## 사이트 테스트 사용 {#section-a5a697c3252e40f184c0b662926170f2}

컬렉터가 실행 중인지 확인하는 한 가지 방법은 전송기에서 사이트 테스트 함수를 활성화하는 것입니다. 사이트 테스트를 활성화하면 전송기가 정기적으로(60초마다) 컬렉터가 실행 중인 웹 서버에 GET 요청을 전송합니다. 사이트 테스트가 웹 서버에서 응답을 받지 못하면 syslog에 오류 메시지를 쓰고 [!DNL data workbench server](센서 로그 파일에 기록됨)에 오류 메시지를 보냅니다.

사이트 테스트가 웹 서버로부터 응답을 받으면 큐 파일에서 웹 서버의 패킷을 확인합니다. 패킷이 나타나지 않으면(컬렉터가 이벤트를 캡처하기 위해 실행 중이지 않았음을 표시), 사이트 테스트는 syslog에 오류 메시지를 기록하고 센서 로그 파일에도 기록되는 오류 메시지를 Adobe에 보냅니다.

사이트 테스트가 웹 서버로 보내는 요청에서 사이트 테스트는 사용자 에이전트 값을 &quot;[!DNL Sensor] 테스트&quot;로 설정합니다. 이러한 요청을 데이터 세트에 표시하지 않으려면 &quot;[!DNL Sensor] Test&quot; 사용자 에이전트를 [!DNL Baseline Robots List.txt] 파일에 추가하거나 [!DNL data workbench server]의 [!DNL Lookups] 폴더에 있는 [!DNL Extended Robots List.txt] 파일을 추가합니다.

**전송기에서 사이트 테스트를 활성화하려면**

1. [!DNL Sensor]이(가) 실행 중인 컴퓨터에서 [!DNL txlogd.conf] 파일을 찾아 텍스트 편집기에서 엽니다.

1. [!DNL txlogd.conf] 파일에서 &quot;SiteTest&quot; 행을 찾아 아래와 같이 구성합니다. [!DNL txlogd.conf] 파일에 &quot;SiteTest&quot; 라인이 포함되어 있지 않으면 구성 파일의 끝에 행을 추가하면 됩니다.

   SiteTest http, *serverAddress*, *포트*, *resource*

   여기서 *serverAddress*&#x200B;는 웹 서버의 이름 또는 IP 주소이고, *포트*&#x200B;는 서버의 HTTP 수신 대기 포트이고, *resource*&#x200B;는 사이트 테스트가 서버를 테스트할 때 요청하려는 특정 리소스입니다. *resource*&#x200B;에는 쿼리 문자열이 포함될 수 있습니다.

   예:SiteTest http,localhost,80,/index.jsp

   여러 웹 서버를 테스트하려면 여러 SiteTest 라인을 지정하기만 하면 됩니다.

## 쿠키 확인 중 {#section-365a0182474c4dc9a5372d3e984f53de}

컬렉터가 웹 서버에서 실행 중인지 확인하는 또 다른 방법은 웹 서버가 클라이언트에 돌아오는 응답에서 [!DNL Sensor]이(가) 쿠키를 설정하는지 여부를 확인하는 것입니다. 컬렉터가 작동하는 경우 웹 서버는 &quot;v1st&quot; 쿠키를 반환합니다.

쿠키의 이름을 바꿀 수 있습니다. 이렇게 한 경우 v1가 아닌 지정된 이름을 검색해야 합니다.

자동화된 스크립트 또는 모니터링 에이전트를 사용하여 이 검사를 수행할 수 있습니다. 이 작업에 대한 샘플 스크립트 또는 추가 도움이 필요하면 Adobe 컨설팅 서비스에 문의하십시오.
