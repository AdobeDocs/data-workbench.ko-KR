---
description: 참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 가 호출되면 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터가 수집됩니다.
title: 참조 페이지 태그 실행 스크립트 편집
uuid: 0db00b89-e420-423d-9b88-8b724baa828f
exl-id: bc922b59-716e-4e92-84b5-59a52620df03
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 7%

---

# 참조 페이지 태그 실행 스크립트 편집{#editing-the-reference-page-tag-execution-script}

{{eol}}

참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 가 호출되면 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터가 수집됩니다.

을 수정할 수 있습니다 [!DNL Reference Page Tag Execution Script] Adobe 컨설팅 서비스 팀과 회의를 하는 동안 식별될 수 있는 추가 정보를 수집하기 위해 다음 [!DNL Reference Page Tag Execution Script] 는 웹 페이지에 큰 다운로드를 추가하지 않도록 상대적으로 작습니다.

다음 [!DNL Reference Page Tag Execution Script] 라는 파일에 코드가 제공됩니다 [!DNL zig.js]:

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

를 사용하여 데이터 수집을 용이하게 하려면 [!DNL Reference Page Tag]에서 다음 단계를 완료합니다.

1. 1픽셀을 1픽셀 이미지 파일(이름)로 만들거나 배치합니다. [!DNL zag.gif] 웹 서버에 있는 디렉토리에 추가합니다.
1. 웹 사이트 또는 Adobe 관리 서비스 도메인의 적절한 도메인을 참조하도록 cd 변수를 수정합니다. [!DNL zag.gif] 파일이 참조되었습니다. 파일에 대한 참조는 [!DNL zig.js] 파일 함수 위에 있어야 합니다. 예:

   ```
   //www.mysite.com
   ```

1. cu 변수를 수정하여 [!DNL zag.gif] 파일. 예

   ```
   /scripts
   ```

1. 에 대해 적절한 캐시 제어 헤더가 설정되었는지 확인합니다. [!DNL zag.gif] 및 [!DNL zig.js] 파일.
