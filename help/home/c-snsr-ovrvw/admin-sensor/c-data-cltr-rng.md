---
description: 다른 메서드를 사용하여 컬렉터가 실행 중인지 확인합니다.
solution: Insight
title: 데이터 수집기가 실행 중인지 확인
uuid: e5b9b12a-b8a5-4c00-abe5-e824516d46b7
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 데이터 수집기가 실행 중인지 확인{#confirming-that-the-data-collector-is-running}

다른 메서드를 사용하여 컬렉터가 실행 중인지 확인합니다.

**권장 빈도:** 5-10분마다

* [전송기에서 사이트 테스트 기능을 사용합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-a5a697c3252e40f184c0b662926170f2)
* [[!DNL 센서]에서 쿠키를 설정하는지 확인합니다.](../../../home/c-snsr-ovrvw/admin-sensor/c-data-cltr-rng.md#section-365a0182474c4dc9a5372d3e984f53de)

## 사이트 테스트 사용 {#section-a5a697c3252e40f184c0b662926170f2}

컬렉터가 실행 중인지 확인하는 한 가지 방법은 전송기에서 사이트 테스트 기능을 활성화하는 것입니다. 사이트 테스트를 활성화하면 전송기가 정기적으로(60초마다) 컬렉터가 실행 중인 웹 서버에 GET 요청을 전송합니다. 사이트 테스트가 웹 서버로부터 응답을 받지 못하면, syslog에 오류 메시지를 쓰고 오류 메시지를 [!DNL data workbench server] 센서 로그 파일에 기록합니다.

사이트 테스트가 웹 서버로부터 응답을 받으면, 웹 서버로부터 패킷에 대한 대기열 파일을 찾습니다. 패킷이 나타나지 않는 경우(이벤트 캡처 위해 컬렉터가 실행되고 있지 않음을 나타냅니다) 사이트 테스트는 syslog에 오류 메시지를 기록하고 Adobe에 오류 메시지를 보냅니다(센서 로그 파일에도 기록됨).

사이트 테스트가 웹 서버로 전송하는 요청에서 사이트 테스트는 사용자-에이전트 값을 &quot;테스트&quot;로 [!DNL Sensor] 설정합니다. 이러한 요청이 데이터 세트에 표시되지 않게 하려면 &quot;테스트 [!DNL Sensor] &quot; 사용자-에이전트를 파일 또는 [!DNL Baseline Robots List.txt] 폴더의 [!DNL Extended Robots List.txt] 파일에 추가합니다 [!DNL Lookups] [!DNL data workbench server].

**전송기에서 사이트 테스트를 활성화하려면**

1. 컴퓨터에서 실행 중인 [!DNL txlogd.conf] 파일을 찾아 텍스트 편집기에서 [!DNL Sensor] 엽니다.

1. 파일에서 &quot;SiteTest&quot; 줄을 찾아 아래와 같이 구성합니다. [!DNL txlogd.conf] 파일에 &quot;SiteTest&quot; 라인이 포함되어 있지 않으면 구성 파일의 끝에 행을 추가하면 됩니다. [!DNL txlogd.conf]

   SiteTest http, *serverAddress*, *포트*, *리소스*

   여기서 *server* Address는 웹 서버의 이름 또는 IP 주소이고 *포트는* 서버의 HTTP 수신 포트이며 *리소스는* 서버 테스트 시 사이트 테스트를 요청할 특정 리소스입니다. 리소스에는 ** 쿼리 문자열이 포함될 수 있습니다.

   예:SiteTest http,localhost,80,/index.jsp

   여러 웹 서버를 테스트하려면 여러 SiteTest 라인을 지정하기만 하면 됩니다.

## 쿠키 확인 {#section-365a0182474c4dc9a5372d3e984f53de}

웹 서버에서 컬렉터가 실행 중인지 확인하는 또 다른 방법은 웹 서버가 클라이언트에 반환되는 응답에서 쿠키를 [!DNL Sensor] 설정하는지 확인하는 것입니다. 컬렉터가 작동하는 경우 웹 서버는 &quot;v1st&quot; 쿠키를 반환합니다.

쿠키의 이름을 변경할 수 있습니다. 그렇게 한 경우 v1st가 아닌 지정된 이름을 찾아야 합니다.

자동화된 스크립트 또는 모니터링 에이전트를 사용하여 이 검사를 수행할 수 있습니다. 이 작업에 대한 샘플 스크립트 또는 추가 도움말은 Adobe 컨설팅 서비스에 문의하십시오.
