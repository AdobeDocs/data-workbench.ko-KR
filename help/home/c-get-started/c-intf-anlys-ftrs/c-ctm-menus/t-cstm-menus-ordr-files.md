---
description: 해당 메뉴와 연관된 order.txt 파일을 편집하여 모든 메뉴의 모양을 사용자 정의할 수 있습니다.
title: order.txt 파일을 사용하여 메뉴 사용자 정의
uuid: 4346114a-05d0-4d15-9633-09c9d869cdd6
exl-id: 3803a56f-19b7-4792-a277-97f76c11ec0e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 2%

---

# order.txt 파일을 사용하여 메뉴 사용자 정의{#customize-a-menu-using-order-txt-files}

해당 메뉴와 연관된 order.txt 파일을 편집하여 모든 메뉴의 모양을 사용자 정의할 수 있습니다.

이 섹션의 단계는 모든 유형의 메뉴에 적용됩니다.

**order.txt 파일을 편집하여 메뉴를 사용자 정의하려면**

1. [!DNL Profile Manager]의 *프로필 이름* 열에서 [!DNL order.txt] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;를 클릭합니다.
1. [!DNL User] 열에서 [!DNL order.txt] 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다. [!DNL order.txt] 파일이 표시됩니다.

   ![단계 정보](assets/cfg_ordertxt.png)

1. (선택 사항) 원하는 경우 파일 맨 위에 [포함] 또는 [배타적] 설정을 추가하거나 변경합니다. 이 설정은 [!DNL order.txt] 파일에 나열되지 않고 [!DNL Profile Manager]에 있는 항목이 메뉴에 나열되는지 여부를 제어합니다. 옵션은 다음과 같습니다.

   * **[포함]:** 기본 설정입니다. 이 설정을 사용하면 메뉴 아래쪽에 [!DNL order.txt]파일에 지정되지 않은 메뉴 항목이 알파벳순으로 나열됩니다. 예를 들어 [!DNL Profile Manager]에 위의 [!DNL order.txt]에 나열된 프로파일 항목 외에 프로필 항목이 포함된 경우 프로필은 데이터 아래에 표시됩니다.

   * **[배타적]:** 이 설정을 사용하면 메뉴 항목에 지정되지 않은 메뉴  [!DNL order.txt] 항목이 메뉴에서 제외됩니다. 예를 들어 [!DNL Profile Manager]에 위의 [!DNL order.txt]에 나열된 항목 외에 프로필 항목이 포함된 경우 메뉴의 아무 곳에도 프로필이 표시되지 않습니다.

   * **blank:** 파일  [] 맨 위에 포함 또는 제외 [] 가 표시되지 않으면 Data Workbench에서 메뉴 항목을 포함 [으로 표시합니다].

