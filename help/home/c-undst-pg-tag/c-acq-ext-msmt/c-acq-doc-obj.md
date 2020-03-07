---
description: JavaScript 문서 객체 모델을 사용하면 zig.js 파일에 대한 요청을 늘리기 위해 추가 스크립팅 방법을 사용할 수 있습니다.
solution: Analytics
title: 문서 객체 가져오기
topic: Data workbench
uuid: 7681c337-b147-4937-9d9c-0ff48d9bdd00
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 문서 객체 가져오기{#acquiring-document-objects}

JavaScript 문서 객체 모델을 사용하면 zig.js 파일에 대한 요청을 늘리기 위해 추가 스크립팅 방법을 사용할 수 있습니다.

META 태그 값, DIV 태그의 ID 값 등과 같은 정보는 이름으로 참조하고 분석에 사용할 변수로 수집할 수 있습니다. 예를 들어 HTML 문서의 META 요소 내에 포함된 정보를 동적으로 캡처하려면 다음 JavaScript 구문을 사용할 수 있습니다.

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var m0 = document.getElementsByTagName('META')[0]; //define the first instance of META 
var metacontent = m0.getAttribute('content'); //get the ‘content’ value of META 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_1"] = metacontent; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_1= | METAVALUE 쿼리 문자열 변수와 연결된 값입니다. 이 값은 HTML 문서의 META 요소 내의 데이터를 나타냅니다. | v_1=이 페이지는 주문 감사 페이지 관련 컨텐츠를 제공합니다. |

데이터가 수집되면 분석 및 보고 목적으로 이 측정 데이터를 처리하도록 데이터 워크벤치 서버를 구성할 수 있습니다.
