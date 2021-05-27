---
description: 웹 페이지에서 양식에 입력된 값은 JavaScript를 사용하여 수집된 후 이후에 요청된 페이지의 쿼리 문자열(양식 제출 시)에 추가할 수 있습니다.
title: 일반 정보
uuid: 401816a5-1d95-48e6-bedf-ee2a5dbd2d50
exl-id: 9effc72b-e75f-423c-87ec-6ac25edee8d6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 3%

---

# 일반 정보{#general-information}

웹 페이지에서 양식에 입력된 값은 JavaScript를 사용하여 수집된 후 이후에 요청된 페이지의 쿼리 문자열(양식 제출 시)에 추가할 수 있습니다.

다음 예제에 나와 있습니다. HTML 페이지에서 사용되는 양식 유효성 검사 스크립트 뒤에 이 JavaScript를 포함하십시오.

```
<html> 
<head> 
</head> 
<script language="JavaScript"> 
 
function AppendFormValues() 
{ 
 
for(var i = 0; i < document.formname.length; i++) 
{ 
var item = document.formname.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
formvalues += formitem + '=' + formvalue + '&'; 
} 
document.formname.action = document.formname.action + '?' + formvalues; 
 
} 
</script> 
<body> 
<form name="formname" action="thankyou.asp" method="POST" onSubmit="AppendFormValues();"> 
<input name="NAME" size="50" value=""></input>name<br/> 
<input name="CITY" size="50" value=""></input>city<br/> 
<input name="STATE" size="50" value=""></input>state<br/> 
<input name="ZIP" size="10" value=""></input>zip<br /> 
<input type="submit" name="submit" value="submit"/> 
</body> 
</html> 
```

이 예제에서는 브라우저 사용자가 양식에 입력한 값을 다음과 같이 FORM Action 값에 표시된 후속 &quot;confirm.asp&quot; 페이지에 추가합니다.

```
http://www.myserver.com/thankyou.asp?v_1=John Smith&v_2=Los Angeles&v_3=California&v_4=90210
```

다음 확장 측정은 [!DNL Sensor]에 의해 수집된 기준 측정 외에 이 요청과 함께 획득됩니다.

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_1 | NAME 양식 필드에 연결된 값입니다. | v_1=John Smith |
| v_2 | CITY 양식 필드에 연결된 값입니다. | v_2=로스앤젤레스 |
| v_3 | STATE 양식 필드에 연결된 값입니다. | v_3=California |
| v_4 | ZIP 양식 필드와 관련된 값입니다 | v_4=90210 |
