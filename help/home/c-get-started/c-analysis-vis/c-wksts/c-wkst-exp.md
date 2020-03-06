---
description: 워크시트 표현식 및 셀 참조 사용에 대한 개념 정보입니다.
solution: Analytics
title: 워크시트 표현식
topic: Data workbench
uuid: be57d6bd-3e13-4c90-9034-8e0f2b8315aa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 워크시트 표현식{#worksheet-expressions}

워크시트 표현식 및 셀 참조 사용에 대한 개념 정보입니다.

다음 워크시트는 은행 웹 사이트의 온라인 응용 프로그램 양식에 제공된 응용 프로그램 마법사 페이지를 보는 방문자에 대한 세부 정보를 제공합니다.

![](assets/client-wkst.png)

* 열 A는 평가할 방문자 카테고리 목록을 보여줍니다.레퍼러 A의 방문자, 참조 방문자 및 참조 방문자.
* 열 B는 지금 적용 페이지를 본 각 카테고리의 방문자 수를 표시합니다.
* 열 C는 지금 적용 페이지와 애플리케이션 마법사 페이지를 모두 본 방문자를 보여줍니다.
* 열 D에는 애플리케이션 마법사 페이지를 본 세 가지 카테고리의 지금 적용 뷰어 비율이 포함되어 있습니다.

이 워크시트는 지금 적용 페이지를 본 레퍼러 A에서 참조한 방문자 중 약 55%가 애플리케이션 마법사 페이지를 본 것으로 보여줍니다.

다음 표에서는 이전 예제에서 워크시트에 대한 샘플 공식을 제공합니다.

<table id="table_0F5EFDB58040465AB599E6BE93324822"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 워크시트 셀 </th> 
   <th colname="col2" class="entry"> 공식 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>B2 </p> <p>지금 적용 페이지를 본 방문자 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> = 방문자[페이지="/applynow/default.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B3 </p> <p>지금 적용 페이지를 본 참조된 방문자 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> = Referred_Visitors[Page="/applynow/default.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B4 </p> <p>지금 적용 페이지를 본 레퍼러 A의 참조 방문자 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> = Referred_Visitors[Page="/applynow/default.asp" </span> </p> <p> AND <span class="filepath"> 레퍼러="참조 A"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C2 </p> <p>지금 적용 페이지와 애플리케이션 마법사 페이지를 본 방문자 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> = 방문자[페이지="/applynow/default.asp" </span> </p> <p> AND <span class="filepath"> Page="/applynow/appwizard.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C3 </p> <p>지금 적용 페이지와 애플리케이션 마법사 페이지를 본 참조 방문자 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> = Referred_Visitors[Page="/applynow/default.asp" </span> </p> <p> AND <span class="filepath"> Page="/applynow/appwizard.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C4 </p> <p>지금 적용 페이지 및 애플리케이션 마법사 페이지를 본 레퍼러 A의 참조 방문자 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> = Referred_Visitors[Page="/applynow/default.asp"</span> </p> <p> AND <span class="filepath"> Page="/applynow/appwizard.asp"</span> </p> <p> AND <span class="filepath"> 레퍼러="참조 A"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D2 </p> <p>지금 적용 페이지 및 애플리케이션 마법사 페이지를 본 방문자 비율 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> = C2/B2*100</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D3 </p> <p>지금 적용 페이지 및 애플리케이션 마법사 페이지를 본 참조 방문자 비율 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> = C3/B3*100</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D4 </p> <p>지금 적용 페이지 및 애플리케이션 마법사 페이지를 본 레퍼러 A의 참조 방문자 비율 </p> </td> 
   <td colname="col2"> <p><span class="filepath"> = C4/B4*100</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

다른 시각화와 마찬가지로, 작업공간에서 다른 시각화에서 선택하면 워크시트도 자동으로 업데이트됩니다. 선택을 하는 방법에 대한 자세한 내용은 시각화에서 [선택 만들기를 참조하십시오](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746).

다음 웹 데이터 예제에서는 일 시각화별 세션에서 몇 일 동안의 세션 데이터가 선택되었습니다. 이 워크시트는 선택한 기간 동안 지금 적용 페이지를 본 레퍼러 A의 방문자 중 약 69%가 애플리케이션 마법사 페이지를 열람했음을 보여줍니다. 이 선택 사항(위의 예에서 보듯이)이 없는 경우 레퍼러 A의 방문자 중 약 55%가 지금 적용 페이지와 애플리케이션 마법사 페이지를 보았습니다.

![](assets/client-exp.png)

## 셀 참조 사용 {#section-0004e315c9c94d359b1a8a39794ba555}

자체 또는 워크시트의 다른 표현식 내에서 셀 참조로 문자열을 대체할 수 있습니다.

* **단순 셀 참조:** 셀 A2에는 머리글로 사용되는 방문자 텍스트가 포함되어 있습니다. 셀 B2에는 [!DNL eval(A1)]으로 평가되는 값이 들어 [!DNL =Visitors]있습니다.

* **필터 셀 참조:** 셀 A5에는 어제 날짜가 포함되어 있습니다. 셀 B5에는 어제 방문자 수로 평가되는 [!DNL[ 방문자 수=A5 ]]가 포함되어 있습니다.

* **연결된 셀 참조:** 셀 A5에는 오늘 날짜가 포함되어 있고 셀 A6에는 08:00 ~ 08:59의 1시간 기간이 포함되어 있습니다. 셀 B6에는 현재 오전 8:00에서 오전 9:00 사이 방문자 수로 평가되는[ [!DNL 방문자 시간=A5+&quot;&quot;+A6 ]]이 포함되어 있습니다.

