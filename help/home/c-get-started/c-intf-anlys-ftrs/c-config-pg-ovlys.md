---
description: 페이지 오버레이는 사이트 응용 프로그램에서만 구성되지만 다른 응용 프로그램용으로 구성할 수 있습니다.
solution: Analytics
title: 페이지 오버레이 구성
topic: Data workbench
uuid: c4c612ed-5154-4b20-96ab-24b74fba19a2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 페이지 오버레이 구성{#configure-a-page-overlay}

페이지 오버레이는 사이트 응용 프로그램에서만 구성되지만 다른 응용 프로그램용으로 구성할 수 있습니다.

다른 응용 프로그램에 대한 페이지 오버레이 구성에 대한 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오.

페이지 오버레이 시각화는 HTML 링크 분석을 위한 도구입니다. 특정 페이지에 대한 오버레이를 요청할 때 데이터 워크벤치에서는 웹 브라우저에 표시되는 대로 실제 페이지의 스냅숏을 만들고 사용자가 정의하는 정규 표현식 목록에 따라 링크를 나타내는 HTML 코드를 구문 분석합니다. 선택한 페이지의 각 링크에 대해 첫 번째 일치 항목이 발견될 때까지 목록에서 작업하여 정규 표현식 패턴 일치를 찾으려고 시도합니다. 일치하는 항목이 있으면 페이지 오버레이에서 링크가 강조 표시된 상태로 나타납니다.

페이지 오버레이는 페이지 오버레이가 포함된 작업 영역에 색상 범례를 추가할 때만 데이터를 표시합니다.

>[!NOTE]
>
>페이지 오버레이를 구성하려면 신중한 구성 작업이 필요하며 링크가 데이터에 잘못 매핑되는 경우 잘못된 결과를 만들 수 있습니다. 특정 사이트에 대한 페이지 오버레이 구성과 관련된 작업은 사이트 페이지의 HTML 코드 내에서 링크가 표시되는 방식에 따라 달라집니다.

페이지 오버레이는 본질적으로 사용자에게 &quot;사람들이 클릭하는 곳&quot;이라는 정신 모델을 표시합니다. 시각화를 지원하는 데이터가 이 모델과 일치하지 않는 경우 혼동 가능성이 높습니다.

에서 [!DNL Site]링크는 일반적으로 다음 URI 또는 다음 링크 차원의 요소를 표시하지만 분석에 적합한 차원에 링크를 매핑할 수 있습니다. 다른 차원에 대한 페이지 오버레이 구성에 대한 자세한 내용은 Adobe 컨설팅 서비스에 문의하십시오.

>[!NOTE]
>
>페이지 오버레이에 페이지 차원을 사용하지 않는 것이 좋습니다. 사용자는 페이지 차원의 요소 이름을 변경하여 페이지 오버레이 기능이 의존하는 링크 구문을 변경할 수 있습니다.

에 대한 페이지 오버레이를 구성하려면 [!DNL Site]다음 두 개의 파일을 편집해야 합니다.

* **[!DNL Page Overlay.vw]:**이 파일은 페이지 오버레이 시각화를 만들기 위한 템플릿 파일입니다. 페이지 오버레이를 구성하는 프로필에 하나 이상의 템플릿 파일이 있어야 합니다.
* **[!DNL Page Overlay Link Templates.cfg]:**페이지 오버레이 시각화가 페이지를 로드할 때, 페이지 및 해당 대상의 링크를 자동으로 식별합니다. 이러한 링크를 데이터의 요소에 연결하려면 이 파일에서 정규 표현식 세트를 정의해야 합니다.

   차원의 요소와 일치하도록 여러 정규 표현식을 정의할 수 있습니다. 표현식을 정의하는 순서는 중요합니다. 특정 페이지에 대한 오버레이를 요청할 때 데이터 워크벤치에서는 웹 브라우저에 표시되는 대로 실제 페이지의 스냅숏을 만들고 사용자가 정의하는 정규 표현식 목록에 따라 링크를 나타내는 HTML 코드를 구문 분석합니다. 선택한 페이지의 각 링크에 대해 첫 번째 일치 항목이 발견될 때까지 목록에서 작업하여 정규 표현식 패턴 일치를 찾으려고 시도합니다. 차원 요소와 일치하는 첫 번째 표현식은 사용되는 표현식입니다. 따라서 가장 구체적인 일치 패턴으로 정규 표현식을 먼저 나열하고 그 다음에 덜 구체적인 표현식을 나열하는 것이 좋습니다. 일치하는 항목이 있으면 페이지 오버레이 시각화에서 링크가 강조 표시된 상태로 표시됩니다.

**사이트에 대한 페이지 오버레이를 구성하려면**

1. I

   에서 [!DNL Profile Manager]> **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**&#x200B;로 이동합니다.

   >[!NOTE]
   >
   >차원 요소 디렉토리에는 차원 요소를 마우스 오른쪽 단추로 클릭하면 나타나는 컨텍스트 메뉴 항목이 포함되어 있습니다. 예를 들어 URI 테이블을 연 다음 URI 요소를 선택합니다. URI를 마우스 오른쪽 단추로 클릭하면 페이지 오버레이가 나타납니다.

1. URI 폴더에서 [!DNL Page Overlay.vw] 파일 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다. 이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.
1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**&#x200B;를 클릭합니다.
1. 도메인(필요한 경우 브라우저 높이)을 지정합니다.

   ```
   window = simpleBorderWindow: 
     client = scrollWindow: 
       client = PageOverlay: 
         URI Template = string: http://%Domain%%Element%
         URI Parameters = map: 
           Domain = string: domain name
           Element = ref: Element/Name
         Dim = ref: wdata/model/dim/URI
         Dim Element = ref: Element/Name
         Level = ref: wdata/model/dim/Page View
         Group = ref: wdata/model/dim/Session
         Browser Height = int: browser height
     pos = v3d: (518, 202, 0)
     size = v3d: (810, 610, 0)
     titleBar = editor: 
       size = v3d: (61, 19, 0)
       text = string: 
   ```

1. 파일을 저장합니다.
1. 이 변경 사항을 작업 프로필의 모든 사용자가 사용할 수 있도록 하려면 [!DNL Profile Manager]열에서 해당 [!DNL .vw] 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL working profile name]***&#x200B;을 클릭합니다.

   >[!NOTE]
   >
   >다른 사이트 또는 하위 도메인에 대한 추가 템플릿 파일을 만들 수 있습니다. 만든 각 템플릿이 에 나타납니다 [!DNL Page Overlay menu].

