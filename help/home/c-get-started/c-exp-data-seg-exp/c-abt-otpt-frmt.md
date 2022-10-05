---
description: 출력 형식을 지정하는 지침입니다.
title: 출력 형식
uuid: 12086f14-bad1-4d27-82fb-533e877d0a04
exl-id: e695eaf4-ebe5-4dd1-8191-8045021d6411
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---

# 출력 형식{#output-format}

{{eol}}

출력 형식을 지정하는 지침입니다.

* 각 지표 또는 차원 이름은 퍼센트 기호(%)로 시작하고 끝나야 합니다.

   * %XYZ%은(는) 수준 요소에 해당하는 차원 XYZ의 요소를 지정합니다. 차원 XYZ가 수준이 있는 일대일 또는 일대다 차원이 아닌 경우 오류가 생성됩니다.
   * %=XYZ% 은(는) 주어진 레벨 요소에 대한 지표 또는 지표 공식 XYZ의 값을 지정합니다.

* 두 개 이상의 Dimension 이름은 밑줄이 필요하지 않습니다.
* 두 단어 이상의 지표 이름에는 밑줄이 필요합니다.

>[!NOTE]
>
>Ctrl 키를 누른 채 [!DNL Output Format] 필드, [!DNL Insert menu] 이 나타납니다. 이 메뉴에는 구분 기호로 자주 사용되는 특수 문자 목록(예: Tab)이 포함되어 있습니다.

세그먼트에 대한 세션 기간 데이터를 내보내려면 세션 기간 지표를 기반으로 새 지표를 만들어야 합니다. 새 지표. 이것은 [!DNL Output Format] 세그먼트 내보내기 필드에서 Microsoft Excel에서 1시간 미만의 지속되는 세션을 올바르게 해석할 수 있습니다. 새 세션 기간 지표를 만들려면 [!DNL Session Duration.metric] 파일( [!DNL Profile Manager])를 클릭하고 ftime 문자열에 파운드 기호(#)를 삽입합니다. [!DNL ftime = string: %#H:%M:%S]

파운드 기호는 행간 &quot;0&quot;을 1시간 미만의 세션 기간에 추가합니다. 그 결과 Excel은 0을 해석합니다:53:21 - 53분 21초 다른 이름으로 새 지표를 저장하고, [!DNL User] 열 및 클릭 **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.
