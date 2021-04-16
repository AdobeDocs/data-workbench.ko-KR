---
description: 참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 호출 시 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터의 수집으로 이루어집니다.
title: 참조 페이지 태그 실행 스크립트 편집
uuid: 0db00b89-e420-423d-9b88-8b724baa828f
exl-id: bc922b59-716e-4e92-84b5-59a52620df03
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 7%

---

# 참조 페이지 태그 실행 스크립트 편집{#editing-the-reference-page-tag-execution-script}

참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 호출 시 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터의 수집으로 이루어집니다.

Adobe 컨설팅 서비스 팀과의 회의를 수집하는 동안 확인할 수 있는 추가 정보를 수집하도록 [!DNL Reference Page Tag Execution Script]을 수정할 수 있습니다. [!DNL Reference Page Tag Execution Script]의 크기는 웹 페이지에 다운로드가 많이 추가되지 않도록 상대적으로 작습니다.

다음 [!DNL Reference Page Tag Execution Script] 코드가 [!DNL zig.js]라는 파일에 제공됩니다.

```
//REFERENCE PAGE TAG 
// CONSTANTS 
var ct = "<img src="; 
var cd = "[PATH_TO_WEB_SERVER]"; //this should contain the domain of 
                               //the web site that will host the 
                                //page tag 
 
var cu = "[PATH_TO_WEB_PAGE_TAG_CODE]/zag.gif?Log=1";  
                                 //this should contain the full path to 
                                 //the zag.gif file (excluding domain) 
                                 //and include the query string of log=1 
var ce = ">"; 
var c = {}; 
c["sw"] = screen.width; 
c["sh"] = screen.height; 
c["cd"] = screen.colorDepth; 
var co = ""; 
 
for ( cKey in c ) { 
co = co+"&"+cKey+"="+escape(c[cKey]); 
} 
document.write(ct,cd,cu,co,ce); 
 
var d = {}; 
d["dt"] = document.title; 
d["dr"] = document.referrer; 
d["cb"] = new Date().getTime(); 
var vo = ""; 
 
if (typeof v != "undefined") { 
for ( vKey in v ) { 
vo = vo+"&"+vKey+"="+escape(v[vKey]); 
} 
} 
for ( dKey in d ) { 
vo = vo+"&"+dKey+"="+escape(d[dKey]); 
} 
document.write(ct,cd,cu,vo,ce); 
//END REFERENCE PAGE TAG 
```

[!DNL Reference Page Tag] 사용을 통해 데이터 수집을 용이하게 하려면 다음 단계를 완료하십시오.

1. 웹 서버에 있는 디렉토리에 [!DNL zag.gif]이라는 1픽셀 이미지 파일을 만들거나 가져옵니다.
1. [!DNL zag.gif] 파일이 참조되는 웹 사이트 또는 Adobe 관리 서비스 도메인의 적절한 도메인을 참조하도록 cd 변수를 수정합니다. 파일에 대한 참조는 [!DNL zig.js] 파일 함수 실행을 통해 만들어집니다. 예를 들어,

   ```
   //www.mysite.com
   ```

1. [!DNL zag.gif] 파일 위치에 대한 적절한 경로를 참조하도록 ccu 변수를 수정합니다. 예

   ```
   /scripts
   ```

1. [!DNL zag.gif] 및 [!DNL zig.js] 파일에 대해 적절한 캐시 제어 헤더가 설정되었는지 확인합니다.