1. 의 Context 폴더에서 [!DNL Profile Manager]파일 옆의 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL Page Overlay Link Templates.cfg] 을 **[!UICONTROL Make Local]**&#x200B;클릭합니다.

   이 파일에 대한 확인 표시가 [!DNL User] 열에 나타납니다.

1. 새로 만든 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**&#x200B;를 클릭합니다.
1. 마우스 오른쪽 버튼을 클릭하고 **[!UICONTROL Link Templates]** > **[!UICONTROL Add new]** **[!UICONTROL Regular Expression]**&#x200B;를 클릭합니다.
1. 필요에 따라 LinkRegex 벡터의 매개 변수를 편집합니다.

<table id="table_24DD4BB5009542F7BB1DA3318E2E6E2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 이 매개 변수의 경우... </th> 
   <th colname="col2" class="entry"> 이 정보 제공... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>차원 </p> </td> 
   <td colname="col2"> <p>링크로 표시되는 차원(일반적으로 다음 URI 차원)입니다. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>표현식 </p> </td> 
   <td colname="col2"> <p>HTML 링크의 관련 부분을 선택하여 차원에서 다음 요소를 찾는 데 사용되는 정규 표현식. 정규 표현식은 정확히 일치해야 하며 원하는 출력 패턴은 괄호로 그룹화됩니다. 정규 표현식에 대한 자세한 내용은 데이터 집합 <i>구성 안내서를 참조하십시오</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>출력 패턴 </p> </td> 
   <td colname="col2"> <p>차원 매개 변수의 결과 요소를 추출하는 데 사용되는 정규 표현식의 출력 패턴입니다. </p> </td> 
  </tr> 
 </tbody> 
</table>

다음 샘플 파일은 세 개의 정규 표현식을 보여 줍니다.

![](assets/cfg_PageOverlayLinkTemplates_Example.png)

1. 파일을 저장하려면 창 **[!UICONTROL (modified)]** 맨 위에 있는 을 마우스 오른쪽 버튼으로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.
1. 작업 프로필의 모든 사용자가 이 변경 내용을 사용할 수 있도록 하려면 [!DNL Page Overlay Link Templates.cfg] 열에서 확인 표시를 마우스 오른쪽 단추로 클릭하고 [!DNL User] > **[!UICONTROL Save to]** &lt; *>**[!UICONTROL working profile name]***&#x200B;를 클릭합니다.

