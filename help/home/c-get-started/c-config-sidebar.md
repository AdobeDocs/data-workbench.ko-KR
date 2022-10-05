---
description: 사이드바는 정기적으로 사용되는 기능에 액세스할 수 있고 작업 공간 간을 이동할 때 시각화를 유지합니다.
title: 사이드바 구성
uuid: 0d2f0b9a-56a9-4f27-aaa6-1f9bf7fcab2d
exl-id: 75ccc869-8ced-4beb-b3d7-ed7febe347f9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 1%

---

# 사이드바 구성{#configure-the-sidebar}

{{eol}}

사이드바는 정기적으로 사용되는 기능에 액세스할 수 있고 작업 공간 간을 이동할 때 시각화를 유지합니다.

관리자는 사이드바를 사용자 지정하여 다양한 사용자 그룹에 적합하도록 만든 다음, 프로필로 사이드바를 배포할 수 있습니다.

사이드바는 필터 및 로컬 재정의를 추적하는 데 이상적입니다. 사이드바를 사용하지 않으려면 숨길 수 있습니다.

## 사이드바에 시각화 추가 {#section-666f70a405db4f8d8eaffa567ffcac06}

1. Data Workbench 시작.
1. 사이드바에서 **[!UICONTROL Add]** > *&lt;**[!UICONTROL item]**>*. 예를 들어 [!DNL Selections Panel], [!DNL Filters Panel] 또는 [!DNL Table]라는 쿠키를 설정할 수 있습니다. 

   다음 사이드바 패널은 표준 Data Workbench 설치에서 사용할 수 있습니다. 특정 프로필에서 더 많은 항목을 사용할 수 있습니다.

   * **선택 패널:** 현재 작업 공간에서 활성 상태인 항목을 이해할 수 있습니다. 다음 [!DNL Selections Panel] 를 새로 선택할 때마다 업데이트됩니다. 을 클릭하여 선택 항목을 지울 수 있습니다 **[!UICONTROL x]**. 자세한 내용은 [시각화에서 선택](../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746) 를 참조하십시오.
   * **필터 패널:** 저장된 필터를 쉽게 로드하고 적용할 수 있습니다. 여러 필터를 로드하고, 필터 옆의 확인란을 클릭하여 각 필터를 독립적으로 활성화하거나 비활성화할 수 있습니다. 자세한 내용은 [필터 편집기](../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).
   * **로컬 재정의 패널:** 이 패널에는 프로필의 개인 복사본에서 수정한 지표, 차원 및 필터가 표시됩니다. 이렇게 하면 클라이언트에 데이터가 표시되는 방식과 다른 사용자의 데이터 표시 방식 간에 가능한 차이가 발생할 수 있음을 알 수 있습니다. 지표, 차원 또는 필터에 변경 사항을 서버에 저장하면 재정의가 서버에서 제거됩니다 [!DNL Local Overrides panel]. 무시를 클릭한 다음 **[!UICONTROL Revert to Server]**&#x200B;를 입력하면 로컬 재정의가 제거되고 항목이 공유 버전으로 되돌아갑니다.
   * **지표 범례:** 지표 범례를 추가합니다. [!DNL Metric legends] 프로필과 관련된 기준 지표 및 데이터 세트와 관련된 통계(생성된 경우 현재 선택 항목)를 볼 수 있습니다. 자세한 내용은 [지표 범례](../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b).
   * **색상 범례:** 색상 범례를 추가합니다. 전환 및 보존과 같은 지표별로 색상 코드 시각화를 사용하여 거의 모든 위치에서 사용할 수 있습니다 [!DNL Workspace]. 비즈니스 지표를 색상에 연결하면 예외 항목, 예외 사항 및 트렌드를 쉽게 파악할 수 있습니다. 자세한 내용은 [색상 범례](../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).
   * **텍스트 주석:** 메모 패널을 추가합니다. [!DNL Text annotations] 임의의 텍스트를 입력하여 설명 정보나 설명을 추가할 수 있는 창입니다 [!DNL Workspace]. 자세한 내용은 [텍스트 주석 작업](../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777).
   * **표:** 테이블을 추가합니다. 테이블에는 하나 이상의 데이터 차원에 대해 하나 이상의 지표가 표시될 수 있습니다. 자세한 내용은 [표](../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f).
   * **열기:** 저장된 파일을 엽니다.

