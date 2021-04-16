---
description: 웹 페이지는 종종 ASP(Active Server Pages) 프로그래밍 언어를 사용하여 구조화됩니다.
title: ASP별 정보
uuid: 552288cb-b775-4121-8869-322f2a26932b
exl-id: f73235e1-d44a-4056-b1f4-a86879c19483
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 1%

---

# ASP별 정보{#asp-specific-information}

웹 페이지는 종종 ASP(Active Server Pages) 프로그래밍 언어를 사용하여 구조화됩니다.

ASP는 IIS(인터넷 정보 서비스) 내에서 실행되는 Microsoft 기술입니다. 브라우저가 ASP 파일을 요청하면 IIS는 요청을 ASP 엔진에 전달합니다. ASP 엔진은 ASP 파일을 순서대로 읽고 파일에서 스크립트를 실행합니다. 마지막으로 ASP 파일이 일반 HTML로 브라우저에 반환됩니다. ASP는 RESPONSE 또는 REQUEST 개체를 제공하여 다른 용도 외에도 HTML 양식에서 제출한 사용자 쿼리 또는 데이터에 대한 응답이나 요청을 허용합니다.

경우에 따라, 사용자 브라우저의 주소 표시줄에 표시되거나 HTML 코드 자체에 표시될 수 있는 양식에 입력된 값을 URL에 추가하지 않을 수 있습니다. 간단한 서버측 JavaScript를 사용하면 사용자의 브라우저에서 사용할 수 있도록 하거나 HTML 파일에 포함하지 않고도 양식 필드 이름과 해당 값을 로그 파일에 추가할 수 있습니다. 웹 사이트 내의 특정 양식에 입력된 실제 양식 값을 캡처하려면 몇 줄의 코드를 추가하여 양식 값을 로그 요청에 추가해야 합니다.

양식의 처리 페이지에 다음 코드를 포함하여, 입력된 양식 값을 요청 데이터에 추가합니다(제출된 양식 값을 외부 데이터베이스 또는 다른 위치에 쓰는 것 외에도).

```
var sName= Request.Form("Name"); 
var sCity= Request.Form("City"); 
var sState= Request.Form("State"); 
var sZip= Request.Form("Zip"); 
 
Response.AppendToLog("&v_1=" +  sName); 
Response.AppendToLog("&v_2=" +  sCity); 
Response.AppendToLog("&v_3=" +  sState); 
Response.AppendToLog("&v_4=" +  sZip);
```

이 프로세스는 [!DNL Form Processing] 페이지의 요청 데이터에 정의된 대로 양식 값을 추가합니다. 로그 데이터 내에서 추가된 값은 아래 그림과 같이 [!DNL Form Processing] 페이지의 쿼리 문자열로 사용할 수 있습니다. 예를 들어, v_1, v_2, v_3 및 v_4는 이제 적절한 양식 필드에 입력된 데이터를 포함하는 쿼리 문자열입니다. 위의 예에서 설명한 구문은 캡처하려는 추가 양식 필드 및 값에 대해 복제할 수 있습니다.

```
http://www.myserver.com/path/to/formprocessingpage.asp?v_1=John+Smith&v_2=Los+Angeles&v_3=California&v_4=90210
```

모든 양식 필드 및 값을 캡처하고 분석에 사용할 수 있게 하려면 다음 구문을 사용할 수 있습니다.

```
var formvalues = Response.Form; 
Response.AppendToLog(formvalues); 
```

이 예제에서는 HTML 내에 있는 모든 양식 필드를 해당 값과 함께 가져와서 [!DNL Form Processing] 페이지의 로그 항목에 쿼리 문자열로 추가합니다. 여기에는 양식 내에 있는 숨겨진 필드가 포함됩니다.

로그 데이터는 다음 표에 설명된 대로 확장됩니다.

| 수집된 데이터 | 설명 | 예 |
|---|---|---|
| v_1 | NAME 쿼리 문자열과 연결된 값 | v_1=John Smith |
| v_2 | CITY 쿼리 문자열과 연결된 값 | v_2=로스앤젤레스 |
| v_3 | STATE 쿼리 문자열과 연결된 값 | v_3=California |
| v_4 | ZIP 쿼리 문자열과 연결된 값 | v_4=90210 |
