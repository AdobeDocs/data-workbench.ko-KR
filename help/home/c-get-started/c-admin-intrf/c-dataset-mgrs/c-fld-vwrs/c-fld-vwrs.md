---
description: 필드 뷰어는 하나 이상의 데이터 필드의 값이 들어 있는 테이블입니다.
solution: Analytics
title: 필드 뷰어
topic: Data workbench
uuid: 1227b0de-6ae8-4f97-ad3e-5c9ead818ba5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# 필드 뷰어{#field-viewer}

필드 뷰어는 하나 이상의 데이터 필드의 값이 들어 있는 테이블입니다.

값이 표시되는 필드는 데이터 세트의 로그 소스, 변형 또는 확장 차원의 입력 또는 출력입니다. 필드 이름은 열 머리글에 표시되며, 각 행은 소스 데이터의 단일 행에 대한 필드 값을 포함합니다. 필드 뷰어를 사용하면 필드 값을 볼 수 있으므로 [정규 표현식을](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c)작성하고 테스트하는 데 유용합니다.

필드 뷰어를 [!DNL Transformation Dependency] 맵에서 설명선으로 열거나 메뉴에서 독립형 시각화로 열 수 [!DNL Admin] 있습니다.

* 맵에서 필드 뷰어 만들기. [!DNL Transformation Dependency] 맵에서 필드 뷰어를 열면 뷰어가 [!DNL Transformation Dependency] 마우스 오른쪽 단추로 클릭한 로그 소스, 변형 또는 차원에 따라 자동으로 채워집니다. 로그 소스 또는 변환의 경우 뷰어의 필드는 로그 소스 또는 변환의 입력 또는 출력입니다. 차원의 경우 필드는 차원의 입력입니다. 원하는 대로 필드를 추가하거나 제거할 수 있습니다.

* 필드 뷰어를 독립 실행형 시각화로 만듭니다. 필드 뷰어를 독립 실행형 시각화로 열 때 [!DNL Log Processing Field Viewer] 또는 [!DNL Transformation Field Viewer]a를 만들 수 있습니다. 뷰어가 비어 있으므로 뷰어에 원하는 필드를 추가해야 합니다. 의 [!DNL Log Processing Field Viewer]경우 [!DNL Log Processing.cfg] 파일이나 모든 [!DNL Log Processing Dataset Include] 파일에서 필드를 추가할 수 있습니다. 의 [!DNL Transformation Field Viewer]경우 [!DNL Transformation.cfg] 파일이나 모든 [!DNL Transformation Dataset Include] 파일에서 필드를 추가할 수 있습니다.

![](assets/vis_FieldViewer_OneField.png)

>[!NOTE]
>
>필드 뷰어는 테이블 시각화가 아닙니다.따라서 표와 연결된 속성이 없습니다.

필드 뷰어 내의 필드 추가 및 제거 및 필터링에 대한 자세한 내용은 관리 인터페이스를 [참조하십시오](../../../../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).
