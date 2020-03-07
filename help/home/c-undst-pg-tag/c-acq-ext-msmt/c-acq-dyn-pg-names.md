---
description: 일부 사이트에서는 내장 개체 요청을 사용하여 정보를 웹 서버에 전달해야 하므로 실제로 제공된 페이지에 대한 세부 정보가 센서가 획득하여 보고 및 분석에 사용될 수 있습니다.
solution: Analytics
title: 동적 페이지 이름 가져오기
topic: Data workbench
uuid: eaa35023-bbfa-4eb9-9ab7-3986187e5537
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 동적 페이지 이름 가져오기{#acquiring-dynamic-page-names}

일부 사이트에서는 내장 개체 요청을 사용하여 정보를 웹 서버에 전달해야 하므로 실제로 제공된 페이지에 대한 세부 정보가 센서가 획득하여 보고 및 분석에 사용될 수 있습니다.

웹 서버에서 볼 수 있는 페이지의 URL이 브라우저에 표시되는 페이지 컨텐츠를 나타내지 않는 경우 이 요구 사항이 적용될 수 있습니다. 이러한 경우는 개인화 또는 다이내믹 컨텐츠 관리 시스템을 사용하여 페이지에서 제공되는 실제 컨텐츠가 URL, 쿠키, 관련 데이터 및 애플리케이션 로직에 의해 신속하게 결정되는 경우가 많습니다.

추가 측정을 수집하기 위해 포함된 개체를 구현하면 전체 사이트 성능에 미치는 영향이 최소화됩니다. JavaScript 파일을 확장 속성을 수집하는 데 사용되는 개체로 포함하는 것이 좋습니다. (JavaScript 파일은 포함된 이미지를 사용하여 웹 페이지의 레이아웃 및 프레젠테이션에 영향을 주지 않고 포함할 수 있습니다.) 포함된 개체 내에서 전달된 정보를 정확하게 캡처하기 위해 Adobe에서는 일반 이름을 사용하는 것이 좋습니다. Adobe는 이름 지정을 위해 이 개체를 [!DNL zig.js]로 참조합니다. 이 [!DNL zig.js] 파일은 설치된 웹 서버의 해당 디렉토리 내에 만들어야 [!DNL Sensor] 합니다. 요청이 404 오류 코드를 반환하지 않도록 이 파일이 있어야 합니다. 파일 자체의 내용은 중요하지 않습니다. 요청의 결과로 발생하는 네트워크 트래픽 양을 [!DNL zig.js] 최소화하려면 명명된 빈 파일을 사용해야 합니다.

실제로 제공된 페이지에 대한 사용 가능한 이름을 수집하려면 추적할 동적 페이지 또는 고유한 페이지 이름을 추가하려는 JavaScript 코드 줄을 추가해야 [!DNL Sensor] 합니다. 이 코드는 페이지에 JavaScript의 조각을 포함하므로, 페이지가 로드될 때 세 번째 포함된 개체 요청이 웹 서버에 수행됩니다. 이 요청은 웹 서버로 다시 제공된 특정 페이지에 대한 세부 정보를 전송합니다. 실제로 제공된 페이지의 이름은 포함된 개체의 쿼리 문자열(이 경우 JavaScript) 요청에 변수로 웹 서버로 다시 전달됩니다.

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

[!DNL Log=1] 컨텐츠 유형 필터링 규칙과 달리 요청을 [!DNL Sensor] [!DNL Sensor] 기록할 수 있습니다(예: JavaScript의 필터링 및 이미지 요청 저장 전). 선언된 v_pn 변수는 방문자가 실제로 본 페이지의 이름을 [!DNL Site] 알 수 있도록 제공되는 실제 페이지 컨텐츠의 이름을 식별합니다. v_pn 값은 수동으로 또는 다른 스크립트 또는 애플리케이션 코드로 설정할 수 있습니다.

값이 수집되면 데이터 워크벤치 서버가 URI의 증대로 URI에 추가된 쿼리 문자열 변수(예: v_pn=Application Form)의 컨텐츠(예: v_pn=값 쌍)를 사용하도록 구성할 수 [!DNL zag.gif] [!DNL http://www.mysite.com/pageserved.asp?v_pn=Application%20Form][!DNL zag.gif] 있습니다. 모든 HTTP 요청에서 얻은 기준 측정 외에, 이 요청과 함께 확장된 측정을 획득합니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_pn= | v_pn 쿼리 문자열 변수와 연결된 값 | v_pn=응용 프로그램 양식 |

