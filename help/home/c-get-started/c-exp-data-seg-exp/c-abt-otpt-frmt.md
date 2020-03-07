---
description: 출력 형식을 지정하기 위한 지침
solution: Analytics
title: 출력 형식
topic: Data workbench
uuid: 12086f14-bad1-4d27-82fb-533e877d0a04
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 출력 형식{#output-format}

출력 형식을 지정하기 위한 지침

* 각 지표 또는 차원 이름은 퍼센트 기호(%)로 시작하고 끝나야 합니다.

   * %XYZ%은(는) 수준 요소에 해당하는 XYZ 차원의 요소를 지정합니다. 차원 XYZ가 일대일 또는 일대다 수준이 아닌 경우 오류가 생성됩니다.
   * %=XYZ%는 주어진 레벨 요소에 대한 지표 또는 지표 공식 XYZ의 값을 지정합니다.

* 두 단어 이상의 차원 이름에는 밑줄이 필요하지 않습니다.
* 두 단어 이상의 지표 이름에는 밑줄이 필요합니다.

>[!NOTE]
>
>Ctrl 키를 누른 채로 [!DNL Output Format] 필드 내에서 마우스 오른쪽 단추를 클릭하면 [!DNL Insert menu] 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자(예: Tab) 목록이 포함되어 있습니다.

세그먼트에 대한 세션 기간 데이터를 내보내려면 세션 기간 지표를 기반으로 새 지표를 만들어야 합니다. 세그먼트 내보내기 [!DNL Output Format] 필드에서만 사용할 수 있는 새 지표를 사용하면 Microsoft Excel에서 1시간 미만의 지속 가능한 세션을 올바르게 해석할 수 있습니다. 새 세션 지속 시간 지표를 만들려면 [!DNL Session Duration.metric] 파일( [!DNL Profile Manager]에서)을 열고 시간 문자열에 파운드 기호(#)를 삽입합니다. [!DNL ftime = string: %#H:%M:%S]

파운드 기호는 1시간 미만의 세션 기간에 행간 &quot;0&quot;을 추가합니다. 따라서 Excel은 0:53:21을 53분 21초로 해석합니다. 새 지표를 다른 이름으로 저장하고 다른 사람이 사용할 수 있도록 해당 프로필에 업로드합니다. [!DNL User] 열에서 해당 파일에 대한 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*&#x200B;을 클릭합니다.