1. 다음 단계 중 하나 이상을 완료합니다.

   <table id="table_C5D5313DF5E4470499B0B285BA2690F0"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> 이 작업을 수행하려면... </th> 
    <th colname="col2" class="entry"> 다음을 수행합니다... </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>메뉴 항목 순서 변경 </p> </td> 
    <td colname="col2"> <p>Data Workbench에 표시할 순서대로 항목 이름을 입력합니다. </p> <p>예를 들어 각 메뉴 항목 이름이 해당 파일 또는 폴더 이름과 일치하는 경우, <b> 테이블 추가</b>가 먼저 나타나고 <b>시각화 추가</b>, <b>범례 추가</b> 및 <b>노트 추가</b>가 마지막으로 표시됩니다. </p> <p><b>표 추가  </b> </p> <p><b>시각화 추가  </b> </p> <p><b>범례 추가  </b> </p> <p><b>메모 추가 </b> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>메뉴 항목 이름 변경 </p> </td> 
    <td colname="col2"> <p><span class="wintitle"> 프로필 관리자</span>에서 해당 파일 또는 폴더의 이름을 바꾼 다음 <span class="filepath"> order.txt</span> 파일에서 항목의 이름을 변경합니다. </p> <p>예를 들어 새 주석에 주석 추가 이름을 변경하려면 <span class="wintitle"> 프로필 관리자</span>의 주석 추가 폴더의 이름을 새 주석으로 변경한 다음 <span class="filepath"> order.txt</span> 파일의 주석 추가 항목의 이름을 새 주석으로 변경합니다. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>메뉴 항목 숨기기 </p> </td> 
    <td colname="col2"> <p>메뉴 항목을 숨기지만 항목 자체를 삭제하지 않으려면 이름 앞에 빼기 기호(-)를 입력합니다. </p> <p>예를 들어 다음 결과는 <span class="wintitle"> 주석 추가</span>가 메뉴에 나타나지 않는 것입니다. </p> <p>범례 추가 </p> <p>-주석 추가 </p> <p>숨겨진 메뉴 항목을 다시 표시하려면 빼기 기호(-)를 제거하거나 <span class="filepath"> Insight.cfg</span> 파일에서 모두 숨김 취소 매개 변수를 사용하십시오. <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> 인사이트 구성 매개 변수</a>를 참조하십시오. </p> <p>다음 방법을 사용하여 메뉴 항목을 숨길 수도 있습니다. 
    <ul id="ul_CC9A82AFCE784CA49CC912C9256BAC1A"> 
    <li id="li_28C28CA0DE4B4A8F9C2C2C2B3BDD0557"> <p><span class="filepath"> .filter</span>, <span class="filepath"> .metric</span> 또는 <span class="filepath"> .dim</span> 파일의 Show 매개 변수는 각각의 메뉴에서 필터, 파생된 지표 및 차원 및 확장 차원을 숨깁니다. 이 옵션을 사용할 때 항목은 메뉴에 나열되지 않지만 여전히 프로필에 있으며 사용할 수 있습니다. </p> <p>이 매개 변수를 사용하여 필터 및 파생된 지표 및 차원을 숨기려면 <span class="filepath"> .metric</span>, <span class="filepath"> .dim</span> 또는 <span class="filepath"> .filter</span> 파일의 끝에 다음 줄을 추가하십시오. </p> <p><span class="filepath"> show = bool:false</span> </p> <p>이 매개 변수를 사용하여 확장 크기를 숨기려면 <i>데이터 집합 구성 안내서</i>의 10장을 참조하십시오. </p> <p><span class="filepath"> Insight.cfg</span> 파일에서 모두 숨김 취소 매개 변수를 설정하여 이 메서드를 사용하여 숨겨진 항목을 일시적으로 숨김 취소할 수 있습니다. 이 매개 변수에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> 인사이트 구성 매개 변수</a>를 참조하십시오. </p> </li> 
    <li id="li_2CB65D594DD04C59A8D27A17DBF278FA"><span class="filepath"> Transformation.cfg</span> 파일의 Hidden 매개 변수 또는 데이터 세트에 포함된 파일이 차원 메뉴에서 확장 차원을 숨깁니다. 이 옵션을 사용할 때 항목은 메뉴에 나열되지 않지만 여전히 프로필에 있으며 사용할 수 있습니다. <p> <p>참고: 이 방법을 사용하여 확장 차원을 숨길 때는 차원을 숨기려면 데이터 세트를 다시 변환해야 합니다. </p> </p> <p><span class="filepath"> Insight.cfg</span> 파일에서 모두 숨김 취소 매개 변수를 설정하여 이 메서드를 사용하여 숨겨진 항목을 일시적으로 숨김 취소할 수 있습니다. 이 매개 변수에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> 인사이트 구성 매개 변수</a>를 참조하십시오. </p> </li> 
    <li id="li_6E161953FEA44EC18237D88D7173DC60"> <p>0바이트 파일은 모든 유형의 항목을 메뉴에서 숨깁니다. 이 옵션을 사용할 때 빈(0바이트) 파일은 데이터를 포함하는 동일한 이름의 파일이 있는지 숨깁니다. Data Workbench은 0바이트 파일이 없는 것처럼 파일을 처리합니다. 자세한 내용은 <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> 비어 있는(0바이트) 파일을 사용하여 파일 숨기기</a>를 참조하십시오. </p> </li> 
    </ul> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>메뉴 항목 삭제 </p> </td> 
    <td colname="col2"> <p>이 파일이 [Exclusive] 옵션을 사용하도록 설정된 경우 이 파일에서 메뉴 항목을 간단히 삭제할 수 있습니다. 항목 자체는 여전히 프로필에 있지만 메뉴에 나열되지는 않습니다. </p> <p>이 파일이 [포함] 옵션을 사용하도록 설정된 경우 이 파일에서 메뉴 항목 이름을 제거하고 해당 파일을 삭제하거나 0바이트를 사용하여 메뉴에서 항목을 제거해야 합니다. </p> <p>파일 삭제에 대한 자세한 내용은 작업 프로필에서 파일 삭제</a>를 참조하십시오. <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-del-files-wkg-prof.md#task-1e29c25e6c824cc9b51cb651e835856b"> 0바이트 파일에 대한 자세한 내용은 <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> 비어 있는 파일(0바이트) 파일 숨기기</a>를 참조하십시오. </a></p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>그룹 헤더 추가 </p> </td> 
    <td colname="col2"> <p>표시할 머리글 텍스트 앞/뒤에 하이픈 3개를 입력합니다. </p> <p>예를 들어, 다음과 같이 관련 메뉴 항목 집합에 대한 관리 그룹 머리글이 만들어집니다. </p> <p>---관리--- </p> <p>프로필 </p> <p>데이터 집합 </p> <p> <img id="image_DB5BB8A33553499A9FC6B53C544CD4CC" src="assets/cfg_ordertxt_example.png"> </img> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>메뉴의 개별 섹션에 행 추가 </p> </td> 
    <td colname="col2"> <p>선을 표시할 3개의 하이픈을 입력합니다. </p> <p>예를 들어 다음 예제에서는 주석 추가 및 사용자 정의 추가를 구분하는 줄을 만듭니다. </p> <p>주석 추가 </p> <p>— </p> <p>사용자 지정 추가 </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. 파일을 저장하고 닫습니다.
1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL User] 열에서 [!DNL order.txt] 파일의 흰색 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > * **[!UICONTROL working profile name]**&#x200B;를 클릭합니다.
