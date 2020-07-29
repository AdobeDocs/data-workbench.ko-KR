---
description: 새 지표(파생 지표라고도 함)를 정의하고 지표 편집기를 사용하여 기존 지표 정의를 편집합니다.
solution: Analytics
title: 파생 지표를 사용한 작업
topic: Data workbench
uuid: 9767c170-e0cb-47b4-94f1-e9f6950b5926
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 파생 지표를 사용한 작업{#work-with-derived-metrics}

새 지표(파생 지표라고도 함)를 정의하고 지표 편집기를 사용하여 기존 지표 정의를 편집합니다.

이 섹션 및 쿼리 언어 구문에 제공된 것보다 지표에 대한 자세한 [내용은](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)지표, 차원 *및 필터 안내서를 참조하십시오*.

## 파생된 지표 만들기 {#section-d57b98bf0a9940daba4920ff7efc808d}

을 [!DNL Metric Editor] 사용하여 이름, 공식 및 형식별로 새 지표를 정의할 수 있으며 이 지표는 나중에 사용할 수 있도록 User\*profile_name*\Metrics 폴더에 저장됩니다.

1. &#x200B;> [!DNL Metric Editor] 메뉴 옵션을 **[!UICONTROL Admin]** 사용하거나 지표를 만들 폴더의 **[!UICONTROL Profile]** 열을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL User]** > **[!UICONTROL Create]** **[!UICONTROL New Metric]**&#x200B;을 클릭하여 새로 엽니다.

   A가 [!DNL Metric Editor] 표시됩니다.

1. 이름 매개 변수에 새 지표의 이름을 입력합니다.

   공백()은 허용되고 밑줄(_)은 허용되지 않습니다. 또한 다음 심볼은 사용할 수 없습니다.

   `+ - * /`

   ![](assets/vis_MetricEditor_NewAndEditing.png)

1. 공식 매개 변수에서 새 지표에 대한 표현식을 입력합니다. 필터를 대괄호 안에 정의해야 합니다 [ ] in the expression.

   추가 지표 표현식 구문 규칙에 대해서는 지표 [표현식에 대한 구문을 참조하십시오](../../../../home/c-get-started/c-qry-lang-syntx/c-syntx-mtrc-exp.md#concept-bbf440a0307549e088df491b51b51d66).

   다음 표에서는 확장 지표에 대한 샘플 표현식을 제공합니다.

   <table id="table_ED77997FC08F492490DCAC3C4153781C"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> 확장 지표 이름 </th> 
      <th colname="col2" class="entry"> 표현식 </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>첫 번째 세션 비율 </p> </td> 
      <td colname="col2"> <p><span class="filepath"> 세션 [Session_Number="1"]/세션</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>전환 첫 번째 세션 </p> </td> 
      <td colname="col2"> <p><span class="filepath"> 전환 [Session_Number="1"]</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>방문자당 평균 값 </p> </td> 
      <td colname="col2"> <p><span class="filepath"> 가치/방문자</span> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   >[!NOTE]
   >
   >적절한 표현식을 입력하면 미리 보기 라인에 새 지표의 값이 표시됩니다. 식에 오류가 있으면 미리 보기 행에 오류 메시지가 표시됩니다.

1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL (New)]** 클릭합니다 **[!UICONTROL Save]**.

   지표를 저장할 때 새 지표를 나타내는 파일이 사용자 컴퓨터에 Data Workbench 설치 디렉토리 \User\*profile name*\Metrics 폴더에 생성됩니다.

   ![](assets/vis_MetricEditor_NewAndEditing.png)

이제 모든 기본 제공 지표처럼 선택하여 현재 프로필 전체에서 새 지표를 사용할 수 있습니다. 지표 메뉴에 지표가 표시되는 순서를 변경하려면 Order.txt [파일을 사용하여 메뉴 사용자 지정을 참조하십시오](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).

프로파일의 모든 사용자가 만든 지표를 사용하도록 하려면, 아이콘을 사용하여 작업 프로필에 게시해야 합니다 [!DNL Profile Manager]. 작업 [프로필에 파일 게시를 참조하십시오](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

## 파생된 지표 편집 {#section-db6d924cf4e14bcc8d57cfe1059fc797}

1. 또는 [!DNL Profile Manager][!DNL Metrics Manager]프로필 이름 *열에서 편집할 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음* **[!UICONTROL Make Local]**&#x200B;을 클릭합니다.
1. 열에서 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Open]** **[!UICONTROL from the workbench]**&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >시각화 내에서 지표 관련 영역을 마우스 오른쪽 단추로 [!DNL Metric Editor] 클릭하여 지표 메뉴를 표시할 수도 있습니다. 자세한 내용은 지표 및 [차원 메뉴 작업을 참조하십시오](../../../../home/c-get-started/c-vis/c-met-dim-menus.md#concept-50f07ae47c3e4f94ad7d3d7f8293ccac).

1. 에서, 새 파생된 지표 [!DNL Metric Editor]만들기의 단계 2-4를 사용하여 필요에 따라 지표 [정의를 편집하고 저장합니다](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#section-d57b98bf0a9940daba4920ff7efc808d).

   편집한 지표를 프로필의 모든 사용자가 사용하도록 하려면 아이콘을 사용하여 작업 프로필에 게시해야 합니다 [!DNL Profile Manager]. 작업 [프로필에 파일 게시를 참조하십시오](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

