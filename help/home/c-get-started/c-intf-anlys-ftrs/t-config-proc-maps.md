---
description: 프로세스 맵은 애플리케이션 및 데이터 세트에 적합한 기본 차원, 그룹 차원, 레벨 차원 및 지표의 조합에서 작동하도록 구성할 수 있습니다.
title: 프로세스 맵 구성
uuid: e629191e-48b9-4b58-b6aa-3705ff7b387e
exl-id: 0b37e942-4596-45cc-bc31-db147626f4eb
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 1%

---

# 프로세스 맵 구성{#configure-a-process-map}

{{eol}}

프로세스 맵은 애플리케이션 및 데이터 세트에 적합한 기본 차원, 그룹 차원, 레벨 차원 및 지표의 조합에서 작동하도록 구성할 수 있습니다.

프로세스 맵을 구성하면 [!DNL Add Visualization menu].

1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Menu]**&#x200B;를 클릭합니다. **[!UICONTROL Add Visualization]**&#x200B;를 클릭한 다음 구성할 프로세스 맵 유형(2D 지표 맵, 2D 프로세스 맵 또는 3D 프로세스 맵)을 클릭합니다.

   하나 이상 [!DNL *.vw] 파일이 디렉토리에 있습니다.

1. 원하는 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 를 클릭합니다 **[!UICONTROL Make Local]**.
1. 에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. 다음 샘플 파일과 표를 안내서로 사용하여 파일의 매개 변수를 편집합니다.

   ```
   window = simpleBorderWindow: 
     client = processMap: 
       Traffic Metric = ref: wdata/model/metric/metric name
       center = v3d: (-0.741014, 0, 0.0639476)
       color_links = bool: true
       Map = PrefixDim: 
         Name = string: Map
         Base Dimension = ref: wdata/model/dim/base dimension name
         Element Prefixes = vector: 0 items
         Element Names = vector: 0 items
       Map Level = ref: wdata/model/dim/level dimension name
       Map Group = ref: wdata/model/dim/group dimension name
       node_label = vector<bool>: 
       node_positions = vector: 0 items
       quantify_links = int: 2
       range = double: 2.37386
       size = v3d: (430, 290, 0)
       xAxisMetric = ref: wdata/model/metric/metric name for metric map
     pos = v3d: (880, 595, 0)
     size = v3d: (430, 309, 0)
   ```

<table id="table_3F072DB1B68746C49DF9332718982EBE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우.. </th> 
   <th colname="col2" class="entry"> 이 정보 제공.. </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>지표 이름</i> </p> </td> 
   <td colname="col2"> <p>지정된 노드의 값이 노드 크기에 비례하는 지표의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>기본 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>프로세스 맵에서 요소가 노드로 표시되는 차원의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>수준 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>요소를 프로세스 맵으로 드래그하는 기본 차원의 레벨(상위)의 이름입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>그룹 차원 이름</i> </p> </td> 
   <td colname="col2"> <p>노드 간의 연결을 형성하도록 레벨 차원의 요소를 그룹화하는 방법을 결정하는 차원의 이름입니다. 두 노드 사이의 연결은 그룹 차원의 두 요소 이상에 걸쳐 있을 수 없습니다. 프로세스 맵 내의 노드를 기준으로 선택하면 해당 노드에 관련된 그룹 차원의 모든 요소를 선택할 수 있습니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>지표 맵의 지표 이름</i> </p> </td> 
   <td colname="col2"> <p>이 매개 변수는 2D 지표 맵에만 적용됩니다. </p> <p>값이 맵에서 노드의 수평 위치를 결정하는 지표의 이름입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>프로세스 맵의 기본 차원, 그룹 차원, 레벨 차원 및 지표에 대한 자세한 내용은 [프로세스 맵](../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

1. 메모장에서 **[!UICONTROL File]** > **[!UICONTROL Save As]** 기본 차원을 기반으로 새 이름으로 파일을 저장하려면, 즉 *기본 차원 이름*.vw

   (2D 지표 맵을 구성하는 경우, 지표 맵의 지표 이름(즉, *지표 맵의 지표 이름*.vw) 파일을 적절한 프로세스 맵 디렉토리에 저장해야 합니다.

   >[!NOTE]
   >
   >프로세스 맵이 [!DNL *.vw] 파일, [!DNL Save As] 창의 다른 이름으로 저장 유형을 모든 파일로 설정합니다.

1. (선택 사항) 작업 프로필의 모든 사용자가 변경 사항을 사용할 수 있도록 하려면 [!DNL Profile Manager]에서 파일의 확인 표시를 마우스 오른쪽 단추로 클릭합니다. [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.
