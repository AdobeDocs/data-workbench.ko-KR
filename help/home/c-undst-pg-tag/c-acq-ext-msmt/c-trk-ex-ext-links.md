---
description: 타사 웹 사이트 링크에서 활동을 캡처하여 종료 Target 분석을 활성화합니다.
title: 외부 링크에 대한 종료 추적
uuid: 523f5b4c-4600-4d44-82e7-4a8b2db2d266
exl-id: fd7434e9-cd66-408e-baa9-6a0df4039786
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 6%

---

# 외부 링크에 대한 종료 추적{#tracking-exits-to-external-links}

타사 웹 사이트 링크에서 활동을 캡처하여 종료 Target 분석을 활성화합니다.

웹 페이지에는 타사 웹 사이트에 대한 링크가 포함될 수 있으며, 이러한 링크에 걸친 활동을 캡처하여 종료 Target 분석을 사용할 수 있도록 할 수 있습니다. 특히 이러한 레퍼러를 받으면 타사 사이트에서 참조 비용을 지불해야 합니다. 클릭 이벤트는 기본적으로 타사 시스템의 로그 파일에 기록되므로 클릭 이벤트가 로컬로 캡처되도록 링크를 수정해야 합니다. 웹 사이트 내에 있는 타사 링크는 다음과 같이 수정해야 합니다.

```
<A HREF=”http://www.myserver.com/PageExit.htm?v_eurl=http://www.othersite.com”>
```

참조된 [!DNL PageExit.htm] 파일을 만들어야 하며 다음 스크립트를 포함하도록 구조화해야 합니다.

```
<html> 
<head> 
 
<script> 
function getExitURLQuery(variable) 
{ 
 
var query = window.location.search.substring(1); 
var vars = query.split("&"); 
for (var i=0; i<vars.length; i++) 
{ 
var pair = vars[i].split("="); 
if (pair[0] == variable) 
{ 
return pair[1]; 
} 
 }  
} 
</script> 
 
<script> 
location.replace(getExitURLQuery("v_eurl")); 
</script>  
 
</head> 
</html>
```

[!DNL PageExit.htm] 파일에 대해 요청을 수행하면 v_eurl 값이 분석 목적으로 수집됩니다. 또한 [!DNL PageExit.htm]이 로드되면 지정된 v_eurl 대상 위치로 즉시 리디렉션됩니다.

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_eurl | v_eurl 쿼리 문자열 변수와 연결된 값입니다. 이 값은 HTML 페이지 내에 있는 링크의 대상 URL을 나타냅니다. | v_eurl=www.othersite.com |
