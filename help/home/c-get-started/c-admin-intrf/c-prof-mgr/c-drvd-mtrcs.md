---
description: 새 지표(파생 지표라고도 함)를 정의하고 지표 편집기를 사용하여 기존 지표 정의를 편집합니다.
title: 파생 지표를 사용한 작업
uuid: 9767c170-e0cb-47b4-94f1-e9f6950b5926
exl-id: 83467c64-4b9a-44ab-91a2-202c76c89979
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 1%

---

# 파생 지표를 사용한 작업{#work-with-derived-metrics}

{{eol}}

새 지표(파생 지표라고도 함)를 정의하고 지표 편집기를 사용하여 기존 지표 정의를 편집합니다.

지표에 대한 자세한 내용은 이 섹션 및 [쿼리 언어 구문](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)를 참조하고 *지표, Dimension 및 필터 안내서*.

## 파생 지표 만들기 {#section-d57b98bf0a9940daba4920ff7efc808d}

을(를) 사용합니다 [!DNL Metric Editor] 이름, 공식 및 형식별로 새 지표를 정의하려면 나중에 사용할 수 있도록 User\*profile_name*\Metrics 폴더에 저장됩니다.

1. 새 열기 [!DNL Metric Editor] 사용 **[!UICONTROL Admin]** > **[!UICONTROL Profile]** 메뉴 옵션 또는 마우스 오른쪽 단추를 클릭하여 **[!UICONTROL User]** 지표를 만들 폴더의 열과 다음 **[!UICONTROL Create]** > **[!UICONTROL New Metric]**.

   A [!DNL Metric Editor] 표시됩니다.

1. 이름 매개 변수에 새 지표의 이름을 입력합니다.

   공백( )은 사용할 수 있지만 밑줄(_)은 사용할 수 없습니다. 또한 다음 기호를 사용할 수 없습니다.

   `+ - * /`

   ![](assets/vis_MetricEditor_NewAndEditing.png)

1. 공식 매개 변수에서 새 지표에 대한 표현식을 입력합니다. 필터는 대괄호 내에 정의해야 합니다 [ ] 를 입력합니다.

   추가 지표 표현식 구문 규칙에 대해서는 [지표 표현식 구문](../../../../home/c-get-started/c-qry-lang-syntx/c-syntx-mtrc-exp.md#concept-bbf440a0307549e088df491b51b51d66).

   다음 표는 확장 지표에 대한 샘플 표현식을 제공합니다.

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
      <td colname="col1"> <p>첫 번째 세션 변환 </p> </td> 
      <td colname="col2"> <p><span class="filepath"> 변환 [Session_Number="1"]</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>방문자당 평균 값 </p> </td> 
      <td colname="col2"> <p><span class="filepath"> 값/방문자</span> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   >[!NOTE]
   >
   >적절한 표현식을 입력하면 미리 보기 라인에 새 지표의 값이 표시됩니다. 표현식에 오류가 있으면 미리 보기 라인에 오류 메시지가 표시됩니다.

1. 마우스 오른쪽 단추 클릭 **[!UICONTROL (New)]** 을(를) 클릭합니다. **[!UICONTROL Save]**.

   지표를 저장하면 컴퓨터에 새 지표를 나타내는 파일이 Data Workbench 설치 디렉토리 \User\*profile name*\Metrics 폴더에 생성됩니다.

   ![](assets/vis_MetricEditor_NewAndEditing.png)

이제 기본 제공 지표처럼 선택하여 현재 프로필 전체에서 새 지표를 사용할 수 있습니다. 지표 메뉴에 지표가 표시되는 순서를 변경하려면 다음을 참조하십시오 [Order.txt 파일을 사용하여 메뉴 사용자 정의](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).

프로필의 모든 사용자가 작성한 지표를 사용하도록 하려면 을(를) 사용하여 작업 프로필에 게시해야 합니다 [!DNL Profile Manager]. 자세한 내용은 [작업 프로필에 파일 게시](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

## 파생 지표 편집 {#section-db6d924cf4e14bcc8d57cfe1059fc797}

1. 에서 [!DNL Profile Manager] 또는 [!DNL Metrics Manager]에서 *프로필 이름* 열에서 편집할 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Make Local]**.
1. 에서 지표 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.

   >[!NOTE]
   >
   >또한 [!DNL Metric Editor] 시각화 내에서 지표 관련 영역을 마우스 오른쪽 단추로 클릭하여 지표 메뉴를 표시합니다. 자세한 내용은 [지표 및 Dimension 메뉴 작업](../../../../home/c-get-started/c-vis/c-met-dim-menus.md#concept-50f07ae47c3e4f94ad7d3d7f8293ccac).

1. 에서 [!DNL Metric Editor]에서 2-4단계를 사용하여 필요에 따라 지표 정의를 편집하고 저장합니다 [새 파생 지표 만들기](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#section-d57b98bf0a9940daba4920ff7efc808d).

   프로필의 모든 사용자가 편집한 지표를 사용하도록 하려면 를 사용하여 작업 프로필에 게시해야 합니다. [!DNL Profile Manager]. 자세한 내용은 [작업 프로필에 파일 게시](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).
