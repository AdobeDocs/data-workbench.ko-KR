---
description: 워크시트의 셀에 텍스트 또는 표현식을 입력할 수 있습니다.
title: 워크시트에 있는 데이터 사용
uuid: c2331fa5-aa07-4622-8f44-5124c22dffcb
exl-id: 40d9211b-8f5c-4051-8f93-638ffacf45bd
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 3%

---

# 워크시트에 있는 데이터 사용{#work-with-data-in-worksheets}

워크시트의 셀에 텍스트 또는 표현식을 입력할 수 있습니다.

참조된 셀의 텍스트를 표현식으로 처리하는 [!DNL eval( )]을 사용하지 않는 한 워크시트의 모든 표현식 앞에 등호(=)가 옵니다.

지표, 차원 및 필터 구문 규칙의 전체 목록은 [쿼리 언어 구문](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)을 참조하십시오.

**워크시트에 데이터를 입력하려면**

1. 스프레드시트에서 셀을 두 번 클릭하여 편집 모드를 시작합니다. 선택한 셀이 강조 표시됩니다.
1. 원하는 데이터를 셀에 입력하거나 붙여넣습니다.

**한 셀에서 다른 셀로 복사하여 붙여넣으려면**

1. 복사할 데이터가 들어 있는 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]** 을 클릭합니다.
1. 복사한 데이터를 붙여넣을 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]** 를 클릭합니다.

Data Workbench은 적절한 열 및 행을 참조하도록 새 셀의 참조를 자동으로 업데이트합니다.

**셀 그룹에서 다른 셀 그룹에 복사하여 붙여넣으려면**

1. 복사할 데이터가 들어 있는 셀을 선택합니다.
1. 복사할 데이터가 들어 있는 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Copy]** 을 클릭합니다.
1. 복사한 데이터 붙여넣기를 시작할 첫 번째 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Paste]** 를 클릭합니다. 데이터는 첫 번째 셀과 그 아래에 붙여넣습니다.

Data Workbench은 적절한 열 및 행을 참조하도록 새 셀의 참조를 자동으로 업데이트합니다.

**열을 삽입하려면**

* 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Insert Column]** 를 클릭합니다. 새 열이 선택한 열의 왼쪽에 삽입됩니다.

**열을 삭제하려면**

* 삭제할 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Delete Column]** 을 클릭합니다. 열이 제거됩니다.

**행을 삽입하려면**

* 행을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Insert Row]** 를 클릭합니다. 새 행이 선택한 행 위에 삽입됩니다.

**행을 삭제하려면**

* 삭제할 행을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Delete Row]** 를 클릭합니다. 행이 제거됩니다.

**열 크기를 조정하려면**

1. 열 머리글 행에서 크기를 변경할 열의 오른쪽에 있는 분할선 위에 커서를 놓습니다.
1. 을 클릭하고 오른쪽으로 드래그하여 열 너비를 늘리거나 왼쪽으로 드래그하여 열 너비를 줄입니다.

**셀 서식을 지정하려면**

1. 셀을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Format]** 를 클릭합니다.

   ![](assets/mnu_Worksheet_Format.png)

1. 사용 가능한 옵션 메뉴에서 원하는 형식을 클릭합니다.

<table id="table_5788E01E52CC44E7927A0D23760D9EDD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 메뉴 옵션 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>숫자 </p> </td> 
   <td colname="col2"> <p>선택한 숫자 형식을 시간, 날짜, 백분율 또는 십진수와 같이 데이터에 적용합니다. </p> <p>선택한 서식을 제거하려면 <span class="uicontrol"> 기본값</span> 을 클릭하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>양쪽 맞춤 </p> </td> 
   <td colname="col2"> <p>셀 내의 데이터를 왼쪽, 가운데 또는 오른쪽으로 정렬합니다. 기본 양쪽 맞춤은 남아 있습니다. </p> <p>선택한 서식을 제거하려면 <span class="uicontrol"> 기본값</span> 을 클릭하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>색상 </p> </td> 
   <td colname="col2"> <p>선택한 글꼴 색상을 셀 내의 데이터에 적용합니다. 기본 글꼴 색상은 흰색입니다. </p> <p>선택한 서식을 제거하려면 <span class="uicontrol"> 기본값</span> 을 클릭하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표시기 </p> </td> 
   <td colname="col2"> <p>이 셀을 사용하여 지표 표시기를 만듭니다. 자세한 내용은 <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#concept-f0e911b23b2c4e8da3e1ea7b9ae04183"> 지표 표시기 만들기</a> 를 참조하십시오. </p> <p>선택한 서식을 제거하려면 <span class="uicontrol"> 기본값</span> 을 클릭하십시오. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>입력 셀 </p> </td> 
   <td colname="col2"> <p>선택한 셀을 입력 셀로 만듭니다. 자세한 내용은 <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-input-cells.md#concept-08cd2c05a28a43dd9f7698b37e23e590"> 입력 셀 만들기</a> 를 참조하십시오. </p> <p>선택한 서식을 제거하려면 <span class="uicontrol"> 기본값</span> 을 클릭하십시오. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 키보드 단축키 {#section-05301f4d2c60418e86902635a7aeee20}

워크시트 내에서 메모장이나 Microsoft Word와 같은 텍스트 편집기에서 사용할 수 있는 다양한 기본 편집 키보드 단축키를 사용할 수 있습니다.

다음 표에는 워크시트에 데이터를 입력할 때 사용할 수 있는 기본 키보드 단축키가 나와 있습니다.

<table id="table_8E6F73F253B3451CA1DE45EE4F4E69EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 단축키 </th> 
   <th colname="col2" class="entry"> 설명 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>화살표 키 </p> </td> 
   <td colname="col2"> <p>위쪽, 아래쪽, 왼쪽 및 오른쪽 화살표 키를 사용하여 워크시트의 셀에서 셀로 이동합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F2 </p> </td> 
   <td colname="col2"> <p>선택한 셀에 커서를 놓아 셀을 편집합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enter </p> </td> 
   <td colname="col2"> <p>선택한 셀의 편집을 완료합니다. 커서가 셀에서 제거되고 셀 내용이 편집을 반영합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Esc </p> </td> 
   <td colname="col2"> <p>선택한 셀의 편집을 취소합니다. 커서가 셀에서 제거되고 셀 내용이 편집을 시작하기 전에 있었던 내용으로 돌아갑니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>삭제 </p> </td> 
   <td colname="col2"> <p>셀의 내용을 삭제합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+A </p> </td> 
   <td colname="col2"> <p>셀의 내용을 선택합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+c </p> </td> 
   <td colname="col2"> <p>셀의 내용을 복사합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+x </p> <p>Shift+삭제 </p> </td> 
   <td colname="col2"> <p>셀의 내용을 복사하여 제거합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+v </p> <p>Shift+삽입 </p> </td> 
   <td colname="col2"> <p>선택한 셀에 복사한 셀의 내용을 붙여넣습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+z </p> </td> 
   <td colname="col2"> <p>입력을 취소합니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+Shift+z </p> </td> 
   <td colname="col2"> <p>입력을 다시 실행합니다. </p> </td> 
  </tr> 
 </tbody> 
</table>
