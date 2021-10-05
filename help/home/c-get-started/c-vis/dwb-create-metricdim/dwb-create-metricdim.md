---
description: 지표 치수 마법사를 사용하여 새 지표 Dimension을 만듭니다.
title: 지표 치수 마법사
uuid: 77b9bc8e-7625-4fef-9de4-f113f9b2debd
exl-id: 109fbefc-5608-493d-aec9-8337f21eaa70
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 3%

---

# 지표 치수 마법사{#metric-dim-wizard}

지표 치수 마법사를 사용하여 새 지표 Dimension을 만듭니다.

지표 차원은 지표를 새 차원으로 변환합니다. 예를 들어 페이지 보기 수 지표와 방문자 수준을 기반으로 하는 지표 차원은 각 방문자에 대한 총 페이지 보기 수를 기반으로 차원 요소를 표시합니다. 이 차원을 사용하면 차원 요소를 기반으로 현재 정의된 지표를 확장하여 새 차원으로 만들고 저장할 수 있습니다.

## 1단계: 차원 및 지표 선택 {#section-58b6ea7bbba5487ba1a3c264aa3dcb95}

1. **지표 치수 마법사를 엽니다**.

   작업 공간에서 마우스 오른쪽 단추를 클릭하고 **도구** > **지표 치수 만들기**&#x200B;를 선택합니다.

1. **지표 치수 이름을**&#x200B;로 지정합니다.

   기본적으로 이름 필드는 수준 및 지표 선택 사항을 기반으로 자동으로 채워집니다.

1. **Dimension 수준을 선택합니다.** 차원 레벨은 입력을 필터링하고 차원 유형을 정의할 모든 구성 요소 값을 포함하는 상위 차원입니다.

   Dimension 수준은 다음과 같습니다.

   * 클릭스루
   * 히트
   * 제품
   * 방문
   * 방문자

1. **지표를 선택합니다**.

   미리 작성된 지표를 선택하여 지표를 확장하고 지표 차원으로 저장합니다.

   ![](assets/6_4_workstation_metricdim_metric.png)

1. (선택 사항) **지표 공식**&#x200B;을 만듭니다.

   상자를 클릭하여 사용자 지정 지표 공식을 입력합니다. 표현식의 유효성을 검사하는 계산된 미리 보기 값이 나타납니다.

   ![](assets/6_4_workstation_metricdim_create_metric.png)

   자신만의 [지표 표현식](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-mtrc-exp.html)을 추가하거나 다른 지표 편집기 또는 시각화에서 잘라내어 붙여넣을 수 있습니다. 구문 오류, 수식 오류, 정의되지 않은 필터 및 기타 오류가 마법사에서 보고됩니다.

1. **다음**&#x200B;을 클릭합니다.

## 2단계: 버킷 포맷 및 설정 {#section-5bddf3cd306545d7806a501637f80f77}

지표 형식을 선택하고 차원 표현식에 대한 버킷 값을 설정할 수 있습니다.

1. 새 지표 딤에 대해 **형식**&#x200B;을 선택합니다.

   ![](assets/6_4_workstation_metricdim_format_metric.png)

   형식은 시각화에서 열 때 지표가 표시되는 방식을 정의합니다. 이러한 형식은 아래에 정의된 [printf standards](https://www.cplusplus.com/reference/cstdio/printf/) 를 선택합니다.

   ```
   %[flags][width][.precision][length][specifier]
   %
   0.2lf = % _ [flags] 0 [width] .2 [.precision] l [length] f[ specifier]
   ```

   **미리 보기** 필드에서 선택한 지표와 형식을 기준으로 값이 표시됩니다.

1. **버킷 수** 표현식을 추가합니다.

   다양한 범위 또는 버킷으로 지표를 어둡게 정의할 수 있습니다. [0-4], [5-10],..)과 같은 크기를 기반으로 요소의 하위 집합을 반환합니다. Dimension 수준의 요소는 범위에 지표 값이 포함된 요소와 관련이 있습니다. [Dimension 표현식](https://experienceleague.adobe.com/docs/data-workbench/using/client/qry-lang-syntx/c-syntx-dim-exp.html)의 구문에서 버킷 표현식 설명을 참조하십시오.

1. 저장하기 전에 **미리 보기**&#x200B;를 클릭하여 지표 치수 값 테이블을 엽니다.

   ![](assets/6_4_workstation_metricdim_preview.png)

   지표당 테이블 세부 정보 지표 값이 흐려집니다.

1. **Dimension 메뉴에 표시**&#x200B;를 클릭하여 새로 만든 차원을 **파인더**&#x200B;의 **Dimension** 탭에 추가합니다.
1. **다음**&#x200B;을 클릭합니다.

## 3단계: 마침 및 저장 {#section-d9043235b18a425f9de0db668d4b1683}

1. 저장 후 지표 치수 편집기, 그래프 시각화 또는 테이블을 실행하려면 선택합니다.

   | 필드 | 설명 |
   |---|---|
   | 지표 치수 편집기 시작 | 지표 치수 편집기를 엽니다. |
   | Launch 그래프 | 표의 PNG 그래픽을 시작합니다. |
   | 시작 테이블 | 작업 공간에서 선택한 지표의 값과 비교하여 새 지표의 값을 나열하는 열의 값이 있는 테이블을 시작합니다. |

1. **완료**&#x200B;를 클릭하고 저장합니다.

   파일을 저장할 수 있는 저장 대화 상자가 열립니다. 선택한 값 보기 옵션이 작업 영역에서 열립니다.
