---
description: 참조 페이지 태그 실행 호출은 측정 데이터를 수집하려는 웹 페이지에 삽입됩니다.
solution: Analytics
title: 참조 페이지 태그 실행 호출 추가
topic: Data workbench
uuid: 8c682649-d1b1-40a6-a2b2-4ff5a92b732f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 참조 페이지 태그 실행 호출 추가{#adding-reference-page-tag-execution-calls}

참조 페이지 태그 실행 호출은 측정 데이터를 수집하려는 웹 페이지에 삽입됩니다.

HTML 문서의 본문에 포함되어야 하며 해당되는 경우 글로벌 포함 바닥글 내에 배치할 수 있습니다. 팀에서 Adobe 컨설팅 서비스 팀과 회의를 하는 동안 요구 사항을 수집하는 동안 식별될 수 있는 추가 정보를 수집하도록 수정할 [!DNL Reference Page Tag Execution Call] 수 있습니다.

를 사용하여 데이터 수집을 용이하게 하려면 [!DNL Reference Page Tag]다음 단계를 완료하십시오.

1. 다음 코드를 HTML 문서 본문에 복사합니다.

   ```
   <!--//BEGIN REFERENCE PAGE TAG--> 
   <script language="javascript"> 
   var vlc = "0" //Capture Link Click  1=TRUE, 0=FALSE 
   var v = {}; 
   </script> 
   
   <!--//MODIFIY PATH TO ZIG.JS--> 
   <script language="javascript" src="/path/to/zig.js" type="text/javascript"></script> 
   <!--//END REFERENCE PAGE TAG--> 
   
   <noscript> 
   <img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
   </noscript> 
   <!-- END REFERENCE PAGE TAG-->
   ```

1. 파일과 파일의 위치를 [!DNL zig.js] 수정합니다 [!DNL zag.gif] . 예:

   ```
   //www.mysite.com/scripts/zig.js 
   //www.mysite.com/images/zag.gif 
   ```

브라우저가 [!DNL zig.js][!DNL zag.gif] 및 파일을 캐시하지 않도록 웹 서버에 적절한 HTTP Cache-Control 헤더가 설정되어 있는지 확인하십시오. 두 가지 방법 중 하나를 사용하여 HTTP Cache-Control 헤더 정보를 설정할 수 있습니다. 첫 번째 방법은 웹 서버를 통해 HTTP 헤더를 설정하는 것입니다. 두 번째 방법은 스크립트를 사용하여 각 특정 페이지 또는 포함된 개체에 대한 HTTP 헤더를 설정하는 것입니다. 스크립팅 방법을 사용하면 웹 페이지가 JSP 또는 ASP와 같은 프로그래밍 언어를 사용하여 만들어졌어야 합니다. 그러면 페이지가 스크립팅되어 적절한 헤더 정보를 전송합니다. 이 방법에는 다음과 같은 두 가지 명백한 단점이 있습니다.1) 모든 페이지를 코딩하여 헤더를 보내야 하고 2) 페이지가 정적 HTML일 수 없으며, 이는 웹 서버 성능에 일부 영향을 줍니다.

Microsoft IIS 파섹 Netscape iPlanet Web Server에서 제공되는 웹 사이트에서는 사이트의 구성 디렉토리 내의 [!DNL obj.conf] 파일을 편집하여 이 작업을 수행할 수 있습니다. Apache Web Server는 AOLServer를 Tcl 모듈을 사용하여 사용자 정의할 수 있는 포함된 mod_headers 모듈을 사용하여 웹 마스터에게 HTTP 헤더를 사용자 지정하는 기능을 제공합니다. HTTP Cache-Control 헤더를 구현하기 전에 웹 서버 플랫폼별 설명서를 참조하십시오.

일반적으로 HTTP 헤더를 다음과 같이 구성해야 합니다.

```
Cache-Control: no-cache 
Pragma: no-cache 
Expires: -1
```

