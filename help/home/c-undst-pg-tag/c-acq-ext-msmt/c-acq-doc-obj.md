---
description: JavaScript Document Object Model을 사용하여 추가 스크립팅 메서드를 사용하여 zig.js 파일에 대한 요청을 늘릴 수 있습니다.
title: 문서 객체 가져오기
uuid: 7681c337-b147-4937-9d9c-0ff48d9bdd00
exl-id: eae6609c-be86-44cf-a1a1-69ffb43231fa
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 5%

---

# 문서 객체 가져오기{#acquiring-document-objects}

JavaScript Document Object Model을 사용하여 추가 스크립팅 메서드를 사용하여 zig.js 파일에 대한 요청을 늘릴 수 있습니다.

META 태그 값, DIV 태그의 ID 값 등과 같은 정보는 이름별로 참조하고 분석에 사용할 변수로 수집할 수 있습니다. 예를 들어 HTML 문서의 META 요소 내에 포함된 정보를 동적으로 캡처하려면 다음 JavaScript 구문을 사용할 수 있습니다.

```
<!-- BEGIN REFERENCE PAGE TAG-->
<script language="javascript">
var m0 = document.getElementsByTagName('META')[0]; //define the first instance of META
var metacontent = m0.getAttribute('content'); //get the ‘content’ value of META
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE
var v = {};
v["_1"] = metacontent;
</script>

<script language="javascript" src=”https://www.myserver.com/path/to/zig.js" type="text/javascript"></script>

<noscript>
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/>
</noscript>

<!-- END REFERENCE PAGE TAG-->
```

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_1= | METAVALUE 쿼리 문자열 변수와 연결된 값입니다. 이 값은 HTML 문서의 META 요소 내에 있는 데이터를 나타냅니다. | v_1=이 페이지는 주문 감사 인사 페이지와 관련된 컨텐츠를 제공합니다. |

데이터가 수집되면 분석 및 보고를 위해 이 측정 데이터를 처리하도록 Data Workbench 서버를 구성할 수 있습니다.
