---
description: 요청이 수행될 때 추가적인 측정을 수집하기 위해 쿼리 문자열 변수를 JavaScript 요청에 추가할 수 있습니다.
title: 추가 정보 가져오기
uuid: 0a8075e9-4986-42c4-b505-3985b433cf8e
exl-id: ad4f5e08-b7b7-4de3-b0c2-71440facb2d1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---

# 추가 정보 가져오기{#acquiring-additional-information}

요청이 수행될 때 추가적인 측정을 수집하기 위해 쿼리 문자열 변수를 JavaScript 요청에 추가할 수 있습니다.

이러한 변수는 수동으로 또는 페이지 자체의 스크립트로 추가할 수 있습니다.

예를 들어 다음 코드를 사용하여 스크립트를 통해 포함된 개체에 페이지에서 획득할 수 있는 추가 정보를 추가할 수 있습니다.

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

이 예에서 v_1 및 v_2의 스크립트 변수는 웹 페이지 내의 다른 함수에서 파생될 수 있습니다. 변수가 예제로 삽입되었습니다. 각 요청에서 획득한 기준 측정 외에, 위의 URL의 요청과 함께 다음과 같은 확장 측정 수를 획득합니다.

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_pn= | v_pn 쿼리 문자열 변수와 연결된 값 | v_pn=응용 프로그램 양식 |
| v_1= | v_1 쿼리 문자열 변수와 연결된 값 | v_1=99.99 |
| v_2= | v_2 쿼리 문자열 변수와 연결된 값 | v_2=visa |
