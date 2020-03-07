---
description: Hidden 매개 변수나 Show 매개 변수를 사용하여 확장 차원이 데이터 워크벤치의 차원 메뉴에 표시되지 않도록 숨길 수 있습니다.
solution: Analytics
title: 확장 차원 숨기기
topic: Data workbench
uuid: c32f47ad-0246-4611-b54c-0c9f0eb396bd
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# 확장 차원 숨기기{#hiding-extended-dimensions}

Hidden 매개 변수나 Show 매개 변수를 사용하여 확장 차원이 데이터 워크벤치의 차원 메뉴에 표시되지 않도록 숨길 수 있습니다.

두 매개 변수에 대한 적절한 설정을 입력할 때 차원 이름이 데이터 워크벤치의 메뉴에 나열되지 않지만 여전히 프로필에 있으며 사용할 수 있습니다. 모든 데이터 워크벤치 사용자는 파일에서 모두 숨김 취소 매개 변수를 true로 설정하여 일시적으로 숨겨진 차원을 숨길 수 [!DNL Insight.cfg] 있습니다.

모두 숨김 취소 매개 변수에 대한 자세한 내용은 데이터 워크벤치 사용자 안내서의 데이터 워크벤치 구성 매개 변수에 *대한 부록을 참조하십시오*.

다음 섹션에서는 숨김 및 표시 매개 변수를 사용하여 확장 차원을 숨기는 방법을 설명합니다.

* [숨겨진 매개 변수를 사용하여 확장 차원 숨기기](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-7167a6f6241a4bc78f2f322e048d65cf)
* [표시 매개 변수를 사용하여 확장 차원 숨기기](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-4dceb1079c7f40d2bffc686d1f73f8ad)

## 숨겨진 매개 변수를 사용하여 확장 차원 숨기기 {#section-7167a6f6241a4bc78f2f322e048d65cf}

Hidden 매개 변수는 [!DNL Transformation Dataset Configuration] 파일에서 확장 치수를 정의할 때 사용할 수 있는 선택적 매개 변수입니다.

1. 숨길 확장 차원이 정의된 [!DNL Transformation Dataset Configuration] 파일을 엽니다. 기존 [데이터 세트 포함 파일](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077)편집을 참조하십시오.

1. 구성 창에서 원하는 차원에 대한 Hidden 매개 변수를 찾고 *true*&#x200B;를 입력합니다.
1. 파일을 로컬에 저장한 다음 서버의 해당 프로필에 저장합니다. 기존 [데이터 세트 포함 파일](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077)편집을 참조하십시오.

데이터 워크벤치의 차원 메뉴에 확장 차원이 표시되지 않는 데이터 세트 변환이 재변환됩니다. 숨김 매개 변수에 대한 자세한 내용은 확장 [차원을 참조하십시오](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

Hidden 매개 변수의 설정을 변경하는 경우 변경 내용을 적용하려면 데이터 세트를 다시 변환해야 합니다.

## 표시 매개 변수를 사용하여 확장 차원 숨기기 {#section-4dceb1079c7f40d2bffc686d1f73f8ad}

Show 매개 변수는 [!DNL Transformation Dataset Configuration] 파일에서 확장 치수를 정의하는 데 사용할 수 있는 매개 변수 중 하나가 아닙니다. 대신, 생성된 파생된 차원에 대한 매개 변수가 [!DNL .dim] 파일에 정의됩니다. 따라서 표시 매개변수를 사용하여 확장 치수를 숨기려면 먼저 다음 절차에 설명된 대로 확장 치수를 기반으로 하는 파생 치수를 생성해야 합니다.

1. 메모장과 같은 텍스트 편집기를 사용하여 &lt;*dimension name*>.dim이라는 빈 파일을 만듭니다. 파일 이름은 숨길 차원의 이름과 일치해야 합니다. 예를 들어 다음 페이지 차원을 숨기려면 [!DNL Next Page.dim] 파일을 만듭니다.

1. 파일에 다음 텍스트를 추가합니다.

   * entity = ref:wdata/model/dim/Parent/+name
   * show = bool:false

1. 파일의 Dimensions 디렉토리에 파일을 저장합니다. 원하는 경우 파일을 하위 디렉토리에 저장할 수 있습니다.

Show 매개 변수를 사용하여 확장 차원을 숨길 때 데이터 세트를 다시 변환하여 변경 사항을 적용할 필요가 없습니다. 프로필의 로컬 버전(즉, 사용자 폴더에 파일을 저장할 수 있음)에서 차원을 숨기거나 표시하도록 선택하거나, 다른 프로필 사용자가 사용할 수 있도록 [!DNL .dim] [!DNL .dim] 파일을 서버에 저장할 수 있습니다.

표시 매개 변수를 사용하여 지표 및 필터를 숨길 수도 있습니다. 자세한 내용은 데이터 워크벤치 사용자 안내서의 인터페이스 및 분석 기능 *구성 장을 참조하십시오*.