## 사이드바 패널 열기 {#section-cbc8e57491854274a577d47a48c306b8}

저장된 위치 또는 클립보드에서 사이드바 시각화 파일을 열 수 있습니다.

1. 사이드바에서 **[!UICONTROL Add]** > **[!UICONTROL Open]**.
1. 클릭 **[!UICONTROL File]** 를 찾으려면 [!DNL .vw] 추가할 패널의 파일을 클릭하거나 **[!UICONTROL Last Closed Window]**: 클립보드에서 시각화를 가져옵니다.

   또한 **[!UICONTROL From Clipboard]** 클립보드에 복사한 시각화를 붙여넣습니다. 자세한 내용은 [사이드바 패널 복사](../../home/c-get-started/c-config-sidebar.md#section-720ae057632a4b8dbb94412e06a370b1).

## 사이드바 패널 복사 {#section-720ae057632a4b8dbb94412e06a370b1}

1. 패널의 위쪽 테두리를 마우스 오른쪽 단추로 클릭한 다음 **[!UICONTROL Copy]** > **[!UICONTROL Window]**.
1. 패널을 붙여넣으려면 **[!UICONTROL Add]** > **[!UICONTROL Open]** > **[!UICONTROL From Clipboard]**.

## 사이드바 패널 저장 {#section-fb19936b12704fb0a4c592abb579db1d}

사이드바 패널에서 제목 표시줄을 마우스 오른쪽 버튼으로 클릭하고 **[!UICONTROL Save]**.

마찬가지로 저장된 사이드바 시각화를 열 수 있습니다. Data Workbench은 시각화를 [!DNL .vw] 파일을 지정한 위치에 지정합니다.

## 기본 사이드바로 되돌리기 {#section-4d14b8771ad747bba799876267f24831}

사이드바에서 **[!UICONTROL Options]** > **[!UICONTROL Revert]**.

Data Workbench을 닫으면 현재 사이드바 구성이 [!DNL sidebar.vw] 사용자 프로필에 있는 파일입니다. Data Workbench을 열면 시스템이 [!DNL sidebar.vw] 상위 프로필이 아닌 사용자 프로필의 파일입니다.

사용자 프로필에서 사이드바를 삭제하고 상위 프로필에서 사이드바를 다시 로드하는 기본 또는 이전에 저장된 사이드바로 되돌릴 수 있습니다. 관리자는 기본(상위) 사이드바를 [!DNL Profile Manager].

## 추가 상태 패널 파일 사용자 정의 {#section-8d502f3b59cc4331966edec05e896ce1}

시스템 관리자는 [!DNL More Status Panel.vw]. 이렇게 하면 지표 및 차원 값에 대한 컨텍스트 단어가 배치되고 결과를 [!DNL More Status panel] 을 클릭합니다.

를 표시하려면 [!DNL More Status panel] 사이드바에서 다음 예제에 표시된 화살표를 클릭합니다.

![](assets/more_status_panel_arrows.png)

다음 절차에서는 데이터 집합에 있는 일 수를 알려주는 사용자 지정 상태를 만드는 방법에 대한 간단한 예를 보여줍니다.

1. 에서 [!DNL Profile Manager]를 클릭합니다. **[!UICONTROL Sidebar\]**.

1. 에서 [!DNL Base_5_3*] 열에서 로컬 복사본 만들기 [!DNL More Status Panel.vw] 파일.

   이렇게 하려면 파일 확인 표시를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL Make Local]**.

1. 를 엽니다. [!DNL More Status Panel.vw] 파일의 [!DNL .vw] [!DNL Editor] 또는 메모장에서 사용할 수 있습니다.

   ![](assets/more_status_panel_file.png)

1. 을(를) 완료합니다 [!DNL Context] 및 [!DNL Items] 의 필드 [!DNL Editor]. 자세한 내용은 [쿼리 언어 구문](../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f) 를 참조하십시오.

1. 파일을 저장합니다.

   앞의 예에서 값은 다음과 같이 표시되는 상태 공식이 됩니다.

   ![](assets/more_status_panel.png)
