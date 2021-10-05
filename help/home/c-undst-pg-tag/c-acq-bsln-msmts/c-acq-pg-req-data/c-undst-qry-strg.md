---
description: HTTP의 상태를 저장하지 않는 특성으로 인해 쿼리 문자열(cs-uri-query)은 웹 애플리케이션 및 사이트 개발자가 페이지에서 페이지로 정보를 전달하는 데 종종 사용됩니다.
title: 쿼리 문자열 이해
uuid: 7403277d-fbce-4e98-bd42-894142e38d0d
exl-id: b5281e5f-3eb7-4d6a-a7b3-9958cb430621
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 2%

---

# 쿼리 문자열 이해{#understanding-the-query-string}

HTTP의 상태를 저장하지 않는 특성으로 인해 쿼리 문자열(cs-uri-query)은 웹 애플리케이션 및 사이트 개발자가 페이지에서 페이지로 정보를 전달하는 데 종종 사용됩니다.

대부분의 경우 웹 서버에서 [!DNL Sensor]이 정보를 획득하면 쿼리 문자열에 정보가 전달될 수 있습니다. 이러한 정보는 [!DNL Site]에서 사이트의 실제 구조 및 이를 통한 방문자의 경로 및 기타 정보를 조명하는 데 사용할 수 있습니다.

일부 다이내믹 웹 사이트에서는 방문자가 요청하는 실제 페이지를 결정하는 데 쿼리 문자열의 이름=값 쌍(변수)이 중요합니다. 이러한 경우 URL은 다음 또는 유사한 방식으로 구조화할 수 있습니다.

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
```

이 예에서 PAGENAME은 실제로 이 URL의 요청자에게 제공될 페이지의 표시입니다. 많은 웹 로그 분석 도구 및 서비스는 사이트 URL의 쿼리 문자열에서 발생하는 쿼리 문자열 변수를 기반으로 사이트 운영자가 사이트에 있는 페이지를 정의하는 기능을 제한합니다. Data Workbench 서버 및 Data Workbench는 이러한 쿼리 이름을 사용하여 고유한 페이지를 정의하도록 구성할 수 있습니다. 많은 시스템이 다음 URL을 동일한 페이지로 해석하지만 [!DNL Site]은 해석하지 않으므로 중요합니다.

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
https://www.myserver.com/pageserved.asp?PAGENAME=HOME2
```

마찬가지로, 사이트 개발자 및 애플리케이션은 종종 요청 중인 실제 페이지를 식별하는 것과 관련이 없는 많은 쿼리 문자열 변수를 사이트의 URL에 추가합니다. 예는 다음과 같습니다.

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10001
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10002
https://www.myserver.com/pageserved.asp?PAGENAME=HOME&CAMPAIGN=10003
```

이 예에서 쿼리 문자열 변수 CAMPAIGN=가 URL에 추가되었습니다. 이 CAMPAIGN 변수는 방문자가 이 URL을 선택하도록 한 마케팅 캠페인을 나타내는 데 사용됩니다. [!DNL Site] 은 이 CAMPAIGN 정보를 사용하도록 구성하되, 보고 및 분석 목적으로 페이지 목록에서 다음을 간단히 볼 수 있도록 방문자가 본 페이지의 정의와 분리할 수 있습니다.

```
https://www.myserver.com/pageserved.asp?PAGENAME=HOME
```
