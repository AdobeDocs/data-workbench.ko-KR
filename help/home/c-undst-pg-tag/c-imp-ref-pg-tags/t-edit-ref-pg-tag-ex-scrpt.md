---
description: 참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 호출될 때 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터의 수집으로 구성됩니다.
solution: Analytics
title: 참조 페이지 태그 실행 스크립트 편집
topic: Data workbench
uuid: 0db00b89-e420-423d-9b88-8b724baa828f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 참조 페이지 태그 실행 스크립트 편집{#editing-the-reference-page-tag-execution-script}

참조 페이지 태그는 웹 서버에 있는 페이지 태그 실행 스크립트로 구성되며, 호출될 때 사이트 방문자가 요청한 페이지에 대한 모든 클라이언트측 데이터의 수집으로 구성됩니다.

Adobe 컨설팅 서비스 팀과 회의를 [!DNL Reference Page Tag Execution Script] 하는 동안 요구 사항을 수집하는 동안 식별될 수 있는 추가 정보를 수집하도록 을 수정할 수 있습니다. 웹 [!DNL Reference Page Tag Execution Script] 페이지에 다운로드가 크게 추가되는 것을 방지하기 위해 크기는 비교적 작습니다.

다음 [!DNL Reference Page Tag Execution Script] 코드가 [!DNL zig.js]명명된 파일에서 제공됩니다.

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

를 사용하여 데이터 수집을 용이하게 하려면 [!DNL Reference Page Tag]다음 단계를 완료하십시오.

1. 웹 서버에 있는 디렉토리에 이름이 지정된 1픽셀 이미지 파일을 만들거나 [!DNL zag.gif] 가져옵니다.
1. cd 변수를 수정하여 [!DNL zag.gif] 파일이 참조되는 웹 사이트 또는 Adobe 관리 서비스 도메인의 해당 도메인을 참조합니다. 파일에 대한 참조는 [!DNL zig.js] 파일 함수 실행을 통해 만들어집니다. 예:

   ```
   //www.mysite.com
   ```

1. 잘라내기 변수를 수정하여 [!DNL zag.gif] 파일 위치에 대한 적절한 경로를 참조합니다. 예

   ```
   /scripts
   ```

1. 및 파일에 대해 적절한 캐시 제어 헤더가 설정되었는지 [!DNL zag.gif] [!DNL zig.js] 확인합니다.
