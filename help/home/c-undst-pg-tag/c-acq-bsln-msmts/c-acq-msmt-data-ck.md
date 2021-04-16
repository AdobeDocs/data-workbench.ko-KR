---
description: 수집된 기준선 측정 데이터의 일부로서 센서는 웹 서버로부터 요청을 할 때 방문자의 컴퓨터에서 전송된 도메인 쿠키를 수집합니다.
title: 쿠키를 통해 측정 데이터 가져오기
uuid: 34cd6baf-6317-4774-8165-58208698b53c
exl-id: 37c7b5f6-33bf-4373-963a-e08a826e05df
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 2%

---

# 쿠키를 통해 측정 데이터 가져오기{#acquiring-measurement-data-through-cookies}

수집된 기준선 측정 데이터의 일부로서 센서는 웹 서버로부터 요청을 할 때 방문자의 컴퓨터에서 전송된 도메인 쿠키를 수집합니다.

여기에는 방문자가 시스템과 상호 작용할 때 웹 사이트에서 설정하는 지속적인 쿠키와 세션 쿠키가 모두 포함됩니다.

대부분의 경우, 웹 사이트는 방문자를 식별하거나 후속 방문자 세션 내에서 사용할 사용자 입력을 캡처하도록 영구 쿠키를 설정합니다. 영구 쿠키에 기록되고 저장된 모든 정보는 데이터 워크벤치 서버 내의 다른 모든 측정 데이터와 함께 캡처하여 사용할 수 있습니다.

이러한 영구 쿠키의 예는 방문자의 컴퓨터에 있는 도메인 특정 쿠키 내에 있는 숫자 키 형태로 고객 식별자를 포함할 수 있습니다. 사용자를 재방문자로 식별하는 것 외에도, 영구 쿠키를 사용하여 방문자를 재방문자로 더 식별하거나 방문자를 고객 데이터베이스 내에 포함된 정보에 연결하여 오프라인 고객 통계 정보를 [!DNL Site] 내에 표시하고 대화형 분석에 사용할 수 있습니다.

세션 쿠키는 웹 사이트 내의 양식 필드 또는 기타 다이내믹한 인터랙티브 요소를 통해 사용자 입력을 수집하는 좋은 메커니즘이 될 수 있습니다. 사용자 특정 입력 데이터를 캡처하기 위해 양식을 구현하는 웹 사이트의 경우 세션이 활성 상태인 경우에만 세션 쿠키에 정보가 남아 있습니다. 사용자가 웹 사이트를 떠나거나 나중에 세션을 종료하면 정보는 더 이상 사용자의 컴퓨터에 저장되지 않습니다. 그러나 입력한 정보는 [!DNL Sensor]에 의해 캡처되고 [!DNL Site] 내에 측정 데이터로 사용할 수 있습니다.

다음은 세션 쿠키를 사용하여 방문자가 입력한 단일 양식 변수를 캡처하는 예입니다.

```
<html> 
<head> 
<title>Cookie Collection </title> 
 
<script language="JavaScript"> 
function AppendFormValues() 
{ 
 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
document.cookie = cookie; 
 
testform.submit(); 
 
} 
</script> 
</head> 
<body> 
<form name="testform" method="post" action="nextpage.asp"> 
<input type="text" size=15 name="name"><br />enter name 
<br><br> 
 
<a href="javascript:AppendFormValues();">Click Here To </a><br /><br /> 
<br /><br /><br /> 
 
</body> 
</html> 
```

이 예제에서 필드 이름과 양식 필드에 입력된 값을 사용하여 방문자의 컴퓨터에서 세션 쿠키를 설정하기 위해 함수가 호출됩니다. 양식이 제출되고 그 다음 웹 페이지가 요청되면 세션 쿠키 세트가 웹 서버로 전달되어 [!DNL Sensor]에 의해 수집됩니다. 따라서 데이터 워크벤치 서버 내에서 다음 데이터를 사용하여 데이터 분석에 사용할 수 있습니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_1 | v_1 쿠키와 연결된 값입니다. 이 값은 세션 쿠키가 설정되는 결과를 초래하는 양식 필드에 입력한 NAME을 나타냅니다. | v_1=John Smith |

또한 세션 쿠키를 사용하여 양식 필드 또는 HTML 페이지에 있는 여러 가지 포함된 JavaScript 변수를 반복적으로 캡처할 수도 있습니다. 다음 예에서 JavaScript는 HTML 파일 내에 있는 모든 양식 필드를 재귀적으로 캡처하고 적절한 이름=값 쌍으로 세션 쿠키를 설정하는 데 사용됩니다.

```
<script language="JavaScript"> 
 
function AppendFormValues() 
{ 
 
var cookie="formcookie="; 
for (i=0; i<document.testform.length; i++){ 
if (document.testform.elements[i].type =="radio") {            
if (document.testform.elements[i].checked){ 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
} 
} 
else if (document.testform.elements[i].type =="select") { 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var optionindex = eval(document.testform.elements[i].selectedIndex); 
var formvalue = document.testform.elements[i].options[optionindex].value;             
cookie += formitem + "=" + formvalue + "&"; 
} 
else{ 
var item = document.testform.elements[i]; 
var formitem = “v_”+i; 
var formvalue = item.value; 
cookie += formitem + "=" + formvalue + "&"; 
} 
} 
document.cookie = cookie; 
document.testform.submit(); 
} 
 
</script>
```

이 예에서, 세션 쿠키는 양식 내에 있는 모든 양식 필드의 이름과 값으로 방문자의 컴퓨터에 설정됩니다. 여기에는 입력 필드, 확인란, 라디오 단추, 선택 상자 및 텍스트 영역이 포함됩니다. 이 예에서 알 수 있듯이 양식 필드의 수를 알 수 없으므로 모든 양식 이름과 필드 값을 앰퍼샌드로 구분된 단일 문자열로 캡처해야 합니다. 이 단계는 사용자가 한 번에 자신의 컴퓨터에서 가질 수 있는 쿠키 수에 대한 제한 때문에 수행해야 합니다. Microsoft Internet Explorer는 가장 오래된 쿠키를 삭제하기 전에 20개의 세션 쿠키만 표시할 수 있도록 허용합니다.
