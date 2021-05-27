---
description: 참조 페이지 태그를 사용하여 링크 클릭 수를 간편하게 수집하는 데 사용되는 단계입니다.
title: 링크 클릭 추적
uuid: e4c492d2-9c90-4ed7-b997-6c50bdf98f93
exl-id: 0cb743e6-5c6e-4f80-bc77-83d1e706c92b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# 링크 클릭 추적{#tracking-link-clicks}

참조 페이지 태그를 사용하여 링크 클릭 수를 간편하게 수집하는 데 사용되는 단계입니다.

[!DNL Reference Page Tag] 배포를 통해 방문자가 특정 페이지를 방문하는 동안 클릭하는 링크(또는 href 값)를 나타내는 측정 데이터를 수집할 수 있습니다. 일반적으로 이 컬렉션에는 HTML 페이지에 추가 링크 식별자를 구현하는 작업이 포함되지 않습니다.

[!DNL Reference Page Tag] 사용을 통해 링크 클릭 수를 간편하게 수집하려면 다음 단계를 완료하십시오.

1. 다음 코드를 기존 파일 [!DNL zig.js]에 복사합니다.

   ```
   //REFERENCE LINK AND FORM CLICK PAGE TAG 
   //INITIATE FUNCTIONS ONLOAD 
   function addEvent(obj, evType, fn){  
    if (obj.addEventListener){  
      obj.addEventListener(evType, fn, false);  
      return true;  
    } else if (obj.attachEvent){  
      var r = obj.attachEvent("on"+evType, fn);  
      return r;  
    } else {  
      return false;  
    }  
   } 
   addEvent(window, 'load', startCapture); 
   addEvent(window, 'load', startCapture); 
   function startCapture(){ 
   //TO CAPTURE LINK CLICKS 
     if (vlc == "1"){captureLink();} 
     //TO CAPTURE FORM FIELD CLICKS 
     if (vfc == "1"){captureForm();} 
   } 
   //BEGIN LINK CAPTURE PAGE TAG 
   function captureLink(){ 
     if (document.links[0]){ 
       if (document.links){ 
         var links = document.links, link, k=0; 
         while(link=links[k++]) { 
           link.onclick = captureLinkName; 
    } 
       } 
     } 
   } 
   function captureLinkName() { 
     var lc=new Image(); 
     this.parent = this.parentNode; 
     lc.src='zag2.gif?linkname=' + escape(this.name) + "&cd=" + new Date().getTime(); 
   } 
   //END LINK CAPTURE PAGE TAG 
   //BEGIN FORM CLICK CAPTURE PAGE TAG 
   function captureForm(){ 
     if (document.forms[0]) { 
       if(document.forms){ 
    for(i=0; i<document.forms[0].elements.length; i++){ 
           var forms = document.forms[0].elements[i]; 
           forms.onfocus = captureFormName; 
         } 
       } 
     } 
   } 
   function captureFormName() { 
     var fc=new Image(); 
     fc.src='zag3.gif?fieldname=' + escape(this.name) + "&cd=" + new Date().getTime(); 
   } 
   //END FORM CLICK CAPTURE PAGE TAG
   ```

1. 1픽셀씩 1픽셀 이미지 파일 [!DNL zag2.gif]을(를) 만들거나 웹 서버에 있는 디렉터리에 배치합니다.
1. [!DNL lc.src] 변수를 수정하여 [!DNL zag2.gif] 파일이 참조되는 웹 사이트의 적절한 도메인을 참조합니다.

1. [!DNL zag.gif] 및 [!DNL zig.js] 파일에 대해 적절한 캐시 제어 헤더가 설정되었는지 확인합니다.

1. 링크 클릭 값을 수집하려는 HTML 파일 내에서 [!DNL Reference Page Tag Execution Call]을 수정하여 해당 페이지에 대한 링크 클릭 수를 캡처하도록 [!DNL Page Tag Execution Script]에 알려야 합니다. 이렇게 하려면 다음 코드 예제에서 강조 표시된 대로 vlc 변수 값을 &quot;1&quot;으로 변경하십시오.

```
<!-- BEGIN REFERENCE PAGE TAG--> 
<script language="javascript"> 
var vlc = "1" //Capture Link Click  1=TRUE, 0=FALSE 
var vfc = "0"; //Capture Form Field Click  1=TRUE, 0=FALSE 
var v = {}; 
</script> 
 
<script language="javascript" src=”http://www.myserver.com/path/to/zig.js" type="text/javascript"></script> 
 
<noscript> 
<img src="/path/to/zag.gif?Log=1&v_jd=1" border="0" width="1" height="1"/> 
</noscript> 
 
<!-- END REFERENCE PAGE TAG-->
```

| 수집한 데이터 | 설명 | 예 |
|---|---|---|
| v_ln= | 노출 캠페인을 나타내는 값 | v_ln=&quot;약%20Us&quot; |
