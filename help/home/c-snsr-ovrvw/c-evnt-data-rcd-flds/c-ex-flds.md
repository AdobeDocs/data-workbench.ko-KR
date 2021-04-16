---
description: 센서는 서버에서 사용될 경우 서버의 API를 통해 사용할 수 있는 유효한 HTTP 요청이나 응답 헤더 또는 변수에서 이벤트 데이터의 필드를 수집할 수 있습니다.
title: 확장 가능한 필드
uuid: 91b9857e-44a4-497f-b157-51afd30306fe
exl-id: e783d073-cf06-4415-80e1-567b55fdee12
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# 확장 가능한 필드{#extensible-fields}

센서는 서버에서 사용될 경우 서버의 API를 통해 사용할 수 있는 유효한 HTTP 요청이나 응답 헤더 또는 변수에서 이벤트 데이터의 필드를 수집할 수 있습니다.

이러한 데이터 필드를 수집하려면 [!DNL Sensor]에 대한 [!DNL txlogd.conf] 구성 파일에서 원하는 머리글 필드 또는 변수를 지정해야 합니다.

* [요청 헤더](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f)
* [서버 변수](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-74b258bc3e8a4a93a0ee9fb01c067e4b)

## 요청 헤더 {#section-22766692b45546d8bfc93dbe3bc9368f}

다음은 수집될 요청 헤더 필드(예: 호스트, 수락-인코딩, Keep-Alive 등)를 [!DNL txlogd.conf]에서 지정하는 구문입니다.

```
LogHeader RequestHeaderName
```

수집된 데이터는 [!DNL data workbench server]에서 만든 [!DNL .vsl] 파일의 [!DNL Sensor]에서 &quot;cs(RequestHeaderName)&quot;라는 필드에 기록됩니다. 예를 들어 요청 헤더 &quot;호스트&quot;에서 특정 요청 헤더 값을 수집하려면 [!DNL txlogd.conf]에 &quot;LogHeader 호스트&quot;를 입력합니다. 데이터는 이벤트 데이터 레코드의 &quot;cs(호스트)&quot; 필드에 기록됩니다.

## 서버 변수 {#section-74b258bc3e8a4a93a0ee9fb01c067e4b}

[!DNL Sensor] 파일에 포함하는 SpecialLogField 항목을 사용하여 응답 헤더 또는 API 액세스 가능한 서버 변수에서 데이터 필드를 수집할 수  [!DNL txlogd.conf] 있습니다. &quot;LogHeader&quot; 항목 외에 &quot;SpecialLogField&quot; 항목을 사용하여 요청 헤더를 수집할 수도 있습니다. [요청 헤더](../../../home/c-snsr-ovrvw/c-evnt-data-rcd-flds/c-ex-flds.md#section-22766692b45546d8bfc93dbe3bc9368f)를 참조하십시오. 요청 헤더 옵션은 이전 버전과의 호환성을 위해 계속 사용할 수 있습니다.

다음은 [!DNL txlogd.conf]에서 &quot;SpecialLogField&quot;를 지정하는 구문입니다.

```
SpecialLogField cs(log field) = serverVariable stage
```

다음 표는 &quot;SpecialLogField&quot; 항목의 구성 요소에 대한 설명을 포함합니다.

<table id="table_053D5F34D56E4B15A85CA3B4FAD6E1B1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 구성 요소 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> cs(log 필드) </td> 
   <td colname="col2"> 수집된 데이터가 이벤트 데이터 레코드에 기록되는 필드 이름 및 <span class="keyword"> 데이터 워크벤치 서버 </span>에서 만든 <span class="filepath"> .vsl </span> 파일의 이름입니다. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> serverVariable </td> 
   <td colname="col2"> <p>서버의 API를 통해 <span class="wintitle"> 센서 </span>에 사용할 수 있는 모든 서버 변수 </p> <p>예:response.p3p </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 스테이지 </td> 
   <td colname="col2"> <p>vys_log 또는 vys_cookie </p> <p>스테이지를 지정하려면 vys_log 및 vys_cookie에 사용할 수 있는 서버 변수를 알아야 합니다. </p> <p>예:serverVariable response.p3p의 경우 vys_log를 입력합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

확장 가능한 이벤트 데이터 레코드 필드를 수집하도록 [!DNL Sensor]을 구성하는 데 도움이 필요하면 Adobe 컨설팅 서비스에 문의하십시오.
