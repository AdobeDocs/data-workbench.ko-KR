---
description: 참조 페이지 태그 실행 호출은 측정 데이터를 수집하려는 웹 페이지에 삽입됩니다.
title: 참조 페이지 태그 실행 호출 추가
uuid: 8c682649-d1b1-40a6-a2b2-4ff5a92b732f
exl-id: a4f9ab2b-50e8-4e0b-9c87-80dffb697316
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---

# 참조 페이지 태그 실행 호출 추가{#adding-reference-page-tag-execution-calls}

{{eol}}

참조 페이지 태그 실행 호출은 측정 데이터를 수집하려는 웹 페이지에 삽입됩니다.

HTML 문서 본문에 포함해야 하며 해당하는 경우 글로벌 포함 바닥글 내에 배치할 수 있습니다. 다음 [!DNL Reference Page Tag Execution Call] Adobe 컨설팅 서비스 팀과 회의를 하는 동안 요구 사항을 수집하는 동안 식별될 수 있는 추가 정보를 수집하도록 팀이 수정할 수 있습니다.

를 사용하여 데이터 수집을 용이하게 하려면 [!DNL Reference Page Tag]에서 다음 단계를 완료합니다.

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

1. 경로 를 [!DNL zig.js] 및 [!DNL zag.gif] 파일. 예:

   ```
   //www.mysite.com/scripts/zig.js 
   //www.mysite.com/images/zag.gif 
   ```

웹 서버에서 적절한 HTTP Cache-Control 헤더가 설정되었는지 확인하여 [!DNL zig.js]및 [!DNL zag.gif] 브라우저에 의해 파일이 캐시되지 않습니다. 두 가지 방법 중 하나를 사용하여 HTTP Cache-Control 헤더 정보를 설정할 수 있습니다. 첫 번째 방법은 웹 서버를 통해 HTTP 헤더를 설정하는 것입니다. 두 번째 방법은 스크립트를 사용하여 특정 페이지나 포함된 각 개체에 대해 HTTP 헤더를 설정하는 것입니다. 스크립팅 메서드를 사용하면 JSP 또는 ASP와 같은 프로그래밍 언어를 사용하여 웹 페이지를 만들어야 합니다. 그러면 페이지가 스크립팅되어 적절한 헤더 정보를 보냅니다. 이 방법에는 두 가지 분명한 단점이 있습니다. 1) 헤더를 전송하려면 모든 페이지를 코딩해야 하며 2) 페이지가 정적 HTML이 될 수 없으며 이는 웹 서버 성능에 일부 영향을 줍니다.

Microsoft IIS에서 실행되는 웹 사이트는 Microsoft 관리 콘솔을 통해 적절한 HTTP 헤더를 추가할 수 있습니다. Netscape iPlanet Web Server에서 제공되는 웹 사이트는 [!DNL obj.conf] 파일의 이름을 지정합니다. Apache 웹 서버는 Tcl 모듈을 사용하여 AOLServer를 사용자 지정할 수 있는 포함된 mod_headers 모듈을 사용하여 웹 마스터에서 HTTP 헤더를 사용자 지정하는 기능을 제공합니다. HTTP Cache-Control 헤더를 구현하기 전에 웹 서버 플랫폼과 관련된 설명서를 참조해야 합니다.

일반적으로 HTTP 헤더는 다음과 같이 구조화해야 합니다.

```
Cache-Control: no-cache 
Pragma: no-cache 
Expires: -1
```
