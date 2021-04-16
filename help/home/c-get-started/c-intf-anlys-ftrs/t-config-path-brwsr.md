---
description: 경로 브라우저는 응용 프로그램과 데이터 세트에 대해 의미가 있는 기본 차원, 그룹 차원, 레벨 차원 및 지표의 모든 조합에서 작동하도록 구성할 수 있습니다.
title: 경로 브라우저 구성
uuid: 1ba3fb6e-b76f-428f-b6ec-077669c3b305
exl-id: be6a68f7-e3e3-4207-a112-3a4fdd5c5f57
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 2%

---

# 경로 브라우저 구성{#configure-a-path-browser}

경로 브라우저는 응용 프로그램과 데이터 세트에 대해 의미가 있는 기본 차원, 그룹 차원, 레벨 차원 및 지표의 모든 조합에서 작동하도록 구성할 수 있습니다.

경로 브라우저를 구성한 후에는 [!DNL Add Visualization] 메뉴에 다른 경로 브라우저와 함께 나열됩니다.

1. [!DNL Profile Manager]에서 **[!UICONTROL Menu]**&#x200B;을 클릭한 다음 **[!UICONTROL Add Visualization]** 및 **[!UICONTROL Path Browser]**&#x200B;을 클릭합니다.

   하나 이상의 [!DNL *.vw] 파일이 경로 브라우저 디렉토리에 있습니다.

1. 원하는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**&#x200B;을 클릭합니다.
1. [!DNL User] 열에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다.
1. 다음 샘플 파일과 표를 안내선으로 사용하여 파일의 매개 변수를 편집합니다.

   ```
   window = simpleBorderWindow: 
     client = pathBrowser: 
       Left Path = vector: 0 items
       Map = ref: wdata/model/dim/base dimension name
       Map Group = ref: wdata/model/dim/group dimension name
       Map Level = ref: wdata/model/dim/level dimension name
       Metric = ref: wdata/model/metric/metric name
       Right Path = vector: 0 items
       size = v3d: (673, 279, 0)
     pos = v3d: (714, 143, 0)
     size = v3d: (673, 298, 0)
   ```

<table id="table_1DCCB4B24B554B72A781B304B5EB155E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우.. </th> 
   <th colname="col2" class="entry"> 이 정보 제공... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>기본 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>경로 브라우저에 요소가 나타나는 치수의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>그룹 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>경로 브라우저에서 경로를 구성하기 위해 레벨 차원의 요소를 그룹화하는 방법을 결정하는 차원의 이름입니다. 특히 경로 브라우저의 단일 경로와 연관된 레벨 차원 요소는 그룹 차원의 요소를 두 개 이상 확장할 수 없습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>레벨 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>요소를 경로 브라우저로 드래그하는 기본 차원의 레벨(상위)의 이름입니다. 한 기본 차원 요소에서 다음 차원 요소로 경로를 따라가면 한 레벨 차원 요소에서 다음 레벨 차원 요소로 이동합니다. 기본 차원 요소의 경로를 선택하면 레벨 차원의 해당 요소에 대한 데이터를 선택합니다. 선택 영역에는 항상 루트와 관련된 레벨 차원의 요소가 포함되며 경로에 요소를 더 추가하여 다듬습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>지표 이름</i> </p> </td> 
   <td colname="col2"> <p>지정된 요소의 값이 해당 요소로 연결되는 경로의 두께에 비례하는 지표의 이름입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>경로 브라우저에 대한 기본 차원, 그룹 차원, 레벨 차원 및 지표에 대한 자세한 내용은 [경로 브라우저](../../../home/c-get-started/c-analysis-vis/c-path-browsers/c-path-browsers.md#concept-f2e9fdafed6e49c2bd111ab425cd6e2b)를 참조하십시오.

1. 메모장에서 **[!UICONTROL File]** > **[!UICONTROL Save As]**&#x200B;을 클릭하여 그룹 차원(즉, *그룹 차원 이름*.vw)을 기준으로 새 이름으로 파일을 저장합니다.

   파일을 경로 브라우저 디렉토리에 저장해야 합니다.

   >[!NOTE]
   >
   >경로 브라우저가 [!DNL *.vw] 파일로 저장되었는지 확인하려면 [!DNL Save As] 창에서 다른 이름으로 저장을 모든 파일로 설정합니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL Profile Manager]에서 [!DNL User] 열에 있는 파일의 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.
