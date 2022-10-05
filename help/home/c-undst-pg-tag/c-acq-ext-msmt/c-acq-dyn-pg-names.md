---
description: 일부 사이트의 경우, 실제로 제공된 페이지에 대한 세부 정보를 센서가 획득하여 보고 및 분석에 사용할 수 있도록 포함된 개체 요청을 사용하여 웹 서버에 정보를 전달해야 합니다.
title: 동적 페이지 이름 가져오기
uuid: eaa35023-bbfa-4eb9-9ab7-3986187e5537
exl-id: cd94caf0-b0dc-46c1-8f59-3ebb2f703286
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 1%

---

# 동적 페이지 이름 가져오기{#acquiring-dynamic-page-names}

{{eol}}

일부 사이트의 경우, 실제로 제공된 페이지에 대한 세부 정보를 센서가 획득하여 보고 및 분석에 사용할 수 있도록 포함된 개체 요청을 사용하여 웹 서버에 정보를 전달해야 합니다.

웹 서버에서 볼 수 있는 페이지의 URL이 브라우저에 표시되는 페이지 컨텐츠를 나타내지 않는 경우 이 필요가 있을 수 있습니다. 이 경우 개인화 또는 동적 컨텐츠 관리 시스템을 사용하여 페이지에서 제공되는 실제 컨텐츠는 URL, 쿠키, 관련 데이터 및 애플리케이션 로직에 의해 즉시 결정됩니다.

추가 측정을 수집하기 위해 포함된 개체를 구현하면 전체 사이트 성능에 미치는 영향을 최소화할 수 있습니다. Adobe은 확장 속성을 수집하는 데 사용되는 개체로 JavaScript 파일을 포함하는 것을 제안합니다. (JavaScript 파일은 포함된 이미지를 사용할 경우 웹 페이지의 레이아웃 및 프레젠테이션에 영향을 줄 수 없는 경우 포함할 수 있습니다.) 포함된 개체 내에서 전달된 정보를 정확하게 캡처하기 위해 Adobe은 공통 이름을 사용할 것을 제안합니다. Adobe은 이름 지정을 위해 이 객체를 [!DNL zig.js]. 다음 [!DNL zig.js] 파일은 웹 서버의 해당 디렉토리 내에 만들어야 합니다. [!DNL Sensor] 가 설치되어 있습니다. 요청이 404 오류 코드를 반환하지 않도록 이 파일이 있어야 합니다. 파일 자체의 내용은 중요하지 않습니다. 이름이 인 빈 파일을 사용해야 합니다. [!DNL zig.js] 요청 결과로 발생하는 네트워크 트래픽의 양을 최소화하기 위한 것입니다.

대상 [!DNL Sensor] 실제로 제공된 페이지에 대해 사용 가능한 이름을 수집하려면 추적하려는 동적 페이지 또는 고유한 페이지 이름을 추가할 JavaScript 코드 행을 추가해야 합니다. 이 코드에는 JavaScript의 코드 조각이 페이지에 삽입되어 페이지가 로드될 때 세 번째 포함된 개체 요청이 웹 서버에 수행됩니다. 이 요청은 웹 서버에 다시 제공된 특정 페이지에 대한 세부 정보를 보냅니다. 실제로 제공된 페이지의 이름은 포함된 객체의 쿼리 문자열(이 경우 JavaScript) 요청에 변수로 웹 서버에 다시 전달됩니다.

일반적으로 이러한 각 HTML 페이지에 포함된 개체 요청은 다음과 같아야 합니다.

```
<!-- BEGIN REFERENCE PAGE TAG-->
<script language="javascript">
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE
var v = {};
v["_pn"] = "Application Form";
</script>

<script language="javascript" src=”https://www.myserver.com/path/to/zig.js" type="text/javascript"></script>

<noscript>
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/>
</noscript>

<!-- END REFERENCE PAGE TAG-->
```

[!DNL Log=1] 는 [!DNL Sensor] 이 에도 불구하고 요청을 기록하다 [!DNL Sensor] 컨텐츠 유형 필터링 규칙은 반대로 필터링합니다(예: JavaScript에서 필터링 및 저장 전 이미지 요청). 선언된 v_pn 변수는 다음과 같이 제공되는 실제 페이지 컨텐츠의 이름을 식별합니다 [!DNL Site] 방문자가 실제로 본 페이지의 이름을 알아봅니다. v_pn 값은 수동으로 설정하거나 다른 스크립트나 응용 프로그램 코드로 설정할 수 있습니다.

값이 수집되면 Data Workbench 서버가 쿼리 문자열 변수의 내용(예: 이름=값 쌍)을 사용할 수 있도록 구성할 수 있습니다. 예를 들어, v_pn=Application Form) [!DNL zag.gif] URI(예: [!DNL https://www.mysite.com/pageserved.asp?v_pn=Application%20Form]) 를 채울 수 있습니다. [!DNL zag.gif] URI. 모든 HTTP 요청으로 획득된 기본 측정 외에도 이 요청으로 확장 측정을 획득합니다.

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_pn= | v_pn 쿼리 문자열 변수와 연결된 값 | v_pn=응용 프로그램 양식 |
