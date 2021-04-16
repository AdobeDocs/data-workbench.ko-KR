---
description: 일부 사이트의 경우, 정보를 웹 서버로 전달하기 위해 포함된 개체 요청을 사용하여 실제로 제공된 페이지에 대한 세부 정보를 센서가 입수하고 보고 및 분석에 사용할 수 있도록 해야 합니다.
title: 동적 페이지 이름 가져오기
uuid: eaa35023-bbfa-4eb9-9ab7-3986187e5537
exl-id: cd94caf0-b0dc-46c1-8f59-3ebb2f703286
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 1%

---

# 동적 페이지 이름 가져오기{#acquiring-dynamic-page-names}

일부 사이트의 경우, 정보를 웹 서버로 전달하기 위해 포함된 개체 요청을 사용하여 실제로 제공된 페이지에 대한 세부 정보를 센서가 입수하고 보고 및 분석에 사용할 수 있도록 해야 합니다.

웹 서버에서 볼 수 있는 페이지의 URL이 브라우저에 표시되는 페이지 컨텐츠를 나타내지 않는 경우에 필요할 수 있습니다. 이러한 경우는 개인화 또는 동적 컨텐츠 관리 시스템을 사용하여 페이지에서 제공된 실제 컨텐츠가 URL, 쿠키, 관련 데이터 및 애플리케이션 로직에 의해 신속하게 결정되며,

추가 측정을 수집하기 위해 포함된 개체를 구현하면 전반적인 사이트 성능에 미치는 영향이 최소화됩니다. Adobe에서는 JavaScript 파일을 확장 속성을 수집하는 데 사용되는 객체로 포함시키는 것이 좋습니다. (JavaScript 파일은 포함된 이미지를 사용할 경우 웹 페이지의 레이아웃 및 프레젠테이션에 영향을 미치지 않고 포함할 수 있습니다.) 포함된 개체 내에서 전달된 정보를 정확하게 캡처하기 위해 Adobe에서는 공통 이름을 사용하는 것이 좋습니다. 이름 지정을 위해 Adobe은 이 개체를 [!DNL zig.js]으로 참조합니다. [!DNL zig.js] 파일은 [!DNL Sensor]이(가) 설치된 웹 서버의 해당 디렉터리 내에 만들어야 합니다. 요청에서 404 오류 코드를 반환하지 않도록 이 파일이 있어야 합니다. 파일 자체의 내용은 중요하지 않습니다. [!DNL zig.js]이라는 빈 파일을 사용하여 요청의 결과로 발생하는 네트워크 트래픽의 양을 최소화해야 합니다.

[!DNL Sensor]이(가) 실제로 제공된 페이지에 대한 사용 가능한 이름을 수집하려면 추적할 동적 페이지 또는 고유한 페이지 이름을 추가할 동적 페이지에 몇 줄의 JavaScript 코드를 추가해야 합니다. 이 코드는 페이지에 JavaScript의 코드 조각을 포함하므로, 페이지가 로드될 때 세 번째 포함된 개체 요청이 웹 서버에 이루어지도록 합니다. 해당 요청은 웹 서버로 다시 제공된 특정 페이지에 대한 세부 정보를 보냅니다. 실제로 제공된 페이지의 이름은 포함된 객체(이 경우 JavaScript) 요청의 쿼리 문자열에 있는 변수로 웹 서버로 전달됩니다.

일반적으로 이러한 각 HTML 페이지에 포함된 개체 요청은 다음과 같아야 합니다.

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_pn"] = "Application Form"; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

[!DNL Log=1] JavaScript [!DNL Sensor] 에서 필터링하거나 이미지를 저장하기 전에 이미지 요청을 전송하는 것과 같이  [!DNL Sensor] 컨텐츠 유형 필터링 규칙을 무시하고 요청을 기록합니다. 선언된 v_pn 변수는 [!DNL Site]이 방문자가 실제로 본 페이지의 이름을 알 수 있도록 제공되는 실제 페이지 컨텐츠의 이름을 식별합니다. v_pn 값을 수동으로 또는 다른 스크립트 또는 애플리케이션 코드로 설정할 수 있습니다.

값이 수집되면 데이터 워크벤치 서버가 [!DNL zag.gif] URI의 증대로, [!DNL zag.gif] URI에 첨부된 쿼리 문자열 변수(예: v_pn=Application Form)의 내용(예: [!DNL http://www.mysite.com/pageserved.asp?v_pn=Application%20Form])을 사용하도록 구성할 수 있습니다. 모든 HTTP 요청에서 얻은 기본 측정 외에, 이 요청과 함께 확장된 측정을 획득합니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_pn= | v_pn 쿼리 문자열 변수와 연결된 값 | v_pn=응용 프로그램 양식 |
