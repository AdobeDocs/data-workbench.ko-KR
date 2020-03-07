---
description: 쿼리 문자열(cs-uri-query)은 HTTP의 상태 비저장 특성 때문에 웹 애플리케이션 및 사이트 개발자가 페이지에서 페이지로 정보를 전달하는 데 사용되는 경우가 많습니다.
solution: Analytics
title: 쿼리 문자열 이해
topic: Data workbench
uuid: 7403277d-fbce-4e98-bd42-894142e38d0d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 쿼리 문자열 이해{#understanding-the-query-string}

쿼리 문자열(cs-uri-query)은 HTTP의 상태 비저장 특성 때문에 웹 애플리케이션 및 사이트 개발자가 페이지에서 페이지로 정보를 전달하는 데 사용되는 경우가 많습니다.

대부분의 경우, 정보를 웹 서버에서 가져올 때 쿼리 문자열에 전달할 [!DNL Sensor] 수 있습니다. 이러한 정보는 사이트의 실제 구조와 방문자의 경로 및 기타 정보를 [!DNL Site] 비추는 데 사용할 수 있습니다.

일부 동적 웹 사이트에서, 쿼리 문자열의 name=value pairs(변수)는 방문자가 요청하는 실제 페이지를 결정하는 데 중요합니다. 이러한 경우 URL은 다음 또는 유사한 방식으로 구성할 수 있습니다.

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

이 예에서, PAGENAME은 실제로 어떤 페이지가 이 URL의 요청자에게 제공될 것인지를 나타내는 지표입니다. 많은 웹 로그 분석 도구 및 서비스는 사이트 URL의 쿼리 문자열에서 발생하는 쿼리 문자열 변수를 기준으로 사이트 운영자가 사이트의 페이지를 정의하는 기능을 제한합니다. 데이터 워크벤치 서버 및 데이터 워크벤치는 이러한 쿼리 이름을 사용하여 고유 페이지를 정의하도록 구성할 수 있습니다. 많은 시스템에서 다음 URL을 동일한 페이지로 해석하지만 해석하지는 않기 때문에 중요합니다. [!DNL Site]

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
http://www.myserver.com/pageserved.asp?PAGENAME=HOME2
```

마찬가지로 사이트 개발자와 애플리케이션은 요청 중인 실제 페이지를 식별하는 것과 관련이 없는 많은 쿼리 문자열 변수를 사이트의 URL에 추가하는 경우가 많습니다. 예는 다음과 같습니다.

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10001
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10002
http://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10003
```

이 예에서 쿼리 문자열 변수 CAMPAIGN=가 URL에 추가되었습니다. 이 CAMPAIGN 변수는 방문자가 이 URL을 선택하도록 한 마케팅 캠페인을 나타내는 데 사용됩니다. [!DNL Site] 이 캠페인 정보를 사용하도록 구성하되, 보고 및 분석을 위해 페이지 목록에서 다음을 볼 수 있도록 방문자가 본 페이지의 정의와는 별도로 지정할 수 있습니다.

```
http://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

