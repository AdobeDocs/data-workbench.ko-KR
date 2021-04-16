---
description: 요청 시 추가 측정을 수집하도록 쿼리 문자열 변수를 JavaScript 요청에 추가할 수 있습니다.
title: 추가 정보 가져오기
uuid: 0a8075e9-4986-42c4-b505-3985b433cf8e
exl-id: ad4f5e08-b7b7-4de3-b0c2-71440facb2d1
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---

# 추가 정보 가져오기{#acquiring-additional-information}

요청 시 추가 측정을 수집하도록 쿼리 문자열 변수를 JavaScript 요청에 추가할 수 있습니다.

이러한 변수는 페이지 자체에서 수동으로 또는 스크립트로 추가할 수 있습니다.

다음 코드를 예로 들어 스크립트를 사용하여 포함된 개체에 페이지에서 취득할 수 있는 추가 정보를 추가할 수 있습니다.

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
var v = {}; 
v["_pn"] = "Application Form"; 
v["_1"] = “99.99”; 
v["_2"] = "visa"; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
<noscript> 
 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
<!-- END REFERENCE PAGE TAG-->
```

이 예에서 v_1 및 v_2에 대한 스크립트 변수는 웹 페이지 내의 다른 함수에서 파생될 수 있습니다. 변수가 예로 삽입되었습니다. 각 요청에서 얻은 기준 측정 외에 위의 URL의 요청과 함께 다음과 같은 확장 측정을 획득합니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_pn= | v_pn 쿼리 문자열 변수와 연결된 값 | v_pn=응용 프로그램 양식 |
| v_1= | v_1 쿼리 문자열 변수와 연결된 값 | v_1=99.99 |
| v_2= | v_2 쿼리 문자열 변수와 연결된 값 | v_2=visa |
