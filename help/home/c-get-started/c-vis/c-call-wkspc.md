---
description: 설명선은 해당 요소의 가상 선택 항목으로 새 시각화를 만들어 특정 차원 요소에 관심을 끌기 위해 작업 공간에 추가하는 창입니다.
title: 작업 영역에 설명선 추가
uuid: fb3dd74d-da20-40cb-bc96-e56d25003e48
exl-id: fcdb9231-d44a-4287-b799-6a66f7f79432
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 2%

---

# 작업 영역에 설명선 추가{#adding-callouts-to-a-workspace}

설명선은 해당 요소의 가상 선택 항목으로 새 시각화를 만들어 특정 차원 요소에 관심을 끌기 위해 작업 공간에 추가하는 창입니다.

Data Workbench은 표준 콜아웃 유형 세트로 제공됩니다. 구현을 완전히 사용자 정의할 수 있기 때문에 구현에 나타나는 사용 가능한 콜아웃 유형은 이 안내서에 설명된 것과 다를 수 있습니다.

기본적으로 Data Workbench은 다음 설명선을 제공합니다.

* [주석](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-7b6742160b3f4aed872a09c8c023f90d)
* [빈 선 그래프](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [빈 산포도](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [빈 표](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-5dcc0504bdb64ed4976f880e2f7b277f)
* [신뢰 범례](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-386d1293ddc24a0c9cccb332e20db791)
* [지표 범례](../../../home/c-get-started/c-vis/c-call-wkspc.md#section-daa6d372c22246d9827880a9d6e804d8)

>[!NOTE]
>
>콜아웃은 설명선 내에서 선택을 하지 않는 한 선택(즉, 작업 공간 내의 다른 시각화에는 영향을 주지 않음)으로 작동하지 않습니다.

*프로필 이름*\Context\Callout folder of the [!DNL Server] 설치 폴더에 저장된 콜아웃 파일을 구성하여 콜아웃 정의를 추가하거나 편집할 수 있습니다. [설명선 구성](../../../home/c-get-started/c-intf-anlys-ftrs/c-config-callouts.md#concept-f6e91e172f5e4c009245c9c549beb76a)을 참조하십시오.

## 시각화에 주석 콜아웃을 추가하려면 {#section-7b6742160b3f4aed872a09c8c023f90d}

1. 콜아웃을 만들 요소를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Image]** 또는 **[!UICONTROL Add Callout]** > **[!UICONTROL Annotation]** > **[!UICONTROL Text]**&#x200B;를 클릭합니다. 해당 요소에 대한 표시 가능한 연결이 있는 빈 창이 표시됩니다.

   ![](assets/client-call.png)

   그래프 시각화에 설명선을 추가하려면 시각화(기본 축)의 아래쪽을 마우스 오른쪽 단추로 클릭하여 메뉴를 열어야 합니다.

   ![](assets/visualization_callout_linegraph.png)

1. 선택한 내용에 따라 적절한 단계를 완료하십시오.

   * 텍스트 주석의 경우 원하는 텍스트를 설명선에 입력하거나 붙여 넣은 다음 텍스트 서식을 적절하게 지정합니다. [텍스트 주석 작업](../../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777)을 참조하십시오.
   * 이미지 주석의 경우 이미지를 복사한 다음 설명선 내에서 마우스 오른쪽 단추를 클릭하여 원하는 이미지를 설명선에 붙여넣습니다. 클릭 **[!UICONTROL Paste image]**. [이미지 주석 작업](../../../home/c-get-started/c-analysis-vis/c-annots/c-image-annots.md#concept-02081ed7d91c4fdcb8fc863f2a51c962)을 참조하십시오.

## 시각화 {#section-5dcc0504bdb64ed4976f880e2f7b277f}에 빈 표, 선 그래프 또는 산포도 콜아웃을 추가하려면

1. 콜아웃을 만들 요소를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Callout]** > *&lt;**[!UICONTROL callout type]***&#x200B;을 클릭합니다.

   다음 예는 빈 테이블 설명선을 보여줍니다.

   ![](assets/vis_callout_blank_bar_graph.png)

1. 차원을 선택하려면 **[!UICONTROL None]**&#x200B;을 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Change Dimension]** > *&lt;**[!UICONTROL dimension name]***&#x200B;를 클릭합니다.

   >[!NOTE]
   >
   >콜아웃이 있는 시각화 내의 차원을 변경하는 경우 콜아웃은 원래 차원의 요소에 연결되어 전체 시각화에 연결되도록 변경됩니다.

## 시각화 {#section-386d1293ddc24a0c9cccb332e20db791}에 신뢰 범례 콜아웃을 추가하려면

1. 콜아웃을 만들 요소를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Callout]** > **[!UICONTROL Confidence Legend]**&#x200B;을 클릭합니다.

   ![](assets/vis_callout_confidenceLegend.png)

1. 원하는 경우 [!DNL Metric or Formula] 필드를 변경합니다.

표현식 구문 규칙에 대해서는 [쿼리 언어 구문](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)을 참조하십시오. [신뢰 범례](../../../home/c-get-started/c-analysis-vis/c-legends/c-conf-leg.md#concept-73db81c2c218427786c04068aa778efd)를 참조하십시오.

## 시각화 {#section-daa6d372c22246d9827880a9d6e804d8}에 지표 범례 콜아웃을 추가하려면

1. 콜아웃을 만들 요소를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Add Callout]** > **[!UICONTROL Metric Legend]**&#x200B;을 클릭합니다.

   ![](assets/vis_callout_metricLegend.png)

1. 원하는 경우 지표 범례에 지표를 추가하거나 제거합니다.

[지표 범례](../../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b)를 참조하십시오.
