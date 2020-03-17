---
description: 사이드바는 정기적으로 사용되는 기능에 액세스하고 작업 영역 간을 이동할 때 시각화를 유지합니다.
solution: Analytics
title: 세로 막대 구성
topic: Data workbench
uuid: 0d2f0b9a-56a9-4f27-aaa6-1f9bf7fcab2d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 세로 막대 구성{#configure-the-sidebar}

사이드바는 정기적으로 사용되는 기능에 액세스하고 작업 영역 간을 이동할 때 시각화를 유지합니다.

관리자는 사이드바를 사용자 정의하여 다른 사용자 그룹에 적합한 다음 사이드바를 프로필로 배포할 수 있습니다.

사이드바는 필터 및 로컬 오버라이드를 추적하는 데 도움이 되는 데 이상적입니다. 사이드바를 사용하지 않으려면 숨길 수 있습니다.

## 세로 막대에 시각화 추가 {#section-666f70a405db4f8d8eaffa567ffcac06}

1. 데이터 워크벤치를 시작합니다.
1. 세로 막대에서 **[!UICONTROL Add]** > *&lt;**[!UICONTROL item]**>*&#x200B;을 클릭합니다. 예: [!DNL Selections Panel], [!DNL Filters Panel]또는 [!DNL Table].

   다음 사이드바 패널은 데이터 워크벤치의 표준 설치에서 사용할 수 있습니다. 특정 프로필에서 더 많은 항목을 사용할 수 있습니다.

   * **선택 패널:** 현재 작업 영역에서 어떤 선택 사항이 활성 상태인지 이해할 수 있습니다. 새 항목을 선택할 때마다 [!DNL Selections Panel] 업데이트됩니다. 을 클릭하여 선택 사항을 지울 수 **[!UICONTROL x]**&#x200B;있습니다. 데이터를 [선택하는 방법에 대한 자세한 내용은 시각화의](../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746) 선택 사항을 참조하십시오.
   * **필터 패널:** 저장된 필터를 손쉽게 로드하고 적용할 수 있습니다. 여러 필터를 로드하고 옆에 있는 확인란을 클릭하여 각 필터를 개별적으로 활성화하거나 비활성화할 수 있습니다. 편집기 [필터링을 참조하십시오](../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).
   * **로컬 재정의 패널:** 이 패널에는 프로필의 개인 사본에 수정된 지표, 차원 및 필터가 표시됩니다. 이렇게 하면 클라이언트에서 데이터가 표시되는 방법과 다른 사용자의 데이터 표시 방식이 다를 수 있음을 알리는 데 도움이 됩니다. 지표, 차원 또는 필터의 변경 사항을 서버에 저장할 때 재정의가 [!DNL Local Overrides panel]서버에서 제거됩니다. 재지정을 클릭한 다음 을 클릭하면 로컬 재정의가 **[!UICONTROL Revert to Server]**&#x200B;제거되고 항목이 공유 버전으로 돌아갑니다.
   * **지표 범례:** 지표 범례를 추가합니다. [!DNL Metric legends] 프로필과 관련된 기준 지표 및 데이터 세트와 관련된 통계(또는 현재 선택 항목이 있는 경우)를 볼 수 있습니다. 지표 [범례를 참조하십시오](../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b).
   * **색상 범례:** 색상 범례를 추가합니다. 전환 및 유지와 같은 지표별로 시각화를 색상 코드로 작성하고 거의 모든 곳에서 사용할 수 [!DNL Workspace]있습니다. 비즈니스 지표를 색상에 연결하면 예외 항목, 예외 사항 및 트렌드를 쉽게 파악할 수 있습니다. 색상 [범례를 참조하십시오](../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).
   * **텍스트 주석:** 메모 패널을 추가합니다. [!DNL Text annotations] 은 임의의 텍스트를 입력하여 설명 정보나 설명을 추가할 수 있는 창입니다 [!DNL Workspace]. 텍스트 [주석 작업을 참조하십시오](../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777).
   * **표:** 표를 추가합니다. 표는 하나 이상의 데이터 차원에 대해 하나 이상의 지표를 표시할 수 있습니다. 표를 [참조하십시오](../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f).
   * **열기:** 저장된 파일을 엽니다.

## 세로 막대 패널 열기 {#section-cbc8e57491854274a577d47a48c306b8}

저장된 위치 또는 클립보드에서 사이드바 시각화 파일을 열 수 있습니다.

1. 세로 막대에서 **[!UICONTROL Add]** > **[!UICONTROL Open]**&#x200B;을 클릭합니다.
1. 을 **[!UICONTROL File]** 클릭하여 추가할 패널의 [!DNL .vw] **[!UICONTROL Last Closed Window]**&#x200B;파일을 찾거나 을 클릭하여 클립보드에서 시각화를 가져옵니다.

   또한 을 클릭하여 클립보드에 복사한 시각화를 붙여넣을 **[!UICONTROL From Clipboard]** 수 있습니다. 세로 [막대 패널 복사를 참조하십시오](../../home/c-get-started/c-config-sidebar.md#section-720ae057632a4b8dbb94412e06a370b1).

## 세로 막대 패널 복사 {#section-720ae057632a4b8dbb94412e06a370b1}

1. 패널의 위쪽 테두리를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Copy]** > **[!UICONTROL Window]**&#x200B;를 클릭합니다.
1. 패널을 붙여넣으려면 **[!UICONTROL Add]** > **[!UICONTROL Open]** > **[!UICONTROL From Clipboard]**&#x200B;을 클릭합니다.

## 세로 막대 패널 저장 {#section-fb19936b12704fb0a4c592abb579db1d}

세로 막대 패널에서 제목 표시줄을 마우스 오른쪽 버튼으로 클릭하고 을 클릭합니다 **[!UICONTROL Save]**.

마찬가지로 저장된 사이드바 시각화를 열 수 있습니다. 데이터 워크벤치에서는 시각화를 지정한 위치에 [!DNL .vw] 파일로 저장합니다.

## 기본 세로 막대로 되돌리기 {#section-4d14b8771ad747bba799876267f24831}

세로 막대에서 **[!UICONTROL Options]** > **[!UICONTROL Revert]**&#x200B;을 클릭합니다.

데이터 워크벤치를 닫으면 시스템이 사용자 프로필의 [!DNL sidebar.vw] 파일에 현재 사이드바 구성을 저장합니다. 데이터 워크벤치를 열면 시스템은 상위 프로필이 아닌 사용자 프로필에서 [!DNL sidebar.vw] 파일을 로드합니다.

사용자 프로필에서 사이드바를 삭제하고 상위 프로필에서 사이드바를 다시 로드하는 기본 또는 이전에 저장한 세로 막대로 되돌릴 수 있습니다. 관리자는 기본(상위) 사이드바를 에서 업로드하여 로컬 사이드바로 교체할 수 [!DNL Profile Manager]있습니다.

## 추가 상태 패널 파일 사용자 정의 {#section-8d502f3b59cc4331966edec05e896ce1}

시스템 관리자는 에서 공식을 작성할 수 [!DNL More Status Panel.vw]있습니다. 이 경우 지표 및 차원 값에 컨텍스트 단어가 표시되며, 세로 막대의 결과를 표시합니다. [!DNL More Status panel]

세로 막대에 [!DNL More Status panel] 표시하려면 다음 예제에 표시된 화살표를 클릭합니다.

![](assets/more_status_panel_arrows.png)

다음 절차에서는 데이터 세트에 있는 일 수를 알려주는 사용자 지정 상태를 만드는 방법에 대한 간단한 예를 보여줍니다.

1. 에서 [!DNL Profile Manager][! **UICONTROL 사이드바\]를 클릭합니다**.

1. 열에서 파일의 로컬 복사본을 [!DNL Base_5_3*] 만듭니다 [!DNL More Status Panel.vw] .

   이렇게 하려면 파일 확인 표시를 마우스 오른쪽 단추로 클릭하고 을 클릭합니다 **[!UICONTROL Make Local]**.

1. 파일을 메모장 [!DNL More Status Panel.vw][!DNL .vw] [!DNL Editor] 또는 메모장에서 엽니다.

   ![](assets/more_status_panel_file.png)

1. 의 [!DNL Context] 및 [!DNL Items] 필드를 완료합니다 [!DNL Editor]. 구문에 [대한 지침은](../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f) 쿼리 언어 구문을 참조하십시오.

1. 파일을 저장합니다.

   앞의 예제의 값은 다음과 같이 상태 공식이 표시됩니다.

   ![](assets/more_status_panel.png)
