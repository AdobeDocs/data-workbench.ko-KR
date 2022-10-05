---
description: 필드 뷰어는 하나 이상의 데이터 필드 값을 포함하는 테이블입니다.
title: 필드 뷰어
uuid: 1227b0de-6ae8-4f97-ad3e-5c9ead818ba5
exl-id: 53ede4aa-4865-4e67-b3b1-e3e6287f29d7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# 필드 뷰어{#field-viewer}

{{eol}}

필드 뷰어는 하나 이상의 데이터 필드 값을 포함하는 테이블입니다.

값이 표시되는 필드는 데이터 집합의 로그 소스, 변형 또는 확장 차원의 입력 또는 출력입니다. 필드 이름은 열 머리글에 표시되며, 각 행에는 단일 소스 데이터 행에 대한 필드 값이 포함됩니다. 필드 뷰어를 사용하면 필드 값을 볼 수 있으므로 쓰기 및 테스트에 유용합니다 [정규 표현식](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

필드 뷰어를 콜아웃으로 열 수 있습니다 [!DNL Transformation Dependency] 에서 독립형 시각화로 매핑 [!DNL Admin] 메뉴:

* 에서 필드 뷰어 만들기 [!DNL Transformation Dependency] 맵 에서 필드 뷰어를 열 때 [!DNL Transformation Dependency] 매핑하면 마우스 오른쪽 단추로 클릭한 로그 소스, 변형 또는 차원을 기반으로 뷰어가 자동으로 채워집니다. 로그 소스 또는 변환의 경우 뷰어의 필드는 로그 소스 또는 변환의 입력 또는 출력입니다. 차원의 경우 필드는 차원의 입력입니다. 원하는 대로 필드를 추가하고 제거할 수 있습니다.

* 필드 뷰어를 독립형 시각화로 만듭니다. 필드 뷰어를 독립형 시각화로 열면 다음을 만들 수 있습니다 [!DNL Log Processing Field Viewer] 또는 [!DNL Transformation Field Viewer]. 뷰어가 비어 있으므로 뷰어에 원하는 필드를 추가해야 합니다. 대상 [!DNL Log Processing Field Viewer]를 채울 때 [!DNL Log Processing.cfg] 파일 또는 [!DNL Log Processing Dataset Include] 파일. 대상 [!DNL Transformation Field Viewer]를 채울 때 [!DNL Transformation.cfg] 파일 또는 [!DNL Transformation Dataset Include] 파일.

![](assets/vis_FieldViewer_OneField.png)

>[!NOTE]
>
>필드 뷰어는 표 시각화가 아닙니다. 따라서 테이블과 연결된 속성이 없습니다.

필드 뷰어 내에서 필드를 추가 및 제거하고 필터링하는 방법에 대한 자세한 내용은 [관리 인터페이스](../../../../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).
